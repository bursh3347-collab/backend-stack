# Django

> The web framework for perfectionists with deadlines — Python's most complete web framework.

| Metric | Data |
|------|------|
| GitHub | [django/django](https://github.com/django/django) |
| Stars | 87,271 |
| License | BSD-3 |
| Language | Python |
| Age | 20+ years |

## TEMC Scores

| Dimension | Score | Reasoning |
|------|------|------|
| T (Tech) | 85 | Batteries-included: ORM, admin, auth, forms, caching, i18n. Django 5.x with async support. Mature and stable. |
| E (Ecosystem) | 90 | 87k stars. Instagram, Pinterest, Mozilla use it. Massive package ecosystem (Django REST Framework, Celery, etc.). |
| M (Market) | 75 | Strong for traditional web apps but losing new projects to FastAPI for APIs and Next.js for full-stack. |
| C (Combo) | 50 | Python, not TypeScript. Full-stack framework competes with Next.js rather than complementing it. |
| **Overall** | **74.3** | |

## Core Value

- **Batteries-included**: Admin panel, ORM, auth, forms — everything built-in
- **Django Admin**: Auto-generated admin panel from models
- **ORM**: Powerful, mature database abstraction
- **Security**: CSRF, XSS, SQL injection protection built-in
- **Django REST Framework**: Best-in-class API toolkit

## Risks

- Monolithic architecture doesn't fit microservices well
- Async support still catching up to FastAPI
- Template system less relevant in SPA world
- Python, not TypeScript

## 天子点评

Python全栈框架，和Next.js定位重叠。87k Stars反映的是20年积累。Django Admin是杀手锏——10分钟生成后台管理面板。但一人公司已选Next.js全栈，Django的价值仅限于需要Python密集型后台（数据处理/ML Pipeline）的场景。FastAPI更适合API场景。
