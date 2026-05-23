---
title: "Finding bugs across the Python ecosystem with Claude and property-based testing"
vendor: anthropic
source_url: https://red.anthropic.com/2026/property-based-testing/
published_at: 2026-01-14T00:00:00.000Z
crawled_at: 2026-05-23T15:06:50.000Z
word_count: 3500
reading_time_minutes: 18
tags: [property-based-testing, bug-finding, python, claude, llm-agents]
---

# Finding bugs across the Python ecosystem with Claude and property-based testing

January 14, 2026

Muhammad Maaz (MATS), Liam DeVoe (Northeastern University), Zac Hatfield-Dodds, Nicholas Carlini (Anthropic)

We developed an agent that can efficiently identify bugs in large software projects. To do this, our agent infers general properties of code that should be true, and then by applying property-based testing—a technique similar to fuzz testing—we are able to discover bugs in top Python packages like NumPy, SciPy, and Pandas. After extensive manual validation, we are in the process of reporting these bugs to the developers, several of which have already been patched.

## Introduction

Ensuring that programs are bug-free is one of the most challenging aspects of software engineering. Bugs frequently continue to lurk despite the developer's best effort. The most common approach to testing code is with example-based tests: the developer writes out a specific example use-case, and then verifies that the actual output matches the expected output. However, exhaustively covering a program with tests like this is challenging.

In contrast, property-based testing is a software testing paradigm that aims to test whether a general property of the code holds for all inputs. A developer specifies a property or invariant about the program, as well as a description of the kinds of inputs the property accepts. The property-based testing framework then automatically searches for a counterexample.

## Our Property-Based Testing Agent

Our property-based testing agent is built as a custom Claude Code command. The agent takes a single argument, pointing it towards a particular target, either a single Python file, a module, or a function. The agent then follows this process to identify potential bugs:

1. Read and understand the target, by reading code, pulling relevant documentation, and exploring how it relates to the rest of the codebase
2. Propose properties grounded in these findings
3. Write corresponding property-based tests in Hypothesis
4. Run the tests and reflect: if it failed, has the test truly discovered a bug, or does the test need to be adjusted?
5. If the agent is confident it has found a real bug, it writes out a formatted bug report

## Maintainer validation

Our agent found bugs that maintainers consider valid and worth fixing. Examples include a bug in numpy.random.wald that returns negative values (the Wald distribution should only return positive values), a bug in aws-lambda-powertools where slice_dictionary() returns the first chunk repeatedly, and a bug in tokenizers where EncodingVisualizer was missing a closing parenthesis.

## Conclusion

As language models continue to improve, we think agentic property-based testing could become an increasingly valuable complement to human-written testing. The high-level semantic guarantees of property-based testing makes them a natural fit to pair with LLMs during development. LLMs are particularly good at identifying properties that should be true about a given block of code from context.