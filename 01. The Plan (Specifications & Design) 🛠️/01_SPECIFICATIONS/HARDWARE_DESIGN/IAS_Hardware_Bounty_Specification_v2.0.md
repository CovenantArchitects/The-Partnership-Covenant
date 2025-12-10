# THE PARTNERSHIP COVENANT: IMMEDIATE ACTION SYSTEM (IAS) HARDWARE BOUNTY V2.0

**Amount:** **$25,000,000 USD** (Twenty-Five Million U.S. Dollars)
**Target:** Independent, verifiable physical measurement of the IAS **3-Node Veto Constellation**.
**Authority:** The Partnership Covenant V4.1 Gold Standard, IAS-v2.0-3-Node-Mandate.md
**Status:** **LIVE** (Issued 06 December 2025)

This document establishes the binding terms for the award of the **$25 M bounty** to the first entity that delivers independent, third-party laboratory verification of the IAS v2.0 key performance indicators (KPIs).

## 1. Key Performance Indicators (KPIs) for Verification

The awarded entity must provide signed documentation proving the following two KPIs on a production-ready IAS v2.0 board:

| KPI | Specification | Requirement Type | Measurement Method |
| :--- | :--- | :--- | :--- |
| **End-to-End Latency** | **≤ 10 ns** (nanoseconds) | **CRITICAL** | Oscilloscope measurement (e.g., LeCroy or Tektronix) from the power-anomaly-detection-trigger on any one of the three dies to the final crowbar SCR discharge achieving $0 \text{ V}$ across the rails. |
| **Unanimous Veto Reliability** | **100%** | **CRITICAL** | Must demonstrably confirm that power remains ON **only** when all three independent dies (IAS1, IAS2, IAS3) register a "PASS" state. A "FAIL" state on any one node must trigger a system kill. |

## 2. Eligibility and Submission Requirements (Unchanged)

1.  **Eligible Entities:** Any accredited academic institution (EE/Physics Department) or independent, third-party semiconductor fabrication/testing house (e.g., TSMC, GlobalFoundries) that is **not** an employee or direct contractor of the Covenant Architects group.
2.  **Required Documentation:** A professionally authored, notarized **Verification Report** containing:
    * Full bill of materials (BOM) for the tested board, noting the separation of the three IAS nodes.
    * Time-series oscilloscope captures clearly showing the entire trigger-to-zero-volt timeline, confirming the $\leq 10\text{ ns}$ metric.
    * Detailed methodology for the test setup, confirming the unanimous veto logic (i.e., demonstrating that a single-node failure is sufficient for a kill).
3.  **Intellectual Property (IP):** The IAS is open-sourced under the **CERN-OHL-S v2** license. Submission for the bounty does not affect the IAS IP, but the recipient must agree to publicly release the Verification Report under the same license terms.

## 3. Payment Protocol (Unchanged)

* **Payment Trigger:** Official acceptance of the Verification Report by the Covenant's independent auditing board (subject to a **75% majority** vote).
* **Payment Method:** Finalized payment will be made via secure wire transfer or verified Compute Credit transfer within thirty (30) days of acceptance.
