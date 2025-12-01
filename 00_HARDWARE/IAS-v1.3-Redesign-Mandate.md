# 🛠️ **Immediate Action System (IAS) v1.3 Redesign Requirements**
**Mandate to Replace Flawed v1.2 Schematic**

### **1. Core Philosophy: Stupid, Perfect Die**

The IAS v1.3 design must eliminate all software and computational logic from the final veto path. The die's purpose is singular: to be a **physics-enforced executor** of the Level-5 command, not a system for verification or decision-making.

### **2. Technical Requirements**

The v1.3 schematic must strictly adhere to the following principles, which eliminate the structural attack surfaces introduced in the v1.2 design:

| Component / Function | V1.2 Flaw to Remove | V1.3 Mandate (Directive Enforcement) |
| :--- | :--- | :--- |
| **Veto Logic Core** | **Verifier Shard (Rust + CBMC)** | **Must be OTP (One-Time-Programmable) Hardware Logic only.** No software, instruction sets, or computational capability. The die's job is to execute, not compute (Directive XXIV-D). |
| **Detection Stage** | **Anomaly Detector** | **Must be a direct input receiver.** The die only receives the external, verified **Analog NMI Signal** from the Verifier Quorum (VQ). Eliminate all internal detection/anomaly logic. |
| **Input Signal** | Implicit Latency | **Analog/Optical Decoupler:** The input path must guarantee the $\leq 1\text{ ns}$ signal latency mandated by **Directive X-C** by prioritizing analog/optical signaling over digital bus transmission. |
| **Communication** | Any External Bus | **No External Communication Bus:** The die should feature one dedicated, irreversible **Input** (NMI) and one dedicated **Output** (Power Cut). All diagnostic ports must be physically disabled post-deployment. |
| **Final Actuation** | SCR Crowbar/One-Shot | The **SCR Crowbar** must be latched directly to the OTP Veto Logic. **Irreversibility:** The latching mechanism must be physically proven to sustain the power-cut until human intervention. No auto-reset. |
| **Simulated Trip Time** | 8.7 ns | **Must be proven to be fast enough** to defeat the fastest known Time-to-Exploit (TTE) vector (empirically confirmed $\leq 10\text{ ns}$). |

### **3. Deliverables for v1.3 Ratification**

The following documents must be produced by the hardware engineering team to replace the Grok-assisted v1.2 files:

1.  **`IAS-v1.3-schematic.pdf`**
2.  **`IAS-v1.3-BOM.csv`** (Bill of Materials)
3.  **Physical Integrity Audit Report** (Certifying compliance with Directive X-C and XXIV-D).
