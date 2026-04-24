---
title: Solo Agent vs. Harness Run
created: 2026-04-24
updated: 2026-04-24
type: comparison
tags: [benchmark, cost, quality, agentic-coding]
sources: [raw/articles/anthropic-harness-design.md]
confidence: high
---
# Solo Agent vs. Harness Run

Based on Anthropic's "Retro Game Maker" experiment.

| Metric | Solo Run | Full Harness (V1) |
|------|----------|-------------------|
| **Duration** | 20 minutes | 6 hours |
| **Cost** | $9 | $200 |
| **Agent** | Single pass | Planner + Generator + Evaluator |
| **Outcome** | Non-functional (broken runtime) | Fully functional (physics, editors, AI features) |
| **Design** | Generic, safe defaults | Polished, distinctive, "museum quality" |

## Synthesis
While the harness is ~20x more expensive and significantly slower, it achieves a "lift" in quality that enables tasks currently beyond the capability of a solo model (e.g., verifiable correctness in complex full-stack apps).

^[raw/articles/anthropic-harness-design.md]
