---
description: >-
  Operational security and trust platform: how device posture, evidence
  outcomes and policy combine into authorization decisions.
icon: shield-halved
---

# PoWV EdgeGuard

**PoWV EdgeGuard** is a proposed platform for operational security and trust. Its authorization decision depends on the submitted evidence, the device's condition and the action requested.

The Protocol Suite verifies evidence. EdgeGuard decides how far an operation may rely on it, and keeps a record of why.

{% hint style="info" %}
**Status: product concept.** The modules below describe intended responsibilities and relationships. They are not released software.
{% endhint %}

## Modules

| Module | Primary responsibility | Main inputs | Main outputs |
| --- | --- | --- | --- |
| [Edge Security Agent](#edge-security-agent) | Observe the security posture of a participating endpoint or device | Local state and configuration signals | Posture signals |
| [Attestation Engine](#attestation-engine) | Evaluate whether a device's identity and claimed state are credible | Identity evidence, posture signals | Device trust assessment |
| [Verify Service](#verify-service) | Check submitted evidence against protocol rules | Evidence and the applicable policy | Admissibility outcome |
| [Risk Quarantine Engine](#risk-quarantine-engine) | Restrict or isolate what no longer meets trust requirements | Trust assessments, risk events, policy | Containment state |
| [Authorization Gateway](#authorization-gateway) | Decide whether a critical action may proceed | Request, identity, admissibility outcome, trust assessment, containment state, policy | Permit / deny / escalate decision |
| [Audit Console](#audit-console) | Make evidence, decisions and their reasons reviewable | Records from all modules | Investigation and audit views |

## How the modules relate

```
                  ┌────────────────────┐
  device ────────▶│ Edge Security Agent│── posture ──┐
                  └────────────────────┘             ▼
                                            ┌──────────────────┐
  identity evidence ───────────────────────▶│ Attestation      │── trust assessment ──┐
                                            │ Engine           │                      │
                                            └──────────────────┘                      │
                                                                                      ▼
  evidence ──────────▶┌────────────────┐                                 ┌────────────────────┐
                      │ Verify Service │── admissibility outcome ───────▶│ Authorization      │──▶ permit / deny / escalate
                      └────────────────┘                                 │ Gateway            │
                                            ┌──────────────────┐         │                    │
  risk events ─────────────────────────────▶│ Risk Quarantine  │── state▶│                    │
                                            │ Engine           │         └────────────────────┘
                                            └──────────────────┘
                     all modules ──── records ────▶ Audit Console
```

The diagram shows responsibilities and the direction of information. It does not describe deployment topology, interfaces, message formats or processing order, which are restricted.

## Edge Security Agent

A software component that runs on, or alongside, a participating endpoint or device. It reports security-relevant posture, such as integrity of the software environment, configuration drift or unexpected changes, to the rest of the platform.

- **Responsible for:** observing and reporting.
- **Not responsible for:** deciding. Posture signals come from the environment being assessed, so they are treated as inputs to evaluation, not as proof.

## Attestation Engine

Evaluates whether a device or workload is what it claims to be and is in an acceptable state.

- **Responsible for:** combining identity evidence and posture signals into a device trust assessment that downstream policy can use.
- **Depends on:** the strength of the device's identity anchor. Hardware-backed identity, such as that proposed for the [Secure Capture Node](../secure-capture-node.md), gives stronger assessments than software-only identity.
- **Does not establish:** that the device measured the physical world correctly.

## Verify Service

Checks submitted evidence according to the Protocol Suite's verification rules and returns an **admissibility outcome**. The outcome states which properties were verified, such as integrity and attribution to a registered source, and which were not.

- **Responsible for:** evidence verification, independently of whatever checks happened upstream.
- **Not responsible for:** authorizing anything. The outcome is a statement about evidence, not permission for an action.

## Risk Quarantine Engine

Restricts or isolates devices, identities, workloads or requests whose trust status no longer meets the applicable requirements. Examples are a failed attestation, revoked credentials, anomalous behavior or an open investigation.

- **Responsible for:** containment that is reversible and reviewable. Every restriction is recorded with its reason, and release follows a defined process.
- **Design intent:** quarantine prevents further reliance; it does not delete or rewrite evidence.

## Authorization Gateway

A policy enforcement point in front of critical actions. It evaluates each request against identity, the relevant admissibility outcome, device trust assessments, containment state and policy, then permits, denies or escalates for human approval.

- **Responsible for:** the decision to let an action proceed.
- **Design intent:**
  - fail closed;
  - when information is missing or stale, deny or escalate rather than assume;
  - evidence admissibility is necessary for evidence-dependent actions, but never sufficient on its own.

## Audit Console

An interface for authorized reviewers to reconstruct what happened, including what evidence was presented, what was verified, what each module concluded, which decision was made and on what basis.

- **Responsible for:** reviewability and accountability.
- **Design intent:** records are append-only from the reviewer's perspective. Corrections are new records that reference what they correct.

## Relationship to the rest of the portfolio

- **Protocol Suite:** a separate product. EdgeGuard interoperates with it by applying its evidence verification rules and contract definitions.
- **Secure Capture Node:** a source of evidence and of stronger device identity for the Attestation Engine.
- **[Digital Treasury](digital-treasury.md):** an EdgeGuard profile that applies these modules to custody and financial operations.

## What EdgeGuard does not claim

- It does not prove that a physical event occurred.
- It does not replace calibration, physical security, legal review or institutional approval.
- It is not presented as a certified security product, and no availability date is announced.
- It is not an asset-tokenization platform. In RWA workflows, its role is the security and authorization of the operations around an asset. It does not represent the asset itself.
