<div align="center">

# Jill Vekariya

**Machine learning systems · Backend reliability · Third-year engineering student, Ahmedabad**

[![Portfolio](https://img.shields.io/badge/Portfolio-jill--vekariya.github.io-0f6e6e?style=for-the-badge)](https://jill-vekariya.github.io/Jill-Vekariya/)
[![Email](https://img.shields.io/badge/Email-jillvekariya.10%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jillvekariya.10@gmail.com)

</div>

I build ML systems the way production teams have to: a measured offline experiment first, then a versioned service with tests, Docker, CI and recorded results that someone else can replay. Every repository below has a live demo, a passing pipeline and a document that says what did not work.

**Open to ML/AI internships for 2027.**

## Flagship: SafeHeal AI

**[safeheal-ai](https://github.com/Jill-Vekariya/safeheal-ai)** — Kubernetes incident diagnosis where a language model proposes and a separate deterministic controller decides what is allowed to change.

- The model never holds credentials. A policy-checked controller executes under RBAC, writes every decision to a durable audit journal, and refuses anything outside an allowlist.
- CI creates a real kind cluster on every push, injects faults, verifies recovery against Prometheus metrics and traces, and archives the evidence.
- A controlled study compares rule-based, AI-proposed and native Kubernetes recovery on the same faults (5/5, 2/5, 0/5 successful recoveries), with the failed runs kept, not deleted.
- 581 tests; raw study artifacts are checksum-verified by [`scripts/reproduce.py`](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/scripts/reproduce.py).

[Simulation](https://jill-vekariya.github.io/safeheal-ai/) · [Study](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/evidence/public-release/CPU_STUDY.md) · [Architecture](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/ARCHITECTURE.md) · [Design decisions](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/docs/DESIGN_DECISIONS.md)

## Other projects

| Project | One line | Result worth knowing | Links |
| --- | --- | --- | --- |
| **[Agent Reliability Harness](https://github.com/Jill-Vekariya/agent-reliability-harness)** | Test bench for an LLM SQL agent: read-only sandboxed execution, typed answer grading, exact trace replay, durable PostgreSQL job workflow. | Docker acceptance with verified crash recovery: six table fingerprints matched after a fresh restore. | [Trace explorer](https://jill-vekariya.github.io/agent-reliability-harness/) · [Recovery study](https://github.com/Jill-Vekariya/agent-reliability-harness/blob/main/docs/stage6/CASE_STUDY.md) |
| **[ReleaseLens](https://github.com/Jill-Vekariya/ReleaseLens)** | Documentation retrieval scoped to an exact release and access policy; saved answers keep immutable citations and are queued for review when sources change. | 70-question retrieval study across 14 snapshots and 534 passages; 185 Python and 16 browser tests in CI. | [Demo](https://jill-vekariya.github.io/ReleaseLens/) · [Retrieval study](https://github.com/Jill-Vekariya/ReleaseLens/blob/main/docs/V3_REPORT.md) |
| **[Atlas](https://github.com/Jill-Vekariya/atlas-recsys)** | Cold-start recommendations: PyTorch two-tower retriever, FAISS search, LightGBM ranker, FastAPI serving with canary, fallback and rollback. | The validation-selected model lost to the popularity baseline on test (0.234 vs 0.260 NDCG@10); the case study explains why and what changed. | [Live lab](https://jill-vekariya.github.io/atlas-recsys/) · [Case study](https://github.com/Jill-Vekariya/atlas-recsys/blob/main/docs/MODEL_SELECTION_CASE_STUDY.md) |
| **[Sentinel](https://github.com/Jill-Vekariya/sentinel-fraud-platform)** | Fraud scoring with idempotent decisions, a transactional outbox and at-least-once Kafka-compatible streaming. | Holdout PR-AUC 0.764 on 284,807 real anonymised transactions with chronological splits. | [Demo](https://jill-vekariya.github.io/sentinel-fraud-platform/) · [Benchmark](https://github.com/Jill-Vekariya/sentinel-fraud-platform/blob/main/docs/REAL_BENCHMARK.md) |

## How I work

- Chronological splits and held-out tests before any model claim; negative results are written up, not hidden.
- Pinned dependencies, lockfiles, digest-pinned base images and dependency audits in CI.
- Services ship with health checks, read-only runtime users, resource limits and an audit trail.
- Python, PyTorch, scikit-learn, XGBoost, LightGBM, FAISS, FastAPI, PostgreSQL, SQLite, Redis, Kafka, Docker, Kubernetes, Prometheus, GitHub Actions.

## Contact

Email is fastest: [jillvekariya.10@gmail.com](mailto:jillvekariya.10@gmail.com). Walkthroughs, source and recorded results are linked from each repository and from the [portfolio](https://jill-vekariya.github.io/Jill-Vekariya/).
