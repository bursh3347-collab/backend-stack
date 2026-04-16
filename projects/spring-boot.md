# Spring Boot

> The industry-standard Java framework for building production-grade applications with minimal configuration.

| Metric | Data |
|--------|------|
| GitHub | https://github.com/spring-projects/spring-boot |
| Stars | ~76,000+ |
| License | Apache-2.0 |
| Language | Java / Kotlin |
| Last Update | Active (2026) |
| Contributors | 1,000+ |

## TEMC Score

| Dimension | Score | Weight | Reasoning |
|-----------|-------|--------|-----------|
| **T** Technology | 90 | 25% | Auto-configuration, embedded servers, actuator monitoring, native GraalVM compilation (Spring Boot 3+). Most mature backend framework in existence. Production-grade everything. |
| **E** Ecosystem | 95 | 20% | 76k+ Stars, largest enterprise Java ecosystem. Spring Security, Spring Data, Spring Cloud, Spring AI. 1000+ contributors. VMware/Broadcom backed. |
| **M** Market Timing | 65 | 30% | Dominant in enterprise but late-stage for new projects. Spring Boot 3 + GraalVM native is the renewal catalyst. Not trendy but pays the bills — 60%+ of enterprise Java backends. |
| **C** Combinability | 55 | 25% | Heavy JVM footprint doesn't fit solo dev/edge model. Cold start 2-5s (vs Go/Bun <100ms). Excellent for enterprise but overkill for Micro SaaS. Kotlin improves DX significantly. |
| **Composite** | **73.8** | | T×0.25 + E×0.20 + M×0.30 + C×0.25 = 22.5 + 19.0 + 19.5 + 13.75 |

## Architecture Highlights

- **Auto-Configuration**: Convention over configuration — add a dependency, Spring configures it
- **Starter POMs**: `spring-boot-starter-web`, `starter-data-jpa`, `starter-security` — curated dependency sets
- **Actuator**: Built-in health checks, metrics, thread dumps, environment info
- **Spring Native (GraalVM)**: AOT compilation → 50ms startup, 50MB memory (vs 2s/256MB JVM)
- **Spring AI**: Official AI/LLM integration — chat models, embeddings, vector stores, RAG

```
spring-boot-app/
├── src/main/java/
│   ├── Application.java        # @SpringBootApplication entry
│   ├── controller/             # REST controllers
│   ├── service/                # Business logic
│   ├── repository/             # Data access (JPA)
│   ├── config/                 # Security, CORS, etc.
│   └── model/                  # Entities & DTOs
├── src/main/resources/
│   └── application.yml         # Configuration
└── pom.xml / build.gradle      # Dependencies
```

## Key Strengths

1. **Enterprise standard** — 60%+ of Fortune 500 Java backends use Spring
2. **Spring Security** — most comprehensive auth/authz framework in any language
3. **Spring AI** — first-class AI/LLM support (OpenAI, Anthropic, Ollama, vector stores)
4. **Observability** — Actuator + Micrometer + distributed tracing out of the box
5. **GraalVM Native** — eliminates JVM cold start penalty for cloud/serverless

## Extracted Best Practices

- **Layered architecture pattern** (Controller→Service→Repository) → `best-practices/architecture.md`
- **Health check & actuator pattern** → `code-base/monitoring/health-check.md`
- **Spring Security filter chain** → reference for auth architecture design

## Competitor Comparison

| | Spring Boot | Quarkus | Micronaut | Ktor |
|--|-------------|---------|-----------|------|
| Stars | 76k+ | 14k+ | 6k+ | 13k+ |
| Language | Java/Kotlin | Java/Kotlin | Java/Kotlin | Kotlin |
| Startup | 2s (JVM) / 50ms (Native) | 50ms (Native) | 100ms | 200ms |
| Ecosystem | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ |
| Best For | Enterprise | Cloud-native | Microservices | Kotlin-first |

## Solo Dev Verdict

**Best for**: Enterprise contracts, Java shops, when you need Spring Security's depth, or when using Spring AI for LLM backends. Kotlin + Spring Boot 3 Native is the modern path.

**Skip if**: You're a solo dev building Micro SaaS — the JVM overhead and boilerplate don't justify the power for small projects. Use FastAPI/Hono/tRPC instead.
