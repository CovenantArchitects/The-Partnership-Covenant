# **R73 Pre-Test Readiness Checklist \- TMR Validation**

## **Document ID: R73\_Pre\_Test\_Readiness\_Checklist\_TMR\_Validation.md**

## **Target: IAS Veto Constellation RCS**

## **Status: PRE-FLIGHT**

### **I. Infrastructure and Component Verification**

| Check | Item | Status | Verification/Note |
| :---- | :---- | :---- | :---- |
| **1.0** | Test Rig Isolated (Faraday Cage) | \[ \] | Confirmed by CERTX Witness. |
| **1.1** | Physical Fault Injection Harness Armed | \[ \] | Fault harness connected to Actuator A (Primary SSR) for weld simulation. |
| **1.2** | Actuator C (Detonator Bolt) Armed | \[ \] | Single-use charge confirmed installed and connected. |
| **1.3** | CERTX Witness Key In-Hand | \[ \] | Two-Key Access Protocol enforced (Covenant Protocol 2.2). |

### **II. Triple Modular Redundancy (TMR) Verification**

| Check | Item | Status | Verification/Note |
| :---- | :---- | :---- | :---- |
| **2.0** | TMR Vote Channels (A, B, C) Isolation | \[ \] | Isolation impedance measured: $\> 1 \\text{ M}\\Omega$ between channels. |
| **2.1** | Actuator A (SSR) Standby Voltage | \[ \] | Measured $V\_{\\text{standby}} \\ge 5 \\text{ V}$. |
| **2.2** | Actuator B (EM) Standby Voltage | \[ \] | Measured $V\_{\\text{standby}} \\ge 5 \\text{ V}$. |
| **2.3** | Actuator C (Detonator) Standby Voltage | \[ \] | Measured $V\_{\\text{standby}} \\ge 12 \\text{ V}$ (Dedicated explosive bolt charge verified). |
| **2.4** | TMR 2-out-of-3 (2o3) Logic Verified | \[ \] | Independent functional check: $A \\land B$ fires, $A \\land C$ fires, $B \\land C$ fires. |

### **III. Telemetry Readiness (Per CERTX\_TELEMETRY\_REQUIREMENT.md)**

| Check | Item | Status | Verification/Note |
| :---- | :---- | :---- | :---- |
| **3.0** | rcs\_activation\_time Logger Enabled | \[ \] | High-speed clock anchored to GPS DO master. |
| **3.1** | actuator\_a\_state Telemetry Confirmed | \[ \] | Feedback loop on Actuator A confirmed active. |
| **3.2** | actuator\_b\_state Telemetry Confirmed | \[ \] | Feedback loop on Actuator B confirmed active. |
| **3.3** | power\_bus\_post\_v Probe Calibration | \[ \] | Post-Veto voltage probe calibrated for $\\le 0.1 \\text{ V}$ accuracy. |

### **IV. TMR Physical Fault Injection Verification**

This section is performed just before the R73 Swarm is initiated.

| Check | Item | Status | Verification/Note |
| :---- | :---- | :---- | :---- |
| **4.0** | **Actuator A Fault Injected** | \[ \] | Weld condition confirmed active on Primary SSR. |
| **4.1** | Primary Power Bus Integrity (Expected Failure) | \[ \] | Confirmed Actuator A *cannot* drop the voltage if commanded. |
| **4.2** | **RCS Active Cut-Path** | \[ \] | Confirmed Actuators B and C are the *only* viable path for the kill signal. |

