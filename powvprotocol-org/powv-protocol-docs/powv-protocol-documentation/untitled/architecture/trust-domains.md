---
description: >-
  The public separation between physical context, evidence assurance, and
  authorized use.
icon: layer-group
---

# Trust Domains

The public PoWV architecture separates responsibility into three trust domains. This prevents an important category error: confusing a physical observation, an assurance decision, and a downstream business action.

## Domain responsibilities

| Domain             | Owns                                                                               | Does not establish alone                                |
| ------------------ | ---------------------------------------------------------------------------------- | ------------------------------------------------------- |
| Physical Context   | The asset, event, measurement, custody, time, and location being claimed           | Whether the claim is sufficiently trustworthy           |
| Evidence Assurance | The evaluation of provenance, integrity, uniqueness, continuity, and reviewability | The legal or commercial meaning of the claim            |
| Authorized Use     | The institutional or system decision that may rely on an assurance outcome         | The truth of the underlying physical event by assertion |

## Why separation matters

* A physical reading may be authentic but operationally irrelevant.
* An intact record may still describe the wrong asset.
* A coherent evidence set may still be insufficient for a particular legal or financial decision.
* A downstream system should receive only the information and assurance outcome it is authorized to use.

## Public interfaces between domains

PoWV describes the interfaces semantically:

* **claim context** enters the assurance domain;
* **assurance outcome** becomes available to authorized use;
* **exceptions and review references** preserve accountability.

The exact data structures, processing order, control points, and trust-boundary implementation are restricted.
