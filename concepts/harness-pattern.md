---
title: Harness Design Pattern
created: 2026-04-24
updated: 2026-04-24
type: concept
tags: [design, architecture, reliability, engineering]
sources: [raw/articles/anthropic-harness-design.md]
confidence: high
---
# Harness Design Pattern

The **Harness** is a design pattern used for managing the lifecycle, observability, and reliability of long-running applications (e.g., web servers, background workers).

## Core Principles
1. **Separation of Concerns**: Application logic is decoupled from "harness" logic (signals, health checks).
2. **Graceful Shutdown**: Handling `SIGTERM` to allow the application to finish pending work before exiting.
3. **Observability**: Standardized logging and metrics, often offloaded to a sidecar.
4. **Health Monitoring**: Implementation of `/healthz` or similar endpoints to indicate readiness and liveness.

See also: [[sidecar-pattern]], [[graceful-shutdown]].

^[raw/articles/anthropic-harness-design.md]
