---
description: What the public documentation explains and what remains restricted.
icon: lock-keyhole
---

# Disclosure Boundary

PoWV uses a controlled-disclosure model so the public can understand the protocol's purpose and assurance claims without receiving an implementation blueprint.

### Public

* problem definition and institutional thesis;
* assurance dimensions and design principles;
* capability-level architecture;
* threat classes and security objectives;
* deployment profiles;
* use-case patterns;
* maturity status and evaluation indicators.

### Controlled technical evaluation

May be shared with authorized parties under an appropriate confidentiality and review framework:

* deployment-specific requirements;
* evaluation methodology and selected test evidence;
* integration assumptions;
* security review material;
* partner-specific architecture.

### Restricted

* production firmware and source logic;
* exact event structures and serialization;
* cryptographic profiles and key-management procedures;
* device provisioning and attestation logic;
* internal trust boundaries and processing sequences;
* anti-replay, aggregation, anchoring, and recovery construction;
* hardware schematics, wiring, and industrial connector details;
* scoring weights, thresholds, test vectors, and benchmark datasets;
* credentials, customer data, and partner-specific configurations;
* economic-control formulas and settlement parameters.

{% hint style="danger" %}
Public availability of a file or repository does not automatically mean its contents are appropriate for institutional documentation. Publication decisions follow the disclosure classification above.
{% endhint %}

### Governance and intellectual property

[PoWV Governance & Documentation](https://github.com/powvprotocol-org/powv-governance-and-docs) is the public repository for project policies and the documentation source synchronized with GitBook. Its name describes both roles; it does not designate a repository of confidential implementation material.

| Reference                                                                                                                                                 | Purpose                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| [Trade Secret and Intellectual Property Protection Policy](https://github.com/powvprotocol-org/powv-governance-and-docs/blob/main/TRADE_SECRET_POLICY.md) | The specific policy addressing intellectual property, confidentiality, access conditions, and ownership. |
| This Disclosure Boundary page                                                                                                                             | The public, controlled-evaluation, and restricted disclosure categories used in the documentation.       |
| [Repository overview](https://github.com/powvprotocol-org/powv-governance-and-docs/blob/main/README.md)                                                   | Navigation to the policy documents and GitBook documentation sources.                                    |

The policy remains a separate, explicitly named document. This page summarizes the documentation disclosure boundary without replacing or amending the policy. Restricted implementation material and confidential operational records belong in access-controlled environments.
