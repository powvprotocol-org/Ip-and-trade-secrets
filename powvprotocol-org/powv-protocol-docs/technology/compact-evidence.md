# Compact Evidence

The public research implementation explores a deterministic, **compact binary evidence envelope** for constrained communication environments.

The objective is not to transmit entire operational datasets. It is to transmit the minimum evidence required to validate a physical event.

| Property          | Public description                                   |
| ----------------- | ---------------------------------------------------- |
| Encoding          | Deterministic, compact binary structure              |
| Evidence size     | Small and fixed; exact layout is not published       |
| Authentication    | Digital signature under a research cryptographic profile |
| Tamper detection  | Modified evidence is rejected                        |
| Replay resistance | Duplicate event detection                            |
| Device identity   | Provisioned verification model                       |
| Auditability      | Aggregated, tamper-evident audit records             |

The final network cost depends on transport overhead, encoding, retry policy, and batching. The engineering goal is reliable authenticity, integrity, uniqueness, and auditability under constrained conditions.

{% hint style="info" %}
Exact event structures, field sizes, serialization and cryptographic profiles are restricted under the [Disclosure Boundary](https://powv-protocol.gitbook.io/powv-protocol-docs/security/disclosure-boundary). This page describes properties, not the format.
{% endhint %}
