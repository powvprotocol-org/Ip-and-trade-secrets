---
description: >-
  How the proposed PoWV products relate to the protocol, to each other and to
  the decisions they support.
icon: boxes-stacked
---

# Product Portfolio

{% hint style="warning" %}
**Product proposals, not available products.**

This section describes intended product roles and architecture. No product described here is generally available, certified or deployed in production. Current maturity is stated on each page and summarized in [Maturity and Availability](maturity.md).
{% endhint %}

PoWV addresses one problem: digital systems increasingly make financial, operational and regulatory decisions about physical things they cannot observe directly. The protocol proposes an evidence layer between physical operations and the systems that rely on them.

The research behind PoWV is broader than security engineering. It includes:

- physical asset backing;
- institutional recognition of economic value;
- **real-world asset (RWA) tokenization**;
- trade finance;
- potential financial settlement.

Recent engineering work concentrates on the foundation those uses depend on: evidence admissibility, provenance, security and operational authorization. That focus narrows what is built first. It does not narrow the thesis.

The portfolio turns the thesis into four product proposals. Each has a bounded role. No single product is expected to resolve, alone, the question of whether a physical claim is true.

## Four layers from physical asset to financial instrument

The portfolio is organized around a strict separation between four layers. Each layer answers a different question, and a positive answer in one layer is never assumed in the next.

| Layer | Question it answers | Who is responsible | PoWV role |
| --- | --- | --- | --- |
| **1. Physical evidence generation and verification** | What was observed about the asset or event, and can that evidence be checked? | Capture source and verifier | **Core:** Secure Capture Node, Protocol Suite |
| **2. Operational trust and authorization** | May this actor take this action now, relying on this evidence? | Operator, under its own policy | **Core:** EdgeGuard and the Digital Treasury profile |
| **3. Institutional recognition** of an underlying asset or economic right | Does an economically valid asset or right exist that the institution accepts? Evidence of physical backing informs this decision; it does not decide it. | Responsible institution, contract, applicable law | **Supplies evidentiary assurance.** The recognition decision is not PoWV's. |
| **4. Downstream tokenization, financing, custody and settlement** | How is the recognized right represented, financed, held and transferred, and when is a transfer final? | Issuers, financiers, custodians, settlement systems | **Intended to support.** PoWV does not operate these functions. |

{% hint style="info" %}
**Current scope.** PoWV does not operate a production token issuance, custody, exchange or settlement platform. Its verification infrastructure is intended to support downstream RWA workflows (layers 3 and 4) where appropriate. RWA tokenization and settlement remain part of the research thesis, subject to technical, legal, regulatory and market validation.
{% endhint %}

## Portfolio at a glance

```
PoWV Secure Capture Node  ◀──▶  PoWV Protocol Suite  ◀──▶  PoWV EdgeGuard
where evidence originates       shared verification       where evidence and device trust
(hardware concept)              rules, evidence            inform operational decisions
                                lifecycle, contracts       ├── Edge Security Agent
                                                           ├── Attestation Engine
                                                           ├── Risk Quarantine Engine
                                                           ├── Authorization Gateway
                                                           ├── Verify Service
                                                           ├── Audit Console
                                                           │
                                                           └── PoWV Digital Treasury
                                                               (EdgeGuard profile for custody
                                                                and financial operations)
                │
                ▼
   Downstream RWA infrastructure (not operated by PoWV)
   institutional recognition · tokenization · financing · custody · settlement
```

The **Protocol Suite**, **EdgeGuard** and the **Secure Capture Node** are distinct products. They interoperate through the Suite's shared verification rules and contracts, and each can be evaluated on its own terms; none is defined as a sub-component of another. **Digital Treasury** is the one deliberate exception: it is a profile of EdgeGuard.

| Product | Role | What it is not | Maturity |
| --- | --- | --- | --- |
| [PoWV Protocol Suite](protocol-suite.md) | Foundational verification infrastructure: evidence lifecycle, verification rules, provenance and contract governance. Potential applications in RWA, traceable physical assets, enterprise finance and tokenization readiness | Not a single end-user application, and not a token issuer | Research architecture; selected software behavior demonstrated in controlled environments |
| [PoWV EdgeGuard](edgeguard/README.md) | Operational security and trust platform that turns device posture, evidence outcomes and policy into authorization decisions | Not a proof that a physical event occurred | Product concept |
| [PoWV Secure Capture Node](secure-capture-node.md) | Dedicated hardware for attributable acquisition of physical events | Not a guarantee that a measurement is correct | Hardware concept; precursor laboratory work only |
| [PoWV Digital Treasury](edgeguard/digital-treasury.md) | EdgeGuard profile for custody and financial environments: trusted authorization of financial operations, alongside custody systems and tokenized-asset infrastructure | Does not itself issue, hold or settle financial assets | Market profile concept |

## How the products relate

The products follow the path that a physical claim takes before anyone relies on it:

1. **Origin.** A physical event is measured, and the **Secure Capture Node** is proposed as an attributable point of acquisition.
2. **Evidence.** The **Protocol Suite** defines how that measurement becomes digital evidence with verifiable integrity and provenance.
3. **Assessment.** **EdgeGuard** combines the evidence outcome with device trust, operational risk and policy.
4. **Decision.** An authorized system or person decides whether an action may proceed. **Digital Treasury** applies this decision step to environments where the action moves value.
5. **Recognition.** A responsible institution decides whether the evidence supports recognizing an underlying asset or economic right. PoWV supplies **evidentiary assurance** to that decision; it does not make it.
6. **Downstream use.** A recognized right may be **tokenized, financed, held in custody or settled** by the systems responsible for those functions. PoWV evidence and authorization records are intended to remain referenceable throughout that lifecycle.

See [Trust Boundaries Across the Portfolio](trust-boundaries.md) for the terminology used at each step.

## Relationship to the protocol documentation

The product pages build on the public protocol documentation:

- **Trust domains:** Physical Context, Evidence Assurance and Authorized Use.
- **Evidence model:** claim, supporting evidence, assurance policy and assurance outcome.
- **Published validation records:** the September 2026 records.

Product names describe intended roles. They do not add security properties beyond those documented and evidenced elsewhere.

## Disclosure

These pages are capability-level descriptions under the PoWV [Disclosure Boundary](https://powv-protocol.gitbook.io/powv-protocol-docs/security/disclosure-boundary). They do not publish:

- interfaces, event structures or serialization;
- cryptographic profiles or key-management procedures;
- device provisioning, firmware or hardware designs;
- scoring weights, thresholds or test material;
- partner-specific configurations.
