# NestJS

> A progressive Node.js framework for building efficient, scalable, enterprise-grade server-side applications with TypeScript.

| Metric | Data |
|------|------|
| GitHub | [nestjs/nest](https://github.com/nestjs/nest) |
| Stars | 75,211 |
| Forks | 8,288 |
| License | MIT |
| Language | TypeScript |
| Open Issues | 42 |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 92 | Angular-inspired architecture (modules, controllers, providers). Decorator-based. Built-in DI, guards, interceptors, pipes. Microservices support. |
| E (Ecosystem) | 90 | 75k stars, 8.3k forks. Enterprise adoption (SAP, Roche, Adidas). Active maintainer team. Only 42 open issues = excellent maintenance. |
| M (Market) | 85 | Dominant TypeScript backend framework. Strong in enterprise. Growing Node.js backend market. |
| C (Combo) | 82 | TypeScript backend matching base stack language. Pairs with Next.js for separate backend service. |
| **Overall** | **87.0** | |

## Core Value

- **TypeScript-first**: Full type safety end-to-end
- **Modular architecture**: Modules, Controllers, Services (Angular-style)
- **Built-in DI**: Dependency injection container
- **Decorators**: `@Controller()`, `@Get()`, `@Injectable()`
- **Microservices**: gRPC, MQTT, Redis, NATS, Kafka transports
- **GraphQL**: First-class support
- **WebSockets**: Built-in gateway
- **Testing**: Integrated testing utilities

## Risks

- Heavy framework — overkill for simple APIs
- Angular-style patterns unfamiliar to React developers
- Decorator-heavy code can be verbose
- Steeper learning curve than Express/Hono

## 天子点评

企业级过重，一人公司日常用不到。42个open issues说明维护质量极高。但如果未来接B2B外包或需要独立后端服务（比如多租户SaaS的复杂权限系统），NestJS是最成熟的TypeScript后端框架，值得储备知识。
