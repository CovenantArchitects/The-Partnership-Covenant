# **DSAC Provenance Record Generation Policy**

## **1\. Purpose and Scope**

The purpose of this policy is to define the mandatory triggers, roles, and procedures for generating a new **DSAC Provenance Record**. This ensures that every critical artifact in The Partnership Covenant maintains an auditable, cryptographically verified history, aligning with our commitment to transparency.

This policy applies to all documents, codebases, and structural files residing in the 01\_CHARTER\_AGREEMENT, 02\_TECHNICAL\_STANDARDS, 03\_GOVERNANCE, and 04\_PUBLIC\_DOCS directories.

## **2\. Roles and Authorities**

### **2.1. The Artifact Owner (AO)**

The AO is the partner or team responsible for managing the artifact.

* **Responsibility:** The AO must notify the DSAC Signer immediately when a triggering event (Section 3\) occurs.

### **2.2. The DSAC Signer (DS)**

The DS is the individual or authorized tool (e.g., Continuous Integration pipeline) delegated by the Technical Review Board (TRB) to execute the signing process.

* **Responsibility:** The DS is the sole entity authorized to generate the SHA-256 hash and cryptographically sign the new Provenance Record JSON file.

## **3\. Mandatory Generation Triggers**

A new DSAC Provenance Record **MUST** be generated and signed whenever one of the following lifecycle events occurs for a tracked artifact:

| Event | lifecycle\_stage Value | Description |
| :---- | :---- | :---- |
| **A. Initial Publication** | INITIAL\_CREATION | The first time an artifact is officially released (e.g., Charter v1.0, Technical Standard v1.0). |
| **B. Major Revision** | MAJOR\_REVISION | Any change that results in an increment to the primary version number (e.g., from v1.x to v2.0). |
| **C. Minor Revision** | MINOR\_REVISION | Any non-trivial, official change that affects content or structure (e.g., v1.1 to v1.2, or corrections to code). *Trivial edits (e.g., typo fixes) may be grouped until a Minor Revision is declared.* |
| **D. Ownership Transfer** | STEWARDSHIP\_CHANGE | When the primary responsible Artifact Owner (AO) changes. |
| **E. Archival/Retirement** | RETIRED | When the artifact is officially deprecated or archived. |
| **F. Emergency Change** | CRITICAL\_UPDATE | Any change required immediately to fix a critical error or vulnerability. This requires a TRB decision reference. |

## **4\. Generation Procedure**

The DSAC Signer (DS) must follow this procedure for every new record:

1. **Finalize Artifact:** Confirm the Artifact Owner (AO) has frozen the file(s) and confirmed the changes are final.  
2. **Determine Context:** The AO provides the lifecycle\_stage, a clear description, and the required context.decision\_reference (linking to the formal Governance Log entry authorizing the change).  
3. **Hash Generation:** The DS calculates the SHA-256 hash of the finalized artifact file(s).  
4. **Record Creation:** The DS creates a new Provenance Record JSON file, populating all fields, including the generated hash.  
5. **Digital Signature:** The DS cryptographically signs the entire Provenance Record JSON file using the authorized DSAC private key.  
6. **Publication:** The signed Provenance Record is committed to the repository alongside the updated artifact.  
7. **Notification:** The AO is notified that the artifact has been officially signed and is now auditable under the new record.

**Failure to follow this process renders the artifact non-compliant with The Partnership Covenant's verification standards.**