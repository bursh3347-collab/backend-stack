![Stars](https://img.shields.io/github/stars/bursh3347-collab/backend-stack?style=flat-square)
![License](https://img.shields.io/github/license/bursh3347-collab/backend-stack?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/bursh3347-collab/backend-stack?style=flat-square)

[English](README.md) | [中文](README_CN.md)

# ⚙️ backend-stack

> ⭐ Maturity: L1 Growing

Top backend frameworks deep-dived, compared, and scored using the **TEMC framework** (Technology · Ecosystem · Market Timing · Combinability). Extracted best practices and architecture analysis from 7 high-star projects on GitHub.

Part of the [Open Source Knowledge Restructuring Project](https://github.com/bursh3347-collab).

## 📈 Trending This Week (Updated: 2026-04-15)

| Rank | Project | Stars | Weekly Δ | Trend |
|------|---------|-------|----------|-------|
| 1 | [FastAPI](https://github.com/fastapi/fastapi) | 97,240 | +700 | 🚀 |
| 2 | [Django](https://github.com/django/django) | 87,271 | +300 | → |
| 3 | [NestJS](https://github.com/nestjs/nest) | 75,211 | +350 | ↑ |
| 4 | [Express.js](https://github.com/expressjs/express) | 68,941 | +200 | → |
| 5 | [tRPC](https://github.com/trpc/trpc) | 39,986 | +250 | ↑ |
| 6 | [Fastify](https://github.com/fastify/fastify) | 36,050 | +200 | → |
| 7 | [Hono](https://github.com/honojs/hono) | 29,951 | +500 | 🚀 |

## 📊 Project Rankings (by TEMC Score)

| Rank | Project | Stars | TEMC | Language | Best For |
|------|---------|-------|------|----------|----------|
| 1 | [tRPC](projects/trpc.md) | 40.0k | **87.8** | TypeScript | End-to-end type safety |
| 2 | [Hono](projects/hono.md) | 30.0k | **87.3** | TypeScript | Edge, multi-runtime |
| 3 | [NestJS](projects/nestjs.md) | 75.2k | **87.0** | TypeScript | Enterprise backend |
| 4 | [FastAPI](projects/fastapi.md) | 97.2k | **85.3** | Python | ML/AI APIs |
| 5 | [Fastify](projects/fastify.md) | 36.1k | **80.6** | JS/TS | High-perf Node.js |
| 6 | [Express.js](projects/expressjs.md) | 68.9k | **78.3** | JavaScript | Legacy, simple |
| 7 | [Django](projects/django.md) | 87.3k | **74.3** | Python | Full-stack Python |

> **TEMC** = Technology (25%) + Ecosystem (20%) + Market Timing (30%) + Combinability (25%)

## 🏆 Solo Dev Verdict

```
Primary:    tRPC (with Next.js) — zero-codegen type safety
API layer:  Hono — for standalone API routes or edge functions
ML/AI:      FastAPI — when you need Python ML libraries
```

## 📂 Structure

```
backend-stack/
├── projects/                      # Individual project deep-dives
│   ├── trpc.md
│   ├── hono.md
│   ├── nestjs.md
│   ├── fastapi.md
│   ├── fastify.md
│   ├── expressjs.md
│   └── django.md
├── best-practices/
│   ├── api-design.md              # API design patterns
│   └── microservices-patterns.md  # When to split, how to communicate
├── comparison.md                  # Horizontal comparison table
├── roadmap.md                     # Backend tech trends & predictions
├── CONTRIBUTING.md
├── SOURCES.md
└── README.md
```

## 📝 How to Use

1. **Compare** — Start with [comparison.md](comparison.md) to see all frameworks side-by-side
2. **Deep-dive** — Read the analysis for your chosen framework in `projects/`
3. **Apply** — Use patterns from `best-practices/` in your own project
4. **Stay current** — Check [roadmap.md](roadmap.md) for where the ecosystem is heading

## License

Analysis content: MIT. Individual projects retain their original licenses.
