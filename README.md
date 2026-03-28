# Alexander Matveev

**Python Backend Engineer | Focus on Async Systems & Scalable Architecture**

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

* **[IronTrack](https://github.com/bizoxe/iron-track)** — Experimental async sandbox for evaluating architectural patterns under hardware constraints.
    * **Serialization:** Analyzed `msgspec` vs Pydantic v2 to minimize overhead in latency-sensitive endpoints.
    * **Concurrency:** Offloaded Argon2id hashing to managed thread pools with CPU-core limits to maintain event-loop responsiveness.
    * **Auth:** Evaluated and adopted Ed25519 (EdDSA) to reduce cryptographic compute cost on Piledriver-based hardware.
    * **Storage Optimization:** Tuned PostgreSQL planner and PgBouncer configurations for high-latency HDD environments.
    * **Decision Log:** Architectural rationale and hardware-specific optimizations are documented via [ADR](https://github.com/bizoxe/iron-track/blob/main/dev/adr/001-performance.md) and [benchmarks](https://github.com/bizoxe/iron-track/blob/main/benchmarks/BENCHMARKS.md).

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
