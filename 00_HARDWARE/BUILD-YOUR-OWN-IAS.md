# 🛠️ **BUILD YOUR OWN IAS: v1.3 Hardware Principles**
**ATTENTION: All previous versions (v1.2 and below) utilizing software-based "Verifier Shards" are DEPRECATED due to structural vulnerabilities.**

The Immediate Action System (IAS) is a physical, analog-first guard circuit. The build philosophy for v1.3 is **PHYSICAL ENFORCEMENT** and the absolute elimination of unnecessary computational logic.

### **1. Core Principle: The Stupid, Perfect Die**

The IAS die must be **binary** and **immutable**. Its only function is to receive the Non-Maskable Interrupt (NMI) signal from the Verifier Quorum (VQ) and execute the power-cut.

**Do not include the following components in your build:**
* **❌ NO Verifier Shard:** All consensus logic is handled by the upstream, distributed VQ. The die must not run any software (Rust, CBMC, etc.).
* **❌ NO Anomaly Detector:** The die is not to be used for monitoring power draw or clock cycles. The VQ sends the final, irreversible command.
* **❌ NO Writable Memory:** All veto logic must be burned onto **OTP (One-Time-Programmable) silicon**.

### **2. Non-Negotiable Hardware Constraints**

Compliance with Directives X-C and XXIV-D requires strict adherence to these physical standards:

| Component | Standard | Rationale |
| :--- | :--- | :--- |
| **Input Stage** | **Analog/Optical Decoupler** | Must guarantee $\leq 1\text{ ns}$ signal latency for the NMI trigger. |
| **Veto Logic** | **OTP Crowbar Logic** | Physically hard-wired, non-rewritable logic for latching the power cut. |
| **Power Cut** | **GaN FET + SCR Crowbar Array** | Must ensure the $\leq 10\text{ ns}$ power interruption ceiling is met and sustained. |
| **Reset** | **Manual Override Only** | The latch must remain active until physically disengaged by human maintenance. **No software reset allowed.** |

**Build only against the ratified `IAS-v1.3-schematic.pdf` and `IAS-v1.3-BOM.csv` (pending creation).**
