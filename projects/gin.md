# Gin

> High-performance HTTP web framework for Go, featuring a Martini-like API with much better performance.

| Metric | Data |
|--------|------|
| GitHub | https://github.com/gin-gonic/gin |
| Stars | ~80,000+ |
| License | MIT |
| Language | Go |
| Last Update | Active (2026) |
| Contributors | 400+ |

## TEMC Score

| Dimension | Score | Weight | Reasoning |
|-----------|-------|--------|-----------|
| **T** Technology | 88 | 25% | Radix-tree routing, zero-allocation design, middleware chaining, JSON validation via binding tags, built-in crash recovery. Consistently benchmarks 2-5x faster than Express/FastAPI. |
| **E** Ecosystem | 85 | 20% | 80k+ Stars, 400+ contributors, massive Chinese + global community. Rich middleware ecosystem (CORS, auth, rate-limit, Swagger). De facto standard for Go web services. |
| **M** Market Timing | 78 | 30% | Mature and dominant in Go ecosystem. Not "new" but extremely stable. Go adoption in cloud-native/DevOps continues growing. Late-stage but still the default choice. |
| **C** Combinability | 80 | 25% | Pairs with GORM, Wire DI, Go-Redis, gRPC. Compiles to single binary = trivial Docker deployment. Good fit for microservices behind a Next.js/tRPC frontend. |
| **Composite** | **82.2** | | T×0.25 + E×0.20 + M×0.30 + C×0.25 = 22.0 + 17.0 + 23.4 + 20.0 |

## Architecture Highlights

- **Radix Tree Router**: O(log n) route matching, supports path params, wildcards, groups
- **Middleware Pipeline**: `Use()` → `Next()` chain, similar to Express but compiled Go speed
- **Context Object**: `gin.Context` carries request/response/params/bindings — single allocation per request
- **Binding & Validation**: Struct tags for JSON/XML/form binding with `go-playground/validator`
- **Recovery Middleware**: Built-in panic recovery, never crashes the server

```
gin/
├── gin.go            # Engine (router + middleware)
├── context.go        # Core Context object
├── routergroup.go    # Route grouping
├── tree.go           # Radix tree implementation
├── binding/          # JSON/XML/Form/Query binding
├── render/           # JSON/HTML/XML/YAML renderers
└── recovery.go       # Panic recovery middleware
```

## Key Strengths for Solo Dev

1. **Single binary deployment** — `go build` → one file → Docker scratch image < 20MB
2. **Goroutine concurrency** — handles 10k+ concurrent connections out of the box
3. **Type safety** — Go's compiler catches errors at build time
4. **Fast cold start** — ideal for serverless/cloud functions
5. **Battle-tested** — used by Alibaba, Tencent, ByteDance at massive scale

## Extracted Best Practices

- **Radix tree routing pattern** → `code-base/api/routing/radix-tree.md`
- **Middleware chaining design** → `code-base/api/middleware/chain-pattern.md`
- **Struct-tag validation pattern** → `code-base/api/validation/struct-tags.md`

## Competitor Comparison

| | Gin | Fiber | Echo | Chi |
|--|-----|-------|------|-----|
| Stars | 80k+ | 35k+ | 30k+ | 19k+ |
| Performance | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| API Style | Express-like | Express-like | Echo-style | stdlib-compatible |
| Maturity | Very High | Medium | High | High |
| Best For | General Go APIs | Max throughput | Clean API | stdlib purists |

## Solo Dev Verdict

**Best for**: Microservices, high-performance APIs, cloud-native backends when you need Go's speed + deployment simplicity. Pair with a TypeScript frontend (Next.js/tRPC) for full-stack.

**Skip if**: You're all-in on TypeScript (use Hono/Fastify instead) or need rapid prototyping (FastAPI is faster to write).
