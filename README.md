# Alexander Matveev

**Python Backend Engineer | Async Performance & Architecture**

---

**Backend Development**
- **Core:** Python (Asyncio), Pydantic v2, Type-safe development (Mypy strict).
- **Frameworks:** FastAPI.
- **Data Access:** SQLAlchemy v2.0 & Advanced Alchemy (Repository & Service patterns), Alembic.
- **Data Layer:** PostgreSQL (Query Optimization), Valkey (Redis fork), PgBouncer.

**Infrastructure & Quality**
- **Environment:** Linux (Debian 12), Angie (Nginx fork).
- **DevOps & Automation:** Docker & Docker Compose, GitHub Actions, Bash scripts, Dependabot.
- **Quality Control:** Pytest, Static Analysis (Ruff, Mypy), Conventional Commits, ADR.

---

### Projects in Focus

* **[IronTrack](https://github.com/bizoxe/iron-track)** — research-oriented backend platform for experimenting with production patterns under constrained infrastructure.
- Reduced P99 latency by 6.5x **compared to standard Pydantic models** by using `msgspec` structs for serialization.
- Resolved event-loop blocking by moving CPU-bound Argon2id hashing to managed thread pools.
- Migrated to **Ed25519 (RFC 8037)**, improving authorization throughput by 48% on **legacy CPU** compared to RSA-256.
- Tuned PostgreSQL for high-latency storage (HDD) and configured PgBouncer transaction pooling.
- Architectural decisions are recorded in [ADR](https://github.com/bizoxe/iron-track/blob/main/dev/adr/001-performance.md); performance data is available in [BENCHMARKS](https://github.com/bizoxe/iron-track/blob/main/benchmarks/BENCHMARKS.md).

---

### GitHub Metrics

<p align="left">
  <img src="./github-metrics.svg" alt="GitHub Metrics">
</p>

---

### Contact Details

<p align="left">
<a href="https://t.me/bizoxe187" target="blank"><img src="https://img.shields.io/static/v1?label=Telegram&message=Chat&color=2CA5E0&style=flat-square&logo=telegram" alt="Telegram" /></a>
<a href="https://linkedin.com/in/alexander-matveev-dev" target="blank"><img src="https://img.shields.io/static/v1?label=LinkedIn&message=Connect&color=0077B5&style=flat-square&logo=linkedin" alt="LinkedIn" /></a>
</p>
