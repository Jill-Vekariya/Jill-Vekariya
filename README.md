# Hi, I'm Jill Vekariya

Third-year computer science student from Gujarat, India, working on machine learning and the backend systems that serve it. I'm looking for an **ML/AI internship** (summer 2027 or earlier).

<!-- TODO: replace the placeholders below with your real details -->
📍 Gujarat, India · 🎓 B.Tech CSE, [Your College], batch of 2028 · ✉️ [jillvekariya.10@gmail.com](mailto:jillvekariya.10@gmail.com) · [LinkedIn](https://www.linkedin.com/in/YOUR-HANDLE)

## Projects

| Project | What it does | What I learned | Links |
| --- | --- | --- | --- |
| **[Atlas](https://github.com/Jill-Vekariya/atlas-recsys)** | Cold-start recommender: PyTorch two-tower retriever + FAISS + LightGBM ranker, served through FastAPI with canary routing and rollback. | My validation-selected model lost to a popularity baseline on the final test (0.234 vs 0.260 NDCG@10). I learned to distrust single-seed selection and to evaluate chronologically. | [Browser lab](https://jill-vekariya.github.io/atlas-recsys/) · [Case study](https://github.com/Jill-Vekariya/atlas-recsys/blob/main/docs/MODEL_SELECTION_CASE_STUDY.md) |
| **[Agent Reliability Harness](https://github.com/Jill-Vekariya/agent-reliability-harness)** | Evaluates a SQL agent with read-only tools, typed answer grading and strict trace replay; a FastAPI/PostgreSQL workflow adds durable jobs and recovery. | How to make agent behaviour reproducible: record every tool call, replay it exactly, and test crash recovery with table fingerprints. | [Trace explorer](https://jill-vekariya.github.io/agent-reliability-harness/) · [Recovery study](https://github.com/Jill-Vekariya/agent-reliability-harness/blob/main/docs/stage6/CASE_STUDY.md) |
| **[ReleaseLens](https://github.com/Jill-Vekariya/ReleaseLens)** | Documentation retrieval scoped to a release and access policy; saved answers keep their original cited evidence when the docs change. | A citation existing is not the same as a citation supporting the answer. Filtering by ACL before top-k matters for both recall and leakage. | [Demo](https://jill-vekariya.github.io/ReleaseLens/) · [Retrieval study](https://github.com/Jill-Vekariya/ReleaseLens/blob/main/docs/V3_REPORT.md) |
| **[Sentinel](https://github.com/Jill-Vekariya/sentinel-fraud-platform)** | Fraud scoring (XGBoost + Isolation Forest) on 284k real transactions, with idempotent decisions and a transactional outbox for at-least-once streaming. | Exactly-once is a lie you tell consumers; design for duplicates. Holdout PR-AUC 0.764 with chronological splits. | [Demo](https://jill-vekariya.github.io/sentinel-fraud-platform/) · [Benchmark](https://github.com/Jill-Vekariya/sentinel-fraud-platform/blob/main/docs/REAL_BENCHMARK.md) |
| **[SafeHeal AI](https://github.com/Jill-Vekariya/safeheal-ai)** | Kubernetes incident diagnosis where the model proposes and a separate deterministic controller decides what may change. | In the recorded study a fixed rule beat the AI (5/5 vs 2/5). Keeping the model away from credentials made that comparison safe to run. | [Simulation](https://jill-vekariya.github.io/safeheal-ai/) · [Study](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/evidence/public-release/CPU_STUDY.md) |

Smaller and ongoing: [python_lab](https://github.com/Jill-Vekariya/python_lab) (numbered coursework exercises with tests and CI, since Jan 2025).

## Tools I use

`Python` `SQL` `PyTorch` `FAISS` `LightGBM` `XGBoost` `FastAPI` `Pydantic` `PostgreSQL / pgvector` `SQLite` `Docker` `Kubernetes` `Kafka` `pytest` `GitHub Actions`

## How I build

I use AI coding assistants heavily, and I say so in each repo. My job is the part the assistant can't do: choosing the problem, deciding what counts as evidence, reproducing results, and debugging what breaks. Every project above has CI, locked dependencies and recorded experiments, including the ones that didn't go my way. Each repo's `docs/` folder records what was AI-assisted and what I verified myself.

<!-- TODO: once you've written your own regression test / fix in each repo, link the commits here under "Independent contributions". -->

## Currently

- Working through the code of each project and writing my own regression tests and fixes.
- Exploring execution-rewarded text-to-SQL fine-tuning on small models.
- Open to internship conversations: email is fastest.
