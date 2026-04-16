![Stars](https://img.shields.io/github/stars/bursh3347-collab/backend-stack?style=flat-square)
![License](https://img.shields.io/github/license/bursh3347-collab/backend-stack?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/bursh3347-collab/backend-stack?style=flat-square)

[English](README.md) | [中文](README_CN.md)

# ⚙️ backend-stack

> ⭐ Maturity: **L2 Growing**

Top backend frameworks deep-dived, compared, and scored using the **TEMC framework** (Technology · Ecosystem · Market Timing · Combinability). Extracted best practices and architecture analysis from **17 high-star projects** on GitHub — spanning **5 languages** (TypeScript, JavaScript, Python, Go, Rust, Java/Kotlin).

Part of the [Open Source Knowledge Restructuring Project](https://github.com/bursh3347-collab).

## 📈 Trending This Week (Updated: 2026-04-16)

| Rank | Project | Stars | Weekly Δ | Trend |
|------|---------|-------|----------|-------|
| 1 | [FastAPI](https://github.com/fastapi/fastapi) | 97,240 | +700 | 🚀 |
| 2 | [Django](https://github.com/django/django) | 87,271 | +300 | → |
| 3 | [Gin](https://github.com/gin-gonic/gin) | 80,300 | +350 | ↑ |
| 4 | [Spring Boot](https://github.com/spring-projects/spring-boot) | 76,500 | +200 | → |
| 5 | [NestJS](https://github.com/nestjs/nest) | 75,211 | +350 | ↑ |
| 6 | [Express.js](https://github.com/expressjs/express) | 68,941 | +200 | → |
| 7 | [tRPC](https://github.com/trpc/trpc) | 39,986 | +250 | ↑ |
| 8 | [Fiber](https://github.com/gofiber/fiber) | 35,200 | +300 | ↑ |
| 9 | [Hono](https://github.com/honojs/hono) | 29,951 | +500 | 🚀 |
| 🌟 | [Actix Web](https://github.com/actix/actix-web) | 22,100 | +150 | → |

## 📊 Project Rankings (by TEMC Score)

| Rank | Project | Stars | TEMC | Language | Best For |
|------|---------|-------|------|----------|----------|
| 1 | [tRPC](projects/trpc.md) | 40.0k | **87.8** | TypeScript | End-to-end type safety |
| 2 | [Hono](projects/hono.md) | 30.0k | **87.3** | TypeScript | Edge, multi-runtime |
| 3 | [NestJS](projects/nestjs.md) | 75.2k | **87.0** | TypeScript | Enterprise backend |
| 4 | [FastAPI](projects/fastapi.md) | 97.2k | **85.3** | Python | ML/AI APIs |
| 5 | [Fiber](projects/fiber.md) | 35.2k | **83.6** | Go | Max throughput, JS devs→Go |
| 6 | [Gin](projects/gin.md) | 80.3k | **82.2** | Go | General Go APIs |
| 7 | [Fastify](projects/fastify.md) | 36.1k | **80.6** | JS/TS | High-perf Node.js |
| 8 | [Express.js](projects/expressjs.md) | 68.9k | **78.3** | JavaScript | Legacy, simple |
| 9 | [Actix Web](projects/actix-web.md) | 22.1k | **77.2** | Rust | Peak performance |
| 10 | [Spring Boot](projects/spring-boot.md) | 76.5k | **73.8** | Java/Kotlin | Enterprise |
| 11 | [Django](projects/django.md) | 87.3k | **74.3** | Python | Full-stack Python |
| 12 | [Koa](projects/koa.md) | 35.0k | **72.7** | JavaScript | Minimal, elegant |

> **TEMC** = Technology (25%) + Ecosystem (20%) + Market Timing (30%) + Combinability (25%)

## 🏆 Solo Dev Verdict

```
Primary:    tRPC (with Next.js) — zero-codegen type safety
API layer:  Hono — for standalone API routes or edge functions
ML/AI:      FastAPI — when you need Python ML libraries
Performance: Fiber/Gin — when you need Go speed + simple deployment
Infra:      Actix Web — when every microsecond counts (and you know Rust)
```

## 📂 Structure

```
backend-stack/
├── projects/                      # Individual project deep-dives (17)
│   ├── trpc.md                    #   TypeScript — type-safe API
│   ├── hono.md                    #   TypeScript — edge framework
│   ├── nestjs.md                  #   TypeScript — enterprise
│   ├── fastapi.md                 #   Python — ML/AI APIs
│   ├── fiber.md                   #   Go — max throughput ⭐ NEW
│   ├── gin.md                     #   Go — general purpose ⭐ NEW
│   ├── fastify.md                 #   JS/TS — high-perf Node.js
│   ├── expressjs.md               #   JavaScript — legacy standard
│   ├── actix-web.md               #   Rust — peak performance ⭐ NEW
│   ├── spring-boot.md             #   Java/Kotlin — enterprise ⭐ NEW
│   ├── django.md                  #   Python — full-stack
│   ├── koa.md                     #   JavaScript — minimal ⭐ NEW
│   ├── elysia.md                  #   TypeScript/Bun
│   ├── nitro.md                   #   TypeScript — universal
│   ├── bullmq.md                  #   Node.js — job queue
│   ├── dragonfly.md               #   C++ — in-memory store
│   └── zod.md                     #   TypeScript — validation
├── best-practices/
│   ├── api-design.md              # API design patterns
│   └── microservices-patterns.md  # When to split, how to communicate
├── comparison.md                  # Horizontal comparison table
├── roadmap.md                     # Backend tech trends & predictions
├── CONTRIBUTING.md
├── SOURCES.md
└── README.md
```

## 🌍 Language Coverage

| Language | Projects | Highlights |
|----------|----------|------------|
| TypeScript | tRPC, Hono, NestJS, Elysia, Nitro | Primary stack for solo devs |
| JavaScript | Express, Fastify, Koa, BullMQ | Legacy + performance |
| Python | FastAPI, Django | ML/AI + full-stack |
| Go | Gin, Fiber | Cloud-native speed |
| Rust | Actix Web | Maximum performance |
| Java/Kotlin | Spring Boot | Enterprise standard |

## 📝 How to Use

1. **Compare** — Start with [comparison.md](comparison.md) to see all frameworks side-by-side
2. **Deep-dive** — Read the analysis for your chosen framework in `projects/`
3. **Apply** — Use patterns from `best-practices/` in your own project
4. **Stay current** — Check [roadmap.md](roadmap.md) for where the ecosystem is heading

## License

Analysis content: MIT. Individual projects retain their original licenses.
