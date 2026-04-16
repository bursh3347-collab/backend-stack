# Fiber

> Express-inspired web framework built on top of Fasthttp, the fastest HTTP engine for Go.

| Metric | Data |
|--------|------|
| GitHub | https://github.com/gofiber/fiber |
| Stars | ~35,000+ |
| License | MIT |
| Language | Go |
| Last Update | Active (2026) |
| Contributors | 200+ |

## TEMC Score

| Dimension | Score | Weight | Reasoning |
|-----------|-------|--------|-----------|
| **T** Technology | 90 | 25% | Built on Fasthttp (10x faster than net/http). Zero-allocation routing, prefork mode, WebSocket, rate limiting, CSRF built-in. Fiber v3 adds generics + improved middleware. |
| **E** Ecosystem | 78 | 20% | 35k+ Stars, growing fast. 50+ official middleware packages. Strong community but smaller than Gin. Good docs, active Discord. |
| **M** Market Timing | 82 | 30% | Mid-stage growth. Captures Express.js developers moving to Go. Fiber v3 is the maturity catalyst. Performance-first trend in backend aligns perfectly. |
| **C** Combinability | 82 | 25% | Express-like API = lowest learning curve for JS/TS devs moving to Go. Pairs with GORM, Ent, go-redis. Single binary deployment. Excellent for API microservices behind Next.js. |
| **Composite** | **83.6** | | T×0.25 + E×0.20 + M×0.30 + C×0.25 = 22.5 + 15.6 + 24.6 + 20.5 |

## Architecture Highlights

- **Fasthttp Engine**: Doesn't use `net/http` — custom HTTP parser, worker pool, zero-copy buffers
- **Express-Compatible API**: `app.Get()`, `app.Post()`, `app.Use()` — familiar to JS developers
- **Prefork Mode**: Spawns multiple processes (one per CPU core) for maximum throughput
- **Built-in Middleware**: 50+ packages — CORS, compress, cache, limiter, logger, monitor, session
- **Fiber v3**: Generics support, improved routing, better error handling

```
fiber-app/
├── main.go              # app := fiber.New() + routes
├── handlers/            # Route handlers
├── middleware/           # Custom middleware
├── models/              # Data models
├── config/              # App configuration
└── go.mod               # Dependencies
```

## Key Strengths for Solo Dev

1. **Fastest Go framework** — Fasthttp benchmarks 2-3x faster than Gin in raw throughput
2. **Express-like API** — JS developers feel at home immediately
3. **50+ built-in middleware** — rate limiting, CSRF, session, cache all included
4. **Prefork mode** — saturate all CPU cores with one flag
5. **Monitor middleware** — built-in `/metrics` dashboard for observability

## Extracted Best Practices

- **Prefork concurrency pattern** → `code-base/deploy/prefork-pattern.md`
- **Zero-copy buffer design** → reference for high-performance networking
- **Express-to-Go migration pattern** → `best-practices/migration/express-to-fiber.md`

## Competitor Comparison

| | Fiber | Gin | Echo | Chi |
|--|-------|-----|------|-----|
| Stars | 35k+ | 80k+ | 30k+ | 19k+ |
| HTTP Engine | Fasthttp | net/http | net/http | net/http |
| Raw Speed | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| Express-like | ✅ Yes | ✅ Partial | ❌ No | ❌ No |
| stdlib Compatible | ❌ No | ✅ Yes | ✅ Yes | ✅ Yes |
| Best For | Max perf + JS devs | General purpose | Clean API | stdlib fans |

## ⚠️ Key Trade-off

Fiber uses Fasthttp which is **not compatible with `net/http`** — you can't use standard Go HTTP middleware or handlers directly. This is the price of speed. Gin/Chi use `net/http` and are stdlib-compatible.

## Solo Dev Verdict

**Best for**: JS/Express developers who want Go performance without learning a new API paradigm. Maximum throughput APIs, real-time services, high-concurrency microservices.

**Skip if**: You need stdlib compatibility (use Gin/Chi) or your team is already comfortable with Gin's conventions.
