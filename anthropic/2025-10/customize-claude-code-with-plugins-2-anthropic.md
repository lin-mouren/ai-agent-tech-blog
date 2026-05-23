---
title: "Customize Claude Code with plugins"
vendor: anthropic
source_url: https://www.anthropic.com/news/claude-code-plugins
published_at: 2025-10-09T09:54:43.000Z
crawled_at: 2026-05-23T14:44:14.000Z
word_count: 700
reading_time_minutes: 4
tags: [claude-code, plugins, MCP, developer-tools, Anthropic]
---

October 9, 2025

# Customize Claude Code with plugins

Claude Code now supports plugins: custom collections of slash commands, agents, MCP servers, and hooks that install with a single command.

## Share your Claude Code setup with plugins

Slash commands, agents, MCP servers, and hooks are all extension points you can use to customize your experience with Claude Code. We built plugins to make sharing easier.

Plugins are a lightweight way to package and share any combination of:

- **Slash commands**: Create custom shortcuts for frequently-used operations
- **Subagents**: Install purpose-built agents for specialized development tasks
- **MCP servers**: Connect to tools and data sources through the Model Context Protocol
- **Hooks**: Customize Claude Code's behavior at key points in its workflow

You can install plugins directly within Claude Code using the `/plugin` command, now in public beta. They're designed to toggle on and off as needed.

## Use cases

Plugins help you standardize Claude Code environments around best practices: enforcing standards, supporting users, sharing workflows, connecting tools through MCP, and bundling customizations.

## Plugin marketplaces

Anyone can build and host plugins and create plugin marketplaces. To host a marketplace, all you need is a git repository with a properly formatted `.claude-plugin/marketplace.json` file.

## Getting started

Plugins are now in public beta for all Claude Code users. Install them with the `/plugin` command and they'll work across your terminal and VS Code.