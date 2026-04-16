# Zod

> TypeScript-first schema validation with static type inference

| Metric | Data |
|--------|------|
| GitHub | [colinhacks/zod](https://github.com/colinhacks/zod) |
| Stars | ~35,000 |
| License | MIT |
| Language | TypeScript |
| Last Updated | Active (v4.x in development) |
| Contributors | 300+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 92 | Industry standard for TS schema validation. v4 brings 2-7x performance boost, 50% smaller bundle, JSON Schema output. Zero dependencies. Compile-time + runtime type safety |
| E (Ecosystem) | 95 | 35k stars, integrated into everything: tRPC, React Hook Form, Astro, Hono, Elysia, Next.js server actions, Drizzle. npm 25M+ weekly downloads. Massive plugin ecosystem |
| M (Market) | 85 | De facto standard. Every new TypeScript project uses Zod. Competitors (Valibot, ArkType) exist but Zod's ecosystem moat is enormous. v4 addresses performance gap |
| C (Combo) | 95 | Essential building block. Used in: API validation, form validation, env vars, config files, AI function calling schemas, database schema inference. Works with everything in your stack |
| **Overall** | **92** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
The TypeScript ecosystem's universal schema language. Define a schema once, get runtime validation AND static types. Zod is to TypeScript what JSON Schema is to REST APIs — but better.

## Architecture Highlights
- **Zero dependencies** — Entire library is self-contained
- **Type inference** — `z.infer<typeof schema>` extracts TypeScript types from runtime schemas
- **Composable** — Schemas compose with `.merge()`, `.extend()`, `.pick()`, `.omit()`
- **v4 improvements** — New `z.interface()` for faster object validation, `@zod/mini` for minimal bundle
- Monorepo: zod (core), @zod/mini (treeshakeable), integrations

## Key Modules
1. **Core Schemas** — string/number/boolean/date/enum/union/intersection/tuple
2. **Object Schemas** — z.object() with .merge/.extend/.pick/.omit/.partial
3. **Transforms** — .transform(), .refine(), .superRefine() for custom logic
4. **Coercion** — z.coerce.string() for automatic type coercion
5. **JSON Schema** — z.toJSONSchema() (v4) for OpenAPI/JSON Schema generation

## Solo Dev Verdict
🟢 **Non-negotiable. Use it in every TypeScript project.** Zod is the foundation layer — API input validation, env var parsing, form validation, AI function schemas, config validation. The ecosystem integration is so deep that NOT using Zod creates friction. v4 fixes the only real complaint (performance).

## Anti-Pattern Warning
- v3 → v4 migration has breaking changes (plan ahead)
- Bundle size was a concern in v3 (fixed in v4 with @zod/mini)
- Over-engineering: don't create Zod schemas for internal-only types that don't cross trust boundaries
- Competitors (Valibot, ArkType) are faster for specific use cases
