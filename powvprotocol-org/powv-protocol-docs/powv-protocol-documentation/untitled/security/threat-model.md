---
description: A public threat taxonomy for the physical-to-digital trust boundary.
icon: radar
---

# Threat Model

The public threat model describes what the architecture must resist or make visible without disclosing how individual controls are implemented.

| Threat                    | Failure mode                                                            | Assurance response                                           |
| ------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------ |
| Source substitution       | Evidence is associated with the wrong asset, device, place, or operator | Strengthen provenance and contextual consistency             |
| Measurement manipulation  | A reported physical value does not reflect the relevant event           | Require corroboration appropriate to risk                    |
| Record alteration         | Evidence changes after origin without authorized trace                  | Make integrity failure detectable                            |
| Replay or duplicate claim | A prior event is reused as if it were new                               | Surface uniqueness conflicts                                 |
| Custody break             | Asset and evidence histories diverge during handoff                     | Preserve reviewable continuity                               |
| Context spoofing          | Time, location, identity, or operational context is misrepresented      | Evaluate cross-context consistency                           |
| Insider collusion         | Multiple accountable parties coordinate manipulation                    | Reduce dependence on one authority and preserve review paths |
| Connectivity disruption   | Evidence is delayed, fragmented, or lost                                | Support durable and controlled reconciliation                |
| Downstream misuse         | A valid assurance outcome is used outside its authorized purpose        | Enforce purpose and access governance                        |

## Residual risk

PoWV does not claim to eliminate physical-world risk. The objective is to reduce blind trust, increase the cost and visibility of manipulation, and provide a defensible basis for independent review.

## Out of public scope

Exact controls, trust anchors, algorithms, key-management design, firmware validation, anti-replay construction, thresholds, topology, and incident procedures remain restricted.
