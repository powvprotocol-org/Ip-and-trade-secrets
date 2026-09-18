---
description: >-
  Evaluation indicators for completeness, coverage, continuity, exceptions, and
  auditability.
icon: chart-mixed
---

# Assurance Metrics

Metrics turn architectural claims into testable evaluation questions. The indicators below define a public measurement framework; they are **not published performance results**.

#### Evidence Completeness

* **What it evaluates:** Whether the required evidence categories for an applicable policy are present
* **Public status:** Defined for validation

***

#### Verification Coverage

* **What it evaluates:** Whether submitted claims are evaluated against all applicable assurance dimensions
* **Public status:** Defined for validation

***

#### Conflict Detection

* **What it evaluates:** Whether repeated, inconsistent, or mutually exclusive claims are surfaced
* **Public status:** Defined for validation

***

#### Custody Continuity

* **What it evaluates:** Whether required handoffs remain connected to a reviewable evidence history
* **Public status:** Defined for validation

***

#### Exception Rate

* **What it evaluates:** The share of claims requiring authorized review or additional evidence
* **Public status:** Deployment-specific

***

#### Audit Resolution Time

* **What it evaluates:** Time required for an authorized reviewer to trace a decision to its evidence basis
* **Public status:** Benchmark not yet public

***

#### Recovery Integrity

* **What it evaluates:** Whether evidence created under constrained connectivity is reconciled without losing reviewability
* **Public status:** Benchmark not yet public

***

#### Decision Traceability

* **What it evaluates:** Whether an assurance outcome retains a clear, authorized rationale
* **Public status:** Defined for validation

## Interpretation rules

* Metrics must be evaluated against a defined deployment profile and evidence policy.
* A low exception rate is not automatically positive; it may also indicate weak detection.
* Completeness does not guarantee truthfulness.
* Performance measurements must be reproducible before being presented publicly.
* Production claims require controlled validation beyond a research sandbox.

{% hint style="warning" %}
Thresholds, scoring weights, acceptance rules, test vectors, benchmark datasets, and internal validation logic are restricted.
{% endhint %}
