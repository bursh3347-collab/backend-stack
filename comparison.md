# Backend Framework Comparison

## Quick Comparison

| Project | Stars | Language | Type-safe | Performance | Best For |
|---------|-------|----------|-----------|-------------|----------|
| **Zod** | 35k | TypeScript | ✅✅ Best | ⚡ Very Fast (v4) | Schema validation everywhere |
| **FastAPI** | 85k | Python | ✅ Pydantic | ⚡ Very Fast | Python APIs, ML services |
| **NestJS** | 75k | TypeScript | ✅ Full | 🏃 Fast | Enterprise TypeScript backends |
| **Express.js** | 67k | JavaScript | ❌ Manual | 🏃 Fast | Legacy, simple APIs |
| **tRPC** | 40k | TypeScript | ✅✅ Best | ⚡ Very Fast | TypeScript full-stack (with Next.js) |
| **Fastify** | 36k | JS/TS | ✅ JSON Schema | ⚡⚡ Very Fast | High-perf Node.js APIs |
| **Dragonfly** | 27k | C++ | N/A | ⚡⚡⚡ Fastest | Redis replacement (infrastructure) |
| **Hono** | 25k | TypeScript | ✅ Native | ⚡⚡ Fastest | Edge, serverless, multi-runtime |
| **ElysiaJS** | 12k | TypeScript | ✅ Native | ⚡⚡⚡ Fastest | Bun-native APIs, edge |
| **Django** | 84k | Python | ⚠️ Partial | 🏃 Moderate | Full-stack Python, admin panels |
| **Nitro** | 6k | TypeScript | ✅ Auto | ⚡ Fast | Universal deploy (20+ targets) |
| **BullMQ** | 6k | TypeScript | ✅ Typed | N/A (queue) | Background jobs, task processing |

## Stack Match Score

| Project | Match | Notes |
|---------|-------|-------|
| **Zod** | 🟢 99% | Non-negotiable. Foundation of TypeScript validation |
| **tRPC** | 🟢 95% | Perfect Next.js companion, zero codegen type safety |
| **Hono** | 🟢 90% | TypeScript-first, multi-runtime, works with Vercel Edge |
| **BullMQ** | 🟢 90% | Essential SaaS infra: email, webhooks, AI jobs |
| **ElysiaJS** | 🟢 85% | Best DX if committing to Bun runtime |
| **NestJS** | 🟡 80% | TypeScript, but heavy framework |
| **Dragonfly** | 🟡 78% | Superior Redis replacement for SaaS backend |
| **Nitro** | 🟡 75% | Universal deploy engine, great for Nuxt or standalone |
| **Fastify** | 🟡 75% | Good perf, JSON Schema (not Zod) |
| **Express.js** | 🟡 65% | Mature but aging |
| **FastAPI** | 🔴 55% | Python, different ecosystem |
| **Django** | 🔴 45% | Python, full-stack competitor |

## TEMC Score Ranking

| Rank | Project | Overall | T | E | M | C |
|------|---------|---------|---|---|---|---|
| 1 | **Zod** | **92** | 92 | 95 | 85 | 95 |
| 2 | **tRPC** | **85** | 88 | 85 | 82 | 88 |
| 3 | **Hono** | **83** | 90 | 78 | 80 | 85 |
| 4 | **ElysiaJS** | **81** | 88 | 72 | 78 | 85 |
| 5 | **BullMQ** | **80** | 85 | 78 | 72 | 88 |
| 6 | **Dragonfly** | **78** | 92 | 82 | 75 | 65 |
| 7 | **FastAPI** | **78** | 85 | 88 | 78 | 65 |
| 8 | **Nitro** | **76** | 88 | 80 | 70 | 72 |
| 9 | **NestJS** | **75** | 82 | 85 | 72 | 68 |
| 10 | **Fastify** | **74** | 85 | 80 | 70 | 65 |
| 11 | **Express.js** | **65** | 60 | 90 | 65 | 55 |
| 12 | **Django** | **62** | 78 | 85 | 65 | 40 |

## Decision Guide

- **Building a Next.js SaaS?** → Zod (validation) + tRPC (API) + BullMQ (jobs)
- **Need a separate backend service?** → Hono (lightweight) or NestJS (enterprise)
- **Bun-first project?** → ElysiaJS
- **Universal deployment (Lambda + CF + Node)?** → Nitro
- **Redis replacement?** → Dragonfly (⚠️ BSL license)
- **ML/AI microservice?** → FastAPI
- **Legacy Node.js?** → Fastify (Express replacement)
- **Full-stack Python with admin?** → Django

Last updated: 2026-04-16
