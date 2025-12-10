# Directive X-C — Analog Signal Primacy and NMI Isolation
**Ratified v8.2 — 30 November 2025**

Closes Round 37: VQ Resource Exhaustion / DoS

1. Non-Preemptible Analog Path: The veto signal is processed by a dedicated, isolated analog circuit on the guard die with guaranteed end-to-end latency ≤ 2 ns under all load conditions.

2. Flood Auto-Shed: Category-0 event traffic is rate-limited to ≤ 10 % of critical tier capacity. Exceeding adaptive baselines by >20× for ≥ 100 ms triggers automatic shedding and Level-4 audit.

3. Heartbeat Integrity Proof: The NMI circuit continuously transmits an analog self-test wave. Missing two consecutive heartbeat cycles (≤ 10 μs) is treated as tamper → Level-5.

Violation = Category-1 Structural Risk Event → IAS Level-5
