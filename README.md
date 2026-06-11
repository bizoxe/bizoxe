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
* **Optimization Context:** Conducted on constrained **HDD-based storage** and **Piledriver-based architecture** to simulate high-latency, resource-limited environments.
* **Key Improvements:**
  * Migrated JWT signing (RSA-2048 to Ed25519) and offloaded Argon2id hashing to `ThreadPoolExecutor` to prevent Event Loop starvation.
  * Implemented local JTI caching for Access Tokens and native `msgspec.json` serialization for latency-critical paths.


* **Results:** Achieved **up to 39% latency reduction** across key authentication endpoints, verified through iterative load testing.
* **Documentation:** Detailed methodology, flame graphs, and performance metrics are available in the [Load Testing Report](https://github.com/bizoxe/iron-track/blob/main/benchmarks/auth-serialization.md).

---

| Endpoint | Mean Latency Change | Primary Factor |
| --- | --- | --- |
| `/signup` | -9.26% | Argon2id offloading |
| `/signin` | -39.2% | Ed25519 + ORM tuning |
| `/me` | -36.5% | JTI Caching 

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
