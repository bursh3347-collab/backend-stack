# ⚙️ backend-stack

> ⭐ Maturity: L1 Growing

Extracted best practices and analysis from top backend frameworks on GitHub. Part of the [Open Source Knowledge Restructuring Project](https://github.com/bursh3347-collab).

## 📊 Project Rankings

| Rank | Project | Stars | TEMC | Language | Best For |
|------|---------|-------|------|----------|----------|
| 1 | [tRPC](projects/trpc.md) | 40k | **87.8** | TypeScript | End-to-end type safety |
| 2 | [Hono](projects/hono.md) | 25k | **87.3** | TypeScript | Edge, multi-runtime |
| 3 | [NestJS](projects/nestjs.md) | 75k | **87.0** | TypeScript | Enterprise backend |
| 4 | [FastAPI](projects/fastapi.md) | 85k | **85.3** | Python | ML/AI APIs |
| 5 | [Fastify](projects/fastify.md) | 36k | **80.6** | JS/TS | High-perf Node.js |
| 6 | [Express.js](projects/expressjs.md) | 67k | **78.3** | JavaScript | Legacy, simple |
| 7 | [Django](projects/django.md) | 84k | **74.3** | Python | Full-stack Python |

## 🏆 Recommended for One-Person Company

```
Primary: tRPC (with Next.js) — zero-codegen type safety
API layer: Hono — for standalone API routes or edge functions
ML/AI service: FastAPI — when you need Python ML libraries
```

## 📂 Structure

```
backend-stack/
├── projects/                      # Individual project analyses
├── best-practices/
│   ├── api-design.md              # API design patterns
│   └── microservices-patterns.md  # When to split, how to communicate
├── comparison.md                  # Horizontal comparison
├── SOURCES.md
└── README.md
```

## License

Analysis content: MIT. Individual projects retain their original licenses.
