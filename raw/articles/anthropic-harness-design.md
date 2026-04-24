---
source_url: https://www.anthropic.com/engineering/harness-design-long-running-apps
ingested: {today}
---
# Harness: A Design Pattern for Long-Running Applications

This article describes Anthropic's approach to building and operating long-running applications.
Key components of the Harness pattern:
- Signal handling (SIGTERM, SIGINT) for graceful shutdown.
- Health check endpoints (/healthz).
- Sidecar processes for logging and metrics.
- Standardized configuration and lifecycle management.
