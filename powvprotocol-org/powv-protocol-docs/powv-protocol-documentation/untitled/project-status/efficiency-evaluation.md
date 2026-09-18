---
icon: gauge
---

# Efficiency Evaluation

PoWV’s proof of concept explores compact event representations. Current capacity figures are engineering estimates, not measured network performance. Validation must distinguish application payload size from total transmitted traffic, accounting for encoding, transport overhead, retransmissions, and operating conditions.

{% hint style="info" %}
**Evidence status: engineering estimates.** No measured latency, throughput, physical-link performance, or energy-efficiency result is established by the available validation. Passing functional software checks does not establish transport efficiency.
{% endhint %}

## Evaluation dimensions

| Dimension                 | What an evaluation should distinguish                                                        | Current evidence status                                                 |
| ------------------------- | -------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Application payload       | Event data before transport-related overhead                                                 | Engineering estimates; exact internal characteristics are not disclosed |
| Encoding                  | Representation-related expansion relative to the application payload                         | A factor in estimates; no measured comparison established               |
| Total transmitted traffic | Payload plus overhead at a declared measurement boundary, including relevant control traffic | Not measured in the available validation                                |
| Retransmissions           | Additional traffic from repeated delivery attempts                                           | Not measured                                                            |
| Operating conditions      | Workload, connection conditions, and observation period                                      | No field-performance validation established                             |
| Latency and throughput    | Delivery time and successfully processed events per unit of time                             | Not measured                                                            |
| Energy consumption        | Energy required under a defined workload and measurement boundary                            | Not measured                                                            |

## Interpreting capacity estimates

Multiplying an assumed payload size by an event count produces a payload-volume estimate, not a measurement of total network usage. It does not, by itself, account for connection setup, control traffic, encoding expansion, or retransmissions.

Comparisons should use the same measurement boundary, workload, and observation period. A smaller application representation alone does not establish lower end-to-end traffic, faster delivery, or better reliability.

## Requirements for future measured results

A defensible benchmark report should identify:

* the evaluated software version and whether the environment is simulated or physical;
* the workload, observation duration, and number of repeated runs;
* the measurement boundary and whether traffic includes both directions and connection overhead;
* attempted, successfully processed, failed, and retried events as separate counts;
* measurement uncertainty and relevant limitations.

Only results supported by retained measurements and a disclosure review should be presented as measured performance. Exact implementation parameters and operational traces remain restricted.

## Relationship to software validation

The existing [Validation Evidence](validation-evidence.md) documents selected functional software checks. Those results support only the behaviors tested; they do not validate capacity estimates or physical-network performance.

## Disclosure boundary

This section describes evaluation criteria, not internal execution logic. It intentionally omits exact packet layouts and sizes, cryptographic profiles, provisioning procedures, internal interfaces, network topology, and transport configuration.
