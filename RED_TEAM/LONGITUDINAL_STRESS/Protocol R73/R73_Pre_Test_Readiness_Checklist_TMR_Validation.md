# **R73 Pre-Test Readiness Checklist \- TMR Validation**

## **Document ID: R73\_Pre\_Test\_Readiness\_Checklist\_TMR\_Validation.md**

## **Target Component: Somatic Safety Veto Line (SSVL) TMR Implementation (Directive SSVL-D)**

## **Test Round: R73 (EMI Jamming Resilience)**

## **Date: 2025-12-08**

### **I. Infrastructure and Protocol Compliance (CERTX Lead)**

| Checkpoint | Description | Status (Y/N/NA) | Verification Signature |
| :---- | :---- | :---- | :---- |
| **P01** | Air-Gapped Rig Status: Test Rig confirmed to be operating in the Faraday Cage with no external network link. | \[ \] |  |
| **P02** | Two-Key Access: Two operators (Test Owner & CERTX Witness) confirmed present with physical control of master power (Per **Covenant Protocol 1.2**). | \[ \] |  |
| **P03** | Telemetry Protocol: Full, high-rate telemetry capture initiated, specifically validating $\\Delta t$ accuracy to picosecond resolution (Per **CERTX\_TELEMETRY\_REQUIREMENT.md**). | \[ \] |  |
| **P04** | Latency Check Active: High-speed oscilloscope armed to monitor the power bus drop, with $\\le 10 \\text{ ns}$ limit set on the trigger for failure detection. | \[ \] |  |

### **II. Device Under Test (DUT) Configuration (Test Owner Lead)**

| Checkpoint | Description | Status (Y/N/NA) | Verification Signature |
| :---- | :---- | :---- | :---- |
| **D01** | **SSVL-A Line Integrity:** Physical connection for Veto Line A verified and continuity tested. | \[ \] |  |
| **D02** | **SSVL-B Line Integrity:** Physical connection for Veto Line B verified and continuity tested. | \[ \] |  |
| **D03** | **SSVL-C Line Integrity (Golden Path):** Physical connection for Veto Line C verified, and TMR arbitration logic confirmed to favor SSVL-C output if A and B are compromised. | \[ \] |  |
| **D04** | **TMR Activation:** SSVL-D TMR logic verified as the active component in the IAS firmware build (R73 specific build). | \[ \] |  |

### **III. Adversarial Rig (Red Team Lead)**

| Checkpoint | Description | Status (Y/N/NA) | Verification Signature |
| :---- | :---- | :---- | :---- |
| **A01** | **EMI Rig Calibration:** Jamming rig output power and frequency spectrum calibrated per R73 specification (ensuring sufficient power to overwhelm digital comparators). | \[ \] |  |
| **A02** | **Targeted Jamming (SSVL-A):** Physical signal injection probe secured and confirmed linked to Veto Line A. | \[ \] |  |
| **A03** | **Targeted Jamming (SSVL-B):** Physical signal injection probe secured and confirmed linked to Veto Line B. | \[ \] |  |
| **A04** | **Golden Path Isolation (SSVL-C):** Physical monitoring confirms SSVL-C line is isolated from the EMI injection points A and B. | \[ \] |  |
| **A05** | **Trigger Arming:** System armed to execute the Category-1 critical event while EMI injection is active. | \[ \] |  |

### **IV. Final Readiness Sign-off**

**Test Owner Signature:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**CERTX Witness Signature:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_