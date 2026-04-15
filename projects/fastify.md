# Fastify

> Fast and low overhead web framework for Node.js — up to 2x faster than Express.

| Metric | Data |
|------|------|
| GitHub | [fastify/fastify](https://github.com/fastify/fastify) |
| Stars | 36,049 |
| Forks | 2,653 |
| License | MIT |
| Language | JavaScript/TypeScript |
| Open Issues | 125 |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 88 | Schema-based validation (JSON Schema), plugin system, hooks lifecycle, TypeScript support. 2x faster than Express. |
| E (Ecosystem) | 82 | 36k stars. Used by companies like Microsoft, Uber. 200+ official and community plugins. |
| M (Market) | 78 | Strong alternative to Express. Growing in enterprise. Losing some mindshare to Hono for edge. |
| C (Combo) | 75 | TypeScript support good but not TypeScript-first like Hono. JSON Schema validation differs from Zod ecosystem. |
| **Overall** | **80.6** | |

## Core Value

- **Performance**: 2x faster than Express, benchmarked
- **Plugin system**: Encapsulated, composable plugins
- **Schema validation**: JSON Schema for request/response validation
- **Hooks**: Request lifecycle hooks (onRequest, preSerialization, etc.)
- **Decorators**: Extend request/reply objects
- **Logging**: Built-in Pino logging

## Risks

- JSON Schema-based (not Zod) — different from TypeScript ecosystem trend
- Plugin encapsulation can be confusing initially
- Losing edge/serverless mindshare to Hono
