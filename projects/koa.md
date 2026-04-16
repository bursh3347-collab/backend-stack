# Koa

> Next generation web framework for Node.js, designed by the team behind Express.

| Metric | Data |
|--------|------|
| GitHub | https://github.com/koajs/koa |
| Stars | ~35,000+ |
| License | MIT |
| Language | JavaScript / TypeScript |
| Last Update | Active (2026) |
| Contributors | 200+ |

## TEMC Score

| Dimension | Score | Weight | Reasoning |
|-----------|-------|--------|-----------|
| **T** Technology | 80 | 25% | Elegant async/await middleware (upstream/downstream "onion" model). Minimal core (~600 LOC). No bundled middleware = pick exactly what you need. Modern ES2015+ design. |
| **E** Ecosystem | 78 | 20% | 35k+ Stars, created by Express team (TJ Holowaychuk). Large middleware ecosystem but fragmented. Not as actively maintained as Fastify/Hono. Stable but not growing fast. |
| **M** Market Timing | 62 | 30% | Late-stage. Express successor that never fully succeeded Express. Fastify and Hono have taken the "modern Node.js" crown. Still used but declining in new project adoption. |
| **C** Combinability | 75 | 25% | Full Node.js ecosystem access. Easy to pair with any ORM, template engine, or API layer. Good TypeScript support via @types/koa. Lightweight = embeddable in larger architectures. |
| **Composite** | **72.7** | | T×0.25 + E×0.20 + M×0.30 + C×0.25 = 20.0 + 15.6 + 18.6 + 18.75 |

## Architecture Highlights

- **Onion Model Middleware**: Request flows downstream through middleware, response flows back upstream
- **Context Object**: `ctx` wraps Node's req/res with convenience methods (ctx.body, ctx.status, ctx.query)
- **Minimal Core**: ~600 lines of code. No router, no body parser — add only what you need
- **Async/Await Native**: First major framework to embrace async/await (predates Express 5)
- **Error Handling**: Centralized try/catch in middleware — errors bubble up through the onion layers

```
koa-app/
├── app.js              # const app = new Koa()
├── routes/             # koa-router routes
├── middleware/          # Auth, logging, error handling
├── models/             # Data layer
├── package.json        # Dependencies
└── tsconfig.json       # TypeScript config (optional)
```

## Key Strengths

1. **Elegant middleware model** — the "onion" pattern is the cleanest middleware design in Node.js
2. **Minimal footprint** — only ~600 LOC, no bloat, no opinions
3. **Async/await pioneer** — cleaner error handling than Express's callback/next pattern
4. **Context design** — `ctx` object is a better abstraction than raw req/res
5. **Express team pedigree** — designed by the people who knew Express's mistakes

## Extracted Best Practices

- **Onion middleware pattern** → `code-base/api/middleware/onion-model.md`
- **Centralized error handling via middleware** → `best-practices/api-design.md`
- **Context wrapping pattern** → reference for custom framework design

## Competitor Comparison

| | Koa | Express | Fastify | Hono |
|--|-----|---------|---------|------|
| Stars | 35k+ | 67k+ | 36k+ | 30k+ |
| Core Size | ~600 LOC | ~2500 LOC | ~8000 LOC | ~5000 LOC |
| Middleware | Onion model | Linear | Hooks+Encapsulation | Linear |
| Performance | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| TypeScript | Via @types | Via @types | Native | Native |
| Best For | Minimalists | Legacy | Performance | Edge/Multi-runtime |

## ⚠️ Key Trade-off

Koa's minimalism means you assemble everything yourself — router, body parser, static files, sessions. This gives maximum control but requires more decisions upfront. Fastify/Hono give you more out of the box.

## Solo Dev Verdict

**Best for**: Developers who want maximum control over their middleware stack, elegant async patterns, and a minimal foundation. Good for learning how web frameworks work internally.

**Skip if**: You want batteries-included (use Fastify/NestJS) or edge/multi-runtime support (use Hono). For new projects in 2026, Hono or Fastify are better choices unless you have a specific reason for Koa.
