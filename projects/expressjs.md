# Express.js

> Fast, unopinionated, minimalist web framework for Node.js — the most mature and widely-used.

| Metric | Data |
|------|------|
| GitHub | [expressjs/express](https://github.com/expressjs/express) |
| Stars | 68,941 |
| License | MIT |
| Language | JavaScript |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 72 | Simple middleware pattern. Battle-tested. But aging: no built-in TypeScript, no async error handling, callbacks-oriented. Express 5 long-delayed. |
| E (Ecosystem) | 95 | 69k stars. The foundation of Node.js web development. Massive middleware ecosystem (10,000+ packages). |
| M (Market) | 78 | Still the most used Node.js framework but losing ground to Fastify, Hono, NestJS for new projects. |
| C (Combo) | 70 | JavaScript-first (not TypeScript). Next.js API routes replace Express for most use cases. |
| **Overall** | **78.3** | |

## Core Value

- **Simplicity**: Minimalist API, easy to learn
- **Middleware ecosystem**: Thousands of middleware packages
- **Battle-tested**: 14+ years in production
- **Flexibility**: Unopinionated, use what you want

## Risks

- Aging architecture (callback-based core)
- No built-in TypeScript support
- Express 5 perpetually delayed
- Being replaced by Fastify/Hono for new projects

## 天子点评

遗产项目维护用。69k Stars是历史积累，不是当前热度。新项目不推荐——没有内置TypeScript支持、没有async错误处理、Express 5遥遥无期。Next.js API Routes或Hono完全取代Express的场景。读别人代码时需要懂，自己写不用选。
