# Jill-Vekariya

## AI, machine learning and backend engineering portfolio

Five projects exploring bounded agent execution, Kubernetes recovery, source-grounded answers, recommendation systems and transactional risk decisions. Each links implementation, reproducible checks and the limits of its evidence.

[Repositories](https://github.com/Jill-Vekariya?tab=repositories)

## Selected projects

| Project | Engineering discussion | Explore |
| --- | --- | --- |
| **[Agent Reliability Harness](https://github.com/Jill-Vekariya/agent-reliability-harness)** | Read-only SQL execution, typed grading, strict replay and conservative spending reservations | [Saved-trace demo](https://jill-vekariya.github.io/agent-reliability-harness/) · [Code review](https://github.com/Jill-Vekariya/agent-reliability-harness/blob/main/docs/REVIEW_GUIDE.md) |
| **[SafeHeal AI](https://github.com/Jill-Vekariya/safeheal-ai)** | Evidence-backed diagnosis separated from independent allowlisted recovery; failed model trials remain visible | [Demo guide](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/docs/DEMO.md) · [Research report](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/docs/RESEARCH_REPORT.md) |
| **[ReleaseLens](https://github.com/Jill-Vekariya/ReleaseLens)** | Exact release/ACL scope, immutable citations and review after source changes | [Browser demo](https://jill-vekariya.github.io/ReleaseLens/) · [Challenge and limits](https://github.com/Jill-Vekariya/ReleaseLens/blob/main/docs/CHALLENGE_V1.md) |
| **[Atlas](https://github.com/Jill-Vekariya/atlas-recsys)** | Temporal recommendation evaluation, compatible model/index bundles and rollout/rollback | [Browser lab](https://jill-vekariya.github.io/atlas-recsys/) · [Model-selection case study](https://github.com/Jill-Vekariya/atlas-recsys/blob/main/docs/MODEL_SELECTION_CASE_STUDY.md) |
| **[Sentinel](https://github.com/Jill-Vekariya/sentinel-fraud-platform)** | Atomic history/decision/outbox state, event replay, scoring and model rollback | [Browser demo](https://jill-vekariya.github.io/sentinel-fraud-platform/) · [Validation](https://github.com/Jill-Vekariya/sentinel-fraud-platform/blob/main/docs/VALIDATION.md) |

## Questions the code can answer

- What happens when an SQL tool hangs, a saved trace becomes incompatible or provider usage is unknown? Start with [Harness decisions](https://github.com/Jill-Vekariya/agent-reliability-harness/blob/main/docs/DECISIONS.md).
- Why did a fixed rule outperform AI in a narrow recovery study? Inspect [SafeHeal's CPU-study outcomes](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/evidence/public-release/CPU_STUDY.md).
- Why can a valid citation still fail to answer a question? Read [ReleaseLens's migration challenge](https://github.com/Jill-Vekariya/ReleaseLens/blob/main/docs/CHALLENGE_V1.md).
- What should happen when a validation-selected model loses to popularity, or a transaction is retried after model promotion? Inspect Atlas's selection evidence and Sentinel's transaction tests.

## Technologies used meaningfully

Python and SQL · FastAPI and Pydantic · SQLite and PostgreSQL · PyTorch, FAISS and LightGBM · XGBoost and Isolation Forest · Kafka-compatible streaming · Docker and Kubernetes · pytest, Prometheus and GitHub Actions.

## Evidence and ownership

These are AI-assisted portfolio projects. Ownership records distinguish AI implementation/preparation from personally confirmed coding, review and reproduction. Planned exercises are not completed contributions; a prepared explanation is not proof of independent understanding.

Browser demonstrations are separate from Python services, SQL workers, databases and brokers. SafeHeal's live recovery demonstration uses an isolated Docker-kind lab or its documented workflow. Recorded offline/synthetic studies are not production scale, customer impact or guaranteed interview/AI-shortlisting outcomes. READMEs provide the setup, evidence and unresolved limits for each project.

**Contact:** [jillvekariya.10@gmail.com](mailto:jillvekariya.10@gmail.com)
