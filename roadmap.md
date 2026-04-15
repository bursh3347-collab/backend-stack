# 🗺️ Backend Stack Roadmap

> 该分类的技术趋势与发展方向预测（2026-04-15 更新）

## 📊 当前主流

| 技术 | 地位 | 说明 |
|------|------|------|
| Next.js API Routes | 🟢 绝对主流 | 全栈TypeScript项目的默认后端方案 |
| tRPC | 🟢 主流上升 | TypeScript全栈的端到端类型安全首选 |
| FastAPI | 🟢 Python主流 | Python API开发的统治者，97k Stars |
| NestJS | 🟢 企业主流 | 企业级TypeScript后端的标准选择 |
| Express.js | 🟡 遗产主流 | 仍然最多使用，但新项目在流失 |

## 🚀 崛起方向

| 技术 | 趋势 | 对一人公司的影响 |
|------|------|------|
| **Hono** | ↑↑ 最快增长 | Edge-first后端框架，周增500 Stars。Vercel/Cloudflare/Supabase原生支持，一人公司做API微服务首选 |
| **tRPC v11 + RSC** | ↑↑ 深度集成 | Server Components原生支持，Next.js全栈的类型安全更无缝 |
| **Edge Computing** | ↑↑ 范式转移 | 全球边缘节点运行后端代码，冷启动<1ms。Vercel Edge Functions + Hono |
| **Server Actions** | ↑ 简化趋势 | Next.js Server Actions减少独立后端API的需求 |
| **Bun Runtime** | ↑ 替代Node.js | 更快的JS/TS运行时，Hono已原生支持 |
| **AI Gateway** | 🌟 新兴 | 专门处理LLM API调用的后端中间层（速率限制/缓存/路由）|

## 📉 衰退方向

| 技术 | 趋势 | 说明 |
|------|------|------|
| Express.js | ↓ 持续下降 | 新项目选择率下降，Express 5迟迟不发布 |
| GraphQL (纯) | ↓ 被tRPC替代 | TypeScript项目中GraphQL的复杂度不再必要 |
| REST (手写) | ↓ 被自动化取代 | Zod OpenAPI / tRPC / Server Actions减少手写REST |
| Django (新项目) | ↓ 被FastAPI替代 | Python新API项目几乎全选FastAPI |
| Microservices (盲目) | ↓ 回归务实 | Gartner警告40%项目2027前取消，单体+按需拆分成共识 |

## 🔮 6-12个月预测

1. **Hono将突破50k Stars**，成为Edge计算后端框架的事实标准
2. **tRPC v11** 正式发布，Server Components集成成为杀手特性
3. **Server Actions** 将处理60%以上的数据变更场景，减少独立API路由需求
4. **Bun 2.0** 可能成为新项目的默认运行时（替代Node.js）
5. **AI Gateway** 将成为独立品类——处理LLM调用的专用后端中间件
6. **FastAPI** 突破100k Stars，Python生态继续巩固

## 💡 对一人公司的影响

### 核心建议

- **主力：Next.js API Routes + tRPC**：90%的后端需求用这个组合解决
- **补充：Hono**：当需要独立API服务、Edge Functions、Supabase Functions时使用
- **AI服务：FastAPI**：当需要调用Python ML模型时，FastAPI做微服务
- **不要用Express**：除非维护老项目，新代码全部用Hono或tRPC
- **不要盲目微服务**：一人公司单体优先，只在明确需要时拆分

### 后端架构推荐

```
┌──────────────────────────────┐
│        Next.js App           │
│  ┌─────────┐  ┌───────────┐  │
│  │ Server  │  │  tRPC     │  │
│  │ Actions │  │  Router   │  │
│  └─────────┘  └───────────┘  │
└──────────────┬───────────────┘
               │
    ┌──────────┴──────────┐
    │                     │
┌───┴───┐           ┌────┴────┐
│ Hono  │           │ FastAPI │
│ (Edge │           │ (ML/AI  │
│  API) │           │  svc)   │
└───────┘           └─────────┘
```

### 时间分配建议

- 70% 精力：Next.js API Routes + tRPC（核心后端）
- 15% 精力：Hono（Edge/独立API场景）
- 10% 精力：FastAPI（Python ML服务）
- 5% 精力：关注新趋势（Bun, AI Gateway, Server Actions演进）
