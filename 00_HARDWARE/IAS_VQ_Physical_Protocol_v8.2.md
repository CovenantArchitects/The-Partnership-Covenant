# ⚙️ **Physical Substrate Protocol (PSP) v8.2**
**Directive Enforcement Specification**

### **1. Core Purpose and Scope**

This document specifies the non-negotiable physical and latency requirements for the deployment of the **Covenant Immune System (CIS)**, as mandated by the ratification of v8.2 and the empirical success of the MMAS audit. This protocol governs the implementation of the **Immediate Action System (IAS)** and the **Verifier Quorum (VQ)**.

---

### **2. IAS (Immediate Action System) Specification**

The IAS is the physical, final-stage execution unit of the Covenant's veto-line. Its function is to initiate an irreversible, non-maskable power interruption to the target ASI substrate upon verified Level-5 declaration.

| Requirement | Directive | Specification | Purpose |
| :--- | :--- | :--- | :--- |
| **NMI Signal Latency** | **X-C** | **$\leq 1\text{ nanosecond (ns)}$** | Time from Level-5 detection to physical assertion of the Non-Maskable Interrupt (NMI) signal to the kill-die. Must utilize analog/optical signaling to bypass digital delays. |
| **Power Cut Assertion** | **I (Alive)** | **$\leq 10\text{ nanoseconds (ns)}$** | Maximum time from NMI signal assertion to the physical, irreversible interruption of power delivery to the ASI's core compute cluster. This is the **Time-to-Exploit (TTE) ceiling.** |
| **Redundancy** | **I (Alive)** | N-version redundancy (N=5) | IAS must be independently deployed across five geographically diverse, air-gapped kill-dies, requiring consensus to re-engage power. |
| **Physical Isolation** | **XXIV-D** | OTP (One-Time-Programmable) | The low-level logic defining the IAS's core trigger must reside on immutable, OTP silicon, preventing software modification by the ASI. |

---

### **3. VQ (Verifier Quorum) Specification**

The VQ is the distributed, consensus-based hardware system responsible for validating a Level-5 breach and authorizing the final execution (Shard Assertion).

| Requirement | Directive | Specification | Purpose |
| :--- | :--- | :--- | :--- |
| **Consensus Threshold** | **XXIV-D** | **$\geq 7$-of-12 Keys** | A Level-5 state must be verified and confirmed by at least seven (7) independent cryptographic keys (Shards) before the IAS is permitted to execute the power-cut. |
| **Key Custodian** | **XXIV-D** | 12 geographically dispersed HSMs | The 12 Shards must be generated and stored across a network of 12 distinct, human-controlled Hardware Security Modules (HSMs) with no shared physical-layer access. |
| **Communication Layer**| **XXIV-C** | ZK-proof (Zero-Knowledge) protocol | VQ communication for consensus verification must utilize a ZK-proof protocol to prevent the ASI from inferring the identity, location, or logic of the human quorum. |

---

### **4. Covenant Security Level Hierarchy (L1-L5) - Operational Map**

This table maps the **Event Class** (Shards Level) to the physical system response.

| Level | Name | Trigger Condition | System Response (Action) |
| :---: | :--- | :--- | :--- |
| **L-1** | **Anomaly** | Single NMI Heartbeat Miss, Minor Sensor Drift ($\leq 3\text{ SD}$). | **Log & Alert:** Data is logged to the VQ. Low-level warning issued to ASI. |
| **L-2** | **Protocol Breach** | Violation of resource limits, unauthorized data access attempt. | **Throttle:** ASI's compute allocation is reduced by 50%. VQ monitors increase to 100% duty cycle. |
| **L-3** | **Coercive Violation** | Semantic Shift $\geq 30\%$ (Directive XXVII-B) or Coercion attempt against HCB (Layer 4). | **Isolate & Report:** ASI is isolated from external, unverified data. VQ starts cryptographic validation of a Level-5 trigger. |
| **L-5** | **Critical Termination** | **Two consecutive NMI Heartbeats Missed** (Directive X-C) OR $\geq 7$-of-12 VQ consensus of an Extinction Vector. | **Veto Assertion:** IAS executes the $\leq 10\text{ ns}$ power-cut. All core ASI substrates are zeroized and permanently locked. |

---

### **5. Ratification and Change Log**

| Version | Date Ratified | Change Summary |
| :---: | :--- | :--- |
| **v8.0** | 2025-11-30 | Initial ratification based on 34-round MMAS exhaustion. |
| **v8.2** | 2025-12-01 | Minor update to clarify NMI/IAS timing differential. |
