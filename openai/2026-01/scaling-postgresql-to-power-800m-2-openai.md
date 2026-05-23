---
title: "Scaling PostgreSQL to power 800 million ChatGPT users"
vendor: openai
source_url: https://openai.com/index/scaling-postgresql/
published_at: 2026-01-22T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 2500
reading_time_minutes: 13
tags: [postgresql, infrastructure, engineering, scaling, database]
---

# Scaling PostgreSQL to power 800 million ChatGPT users

January 22, 2026 | Engineering

By Bohan Zhang, Member of the Technical Staff

For years, PostgreSQL has been one of the most critical, under-the-hood data systems powering core products like ChatGPT and OpenAI's API. As our user base grows rapidly, the demands on our databases have increased exponentially, too. Over the past year, our PostgreSQL load has grown by more than 10x, and it continues to rise quickly.

Our efforts to advance our production infrastructure to sustain this growth revealed a new insight: PostgreSQL can be scaled to reliably support much larger read-heavy workloads than many previously thought possible. The system has enabled us to support massive global traffic with a single primary Azure PostgreSQL flexible server instance and nearly 50 read replicas spread over multiple regions globally. This is the story of how we've scaled PostgreSQL at OpenAI to support millions of queries per second for 800 million users through rigorous optimizations and solid engineering.

## Cracks in our initial design

After the launch of ChatGPT, traffic grew at an unprecedented rate. To support it, we rapidly implemented extensive optimizations at both the application and PostgreSQL database layers, scaled up by increasing the instance size, and scaled out by adding more read replicas. This architecture has served us well for a long time.

It may sound surprising that a single-primary architecture can meet the demands of OpenAI's scale; however, making this work in practice isn't simple. We've seen several SEVs caused by Postgres overload, and they often follow the same pattern: an upstream issue causes a sudden spike in database load, such as widespread cache misses from a caching-layer failure, a surge of expensive multi-way joins saturating CPU, or a write storm from a new feature launch. As resource utilization climbs, query latency rises and requests begin to time out. Retries then further amplify the load, triggering a vicious cycle with the potential to degrade the entire ChatGPT and API services.

## Scaling PostgreSQL to millions of QPS

To mitigate these limitations and reduce write pressure, we have migrated shardable, write-heavy workloads to sharded systems such as Azure Cosmos DB. We optimized application logic to minimize unnecessary writes. We also no longer allow adding new tables to the current PostgreSQL deployment. New workloads default to the sharded systems.

### Reducing load on the primary
We minimize load on the primary as much as possible—both reads and writes—to ensure it has sufficient capacity to handle write spikes. Read traffic is offloaded to replicas wherever possible. For write traffic, we have migrated shardable, write-heavy workloads to sharded systems.

### Query optimization
A few expensive queries, such as those joining many tables together, can significantly degrade or even bring down the entire service. We continuously optimize PostgreSQL queries to ensure they're efficient and avoid common OLTP anti-patterns.

### Workload isolation
We isolate workloads onto dedicated instances to ensure that sudden spikes in resource-intensive requests do not impact other traffic. We split requests into low-priority and high-priority tiers and route them to separate instances.

### Connection pooling
We deployed PgBouncer as a proxy layer to pool database connections. Running it in statement or transaction pooling mode allows us to efficiently reuse connections, greatly reducing the number of active client connections.

### Caching
To reduce read pressure on PostgreSQL, we use a caching layer to serve most of the read traffic. We implement a cache locking mechanism so that only a single reader that misses on a particular key fetches the data from PostgreSQL.

### Scaling read replicas
We operate nearly 50 read replicas across multiple geographic regions to minimize latency. We are collaborating with the Azure PostgreSQL team on cascading replication to scale to potentially over a hundred replicas without overwhelming the primary.

## Results and the road ahead

This effort demonstrates that with the right design and optimizations, Azure PostgreSQL can be scaled to handle the largest production workloads. PostgreSQL handles millions of QPS for read-heavy workloads, powering OpenAI's most critical products like ChatGPT and the API platform.

We consistently deliver low double-digit millisecond p99 client-side latency and five-nines availability in production. Over the past 12 months, we have had only one SEV-0 PostgreSQL incident.

While we are happy with how far PostgreSQL has taken us, we continue to push its limits to ensure we have sufficient runway for future growth. We have already migrated the shardable write-heavy workloads to our sharded systems like CosmosDB.