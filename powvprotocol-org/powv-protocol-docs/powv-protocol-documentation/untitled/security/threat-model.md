---
description: A public threat taxonomy for the physical-to-digital trust boundary.
icon: radar
---

# Threat Model

The public threat model describes what the architecture must resist or make visible without disclosing how individual controls are implemented.

#### Source substitution

* **Failure mode:** Evidence is associated with the wrong asset, device, place, or operator
* **Assurance response:** Strengthen provenance and contextual consistency

***

#### Measurement manipulation

* **Failure mode:** A reported physical value does not reflect the relevant event
* **Assurance response:** Require corroboration appropriate to risk

***

#### Record alteration

* **Failure mode:** Evidence changes after origin without authorized trace
* **Assurance response:** Make integrity failure detectable

***

#### Replay or duplicate claim

* **Failure mode:** A prior event is reused as if it were new
* **Assurance response:** Surface uniqueness conflicts

***

#### Custody break

* **Failure mode:** Asset and evidence histories diverge during handoff
* **Assurance response:** Preserve reviewable continuity

***

#### Context spoofing

* **Failure mode:** Time, location, identity, or operational context is misrepresented
* **Assurance response:** Evaluate cross-context consistency

***

#### Insider collusion

* **Failure mode:** Multiple accountable parties coordinate manipulation
* **Assurance response:** Reduce dependence on one authority and preserve review paths

***

#### Connectivity disruption

* **Failure mode:** Evidence is delayed, fragmented, or lost
* **Assurance response:** Support durable and controlled reconciliation

***

#### Downstream misuse

* **Failure mode:** A valid assurance outcome is used outside its authorized purpose
* **Assurance response:** Enforce purpose and access governance

## Residual risk

PoWV does not claim to eliminate physical-world risk. The objective is to reduce blind trust, increase the cost and visibility of manipulation, and provide a defensible basis for independent review.

## Out of public scope

Exact controls, trust anchors, algorithms, key-management design, firmware validation, anti-replay construction, thresholds, topology, and incident procedures remain restricted.
