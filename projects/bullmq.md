# BullMQ

> Premium message queue and background job processing for Node.js, built on Redis

| Metric | Data |
|--------|------|
| GitHub | [taskforcesh/bullmq](https://github.com/taskforcesh/bullmq) |
| Stars | ~6,000 |
| License | MIT |
| Language | TypeScript |
| Last Updated | Active (v5.74.1) |
| Contributors | 200+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 85 | Production-grade job queue with Redis backend. Features: rate limiting, job prioritization, delayed jobs, cron scheduling, parent-child flows, sandboxed processors. Multi-language (Node/Python/Elixir/PHP) |
| E (Ecosystem) | 78 | De facto Node.js job queue standard (Bull predecessor had 15k+ stars). Taskforce.sh commercial dashboard. NestJS official integration |
| M (Market) | 72 | Essential infrastructure for any SaaS that needs background processing. Webhook delivery, email sending, report generation, AI inference queues — all need BullMQ |
| C (Combo) | 88 | TypeScript-native, MIT license, perfect stack match. Pairs with Redis/Dragonfly. Critical for SaaS: email queues, Stripe webhook processing, AI batch jobs |
| **Overall** | **80** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
The industry standard for Node.js background job processing. Every SaaS needs async task processing — BullMQ gives you production-grade queues with minimal setup.

## Architecture Highlights
- **Redis-backed** — All state in Redis, workers can be horizontal scaled
- **Lua scripts** — Atomic operations via Redis Lua for correctness
- **Flow producer** — Parent-child job dependencies (DAG workflows)
- **Rate limiter** — Built-in rate limiting per queue or global
- **Sandboxed workers** — Run untrusted code in separate processes
- Dependencies: ioredis, cron-parser, msgpackr, semver

## Key Modules
1. **Queue** — Job creation, scheduling, prioritization
2. **Worker** — Job processing with concurrency control
3. **FlowProducer** — DAG-based job dependency workflows
4. **QueueEvents** — Real-time job lifecycle events
5. **QueueScheduler** — Delayed job and cron scheduling

## Solo Dev Verdict
🟢 **Must-have for any SaaS backend.** If your product sends emails, processes webhooks, generates reports, or runs AI inference — you need BullMQ. MIT license, TypeScript-native, pairs perfectly with your stack. The commercial Taskforce.sh dashboard is optional but nice for monitoring.

## Anti-Pattern Warning
- Requires Redis (adds infra dependency)
- Can be complex for simple use cases (consider in-process queues for tiny projects)
- Job data serialization can be tricky with complex objects
- v5 breaking changes from Bull v4 migration
