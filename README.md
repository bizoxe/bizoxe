# Alexander Matveev

**Python Backend Engineer | Async Performance & Architecture**

---

**Backend Development**
- **Core:** Python (Asyncio), Pydantic v2, Static Typing (Mypy).
- **Frameworks:** FastAPI.
- **Data Access:** SQLAlchemy v2.0 & Advanced Alchemy (Repository & Service patterns).
- **Data Layer:** PostgreSQL (Query Optimization), PgBouncer, Alembic, Valkey (Redis fork).

**Infrastructure & Quality**
- **Environment:** Linux (Debian 12), Angie (Nginx fork).
- **DevOps & CI/CD:** Docker & Docker Compose, GitHub Actions, Bash, Dependabot.
- **Standards & Tooling:** Pytest, Ruff, Conventional Commits, ADR.

---

### Projects in Focus

* **[IronTrack](https://github.com/bizoxe/iron-track)** — Async research environment for experimenting with architectural patterns under constrained infrastructure.
    * **Serialization analysis:** Implemented `msgspec.Struct` models, reducing serialization latency by 6.5x compared to Pydantic v2.
    * **Concurrency tuning:** Offloaded CPU-bound Argon2id hashing to managed thread pools to prevent event-loop blocking.
    * **Auth optimization:** Migrated to Ed25519 (RFC 8037) signatures, increasing throughput by 48% on limited-resource hardware compared to RSA.
    * **Infrastructure-aware DB:** Optimized PostgreSQL for high-latency storage (HDD) and integrated PgBouncer in transaction pooling mode.
    * **Decision Log:** Architectural decisions are recorded in [ADR](https://github.com/bizoxe/iron-track/blob/main/dev/adr/001-performance.md); metrics are available in [BENCHMARKS](https://github.com/bizoxe/iron-track/blob/main/benchmarks/BENCHMARKS.md).

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
