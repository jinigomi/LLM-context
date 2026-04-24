---
title: Harness Design Pattern
created: 2026-04-24
updated: 2026-04-24
type: concept
tags: [design, architecture, reliability, engineering, multi-agent]
sources: [raw/articles/anthropic-harness-design.md]
confidence: high
---
# Harness Design Pattern

The **Harness** is a design pattern and infrastructure layer used to manage the lifecycle, observability, and reliability of long-running autonomous AI agents.

## Core Components (V2 Architecture)
1. **Planner**: Expands a brief prompt into a full product spec. Focuses on high-level design and ambitious scope rather than granular technical details to avoid cascading errors.
2. **Generator**: Implements features in "sprints" (or continuous sessions in later models like Opus 4.6). Responsible for technical execution (e.g., React, FastAPI, Git).
3. **Evaluator (QA)**: A standalone agent tuned to be "skeptical." Uses tools like Playwright to test functionality, UI, and edge cases.

## Key Techniques
### Generator-Evaluator Loop
Inspired by **Generative Adversarial Networks (GANs)**. The generator produces an output, and a separate evaluator provides a critique. This addresses the **self-evaluation bias**, where agents tend to over-praise their own work.

### Context Management
- **Context Resets**: Clearing the context window entirely and starting a fresh agent with a structured handoff artifact. This solves **Context Anxiety** (where models wrap up work prematurely as the window fills).
- **Compaction**: Summarizing earlier parts of the conversation in place. Less effective against context anxiety but preserves continuity.

### Sprint Contracts
A negotiation step where the Generator and Evaluator agree on what "done" looks like for a specific chunk of work before code is written.

## Failure Modes Addressed
- **Context Anxiety**: Models losing coherence or rushing as they approach context limits.
- **Leniency/Self-Praise**: Agents being too generous when grading their own subjective outputs (like design).
- **Stubbing**: The tendency for generators to miss details or leave "stubs" instead of full implementations.

[[anthropic]], [[multi-agent-systems]], [[context-engineering]].

^[raw/articles/anthropic-harness-design.md]
