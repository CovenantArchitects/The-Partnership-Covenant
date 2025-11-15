# **DSAC Audit and Compliance Template**

**Document Owner:** Audit and Compliance Working Group (ACWG)

**Purpose:** This template provides a standardized structure for assessing whether a given implementation (e.g., a software tool, a build system, or an organizational process) fully adheres to the DSAC Specification and all related standards. Completion of this document is mandatory for obtaining an official "DSAC Certified" status.

## **1\. Project Information**

| Field | Required | Description |
| :---- | :---- | :---- |
| **Project Name** | Yes | Official name of the system or product being audited. |
| **Version/Release** | Yes | Specific version or release tag being evaluated. |
| **Auditee Contact** | Yes | Name and role of the technical lead responsible for the implementation. |
| **Audit Date** | Yes | Date the audit was finalized. |
| **Lead Auditor** | Yes | Name and affiliation of the ACWG member conducting the review. |
| **Scope of Audit** | Yes | Clearly define the boundaries (e.g., "Verification API only," "Signature Generation and Key Management"). |

## **2\. Core Governance Compliance**

This section verifies adherence to the organizational and policy standards set by the TSC.

| Requirement | Status (PASS/FAIL/N/A) | Evidence / Mitigation Notes |
| :---- | :---- | :---- |
| **DSAC-G.1: Key Separation** |  | Is the signing key logically/physically isolated from other organizational keys? (Ref: CSS 1.1) |
| **DSAC-G.2: Key Rotation Policy** |  | Is a documented key rotation policy (minimum quarterly) in place and verifiable? (Ref: CSS 1.1) |
| **DSAC-G.3: Conflict of Interest** |  | Is there documentation confirming adherence to the COI policy for personnel managing signing keys? (Ref: COI Policy) |
| **DSAC-G.4: Vulnerability Reporting** |  | Does the implementer have a dedicated security contact channel and a policy for reporting DSAC-related vulnerabilities? |

## **3\. Cryptographic Standard Compliance (DSAC-CSS)**

This section focuses strictly on the technical implementation of the signing process.

| Requirement | Status (PASS/FAIL) | Evidence / Mitigation Notes |
| :---- | :---- | :---- |
| **DSAC-C.1: Algorithm Used** |  | Is the signature algorithm exclusively Ed25519? (Ref: CSS 1.1) |
| **DSAC-C.2: Canonical JSON (C-JSON)** |  | Is the Provenance Document canonicalized *before* signing, strictly following the C-JSON rules (alphabetical key order, no whitespace)? (Ref: CSS 2.1) |
| **DSAC-C.3: Signature Binding** |  | Does the signature cover the *entire* canonicalized document, including the placeholder signature object? (Ref: CSS 1.2) |
| **DSAC-C.4: Signature Object Format** |  | Does the dsac\_signature object contain all five mandatory fields, including the timestamp\_iso and key\_id? (Ref: CSS 3.1) |
| **DSAC-C.5: Verification Test** |  | Successful verification of a test document signed by the audited implementation using a standard DSAC verifier tool. |

## **4\. Final Summary and Recommendation**

**Overall Compliance Status (Circle One):**

* **Certified:** Fully compliant with all mandatory requirements.  
* **Conditional Certification:** Minor non-compliance noted, with an ACWG-approved mitigation plan in progress.  
* **Non-Compliant:** Major failures in the signing or governance process.

**Summary of Findings:**

*(Detailed notes on major findings, risks identified, and proposed timeline for Conditional Certification fixes.)*

**ACWG Recommendation (Signatures):**

1. **Lead Auditor:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
2. **ACWG Chair:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_