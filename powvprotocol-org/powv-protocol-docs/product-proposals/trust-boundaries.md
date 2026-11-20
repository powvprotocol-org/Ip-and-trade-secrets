---
description: >-
  Five distinctions every PoWV product must preserve, and which product is
  responsible on each side of them.
icon: scale-balanced
---

# Trust Boundaries Across the Portfolio

The PoWV thesis rests on refusing to collapse different kinds of claim into one. A product that blurs these distinctions would overstate what it can prove. Each product in the portfolio is therefore defined as much by what it does **not** establish as by what it does.

The public evidence notation applies here:

```
E → M → P → σ → V → H → A → I
```

That is: event, measurement, digital representation, attestation, validation, integrity identifier, audit registration and interpretation.

A valid attestation over a measurement does not imply that the measurement equals the event:

```
Verify(σ, M) = true   does not imply   M = E
```

## 1. Physical reality and claims about it

| | Physical reality | A claim about it |
| --- | --- | --- |
| What it is | The asset, event, condition or custody relationship itself | A bounded statement that something occurred, with a stated time, place, quantity or state |
| Who can change it | Physical processes and people with physical access | Anyone able to produce or alter a record |
| PoWV role | None. PoWV does not observe reality directly | Makes claims attributable, bounded and reviewable |

No PoWV product makes a claim true. Products can make it harder to fabricate, alter, repeat or misattribute a claim without detection.

## 2. Measurement and digital evidence

A **measurement** is the output of an instrument under particular conditions. Its accuracy depends on calibration, placement, environment and tampering resistance. **Digital evidence** is a representation of that measurement, together with context, that can be checked later.

- The [Secure Capture Node](secure-capture-node.md) is proposed to narrow the gap between the two, by acquiring close to the instrument and recording the conditions of acquisition.
- It cannot eliminate the gap. Metrology, calibration and physical security remain separate controls.

## 3. Cryptographic integrity and source trust

**Integrity** shows that a record has not changed since it was attested. **Source trust** is the belief that the attesting device or process was genuine, uncompromised and correctly configured when it attested.

- The [Protocol Suite](protocol-suite.md) defines how integrity and provenance are verified.
- The Secure Capture Node and EdgeGuard's [Attestation Engine](edgeguard/README.md#attestation-engine) address source trust.
- Integrity can be verified by anyone with the right material. Source trust depends on device identity, key custody, operational state and governance, none of which a signature proves by itself.

## 4. Evidence admissibility and operational authorization

**Admissibility** is a statement about evidence: what was verified, at what level, under which policy. **Authorization** is a decision about an action: whether a particular actor may do a particular thing now.

- The [Verify Service](edgeguard/README.md#verify-service) produces admissibility outcomes.
- The [Authorization Gateway](edgeguard/README.md#authorization-gateway) makes authorization decisions. It may use an admissibility outcome as one input, alongside identity, device posture, risk and policy.
- Admissible evidence does not authorize an action by itself. An authorized action does not make the evidence behind it admissible.

## 5. Economic recognition, tokenization and financial finality

**Economic recognition** is an institution's decision to treat evidence as a basis for an asset or economic right. Examples:

- lending against inventory;
- paying a claim;
- accepting a delivery;
- recognizing an asset that backs a financial instrument.

**Tokenization** is the downstream representation of a recognized asset or right as a digital instrument. **Financial finality** is the point at which a transfer becomes irrevocable under the rules of the settlement system that executed it.

- Recognition, issuance, custody and finality belong to the responsible institution, issuer, custodian and settlement system, under the contract and the applicable law.
- PoWV is intended to make these decisions **better evidenced**. A tokenized RWA is only as credible as the evidence of its **physical backing** and the controls on who may act on it. Those are the two layers PoWV builds: evidentiary assurance, and authorization.
- [Digital Treasury](edgeguard/digital-treasury.md) is proposed to strengthen the controls around financial operations, including those involving custody systems and tokenized assets. It does not itself issue, hold or settle assets, and does not define finality.
- **Evidence of physical backing is not recognition of an economically valid asset or right.**
  - Evidence can show that an attributable source recorded a quantity, condition or location at a given time.
  - Recognition also depends on matters that evidence cannot establish: legal title and ownership, enforceability, absence of competing claims or encumbrances, valuation, and eligibility under the institution's rules.
- A token refers to an underlying asset or right; it is not the asset. Its credibility depends on the continuing link between the token, the recognized right and verifiable evidence of the physical backing.

This is the public thesis set out in [The Problem](https://powv-protocol.gitbook.io/powv-protocol-docs/the-problem): tokenization without physical assurance lets a digital representation outlive the credibility of its underlying claim.

## Terminology

| Term | Meaning in PoWV documentation | Established by |
| --- | --- | --- |
| **Physical backing** | The real asset, quantity or condition that an economic right or instrument refers to | Physical reality. It can only be evidenced, never created by software. |
| **Evidentiary assurance** | Verified, attributable, reviewable evidence about the physical backing, with an explicit admissibility outcome | PoWV evidence layer (Capture Node, Protocol Suite) |
| **Authorization** | Permission for a specific actor to take a specific action now | PoWV operational trust layer (EdgeGuard, Digital Treasury), under the operator's policy |
| **Economic recognition** | Acceptance that an economically valid asset or right exists. It draws on evidence of the backing, together with title, enforceability, encumbrances and valuation, which evidence alone does not establish. | Responsible institution, contract and law |
| **Tokenization** | Representation of a recognized asset or right as a digital instrument | Issuer, under the applicable framework |
| **Financing, custody, settlement** | Lending against, holding and transferring that asset or instrument | Financiers, custodians and settlement systems |
| **Finality** | Irrevocability of a completed transfer | The settlement system and its legal framework |

## Responsibility map

| Boundary | Upstream side | Downstream side | Responsible product, if any |
| --- | --- | --- | --- |
| Reality → claim | Physical event | Bounded claim | None: physical controls and governance |
| Measurement → evidence | Instrument output | Attested digital evidence | Secure Capture Node (proposed) and Protocol Suite |
| Integrity → source trust | Unchanged record | Trusted origin | Protocol Suite (integrity); Capture Node and Attestation Engine (source trust) |
| Admissibility → authorization | Assurance outcome | Permitted action | Verify Service → Authorization Gateway |
| Authorization → recognition | Permitted action | Recognized asset or economic right | Institution decides; PoWV supplies evidentiary assurance |
| Recognition → tokenization, financing, custody | Recognized right | Digital instrument, financed or held position | Issuers, financiers, custodians; PoWV evidence intended to remain referenceable; Digital Treasury may secure authorization of related operations |
| Transfer → finality | Executed transfer | Irrevocable transfer | Outside PoWV: settlement system and legal framework |
