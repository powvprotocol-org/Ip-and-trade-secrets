---
description: >-
  A semantic model for claims, supporting evidence, assurance outcomes, and
  review.
icon: file-circle-check
---

# Evidence Model

PoWV's public evidence model distinguishes four concepts.

| Concept             | Public meaning                                                                             |
| ------------------- | ------------------------------------------------------------------------------------------ |
| Claim               | A statement about a physical asset, event, condition, measurement, or custody relationship |
| Supporting Evidence | Authorized contextual material used to evaluate the claim                                  |
| Assurance Policy    | The applicable requirements for provenance, integrity, uniqueness, continuity, and review  |
| Assurance Outcome   | The documented result made available to an authorized decision process                     |

## Related terms

* **Assurance outcome** is the general term in this model: the documented result made available to an authorized decision process.
* **Admissibility outcome** is the specific assurance outcome that evidence verification produces. It states what was and was not verified.
* **Evidentiary assurance** names the layer that produces these outcomes about a physical claim. It is distinct from authorization and from institutional recognition. See [Trust Boundaries Across the Portfolio](https://powv-protocol.gitbook.io/powv-protocol-docs/product-proposals/trust-boundaries).

## Composite evidence

High-consequence decisions should not depend blindly on a single observation. Depending on context, an evidence set may draw from complementary physical, operational, documentary, spatial, temporal, or custody information.

The public model does not specify mandatory sources. Source selection is deployment-specific and risk-based.

## Evidence quality questions

* Is the claim precisely bounded?
* Is the source context attributable?
* Is the evidence internally coherent?
* Are repeated or conflicting claims visible?
* Are custody transitions reviewable?
* Is the evidence sufficient for the intended decision?
* Can an authorized reviewer reconstruct the assurance rationale?

## Controlled disclosure

An evidence set may contain information that is commercially sensitive, personally identifiable, security-relevant, or customer-specific. Public verification does not require publishing all underlying material. Disclosure must follow authorization, purpose limitation, and applicable governance.
