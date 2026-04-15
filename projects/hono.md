# Hono

> Ultrafast web framework for the Edges — works on Cloudflare Workers, Deno, Bun, Node.js, and more.

| Metric | Data |
|------|------|
| GitHub | [honojs/hono](https://github.com/honojs/hono) |
| Stars | ~25,000 |
| License | MIT |
| Language | TypeScript |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 92 | TypeScript-first. Multi-runtime (Node, Deno, Bun, Workers, Lambda). Tiny (~14kb). RPC mode for type-safe client. Zod OpenAPI middleware. |
| E (Ecosystem) | 78 | 25k stars, growing rapidly. Used by Cloudflare, Supabase. Active Japanese developer community. |
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
