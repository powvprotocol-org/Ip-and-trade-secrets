---
description: >-
  Hardware concept for attributable acquisition of physical events, and its
  place in the broader verification architecture.
icon: microchip
---

# PoWV Secure Capture Node

The **PoWV Secure Capture Node** is a proposed dedicated hardware product for acquiring physical events close to the instrument that measures them. It produces evidence that later verification can attribute to an identified device in a known operational state.

{% hint style="warning" %}
**Status: hardware concept.** No Secure Capture Node hardware has been built or validated. The September 18, 2026 laboratory record used general-purpose development equipment to study the acquisition path. It is not a prototype of this product.
{% endhint %}

## Why dedicated capture hardware

The weakest link in a physical-to-digital chain is often the first one: the point where a measurement leaves the instrument and becomes data. Evidence attested far from the instrument can be faithfully protected after the fact and still describe the wrong thing. This is what PoWV research calls the *zero-mile* problem.

The Capture Node is proposed to shorten and harden that first link.

## Intended capabilities

| Capability | Intent | Limit |
| --- | --- | --- |
| Trusted event acquisition | Acquire from the instrument with minimal intermediate handling, and record the conditions of acquisition | Cannot detect an instrument that is miscalibrated or physically manipulated before measurement |
| Device identity | A hardware-anchored identity, so that evidence is attributable to one specific node | Identity shows which device attested. It does not show that the device was used honestly. |
| Key protection | Attestation keys kept in protected hardware and not exportable | Protection depends on the hardware's resistance to physical attack and on provisioning controls |
| Operational integrity | Evidence about the node's own state (software, configuration, tamper indications) available to the [Attestation Engine](edgeguard/README.md#attestation-engine) | A compromised device may misreport. Assessments must allow for this. |
| Constrained connectivity | Evidence that remains verifiable after delay, store-and-forward or intermittent links | Transport performance has not been measured |

## Relationship to the software verification architecture

```
Instrument → Secure Capture Node → evidence → Verify Service ─┐
                       │                                       ├─▶ Authorization Gateway
                       └── identity / state → Attestation Engine ┘
```

- The node **originates** evidence. It does not verify itself.
- The [Protocol Suite](protocol-suite.md) defines how its evidence is verified. Verification works the same way whether evidence comes from a Capture Node or another conforming source; the Capture Node is meant to give stronger **source trust**, not different verification rules.
- [EdgeGuard](edgeguard/README.md) uses the node's identity and state as inputs to device trust and authorization.

## Role in asset-backed workflows

Where a financial instrument refers to a physical asset, the Capture Node is intended to provide **attributable evidence about the physical backing**: that a specific device, in a recorded state, acquired specific measurements at a specific time.

That is evidence **about** the backing, not verification **of** it. Two separate questions remain:

- **Does the backing exist as claimed?** This is established by physical controls and independent inspection.
- **Does it support an economically valid asset or right?** This is a separate institutional recognition decision.

The node's evidence informs both questions and settles neither.

## What the Capture Node does not establish

- That the physical event occurred as measured. Calibration, placement, environment and physical security remain separate controls.
- That the operator acted in good faith.
- Any legal, metrological or regulatory certification.

## Current development maturity

| Area | Status |
| --- | --- |
| Product concept and role in the portfolio | Defined (this page) |
| Laboratory acquisition from a real instrument over a local network | Demonstrated once in a controlled precursor experiment (September 18, 2026), using general-purpose equipment |
| Hardware-anchored identity and protected key storage | Not implemented |
| Device-side verification of evidence | Not demonstrated |
| Secure-element integration, firmware, tamper response | Not implemented |
| Field operation, environmental qualification, certification | Not started |

Board designs, component selection, firmware, provisioning and cryptographic implementation are restricted and are not described publicly.
