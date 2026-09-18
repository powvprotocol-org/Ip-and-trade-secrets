---
description: >-
  Evaluation indicators for completeness, coverage, continuity, exceptions, and
  auditability.
icon: chart-mixed
---

# Assurance Metrics

Metrics turn architectural claims into testable evaluation questions. The indicators below define a public measurement framework; they are **not published performance results**.

| Indicator             | What it evaluates                                                                                  | Public status            |
| --------------------- | -------------------------------------------------------------------------------------------------- | ------------------------ |
| Evidence Completeness | Whether the required evidence categories for an applicable policy are present                      | Defined for validation   |
| Verification Coverage | Whether submitted claims are evaluated against all applicable assurance dimensions                 | Defined for validation   |
| Conflict Detection    | Whether repeated, inconsistent, or mutually exclusive claims are surfaced                          | Defined for validation   |
| Custody Continuity    | Whether required handoffs remain connected to a reviewable evidence history                        | Defined for validation   |
| Exception Rate        | The share of claims requiring authorized review or additional evidence                             | Deployment-specific      |
| Audit Resolution Time | Time required for an authorized reviewer to trace a decision to its evidence basis                 | Benchmark not yet public |
| Recovery Integrity    | Whether evidence created under constrained connectivity is reconciled without losing reviewability | Benchmark not yet public |
| Decision Traceability | Whether an assurance outcome retains a clear, authorized rationale                                 | Defined for validation   |

## Interpretation rules

* Metrics must be evaluated against a defined deployment profile and evidence policy.
* A low exception rate is not automatically positive; it may also indicate weak detection.
* Completeness does not guarantee truthfulness.
* Performance measurements must be reproducible before being presented publicly.
* Production claims require controlled validation beyond a research sandbox.

{% hint style="warning" %}
Thresholds, scoring weights, acceptance rules, test vectors, benchmark datasets, and internal validation logic are restricted.
{% endhint %}
