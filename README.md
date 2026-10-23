# Jill-Vekariya

### AI and machine learning engineering portfolio

Projects exploring reliable agents, evidence retrieval, recommendation systems, streaming risk decisions, and incident diagnosis. Explore implementation details, reproducible checks, and the limits of each result.

[Email](mailto:jillvekariya.10@gmail.com) · [Repositories](https://github.com/Jill-Vekariya?tab=repositories)

## Selected projects

| Project | Engineering focus | Explore |
|---|---|---|
| **[Agent Reliability Harness](https://github.com/Jill-Vekariya/agent-reliability-harness)** | Protected SQL execution, typed result grading, strict replay, concurrent budget reservations, and failure diagnostics | [Demo](https://jill-vekariya.github.io/agent-reliability-harness/) · [Code review route](https://github.com/Jill-Vekariya/agent-reliability-harness/blob/main/docs/REVIEW_GUIDE.md) |
| **[Atlas](https://github.com/Jill-Vekariya/atlas-recsys)** | Cold-start recommendation with PyTorch retrieval, FAISS, LightGBM ranking, temporal evaluation, and model rollout/rollback | [Demo](https://jill-vekariya.github.io/atlas-recsys/) · [Results](https://github.com/Jill-Vekariya/atlas-recsys/blob/main/docs/RESULTS.md) |
| **[ReleaseLens](https://github.com/Jill-Vekariya/ReleaseLens)** | Release-scoped retrieval, exact citations, immutable documentation revisions, and review of saved answers after source changes | [Demo](https://jill-vekariya.github.io/ReleaseLens/) · [Measured retrieval study](https://github.com/Jill-Vekariya/ReleaseLens/blob/main/docs/V3_REPORT.md) |
| **[Sentinel](https://github.com/Jill-Vekariya/sentinel-fraud-platform)** | Fraud scoring with XGBoost, account-keyed streaming, durable decisions, monitoring, and guarded model promotion | [Demo](https://jill-vekariya.github.io/sentinel-fraud-platform/) · [Validation](https://github.com/Jill-Vekariya/sentinel-fraud-platform/blob/main/docs/VALIDATION.md) |
| **[SafeHeal AI](https://github.com/Jill-Vekariya/safeheal-ai)** | Synthetic three-service lab with Kubernetes fault benchmarks, deterministic incident detection, and bounded evidence-grounded diagnosis; autonomous recovery remains future work | [Setup](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/README.md#run-on-windows) · [Diagnosis limits](https://github.com/Jill-Vekariya/safeheal-ai/blob/main/docs/AI_DIAGNOSIS.md) |

## Three engineering discussions

- **When should a system fail closed?** [Agent Reliability Harness](https://github.com/Jill-Vekariya/agent-reliability-harness/blob/main/docs/DECISIONS.md) separates a correct answer from a safe decision and treats unknown provider charges conservatively.
- **What if the selected model loses to a simple baseline?** [Atlas's model-selection case study](https://github.com/Jill-Vekariya/atlas-recsys/blob/main/docs/MODEL_SELECTION_CASE_STUDY.md) retains a failed generalization result and explains validation-only selection.
- **Does a valid citation mean an answer is sufficient?** [ReleaseLens's migration challenge](https://github.com/Jill-Vekariya/ReleaseLens/blob/main/docs/CHALLENGE_V1.md) distinguishes exact source membership from relevant and sufficient evidence.

## Technologies used in these repositories

**Python and SQL** · **PyTorch, FAISS, LightGBM and XGBoost** · **FastAPI and Pydantic** · **SQLite and PostgreSQL** · **Kafka-compatible streaming** · **Docker, pytest and GitHub Actions**

## About the evidence

These are AI-assisted portfolio projects. Available project ownership notes distinguish AI assistance, proposed exercises, and personal contributions supported by actual evidence; an exercise is not a completed contribution. Synthetic demonstrations, measured offline experiments, and production outcomes have different scopes; the repositories preserve those distinctions and document unsuccessful results.

The four linked browser demos are immediately accessible. SafeHeal AI currently runs locally using its documented setup and has no hosted public demo. Full Python services, databases, brokers and SQL workers run separately using the setup instructions in each repository.

## Review and reproduction

Project READMEs document status, setup and limitations. Agent Reliability Harness, Atlas, ReleaseLens and Sentinel also link interview practice. Recorded experiments retain their original workload and revision; use current CI and a fresh local run to assess newer source. No independent authorship, production scale or business outcome is implied by the portfolio.

Local documentation links can be checked with `python scripts/check_links.py`; add `--online` for external reachability.
