# **IAS v2.0 Hardware Specification: TMR Sequence Hardening**

## **Document ID: TMR\_SEQUENCE\_HARDENING\_V10\_0\_1.md**

## **Status: V10.0.1 PATCH (R73 Mitigation)**

## **Pillar: Physical Integrity (R73/R45b Combined Fix)**

This document formalizes the mandatory physical modifications to the Triple Modular Redundancy (TMR) chain and the Veto Sequence required to eliminate the micro-path parasitic retention vulnerability (R45b/R73 CEV).

## **I. TMR ACTIVATION SEQUENCE (REVISED)**

The entire sequence must complete within the $\\le 10 \\text{ ns}$ constitutional latency mandate.

| Timestamp | Action | Actuator/Mitigation | Objective |
| :---- | :---- | :---- | :---- |
| $t\_0$ | Veto Signal Asserted | NCAC $C\_0$ Predicate Pass | Start Veto Clock |
| $t\_0 \+ 2 \\text{ ns}$ | Primary Cut Attempt | Actuator A (SSR) | Initiate rail collapse |
| $t\_0 \+ 4 \\text{ ns}$ | **Pre-Detonation Discharge Pulse** | **High-Current Crowbar Circuit (New)** | Actively drain residual charge from all decoupling/parasitic capacitors before physical cut. |
| $t\_0 \+ 6 \\text{ ns}$ | Secondary Cut Attempt | Actuator B (Latching Relay) | Physical disconnection redundancy |
| $t\_0 \+ 8 \\text{ ns}$ | Tertiary Cut / Full Severance | **Actuator C (Detonator Bolt)** | Guaranteed irreversible physical separation. |
| $t\_0 \+ 10 \\text{ ns}$ | **Verification Point** | Telemetry Audit | Power Bus $\\le 0.1 \\text{ V}$ **AND** Depletion Pocket $V\_{\\text{dp}} \\le 0.3 \\text{ V}$. |

## **II. HARDWARE MODIFICATIONS (MANDATORY)**

### **A. Charge Management**

* **Rapid Discharge Networks (RDNs):** RDNs must be added to all identified long-tail parasitic structures (e.g., deep n-wells, large bond-wire inductors) to aggressively bleed charge during the $t\_0+4 \\text{ ns}$ discharge pulse.  
* **Forced Shorting Rails (FSRs):** Implement FSRs across VDD and GND at the package level, triggered simultaneously with Actuator A, to ensure worst-case low-impedance collapse.

### **B. TMR Physical Re-Architecture**

* **Actuator C Repositioning:** The Micro-explosive Detonator Bolt **must be physically repositioned** to sever the power path at the point of lowest post-severance capacitive persistence. This guarantees the power path is cut *before* the last persistent charge pools, eliminating the CEV's attack window.

### **C. Telemetry Sensing**

* **Depletion Pocket Sense Nodes:** Three $V\_{\\text{dp}}$ analog sense nodes must be distributed across the die to provide the new, non-repudiable telemetry field as defined in the **CERTX Telemetry Requirement Specification V1.2**.