[English](README.md) | [中文](README_CN.md)

# ⚙️ backend-stack

> ⭐ 成熟度: L1 成长期

对 GitHub 上顶级后端框架的深度拆解、横向对比与 **TEMC 评分**（技术 · 生态 · 时机 · 组合）。从 7 个高星项目中提取最佳实践与架构分析。

属于 [GitHub 开源知识重组工程](https://github.com/bursh3347-collab) 的一部分。

## 📈 本分类飙升榜（最近更新：2026-04-15）

| 排名 | 项目 | 总Stars | 周增 | 趋势 |
|------|------|---------|------|------|
| 1 | [FastAPI](https://github.com/fastapi/fastapi) | 97,240 | +700 | 🚀 |
| 2 | [Django](https://github.com/django/django) | 87,271 | +300 | → |
| 3 | [NestJS](https://github.com/nestjs/nest) | 75,211 | +350 | ↑ |
| 4 | [Express.js](https://github.com/expressjs/express) | 68,941 | +200 | → |
| 5 | [tRPC](https://github.com/trpc/trpc) | 39,986 | +250 | ↑ |
| 6 | [Fastify](https://github.com/fastify/fastify) | 36,050 | +200 | → |
| 7 | [Hono](https://github.com/honojs/hono) | 29,951 | +500 | 🚀 |

## 📊 项目排名（按 TEMC 评分）

| 排名 | 项目 | Stars | TEMC | 语言 | 最适场景 |
|------|------|-------|------|------|----------|
| 1 | [tRPC](projects/trpc.md) | 40.0k | **87.8** | TypeScript | 端到端类型安全 |
| 2 | [Hono](projects/hono.md) | 30.0k | **87.3** | TypeScript | Edge/多运行时 |
| 3 | [NestJS](projects/nestjs.md) | 75.2k | **87.0** | TypeScript | 企业级后端 |
| 4 | [FastAPI](projects/fastapi.md) | 97.2k | **85.3** | Python | ML/AI API服务 |
| 5 | [Fastify](projects/fastify.md) | 36.1k | **80.6** | JS/TS | 高性能 Node.js |
| 6 | [Express.js](projects/expressjs.md) | 68.9k | **78.3** | JavaScript | 传统项目/简单场景 |
| 7 | [Django](projects/django.md) | 87.3k | **74.3** | Python | Python全栈 |

> **TEMC** = 技术分(25%) + 生态分(20%) + 时机分(30%) + 组合分(25%)

## 🏆 天子点评（一人公司推荐）

```
首选:     tRPC (配合 Next.js) — 零代码生成的端到端类型安全
API 层:   Hono — 独立 API 路由或 Edge Functions
ML/AI:    FastAPI — 需要 Python ML 库时使用
```

## 📂 仓库结构

```
backend-stack/
├── projects/                      # 单个项目深度分析
│   ├── trpc.md
│   ├── hono.md
│   ├── nestjs.md
│   ├── fastapi.md
│   ├── fastify.md
│   ├── expressjs.md
│   └── django.md
├── best-practices/
│   ├── api-design.md              # API 设计模式
│   └── microservices-patterns.md  # 何时拆分、如何通信
├── comparison.md                  # 横向对比表
├── roadmap.md                     # 后端技术趋势与预测
├── CONTRIBUTING.md
├── SOURCES.md
└── README.md
```

## 📝 使用指南

1. **对比** — 从 [comparison.md](comparison.md) 开始，纵览所有框架
2. **深入** — 阅读 `projects/` 中你感兴趣的框架分析
3. **实践** — 将 `best-practices/` 中的模式应用到你的项目
4. **跟进** — 查看 [roadmap.md](roadmap.md) 了解生态发展方向

## License

分析内容采用 MIT 协议。各项目保留其原始开源协议。
