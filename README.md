# Jill Vekariya

**Machine learning · backend engineering · evaluation**

My portfolio explores how to make model-based systems easier to evaluate,
debug and operate. The projects cover recommendation, retrieval and agent
execution, with working browser demonstrations and source-linked experiments.

**Seeking ML/AI internship opportunities.**
[Email](mailto:jillvekariya.10@gmail.com) · [Repositories](https://github.com/Jill-Vekariya?tab=repositories)

## Start here

| Project | Engineering focus | Explore |
| --- | --- | --- |
| **[Atlas](https://github.com/Jill-Vekariya/atlas-recsys)** | Cold-start recommendation, chronological evaluation and versioned model serving. Includes a case where the validation-selected model lost to popularity on the final test. | [Browser lab](https://jill-vekariya.github.io/atlas-recsys/) · [Experiment](https://github.com/Jill-Vekariya/atlas-recsys/blob/main/docs/MODEL_SELECTION_CASE_STUDY.md) |
| **[Agent Reliability Harness](https://github.com/Jill-Vekariya/agent-reliability-harness)** | Read-only SQL tools, typed answer checks, strict replay and durable local jobs with recovery controls. | [Saved-trace walkthrough](https://jill-vekariya.github.io/agent-reliability-harness/) · [Recovery case study](https://github.com/Jill-Vekariya/agent-reliability-harness/blob/main/docs/stage6/CASE_STUDY.md) |
| **[ReleaseLens](https://github.com/Jill-Vekariya/ReleaseLens)** | Retrieval scoped to a release and access policy; cited answers keep their original evidence when source documentation changes. | [Browser demo](https://jill-vekariya.github.io/ReleaseLens/) · [Retrieval study](https://github.com/Jill-Vekariya/ReleaseLens/blob/main/docs/V3_REPORT.md) |

## Further projects

- **[Sentinel](https://github.com/Jill-Vekariya/sentinel-fraud-platform):** fraud-scoring experiments and transactional event processing, with explicit retry and at-least-once delivery behavior. [Demo](https://jill-vekariya.github.io/sentinel-fraud-platform/) · [Real-data benchmark](https://github.com/Jill-Vekariya/sentinel-fraud-platform/blob/main/docs/REAL_BENCHMARK.md)
- **[SafeHeal AI](https://github.com/Jill-Vekariya/safeheal-ai):** Kubernetes diagnosis separated from a tightly constrained recovery controller. A small recorded study compares native recovery, a fixed rule and AI diagnosis. [Browser simulation](https://jill-vekariya.github.io/safeheal-ai/) · [Study](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/evidence/public-release/CPU_STUDY.md)

## Technologies in the code

- **Languages and APIs:** Python, SQL, FastAPI, Pydantic.
- **Machine learning and retrieval:** PyTorch, FAISS, LightGBM, XGBoost, PostgreSQL/pgvector.
- **Systems and verification:** SQLite, Docker, Kubernetes, Kafka-compatible streaming, pytest, GitHub Actions, Prometheus.

## Evidence and contribution

[Engineering review](docs/ENGINEERING_REVIEW_20261104.md): reproduced failures,
code fixes, dependency audits and verification across the five projects.

Each repository links its setup, recorded results and technical limitations.
The browser demos are distinct from the Python services, databases and recovery
labs. These are portfolio experiments; no production customer impact is claimed.

Implementation, tests and documentation used AI assistance. Repository contribution
records distinguish that assistance from personally verified work; independent
coding and reproduction exercises remain pending where those records say so.
