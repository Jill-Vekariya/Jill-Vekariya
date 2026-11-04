# Repository engineering review — 4 November 2026

This review covers the five project repositories and the profile repository.
It records executable fixes, experiment tooling and the scope of verification.
The pull requests below provide the reviewed code and live CI results.

| Repository | Changes | Local verification | Review |
| --- | --- | --- | --- |
| Atlas | JSON-safe request errors; non-ASCII credential handling; validation sealed before multi-seed test evaluation; patched dependency locks | 56 Python tests and 5 browser-engine tests passed; three synthetic seeds completed | [PR #6](https://github.com/Jill-Vekariya/atlas-recsys/pull/6) |
| Agent Reliability Harness | JSON-safe workflow validation; isolated dependency audit in CI | 203 tests passed; 35 database-dependent tests skipped locally; `make ci`, mypy, lint and fixed regression checks passed | [PR #30](https://github.com/Jill-Vekariya/agent-reliability-harness/pull/30) |
| ReleaseLens | JSON-safe request errors; evidence-sufficiency packets bound to authorized extracts and review identity attestations | 185 Python tests and 16 browser-engine tests passed; 2 PostgreSQL cases skipped locally; six-case packet exercise completed | [PR #7](https://github.com/Jill-Vekariya/ReleaseLens/pull/7) |
| SafeHeal AI | JSON-safe service errors; per-trial Pod rebinding with fixed Deployment identity; predeclared multi-fault comparison | 581 Python tests and 9 browser-engine tests passed; 1 opt-in provider test skipped | [PR #10](https://github.com/Jill-Vekariya/safeheal-ai/pull/10) |
| Sentinel | Retain a failed input before polling a later offset; require a delivery callback; retain uncertain outbox attempts; patched dependency locks | Clean hash-locked install: 33 Python tests passed; hosted-demo and live loopback dashboard integration checks passed | [PR #3](https://github.com/Jill-Vekariya/sentinel-fraud-platform/pull/3) |
| Profile | Run local documentation checks on main pushes as well as pull requests; expose this review | Markdown targets checked locally | This repository |

**Totals:** 1,058 Python tests passed and 38 were skipped. The skipped tests are
not counted as passes. Thirty browser-engine tests passed across Atlas,
ReleaseLens and SafeHeal. Sentinel's two integration drivers exercised hosted
inference, scoring, feedback and the live local dashboard; they do not establish
visual rendering quality.

## Reproduced failures and fixes

Rejected JSON containing `NaN`, `Infinity` or `-Infinity` previously caused error
serialization to raise in four APIs. New regression tests reproduced the failure;
the handlers now return HTTP 422 with field diagnostics and omit arbitrary input
and context values. Atlas also returns HTTP 401 for a non-ASCII supplied API key.

Sentinel's proposed retry loop could poll a later message after scoring failed.
A later successful offset commit would acknowledge the earlier failed input too.
The worker now retains that input until processing and commit succeed. An empty
producer queue is also insufficient evidence of delivery: a successful callback
is required. Regression tests cover both cases and failed before the fixes.

SafeHeal's live multi-fault check exposed reuse of a payment-Pod binding after a
scale-zero trial recreated that Pod. Each attempted trial now binds a fresh backend
while retaining the original Deployment UID/template guard. Three lifecycle
regressions cover legitimate Pod replacement, parent UID/template drift and unique
execution paths across runs. The failed CI run remains linked in the project notes.

## Dependency and CI changes

Scanner-reported findings were patched in four Atlas Python packages and two
Sentinel Python packages, plus Sentinel's transitive JavaScript test dependency.
The updated five Python dependency sets and the Atlas/Sentinel JavaScript locks
reported zero known findings in the scans run for this review. The Python audit
used `pip-audit 2.10.1`; JavaScript locks used `npm audit`.

Relevant published advisories include [Starlette](https://github.com/advisories/GHSA-82w8-qh3p-5jfq),
[pytest](https://github.com/advisories/GHSA-6w46-j5rx-g56g),
[filelock](https://github.com/advisories/GHSA-2g95-wg33-c5x2),
[GitPython](https://github.com/advisories/GHSA-83vg-56qc-22m7)
and [Undici](https://github.com/advisories/GHSA-2m5v-pch6-74hx).

The project workflows now audit locked Python dependencies. Atlas also runs its
browser-engine tests and JavaScript audit in CI; Sentinel audits its browser-test
lock. Branch-push and pull-request duplication is avoided in the expensive
workflows, and stale Atlas/Sentinel runs are cancelled. The profile's Markdown
check now also runs after a main-branch push.

## Verification scope

Local checks used Python 3.12.14 on Linux. PostgreSQL, Docker/broker and Kubernetes
checks run separately in the linked CI workflows. The local machine did not run
a Docker daemon, so local fixture passes are not recorded as live-container
verification. Check the exact pull-request head and CI result for those checks.
Dependency scans cover the audited Python/JavaScript sets, not container operating
system packages or a penetration test.

The temporal study remains synthetic. ReleaseLens packets still have zero
independent human sufficiency reviews. Existing historical reports, failed
experiments, licenses and AI-assistance/contribution records remain preserved.
Independent personal contribution and production impact require their own evidence.
