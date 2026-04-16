# Nitro

> Build and Deploy Universal JavaScript Servers — The engine powering Nuxt, Analog, and more

| Metric | Data |
|--------|------|
| GitHub | [unjs/nitro](https://github.com/unjs/nitro) |
| Stars | ~6,000 |
| License | MIT |
| Language | TypeScript |
| Last Updated | Active (v3.x, daily commits) |
| Contributors | 300+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 88 | Universal deployment to 20+ providers (Vercel/CF Workers/AWS Lambda/Deno/Bun/Node). Auto-imports, file-based routing, built-in storage/cache/database/tasks. Rollup+Rolldown bundling |
| E (Ecosystem) | 80 | Powers Nuxt 3 (57k stars) and Analog. Part of unjs ecosystem (h3, unstorage, ofetch). 300+ contributors. Growing independent usage beyond Nuxt |
| M (Market) | 70 | Universal server engine is a growing category. Competes with Hono for edge-first servers. Nuxt backing ensures longevity but independent adoption still building |
| C (Combo) | 72 | Works with Vercel/Cloudflare. Good for API routes, serverless functions. But Next.js users typically don't need Nitro (they have Next.js API routes). Best for Nuxt or standalone |
| **Overall** | **76** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Write once, deploy everywhere. Nitro abstracts away deployment differences between Node.js, Deno, Bun, Cloudflare Workers, AWS Lambda, Vercel, and 15+ more targets. The h3 HTTP framework underneath is ultralight.

## Architecture Highlights
- **h3** — Ultralight HTTP framework (zero-dependency, Web Standard compatible)
- **Universal presets** — 20+ deployment targets from one codebase
- **Auto-imports** — No import statements needed for common utilities
- **File-based routing** — Convention-over-configuration API routes
- **Built-in primitives** — Storage (unstorage), caching (ocache), database (db0), tasks, WebSocket (crossws)
- **Dual bundler** — Rollup + Rolldown (Rust-based) support

## Key Modules
1. **Runtime** — h3-based server with auto-imports and middleware
2. **Builder** — Rollup/Rolldown bundler with preset-specific optimizations
3. **Storage** — Universal key-value via unstorage (memory/fs/Redis/S3/CF KV)
4. **Database** — db0 connector (SQLite/PostgreSQL/MySQL/D1/Turso)
5. **Tasks** — Built-in task scheduler (cron-like)

## Solo Dev Verdict
🟡 **Excellent tech, situational fit.** If you're building with Nuxt or need truly universal deployment (same code on Lambda AND CF Workers AND Node), Nitro is unbeatable. For Next.js stack users, the value is studying its architecture patterns (h3 is worth learning). The unstorage/db0 abstractions are extractable gems.

## Anti-Pattern Warning
- Primarily designed as Nuxt's server engine, standalone docs still catching up
- Next.js users have overlapping functionality in Next.js API routes
- Smaller community for standalone usage vs Hono or Fastify
- v3 is beta, API may still shift
