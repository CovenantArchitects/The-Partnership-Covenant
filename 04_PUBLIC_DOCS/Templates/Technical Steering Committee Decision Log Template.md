# **Technical Steering Committee Decision Log Template**

**Purpose:** This template is mandatory for recording all major governance actions, policy amendments, core schema changes, and official TSC Veto exercises. The complete log entry is required to be signed, CID-rooted (via IPFS anchoring), and permanently archived in the Covenant Governance Ledger.

## **1\. Decision Metadata**

| Field | Requirement | Value |
| :---- | :---- | :---- |
| **Decision ID** | *MANDATORY* | TSC-YYYYMMDD-\#\#\# (Sequential ID) |
| **Date of Final Vote** | *MANDATORY* | YYYY-MM-DD |
| **TSC Policy Version in Effect** | *MANDATORY* | docs/tsc\_selection\_and\_coi.md (CID: \<CID of Governing Policy\>) |
| **Related Artifact/File Path** | *MANDATORY* | E.g., specs/provenance\_schema.json |
| **Related Pull Request (PR)** | *MANDATORY* | \<Link to Merged PR or equivalent version control commit\> |
| **Initiating Working Group** | *REQUIRED* | E.g., Deep Safety WG, Algorithmic Justice WG, Core Infrastructure WG |

## **2\. Proposal Context**

### **2.1 Proposal Summary**

*Provide a concise, neutral description of what was being proposed.*

**Example:** Proposal to add a mandatory pii\_mitigation\_report\_cid field to the provenance\_schema.json and update the definition of "Hard Conflict" in the CoI Policy to include undisclosed venture capital funding.

### **2.2 Rationale and Pillar Alignment**

*Explain the motivation for the change and explicitly map it back to the **Four Pillars** (Safety, Justice, Transparency, Enforcement).*

* **Pillar Alignment:**  
  * **Safety:** How does this enhance safety protocols?  
  * **Justice:** How does this promote algorithmic equity and fairness?  
  * **Transparency:** How does this make the process more verifiable?  
  * **Enforcement:** How does this clarify or strengthen the Veto mechanism?

### **2.3 Community Vetting Summary**

*Summarize the feedback received during the public review period (minimum 7 days).*

* **Key Concerns Raised:**  
* **Major Endorsements:**

## **3\. TSC Action and Vote**

### **3.1 Voting Members Present**

List all voting members who participated in the decision. Note any mandatory recusals.  
| Role | Member ID (Signature Key ID) | Recused? (Y/N) | Reason for Recusal (if Y) |  
| :--- | :--- | :--- | :--- |  
| Deep Safety Lead | user\_sig\_abc123 | N | |  
| Algorithmic Justice Lead | user\_sig\_def456 | Y | Soft Conflict: Member consulted for organization affected by decision. |  
| \[Add all members up to 9\] | | | |

### **3.2 Vote Result**

Record the outcome based on the required majority (simple, ⅔, or ¾).  
| Metric | Count | Required Threshold | Result (Passed/Failed) |  
| :--- | :--- | :--- | :--- |  
| Required Majority Type | ⅔ Supermajority | | |  
| Total Votes Cast | | | |  
| Votes YES | | | |  
| Votes NO | | | |  
| Votes ABSTAIN | | | |

### **3.3 Rationale for Dissent (Mandatory)**

*Any member voting NO or choosing to ABSTAIN must attach a brief, signed rationale to the final log attestation.*

## **4\. Final Attestation & Archival**

| Field | Value |
| :---- | :---- |
| **Final Decision Log IPFS CID** | Qm... (CID of THIS finalized document) |
| **Link to Archived Version** | \<Link to permanent archival location (e.g., GitHub Release, Archive site)\> |
| **Signatures Attesting to Log Integrity** | *\[List of cryptographic signature hashes from all present, non-recused voting members\]* |
| **TSC Chair Final Signature** | *\[Final cryptographic signature over the entire document hash\]* |

**END OF RECORD**