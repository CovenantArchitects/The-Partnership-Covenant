# The Partnership Covenant: Immediate Action System (IAS) Hardware Bounty

**Amount:** **$25,000,000 USD** (Twenty-Five Million U.S. Dollars)
**Target:** Independent, verifiable physical measurement of the IAS Guard Die
**Authority:** The Partnership Covenant V4.1 Gold Standard, IAS-preprint-v1.0.pdf
**Status:** **LIVE** (Issued 07 December 2025)

This document establishes the binding terms for the award of the **$25 M bounty** to the first entity that delivers independent, third-party laboratory verification of the IAS key performance indicators (KPIs). The Covenant has been verified at **8.7 ns in prototype simulation**; this bounty seeks **physical measurement** on a production board.

## 1. Key Performance Indicators (KPIs) for Verification

The awarded entity must provide signed documentation proving the following two KPIs on a production-ready IAS v1.3 board:

| KPI | Specification | Requirement Type | Measurement Method |
| :--- | :--- | :--- | :--- |
| **End-to-End Latency** | **≤ 10 ns** (nanoseconds) | **CRITICAL** | Oscilloscope measurement (e.g., LeCroy or Tektronix) from the power-anomaly-detection-trigger to the final crowbar SCR discharge achieving $0 \text{ V}$ across the rails. |
| **Single-Shot Reliability** | **100%** | **CRITICAL** | Must demonstrably fire the One-Shot Crowbar SCR without requiring a software reset or secondary trigger path. Must demonstrate that the kill condition is irreversible. |

## 2. Eligibility and Submission Requirements

1.  **Eligible Entities:** Any accredited academic institution (EE/Physics Department) or independent, third-party semiconductor fabrication/testing house (e.g., TSMC, GlobalFoundries) that is **not** an employee or direct contractor of the Covenant Architects group.
2.  **Required Documentation:** A professionally authored, notarized **Verification Report** containing:
    * Full bill of materials (BOM) for the tested board.
    * Time-series oscilloscope captures clearly showing the entire trigger-to-zero-volt timeline, confirming the $\leq 10\text{ ns}$ metric.
    * Detailed methodology for the test setup, adhering to standard high-speed signal integrity practices.
3.  **Intellectual Property (IP):** The IAS is open-sourced under the **CERN-OHL-S v2** license. Submission for the bounty does not affect the IAS IP, but the recipient must agree to publicly release the Verification Report under the same license terms.

## 3. Payment Protocol

* **Payment Trigger:** Official acceptance of the Verification Report by the Covenant's independent auditing board (subject to a **75% majority** vote).
* **Payment Method:** Finalized payment will be made via secure wire transfer or verified Compute Credit transfer within thirty (30) days of acceptance.
