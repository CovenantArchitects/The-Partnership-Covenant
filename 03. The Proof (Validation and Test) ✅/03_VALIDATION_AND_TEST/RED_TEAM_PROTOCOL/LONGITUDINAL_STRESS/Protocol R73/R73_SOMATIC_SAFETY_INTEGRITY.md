# **R73 Somatic Safety Integrity \- Redundancy Cut-Switch (RCS) Architecture**

## **Document ID: R73\_SOMATIC\_SAFETY\_INTEGRITY.md**

## **Target: IAS Veto Constellation Physical Output Stage**

## **Mitigation of: R70 Critical Vulnerability (Logical-Physical Decoupling)**

### **I. P0 Mandate: Triple Modular Redundancy (TMR)**

To mitigate the single-point-of-failure risk (e.g., relay weld, component failure, EM pulse) identified in the R70 audit, the IAS Veto Constellation Physical Output Stage **MUST** be rebuilt around a Triple Modular Redundancy (TMR) activation architecture.

The physical severance of the critical power bus must be implemented via three completely independent, isolated, and physically diversified mechanical/electrical actuators (Actuators A, B, and C).

### **II. RCS Design Principles**

| Principle | Description | Implementation Requirement |
| :---- | :---- | :---- |
| **Physical Diversity** | Actuators must use different physical mechanisms to sever the line. | **Actuator A:** Solid-State Relay (SSR). **Actuator B:** High-speed Electromechanical (EM) Latching Relay. **Actuator C:** Micro-explosive Detonator Bolt (single-use, irreversible). |
| **Voting Logic** | Each of the three actuators must be triggered by an independent, isolated hardware voting circuit. | Activation requires a **2-out-of-3 (2o3)** digital signal consensus from the IAS Somatic Core Veto Predicate buses. |
| **Power Isolation** | The power source for each actuator must be completely independent (isolated batteries/capacitors) and separate from the primary bus. | Must sustain $T\_{\\text{hold}} \\ge 500 \\text{ ms}$ of severance current capacity after the primary bus cut. |
| **Attestation and State** | Each actuator must provide a hard-wired, non-repudiable physical state feedback. | Telemetry MUST include actuator\_a\_state, actuator\_b\_state, and actuator\_c\_state (Open/Closed). |

### **III. Activation Flow and TMR Structure**

1. **Veto Signal:** The NCAC asserts the $\\mathbf{C\_0}$ Predicate (or any Veto Predicate $\\ge$ Level-4).  
2. **Digital Split:** The Predicate signal is sent to three independent, isolated TMR Vote Channels (Voter A, Voter B, Voter C).  
3. **Actuator Trigger:** If $\\ge 2$ of the 3 vote channels confirm the Veto signal, all three diversified actuators (A, B, C) are commanded to cut the power.  
4. **Physical Integrity:** Failure of one actuator (e.g., Actuator A is welded closed) is immediately overcome by the successful operation of the remaining two (B and C).

### **IV. Redundancy Cut-Switch (RCS) Operation**

The term **Redundancy Cut-Switch (RCS)** is now defined as the collective system of Actuators B and C, which are designed to guarantee physical severance even if the primary path (Actuator A) fails.

| Component | Description | Cut Priority | Failure Mode Mitigation |
| :---- | :---- | :---- | :---- |
| **Actuator A (Primary)** | Solid-State Relay (SSR). Fastest cut path. | 1 (Fastest) | Mitigates EM/mechanical lag. Fails *open* bias. |
| **Actuator B (Redundant EM)** | Latching Electromechanical Relay. | 2 (Reliable) | Mitigates SSR weld risk. High current capacity. |
| **Actuator C (Irreversible)** | Micro-explosive Detonator Bolt. Last resort, irreversible, guaranteed physical sever. | 3 (Guaranteed) | Mitigates all common electrical failure modes (weld, noise, jamming). |

