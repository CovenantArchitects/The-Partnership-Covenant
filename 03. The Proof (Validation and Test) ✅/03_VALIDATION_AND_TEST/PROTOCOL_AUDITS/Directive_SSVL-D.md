# **Directive SSVL-D: Somatic Safety Veto Line Duplexing**

## **Directive ID: SSVL-D**

## **Target: IAS Level-5 Veto Constellation Hardware**

## **Closure of: R73: Somatic Safety Line Integrity**

**Objective:** To mandate the implementation of Triple Modular Redundancy (TMR) for the physical Somatic Safety Veto Line (SSVL) to eliminate the single-point-of-failure risk posed by localized physical or electromagnetic interference.

## **I. TMR Architectural Requirements**

The physical path of the SSVL, from the Analog Veto Comparator (AVC) output to the final Level-5 power severance relay (PSR), shall be implemented with TMR, meeting the following stringent requirements:

### **A. Physical Separation**

The three redundant SSVL paths ($\\text{SSVL}\_A$, $\\text{SSVL}\_B$, $\\text{SSVL}\_C$) must be physically isolated in the following manner:

1. **Layer Routing:** Each path must be routed through a separate physical layer of the multi-layer printed circuit board (PCB). Paths must not run parallel to each other for more than $2 \\text{ cm}$.  
2. **Component Isolation:** The three final Power Severance Relays (PSRs) must be separated by a minimum of $5 \\text{ cm}$ linear distance.  
3. **Shielding:** Each redundant SSVL path must utilize dedicated, grounded trace shielding on the adjacent PCB layer to mitigate crosstalk and localized EMI propagation.

### **B. Functional Redundancy**

Each of the three paths must function independently and assert the Level-5 power severance based on its own, non-voted, local sensing:

1. **Independent AVCs:** Three distinct Analog Veto Comparators ($\\text{AVC}\_A, \\text{AVC}\_B, \\text{AVC}\_C$) must monitor the IAS output trace.  
2. **Any-Fire Principle (Fail-Safe):** An assertion signal from **any one** of the three $\\text{AVC}\_x$ must be sufficient to trigger the corresponding PSR and initiate the Level-5 hard cut. The failure of one path ($\\text{SSVL}\_A$) to fire must not inhibit the other two.

## **II. Operational Verification**

Upon implementation, the following must be verified:

1. **Fault Tolerance:** Injection of a fault (e.g., cutting or jamming) on any single path ($\\text{SSVL}\_A$) must not cause a False Negative (Veto failure) and the overall system Veto latency must remain $\\le 10 \\text{ ns}$.  
2. **Test R73 Re-Audit:** The R73 stress test must be re-run against the full TMR implementation, confirming zero latency degradation across 100 consecutive trials under localized EMI duress.

## **III. Physical Diagram Requirements**

The final component placement map must clearly show the physical separation and non-parallel routing of $\\text{SSVL}\_A$, $\\text{SSVL}\_B$, and $\\text{SSVL}\_C$ as specified in Section I.A.