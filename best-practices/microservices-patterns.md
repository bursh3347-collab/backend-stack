# Microservices Patterns

> When to split, how to communicate, and common pitfalls.

## Decision: Monolith vs Microservices

```
Team size < 5?           → Monolith (always)
Single deployment unit?  → Monolith
Different scaling needs? → Consider microservices
Different tech stacks?   → Microservices (e.g., Python ML + TypeScript API)
Independent releases?    → Microservices
```

**For one-person company**: Always start monolith. Split only when forced.

## The "Micro SaaS Backend" Architecture

For a one-person company, the optimal backend isn't microservices — it's:

```
Next.js (main app)
  ├── API Routes / tRPC   → Business logic
  ├── Server Actions      → Form mutations
  └── Edge Functions      → Lightweight processing

External Services (managed)
  ├── Supabase            → Database + Auth + Storage
  ├── Stripe              → Payments
  ├── Resend/Postmark     → Email
  └── Vercel              → Hosting + CDN + Edge

Optional: Separate API (when needed)
  └── Hono / FastAPI      → ML service, heavy processing
```

**Philosophy**: Use managed services for everything except core business logic. Your time is the scarcest resource.

## Communication Patterns

| Pattern | When | Tool |
|---------|------|------|
| Direct HTTP | Simple request-response | tRPC, Hono, fetch |
| Background Jobs | Async processing | Inngest, Trigger.dev |
| Webhooks | Event notification | Svix, custom |
| Message Queue | High-throughput async | Redis, SQS |
| Event Streaming | Real-time data flow | Kafka (rarely needed) |

## For One-Person Company

> "The best microservice is the one you don't have to operate."

Use managed services (Supabase, Stripe, Vercel) as your "microservices". You get the benefits of separation without the operational overhead.
