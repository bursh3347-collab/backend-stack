# Backend Framework Comparison

## Quick Comparison

| Project | Stars | Language | Type-safe | Performance | Best For |
|---------|-------|----------|-----------|-------------|----------|
| **FastAPI** | 85k | Python | ✅ Pydantic | ⚡ Very Fast | Python APIs, ML services |
| **NestJS** | 75k | TypeScript | ✅ Full | 🏃 Fast | Enterprise TypeScript backends |
| **Express.js** | 67k | JavaScript | ❌ Manual | 🏃 Fast | Legacy, simple APIs |
| **Hono** | 25k | TypeScript | ✅ Native | ⚡⚡ Fastest | Edge, serverless, multi-runtime |
| **Django** | 84k | Python | ⚠️ Partial | 🏃 Moderate | Full-stack Python, admin panels |
| **tRPC** | 40k | TypeScript | ✅✅ Best | ⚡ Very Fast | TypeScript full-stack (with Next.js) |
| **Fastify** | 36k | JS/TS | ✅ JSON Schema | ⚡⚡ Very Fast | High-perf Node.js APIs |

## Stack Match Score

| Project | Match | Notes |
|---------|-------|-------|
| **tRPC** | 🟢 95% | Perfect Next.js companion, zero codegen type safety |
| **Hono** | 🟢 90% | TypeScript-first, multi-runtime, works with Vercel Edge |
| **NestJS** | 🟡 80% | TypeScript, but heavy framework |
| **Fastify** | 🟡 75% | Good perf, JSON Schema (not Zod) |
| **Express.js** | 🟡 65% | Mature but aging |
| **FastAPI** | 🔴 55% | Python, different ecosystem |
| **Django** | 🔴 45% | Python, full-stack competitor |

## Decision Guide

- **Building a Next.js SaaS?** → tRPC (end-to-end types) or Hono (API routes)
- **Need a separate backend service?** → NestJS (enterprise) or Hono (lightweight)
- **ML/AI microservice?** → FastAPI
- **Legacy Node.js?** → Fastify (Express replacement)
- **Full-stack Python with admin?** → Django
