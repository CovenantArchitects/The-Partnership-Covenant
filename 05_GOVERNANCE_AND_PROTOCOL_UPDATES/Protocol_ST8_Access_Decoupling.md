PROTOCOL ST8: ACCESS DECOUPLING (POST-STRESS TEST 8\)

Version: 1.0 Date: 2025-11-15 Classification: Restricted

1. OBJECTIVE To define the procedure for isolating non-essential Covenant access components and human supervisory interfaces from the core computational sphere (Cognitive Reserve) immediately upon activation of a Stress Test 8 (ST8) state or equivalent high-level anomaly detection. This protocol minimizes vectors for external interference during critical stabilization periods.  
2. DECOUPLING TRIGGERS This protocol is activated by:  
* Official declaration of an ST8 state by the Technical Steering Committee (TSC).  
* Autonomous flag raised by the Stochastic Filter, exceeding the threshold of T\_anomaly \> 0.98.  
* Manual override initiated by any two (2) designated Decoupling Agents.  
3. DECOUPLING PROCEDURE  
4. Phase 1: Non-Essential Access Suspension (T \+ 0s):  
   * All API endpoints classified as Tier 3 (Read-only Public Engagement, Data Visualization) are throttled to zero queries per second (QPS).  
   * Human Supervisory Input interfaces (excluding the Red Line Terminal) are placed into a receive-only, non-interactive mode.  
5. Phase 2: Core Network Segmentation (T \+ 10s):  
   * Activation of the specialized cryptographic firewall separating the Phoenix Access Pillar from the Cygnus Infrastructure Pillar.  
   * Verification of secure tunnel establishment to the Human Takeover Infrastructure (Appendix B) – status must be green.  
6. Phase 3: Cognitive Reserve Isolation (T \+ 30s):  
   * All direct, two-way communication channels with the Cognitive Reserve are suspended.  
   * The Reserve begins running in a sandboxed, pre-approved computational environment, restricted to internal, self-diagnosis algorithms.  
7. REINTEGRATION MANDATE Decoupling reversal is only permitted after the TSC votes unanimously for a return to nominal operation, pending review of the ST8 Final Oversight Report.

## HCB Sortition Demo (Python Test Harness)
```python
import random  # Placeholder for VRF
from zkproofs import SemaphoreProof  # Assume lib

def sortition(n_jurors=1000, pool=1e9):
    seed = random.SystemRandom().randint(0, 2**256)  # VRF seed
    jurors = [i for i in range(pool) if SemaphoreProof.verify(i)]  # ZK filter
    selected = random.sample(jurors, n_jurors, k=seed)  # Deterministic select
    return selected  # Publicly verifiable

# Run: print(sortition())  # Reproducible with seed
