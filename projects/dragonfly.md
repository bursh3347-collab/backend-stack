# Dragonfly

> A modern replacement for Redis and Memcached — 25x faster, multi-threaded, Redis-compatible

| Metric | Data |
|--------|------|
| GitHub | [dragonflydb/dragonfly](https://github.com/dragonflydb/dragonfly) |
| Stars | ~27,000 |
| License | BSL 1.1 (Business Source License) |
| Language | C++ |
| Last Updated | Active (daily commits) |
| Contributors | 200+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 92 | Multi-threaded shared-nothing architecture, 25x throughput vs Redis on single instance. Novel Dash hash table, tiered storage (RAM+SSD). Full Redis/Memcached API compatibility |
| E (Ecosystem) | 82 | 27k stars, strong VC backing ($40M+ raised), active development. Drop-in Redis replacement = instant ecosystem access |
| M (Market) | 75 | Redis licensing change (SSPL→RSALv2) created massive market opening. Dragonfly + Valkey are the two main alternatives. Enterprise adoption growing |
| C (Combo) | 65 | Great Redis replacement but C++ = can't extract modules for TypeScript stack. Value is as infrastructure, not as code to learn from |
| **Overall** | **78** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Drop-in Redis replacement that's dramatically faster on modern multi-core hardware. Eliminates Redis's single-threaded bottleneck while maintaining full API compatibility.

## Architecture Highlights
- **Shared-nothing multi-threaded** — Each thread owns its data slice, no locks needed
- **Dash hash table** — Novel data structure outperforming Redis's dict
- **Tiered storage** — Hot data in RAM, warm data on NVMe SSD
- **Snapshot without fork()** — Consistent snapshots without Redis's memory-doubling COW problem
- **Full Redis compatibility** — Supports Redis Cluster protocol, Lua scripting, pub/sub

## Key Modules
1. **Server Core** (src/server/) — Multi-threaded event loop with io_uring
2. **Storage Engine** — Dash hash table + tiered memory management
3. **Replication** — Redis-compatible master-replica + Dragonfly-native replication
4. **Cluster** — Redis Cluster protocol compatible sharding
5. **Search** — Full-text search (RediSearch compatible)

## Solo Dev Verdict
🟡 **Excellent infrastructure choice, limited code learning value.** As a Redis replacement for your SaaS backend, Dragonfly is a clear upgrade — docker pull and go. But it's C++ infrastructure, not TypeScript code you'd study or extract. ⚠️ BSL license means you can't offer Dragonfly-as-a-service, but using it for your own SaaS backend is fine.

## Anti-Pattern Warning
- **BSL 1.1 license** — Not truly open source. Free to use, but can't compete with Dragonfly Cloud
- C++ codebase = no module extraction for TypeScript projects
- Overkill for small projects where Redis is already fast enough
- Self-hosting requires more RAM than Redis for small datasets
