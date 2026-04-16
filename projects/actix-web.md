# Actix Web

> A powerful, pragmatic, and extremely fast web framework for Rust.

| Metric | Data |
|--------|------|
| GitHub | https://github.com/actix/actix-web |
| Stars | ~22,000+ |
| License | MIT / Apache-2.0 |
| Language | Rust |
| Last Update | Active (2026) |
| Contributors | 400+ |

## TEMC Score

| Dimension | Score | Weight | Reasoning |
|-----------|-------|--------|-----------|
| **T** Technology | 95 | 25% | Consistently #1 or #2 in TechEmpower benchmarks. Memory-safe without GC. Async/await on Tokio runtime. Type-safe extractors, compile-time route checking. Zero-cost abstractions. |
| **E** Ecosystem | 72 | 20% | 22k+ Stars, strong Rust community. Good middleware ecosystem (actix-cors, actix-identity, actix-session). Limited compared to Express/Spring but growing. Rust adoption accelerating. |
| **M** Market Timing | 75 | 30% | Mid-stage. Rust backend adoption growing (Cloudflare, Discord, AWS use Rust). Not mainstream yet but "Rust for backends" trend is real. WASM compatibility is future catalyst. |
| **C** Combinability | 65 | 25% | Steep learning curve (Rust borrow checker). Excellent with Diesel/SQLx/SeaORM for DB. Compiles to tiny, fast binaries. Hard to integrate with JS/TS ecosystem directly. |
| **Composite** | **77.2** | | T×0.25 + E×0.20 + M×0.30 + C×0.25 = 23.75 + 14.4 + 22.5 + 16.25 |

## Architecture Highlights

- **Actor Model (optional)**: Originally built on Actix actor framework, now optional
- **Tokio Runtime**: Async I/O, work-stealing scheduler, zero-cost futures
- **Type-Safe Extractors**: `web::Path<>`, `web::Query<>`, `web::Json<>` — compile-time request parsing
- **Middleware System**: Tower-compatible, composable middleware layers
- **WebSocket & HTTP/2**: First-class support for real-time and modern protocols

```
actix-app/
├── src/
│   ├── main.rs            # HttpServer::new() + App::new()
│   ├── routes/            # Route handlers
│   ├── models/            # Serde-serializable structs
│   ├── db/                # Diesel/SQLx database layer
│   ├── middleware/         # Auth, logging, CORS
│   └── errors.rs          # Custom error types
├── Cargo.toml             # Dependencies
└── Dockerfile             # Multi-stage build → scratch
```

## Key Strengths

1. **Absolute peak performance** — #1-2 in TechEmpower, 600k+ req/s on commodity hardware
2. **Memory safety without GC** — no null pointers, no data races, guaranteed at compile time
3. **Tiny binaries** — 5-15MB release builds, minimal Docker images
4. **Type-safe everything** — routes, extractors, responses checked at compile time
5. **Security by default** — Rust's ownership model prevents entire classes of vulnerabilities

## Extracted Best Practices

- **Type-safe extractor pattern** → `code-base/api/extractors/type-safe-extractors.md`
- **Compile-time route validation** → reference for API design safety
- **Multi-stage Docker for Rust** → `code-base/deploy/rust-docker.md`

## Competitor Comparison

| | Actix Web | Axum | Rocket | Warp |
|--|-----------|------|--------|------|
| Stars | 22k+ | 20k+ | 24k+ | 10k+ |
| Performance | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| API Ergonomics | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| Tower Compatible | ✅ Yes | ✅ Native | ❌ No | ✅ Yes |
| Best For | Max perf | Modern Rust | Ergonomics | Functional |

## ⚠️ Key Trade-off

Rust's learning curve is steep. The borrow checker will slow you down initially. But once past the curve, you ship code that is both the fastest AND the most memory-safe.

## Solo Dev Verdict

**Best for**: Performance-critical services (real-time, high-frequency APIs, infrastructure), when security is paramount, or when you already know Rust. Excellent for backend services that need to handle extreme load.

**Skip if**: You're prototyping quickly (use FastAPI/Hono), or your team doesn't know Rust — the learning curve ROI only pays off for long-lived, performance-critical services.
