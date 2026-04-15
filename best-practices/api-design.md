# API Design Best Practices

> Synthesized from FastAPI, tRPC, Hono, NestJS, and Fastify patterns.

## 1. Type-Safe API Pattern Comparison

| Approach | How | Codegen? | Best For |
|----------|-----|----------|----------|
| **tRPC** | TypeScript inference | No | Full-stack TypeScript |
| **FastAPI** | Python type hints → OpenAPI | Auto | Python APIs |
| **Hono RPC** | TypeScript inference | No | Multi-runtime APIs |
| **GraphQL** | Schema definition | Optional | Complex data graphs |
| **REST + Zod** | Manual validation | No | Simple APIs |

## 2. Request Validation

Always validate at the boundary:

```typescript
// Hono + Zod
app.post('/users', zValidator('json', z.object({
  name: z.string().min(1),
  email: z.string().email(),
})), (c) => { /* typed input */ })

// tRPC
publicProcedure
  .input(z.object({ name: z.string(), email: z.string().email() }))
  .mutation(({ input }) => { /* typed input */ })
```

## 3. Error Handling Pattern

```typescript
// Consistent error response shape
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Email is required",
    "details": [{ "field": "email", "message": "Required" }]
  }
}
```

## 4. API Versioning

- **URL path**: `/api/v1/users` — simplest, most common
- **Header**: `Accept-Version: v1` — cleaner URLs
- **tRPC approach**: No versioning needed (types enforce compatibility)

## 5. Rate Limiting

Apply at 3 levels:
1. **Global**: 100 req/min per IP (prevent DDoS)
2. **Endpoint**: 10 req/min for expensive operations
3. **User**: 1000 req/hour per authenticated user
