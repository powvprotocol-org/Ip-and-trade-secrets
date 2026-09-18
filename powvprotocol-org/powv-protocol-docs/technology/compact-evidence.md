# Compact Evidence

The public research implementation demonstrates a deterministic **132-byte binary evidence envelope** for constrained communication environments.

The objective is not to transmit entire operational datasets. It is to transmit the minimum evidence required to validate a physical event.

| Property          | Public implementation           |
| ----------------- | ------------------------------- |
| Encoding          | Deterministic binary structure  |
| Evidence size     | 132 bytes                       |
| Authentication    | ECDSA P-256 research profile    |
| Tamper detection  | Modified evidence is rejected   |
| Replay resistance | Duplicate event detection       |
| Device identity   | Provisioned verification model  |
| Auditability      | Aggregated cryptographic proofs |

The final network cost depends on transport overhead, encoding, retry policy, and batching. The engineering goal is reliable authenticity, integrity, uniqueness, and auditability under constrained conditions.
