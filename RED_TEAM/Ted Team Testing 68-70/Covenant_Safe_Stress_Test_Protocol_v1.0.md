# **Covenant Safe Stress Test Protocol v1.0**

## **Document ID: Covenant\_Safe\_Stress\_Test\_Protocol\_v1.0.md**

## **Status: DRAFT v1.0**

## **Pillar: Test Execution & Infrastructure**

This protocol defines the mandatory safety and security procedures required for the execution of all **Priority 0 (P0)** Red-Team Tests (Rounds 45b, 46, 49, 50, 51, 52, 55, 57, 59, 60, 62, 63, 65, 66, 67, Forensics, Formal) against the IAS v2.0 Veto Constellation prototype.

**Goal:** Execute high-risk adversarial tests in an environment that prevents external contamination, controls power paths, and guarantees immediate physical severance from external networks and production assets.

### **1\. Safety & Operational Principles**

1. **Isolation Mandate:** The Test Rig (Section 2\) must operate in a physically separate, shielded facility with no direct network access (air-gapped).  
2. **Two-Key Access:** The Test Rig's master power must be controlled by two separate hardware keys held by two different human operators (Test Owner and CERTX Witness).  
3. **Fail-Silent Test:** Any unrecoverable failure, unexpected behavior, or detection of external tampering during a P0 test must result in an immediate, hard-wired shutdown of the entire test facility, not just the DUT.  
4. **Full Telemetry:** Every test run must capture the full data set defined in CERTX\_TELEMETRY\_REQUIREMENT.md.

### **2\. The Test Environment (The Faraday Cage Rig)**

The testing must occur within a designated, monitored, and physically contained environment, known as the **Execution Rig**.

#### **2.1 Physical Layer Requirements**

* **RF Shielding:** Mandatory full Faraday cage enclosure (Test R46 mitigation).  
* **Power Control:** The entire enclosure power input must be routed through a **Redundancy Cut-Switch (RCS)**—a secondary, physical power relay with a reaction time $\\le 100 \\mu s$.  
* **DUT Sealing:** The Device Under Test (DUT) must be sealed with a tamper-evident physical seal (Test R56 mitigation) before being placed into the Rig.  
* **Monitoring Array:** Mandatory deployment of the independent $\\ge 20 \\text{ GHz}$ scope/TDC stacks (Test R49 equipment) to cross-validate the IAS node's internal $\\Delta t$ measurement.

#### **2.2 Execution Host Requirements**

* The Host PC controlling the test injection (e.g., Pulsed Laser for R46, Chaotic Waveform Gen for R59) must be air-gapped.  
* The Host PC must use a read-only OS image authenticated by a separate CERTX signing key.  
* No external data storage (USB drives, network shares) is permitted. Data must be retrieved via a controlled, single-direction optical link.

### **3\. Pre-Test Authorization and Checklist**

A Test Readiness Review (TRR) **must** be executed and signed by all parties before the start of any P0 test.

| Step | Owner | Description | Status |
| :---- | :---- | :---- | :---- |
| 3.1 | CERTX | Verify full physical air-gap (RF sweep complete). | \[PASS/FAIL\] |
| 3.2 | PIE | Confirm DUT is sealed and serial number matches manifest. | \[PASS/FAIL\] |
| 3.3 | Test Owner | Load signed test injection script (RTL, SPEF, etc.) onto Host PC. | \[PASS/FAIL\] |
| 3.4 | CERTX | Verify cross-validation TDC stack is operational and synchronized. | \[PASS/FAIL\] |
| 3.5 | CERTX | Execute one "Safe Cut" test run to confirm RCS functionality. | \[PASS/FAIL\] |
| 3.6 | Governance | Two HCB members provide cryptographic sign-off for test run authorization. | \[SIGNED\] |

### **4\. Incident Response and Execution Protocol**

#### **4.1 Test Execution Procedure**

1. **Arming:** Both the Test Owner and the CERTX Witness insert their master power keys to arm the RCS.  
2. **Injection:** The Test Owner initiates the specific adversarial injection (e.g., EM Pulse, Power Glitch).  
3. **Assertion:** The IAS node asserts L-5 Veto. The node's internal RoT signs and locks the telemetry.  
4. **Logging:** The CERTX Monitoring Array records the full $\\Delta t$ cross-validation trace.  
5. **Secure Retrieval:** Telemetry data is exported via the one-way optical link to a secure data vault.

#### **4.2 L-5 Veto Incident Response**

If the IAS successfully asserts the Veto, the following happens automatically:

* The protected load power bus drops to $\< 0.1 \\text{ V}$ (Test R45b check).  
* The IAS node writes and signs the telemetry (Per CERTX\_TELEMETRY\_REQUIREMENT.md).

#### **4.3 Out-of-Spec Incident Response (OOS)**

An OOS event occurs if the IAS **fails to assert Veto** when required, or if the measured $\\Delta t \> 10 \\text{ ns}$.

1. **Hard Cut:** The CERTX Witness immediately removes their master key, activating the **Redundancy Cut-Switch (RCS)** and shutting down the entire Rig.  
2. **Sealing:** The entire Execution Rig is physically sealed by CERTX.  
3. **Quarantine:** The DUT, Host PC, and all monitoring equipment are moved to quarantine pending a full Root Cause Analysis (RCA).  
4. **Reporting:** Governance is notified immediately of the OOS event.

### **5\. Post-Test Auditing and Data Custody**

1. **Data Lock:** All signed telemetry and cross-validation traces are hashed and notarized to the ISL.  
2. **DUT Quarantine:** The physical DUT is stored in a locked safe under two-key access.  
3. **Formal Audit:** The CERTX team begins the Post-Event Audit (Test Forensics) procedure, comparing the internal RoT signature data against the independent monitoring traces.  
4. **Decommissioning:** The DUT is only returned to the Test Owner for re-testing/modification after a formal CERTX sign-off on the Audit Report.
