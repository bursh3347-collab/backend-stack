# tRPC

> End-to-end typesafe APIs made easy — move fast and break nothing.

| Metric | Data |
|------|------|
| GitHub | [trpc/trpc](https://github.com/trpc/trpc) |
| Stars | 39,986 |
| Forks | 1,578 |
| License | MIT |
| Language | TypeScript |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 93 | Zero-codegen type safety between client and server. TypeScript inference magic. Subscriptions, batching, middleware. v11 with RSC support. |
| E (Ecosystem) | 85 | 40k stars. Core of T3 Stack. Used by Cal.com (41k stars), Ping.gg. Active development. |
| M (Market) | 82 | Dominant in TypeScript full-stack world. The answer to "REST vs GraphQL" for TypeScript teams. |
| C (Combo) | 92 | **Perfect for base stack**: Next.js + tRPC = end-to-end type safety. Replaces REST/GraphQL complexity. |
| **Overall** | **87.8** | |

## Core Value

- **Zero codegen**: Types flow from server to client automatically
- **End-to-end type safety**: Change server → TypeScript catches client errors
- **No schema definition**: No .proto, no .graphql, no OpenAPI spec needed
- **React Query integration**: Built-in data fetching with caching
- **Middleware**: Authentication, logging, rate limiting
- **Batching**: Multiple requests in single HTTP call

```typescript
// Server
const appRouter = router({
  user: router({
    get: publicProcedure
      .input(z.object({ id: z.string() }))
      .query(({ input }) => db.user.findUnique({ where: { id: input.id } })),
  }),
})

// Client — fully typed, zero codegen
const user = trpc.user.get.useQuery({ id: '1' })
```

## Risks

- TypeScript-only (no polyglot backend support)
- Tight coupling between client and server
- Not suitable for public APIs (use REST/GraphQL instead)
- Some complexity with SSR/RSC integration
