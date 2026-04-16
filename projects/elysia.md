# ElysiaJS

> Ergonomic Framework for Humans — Bun-native web framework with end-to-end type safety

| Metric | Data |
|--------|------|
| GitHub | [elysiajs/elysia](https://github.com/elysiajs/elysia) |
| Stars | ~12,000 |
| License | MIT |
| Language | TypeScript (Bun-native) |
| Last Updated | Active (v1.4.28) |
| Contributors | 100+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 88 | Bun-native performance (21x faster than Express benchmarks), end-to-end type inference without codegen, multi-runtime adapters (Bun/Node/CF Workers), plugin ecosystem with OpenAPI auto-gen |
| E (Ecosystem) | 72 | 12k stars growing fast, active Discord, but ecosystem smaller than Express/Fastify. Plugin library expanding (Swagger, JWT, CORS, GraphQL) |
| M (Market) | 78 | Bun adoption accelerating in 2026, Elysia is THE Bun framework. Edge/serverless trend favors lightweight runtimes. Still niche vs Node.js mainstream |
| C (Combo) | 85 | Perfect Bun companion for solo dev. Works with Cloudflare Workers. Eden treaty = tRPC-like e2e types. Zod/Valibot/ArkType validation built-in |
| **Overall** | **81** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
The fastest TypeScript web framework with the best developer experience. Elysia achieves Express-like simplicity with Fastify-level performance, plus end-to-end type safety that rivals tRPC — all native to Bun runtime.

## Architecture Highlights
- **Sucrose** — Custom static analysis for compile-time route optimization
- **Multi-runtime adapters** — Bun (primary), Node.js, Cloudflare Workers, Web Standard
- **Eden Treaty** — End-to-end type-safe client (like tRPC but for REST)
- **Type-level route validation** — Schema defined once, types flow everywhere
- Minimal dependencies: cookie, memoirist (router), fast-decode-uri-component

## Key Modules
1. **Core Router** (memoirist) — Radix-tree based, compile-time optimized
2. **Type System** — Custom type inference engine, supports TypeBox/Zod/Valibot/ArkType
3. **WebSocket** — Native Bun WebSocket with typed events
4. **Adapter Layer** — Bun/Node/CF Workers/Web Standard abstraction
5. **Plugin System** — Composable plugins with type propagation

## Solo Dev Verdict
🟢 **Strong pick for Bun-first projects.** If you're building a new API and willing to commit to Bun runtime, Elysia gives you the best DX + performance combo. The Eden Treaty makes it a viable tRPC alternative for REST APIs. Risk: Bun ecosystem still maturing.

## Anti-Pattern Warning
- Bun lock-in (though Node adapter exists, it's not the primary target)
- Smaller ecosystem than Express/Fastify for middleware
- Type inference can slow down IDE on very large projects
