# Alexander Matveev

**Python Backend Engineer | Async Systems & Maintainable Architecture**

---

**Stack**
- **Language:** Python 3.12 (asyncio), static typing (Mypy).
- **API:** FastAPI, Pydantic v2, msgspec (hot-path serialization).
- **Data:** PostgreSQL (query optimization), SQLAlchemy 2.0 & Advanced Alchemy (repository & service patterns), Alembic, PgBouncer, Valkey (Redis fork).
- **Infrastructure:** Linux (Debian 12), Bash, Docker & Docker Compose, Angie (nginx fork).
- **Observability:** structlog (non-blocking pipeline), request correlation IDs.
- **Process:** GitHub Actions, Pytest, Ruff, Conventional Commits, ADR.

---

### Project in Focus

**[IronTrack](https://github.com/bizoxe/iron-track)** — an async backend for a realistic domain (workout tracking: RBAC, soft delete, immutable history), deliberately built as an end-to-end case study: schema design → API → observability → hardened deploy. Benchmarked on constrained hardware (AMD FX-8320, HDD) to expose bottlenecks that fast hardware masks.

**Performance engineering on the auth path** — profiled, iterated, verified by load testing:

* JWT signing migrated **RSA-2048 → Ed25519**; Argon2id hashing offloaded to a `ThreadPoolExecutor` to keep the event loop responsive under hashing load.
* Local **JTI caching** for access-token verification — safe by construction: entries are written only after full verification, and forging a valid `jti` (uuid4) requires possessing the token. Cache hits skip signature verification entirely, cutting the auth cost of every protected route.
* `msgspec.json` serialization replacing FastAPI's default encoder on latency-critical paths.

| Endpoint | Mean Latency | P90 | Primary Factor |
|----------|--------------|-----|----------------|
| `/signin` | **−39.2%** (857 → 521 ms) | −38.5% | Ed25519 + ORM query tuning |
| `/me` | **−36.5%** (3.70 → 2.35 ms) | −31.0% | JTI cache (multiplicative: auth on every protected route) |

`/signup` is Argon2id-bound by design — the win there is event-loop responsiveness under hashing load, not endpoint latency.

**Benchmarking discipline** — the spec ([SPEC.md](https://github.com/bizoxe/iron-track/blob/main/benchmarks/SPEC.md)) is designed around the bench: `wrk2` at fixed request rate (coordinated-omission aware), per-module CPU affinity isolating app / DB+pooler / cache / load generator on a shared-FPU CPU, DVFS and TTY noise control, CV < 3% run-stability gate. Iterative report with flame graphs: [Load Testing: Auth & Serialization](https://github.com/bizoxe/iron-track/blob/main/benchmarks/auth-serialization.md). Long-form write-up of the same work: [Analyzing and Troubleshooting Bottlenecks in FastAPI](https://iron-track.hashnode.dev/fastapi-performance-bottlenecks-optimization).

**Engineering process:** ADR-recorded decisions, a schema blueprint kept in lockstep with migrations (same-PR policy), Sphinx-documented API, least-privilege CI, conventional commits with a generated changelog.

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
