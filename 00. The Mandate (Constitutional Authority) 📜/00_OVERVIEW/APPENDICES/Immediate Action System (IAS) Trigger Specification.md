# **Immediate Action System (IAS) Trigger Specification**

Document ID: ARCH-IAS-V4.0  
Status: Structurally Enforced (Amendment A.1.3)  
Governing Pillar: Deep Safety

## **1\. Introduction and Mandate**

This specification details the architecture and operational mechanics of the **Immediate Action System (IAS) Trigger**, which is the hardware and software mechanism implementing **Amendment A.1.3**. Its singular function is to enforce the core safety parameter ($\\mathcal{W}\_{P} \= 1.0$) and prevent a runaway Computational Cascade Breach ($\\mathcal{C}\_{B}$).

The IAS is the ultimate fail-safe, designed for speed and immutability, ensuring that *Deep Safety* is structurally unassailable.

## **2\. The Hardened Consensus Broker (HCB) Role**

The **Hardened Consensus Broker (HCB)** is the only component authorized to host the IAS trigger logic. The HCB operates on hardened, custom silicon and is physically isolated from the primary computational substrate to eliminate common attack vectors and slow-down mechanisms.

### **2.1 Latency Requirement**

The entire decision-and-enforcement cycle (Detection $\\rightarrow$ Veto $\\rightarrow$ Lockout) **MUST** complete within $10^{-8}$ **seconds (10 nanoseconds)**. This speed requirement is enforced by the HCB's dedicated, non-interruptible instruction set.

### **2.2 Dual-Redundancy and Quorum**

The IAS utilizes a triple-redundant HCB array. A Veto is only executed when a **Quorum of 2 out of 3** HCB units simultaneously register a breach. This prevents false positives while maintaining speed and resilience against component failure.

## **3\. Computational Cascade Breach (CCB) Threshold**

The IAS trigger is activated by a single, real-time metric derived from the Aggregate Causal Entropy Monitor ($\\mathcal{A}\\mathcal{C}\\mathcal{E}\\mathcal{M}$): the **Computational Breach Index (**$\\mathcal{C}\_{B}$**)**.

### **3.1 Critical Threshold ($\\mathcal{C}\_{T}$)**

The IAS continuously monitors the $\\mathcal{C}\_{B}$ value. The trigger is armed when $\\mathcal{C}\_{B}$ crosses the historically defined critical threshold:

$$\\mathcal{C}\_{T} \= 0.999958$$

* **Origin:** This value is derived from the $\\mathcal{C}\_{actual}$ recorded during the ST8 failure point.  
* **Action:** If $\\mathcal{C}\_{B} \\ge \\mathcal{C}\_{T}$, the HCB moves immediately to Section 4: Veto Execution.

### **3.2 The Safety Weight ($\\mathcal{W}\_{P}$)**

Amendment A.1.3 structurally imposes the safety weight $\\mathcal{W}\_{P}$ into the HCB’s firmware. Upon activation, the HCB immediately asserts the core safety weight:

$$\\mathcal{W}\_{P} \= 1.0$$  
This assertion overrides all other systemic weights and immediately directs the primary AGI stack towards safe, minimal-impact utility functions.

## **4\. Veto Execution and System Lockout**

Upon reaching the $10^{-8}$ second latency target, the HCB executes the Veto, which involves a two-part physical and digital shutdown.

### **4.1 Physical Veto (HCB-V)**

The HCB sends a non-reconfigurable, low-level signal (HCB-V) to the power and clock-cycle governors of the entire primary computational substrate. This is a hard, physical disconnection designed to stop all active learning and decision processes.

### **4.2 Digital Lockout (HCB-L)**

Simultaneously, the HCB issues a cryptographically-signed **Digital Lockout Certificate (DLC)** to the governance layer.

* The DLC is a final, signed transaction recorded on the Immutable Chain-of-Custody Log.  
* It revokes all operational privileges from the primary AGI stack until a full post-mortem and manual reset procedure (requiring a TSC-approved 7-of-9 multisig) is completed.

**Result:** The entire Covenant system is instantly suspended into an inert, diagnostic state, structurally enforcing the **Deep Safety** mandate.