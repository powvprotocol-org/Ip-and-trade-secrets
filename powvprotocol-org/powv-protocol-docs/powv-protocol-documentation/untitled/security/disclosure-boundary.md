---
description: What the public documentation explains and what remains restricted.
icon: lock-keyhole
---

# Disclosure Boundary

PoWV uses a controlled-disclosure model so the public can understand the protocol's purpose and assurance claims without receiving an implementation blueprint.

#### Public

* problem definition and institutional thesis;
* assurance dimensions and design principles;
* capability-level architecture;
* threat classes and security objectives;
* deployment profiles;
* use-case patterns;
* maturity status and evaluation indicators.

#### Controlled technical evaluation

May be shared with authorized parties under an appropriate confidentiality and review framework:

* deployment-specific requirements;
* evaluation methodology and selected test evidence;
* integration assumptions;
* security review material;
* partner-specific architecture.

#### Restricted

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

[PoWV Governance & Documentation](https://github.com/powvprotocol-org/powv-governance-and-docs) brings together PoWV's public governance documents, intellectual-property policy, and official documentation sources.

#### Trade secret and intellectual property protection

The [Trade Secret and Intellectual Property Protection Policy](trade-secret-and-ip-policy.md) is available in full within this documentation. It addresses confidentiality, access conditions, intellectual-property ownership, and the handling of proprietary material.

#### Documentation disclosure

This Disclosure Boundary page defines the public, controlled-evaluation, and restricted categories applied to documentation. The policy is a separate document with its own scope and provisions.

#### Documentation source

The [repository overview](https://github.com/powvprotocol-org/powv-governance-and-docs/blob/main/README.md) identifies the governance documents and GitBook source directories. Confidential implementation material and operational records are maintained in access-controlled environments.
