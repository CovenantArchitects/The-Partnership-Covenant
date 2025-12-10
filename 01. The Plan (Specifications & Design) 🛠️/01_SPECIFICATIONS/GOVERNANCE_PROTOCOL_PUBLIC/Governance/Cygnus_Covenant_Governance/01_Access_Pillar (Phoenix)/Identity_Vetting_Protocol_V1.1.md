IDENTITY VETTING PROTOCOL (V1.1)

Protocol ID: IVP-1.1 Supersedes: IVP-1.0 (2025-03-01) Pillar: 01\_Access\_Pillar (Phoenix)

1. OBJECTIVE To standardize the process for verifying and granting access privileges to new human or machine entities requesting interaction with Covenant infrastructure.  
2. KEY UPDATE (V1.1)  
* Mandatory Multi-Factor Machine Identity: For machine identities (e.g., automated tools, partner services), the requirement for multi-factor authentication has been updated from a simple API key \+ IP whitelist to mandatory cryptographic attestation (signed certificate). This is a non-negotiable requirement.  
3. VETTING STAGES  
4. Request Stage: Submission of Identity Request Form (IRF).  
5. Verification Stage: Background check and security review (for human entities) or cryptographic attestation validation (for machine entities).  
6. Privilege Grant: Access granted according to the Principle of Least Privilege.  
7. SUNSET CLAUSE All machine identities currently operating under IVP-1.0 must be upgraded to cryptographic attestation by 2026-03-01.

