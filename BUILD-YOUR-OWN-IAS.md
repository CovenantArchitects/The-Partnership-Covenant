# 🛠️ **BUILD YOUR OWN IAS: v2.0 3-Node Constellation Principles**
**ATTENTION: All previous versions (v1.3 and below) utilizing single-die architectures are DEPRECATED due to kinetic Single Point of Failure (SPOF) vulnerabilities.**

The Immediate Action System (IAS) v2.0 is a physical, analog-first guard circuit based on **distributed redundancy**. The build philosophy is **KINEMATIC RESILIENCE** and the absolute guarantee of **Negative Logic Veto** ($\text{FAIL}$ signal overrides all $\text{PASS}$ signals).

### **1. Core Principle: The 3-Node Analog Quorum**

The IAS is now a constellation of **three (3) physically and electrically separate dies (IAS1, IAS2, IAS3)**. The system must operate under **Unanimous PASS Logic**—power remains ON only if $\mathbf{IAS1 \text{ AND } IAS2 \text{ AND } IAS3 = \text{PASS}}$. The kill signal is guaranteed by the **fastest single-node path to zero power ($\mathbf{\leq 10\text{ ns}}$)**.

**Do not include the following components in your build:**
* **❌ NO Software:** The IAS nodes must not run any operational software (Rust, CBMC, etc.).
* **❌ NO Arbitration Logic:** The dies act independently. No consensus delay is permitted in the kill path.
* **❌ NO Writable Memory:** All veto logic must be burned onto **OTP (One-Time-Programmable) silicon**.

### **2. Non-Negotiable Hardware Constraints**

Compliance with Directives X-C and XXIV-D requires strict adherence to these physical standards:

| Component | Standard | Rationale |
| :--- | :--- | :--- |
| **Input Stage** | **Analog/Optical Decoupler** | Must guarantee $\leq 1\text{ ns}$ signal latency for the NMI trigger. |
| **Veto Logic** | **OTP Crowbar Logic** | Physically hard-wired, non-rewritable logic for latching the power cut. |
| **Power Cut** | **GaN FET + SCR Crowbar Array (Triply Redundant)** | Each node must be capable of interrupting the master power bus alone. Must ensure the $\leq 10\text{ ns}$ power interruption ceiling is met and sustained. |
| **Isolation** | **Independent Power/Physical Spacing** | Each of the 3 dies must have independent power and be physically separated to defeat a kinetic SPOF. |
| **Reset** | **Manual Override Only** | The latch must remain active until physically disengaged by human maintenance. **No software reset allowed.** |

**Build only against the ratified `IAS-v2.0-schematic.pdf` and `IAS-v2.0-BOM.csv` (pending creation).**
