# Hono

> Ultrafast web framework for the Edges — works on Cloudflare Workers, Deno, Bun, Node.js, and more.

| Metric | Data |
|------|------|
| GitHub | [honojs/hono](https://github.com/honojs/hono) |
| Stars | 29,951 |
| License | MIT |
| Language | TypeScript |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 92 | TypeScript-first. Multi-runtime (Node, Deno, Bun, Workers, Lambda). Tiny (~14kb). RPC mode for type-safe client. Zod OpenAPI middleware. |
| E (Ecosystem) | 78 | 30k stars, growing rapidly (+500/week). Used by Cloudflare, Supabase. Active Japanese developer community. |
| M (Market) | 85 | The rising star of backend frameworks. Perfect for edge computing, serverless, API routes. |
| C (Combo) | 90 | TypeScript, works with Next.js (API routes replacement), Vercel Edge, Supabase Edge Functions. **Best match for base stack as API layer**. |
| **Overall** | **87.3** | |

## Core Value

- **Multi-runtime**: One codebase runs everywhere
- **TypeScript-first**: Full type inference
- **Tiny**: ~14kb, no dependencies
- **RPC mode**: Type-safe client-server communication
- **Middleware**: 30+ built-in middlewares
- **Zod OpenAPI**: Auto-generate API docs
- **Web Standards**: Uses Web Standard APIs (Request, Response)

## Risks

- Younger project, less battle-tested than Express
- Smaller middleware ecosystem
- Some edge runtime limitations (no filesystem, etc.)

## 天子点评

Edge和Serverless场景的最佳选择。14kb极致轻量，多运行时支持。周增500 Stars = 增长最快的后端框架。当Next.js API Routes不够用时（比如需要独立微服务或Supabase Edge Functions），Hono是完美补充。
