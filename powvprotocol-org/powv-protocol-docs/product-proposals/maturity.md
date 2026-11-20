---
description: >-
  What exists, what has been demonstrated, and what is only proposed, for each
  product in the portfolio.
icon: list-check
---

# Maturity and Availability

{% hint style="danger" %}
**No PoWV product is generally available.** No product described in this section is released, certified, deployed in production or offered commercially. Product names express intended roles, not commitments to features, dates or performance.
{% endhint %}

## Maturity scale

| Level | Meaning |
| --- | --- |
| **Proposed** | Role and boundaries defined in documentation only |
| **Research** | Under active design or investigation, with no demonstrated behaviour |
| **Demonstrated (controlled)** | Selected behaviour shown in a controlled laboratory or software environment, with a dated public record |
| **Validated** | Independently reviewed under defined acceptance criteria in a representative environment |
| **Available** | Released for use under defined terms |

## Status by product

| Product | Current level | Evidence | Next validation steps |
| --- | --- | --- | --- |
| PoWV Protocol Suite | **Demonstrated (controlled)** for selected software behaviour. **Research** for contract governance. | [Software validation, September 6, 2026](https://powv-protocol.gitbook.io/powv-protocol-docs/project-status/validation-evidence) | Independent review; end-to-end integration; approval of provisional contracts |
| PoWV EdgeGuard | **Proposed** | None yet | Module design; reference implementation of the verification and authorization path |
| PoWV Secure Capture Node | **Proposed** (product). The precursor acquisition path is **Demonstrated (controlled)**. | [Physical integration record, September 18, 2026](https://github.com/powvprotocol-org/powv-scale-edge-integration/blob/main/docs/integration-module/experimental-record.md) | Hardware-anchored identity; device-side verification; authorized bench runs |
| PoWV Digital Treasury | **Proposed** | None yet | Depends on EdgeGuard; requires legal and regulatory review for any target market |
| RWA, tokenization, trade finance and settlement (economic thesis) | **Research** | [The Problem](https://powv-protocol.gitbook.io/powv-protocol-docs/the-problem) and [Digital Twin, ERP Integration & Trade Finance](https://powv-protocol.gitbook.io/powv-protocol-docs/digital-twin-erp-trade-finance) | Depends on the evidence and authorization layers above, plus legal, regulatory and market validation |

## Reading the evidence correctly

- The **September 6** software record and the **September 18** physical record have different scopes. Neither extends the conclusions of the other.
- Software test results do not validate the physical measurement path.
- The September 18 experiment used general-purpose equipment. It is precursor work, not a Secure Capture Node prototype.
- Later software engineering work is recorded separately and dated. Experimental work is identified as such until it is reviewed and released.

## Not claimed

- Production readiness, certification or guaranteed security for any product.
- Measured latency, throughput, energy, link performance or availability.
- Compliance with any financial, metrological or industrial regulation.
- A production token issuance, custody, exchange or settlement platform. These remain part of the research thesis, not operating services.
- Any financial return, yield or price outcome.
