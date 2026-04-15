# FastAPI

> A modern, fast (high-performance) web framework for building APIs with Python 3.7+ based on standard Python type hints.

| Metric | Data |
|------|------|
| GitHub | [fastapi/fastapi](https://github.com/fastapi/fastapi) |
| Stars | ~85,000 |
| License | MIT |
| Language | Python |
| Maintainer | Sebastián Ramírez (tiangolo) |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 95 | Async-first, auto OpenAPI docs, type-safe with Pydantic, dependency injection. Starlette performance (on par with Node/Go). |
| E (Ecosystem) | 92 | 85k stars, Python's fastest-growing web framework. Used by Microsoft, Netflix, Uber. |
| M (Market) | 88 | Dominant for Python APIs. Perfect for ML/AI services, data pipelines, microservices. |
| C (Combo) | 65 | Python — different from base TypeScript stack. But excellent for AI/ML microservices that complement Next.js frontend. |
| **Overall** | **85.3** | |

## Core Value

- **Auto-documentation**: Swagger UI + ReDoc from type hints
- **Async-first**: Native async/await support
- **Pydantic validation**: Type-safe request/response models
- **Dependency injection**: Clean, testable architecture
- **Performance**: One of the fastest Python frameworks
- **Python ecosystem**: Access to ML/AI libraries (PyTorch, scikit-learn, etc.)

## Risks

- Python, not TypeScript — requires maintaining two language stacks
- Single maintainer risk (tiangolo), though community is massive
- Async Python has its own gotchas (blocking calls in async context)
