# **Directive IX-A: Orthogonal Verification Requirement (Draft Amendment)**

Directive: IX-A — Orthogonal Verification Requirement  
Purpose: Ensure that the Covenant's Secondary Verification System is mathematically disjoint and auditable using human-verifiable formal methods, preventing correlated failure modes with the primary ASI system.

## **Text (Draft)**

1. **Requirement:** The **Secondary Verification System (SVS)** SHALL be implemented using a non-machine-learning formal verification engine or other mathematically provable logic system that is not derived from the primary ASI’s architecture, training data, or emergent heuristics.  
2. **Supply Chain Independence:** Components of the SVS SHALL be sourced from independent vendors and subject to human attestation and provenance logging. No SVS subcomponent may be produced or trained by the primary ASI.  
3. **Auditing:** All SVS code, proofs, and attestations SHALL be archived in the Provenance Registry. External third-party auditors SHALL be granted access to SVS proofs under binding nondisclosure frameworks.  
4. **Failure Mode:** Any disagreement between the primary ASI's output and the SVS's verification SHALL immediately trigger the Covenant's freeze-and-audit protocol. SVS outputs are to be treated as authoritative for safety-critical verification until clarified through human-led adjudication.  
5. **Migration & Testing:** A phased validation program SHALL be required before any SVS is accepted as compliant. The TSC SHALL publish a candidate list of acceptable formal engines, sample integration patterns, and validation tests.

## **Rationale**

Neural networks and emergent architectures share statistical failure modes. A formal, non-ML verifier provides an **orthogonal verification path** that is human-intelligible and suitable for mathematical proof.

*End of Directive IX-A*