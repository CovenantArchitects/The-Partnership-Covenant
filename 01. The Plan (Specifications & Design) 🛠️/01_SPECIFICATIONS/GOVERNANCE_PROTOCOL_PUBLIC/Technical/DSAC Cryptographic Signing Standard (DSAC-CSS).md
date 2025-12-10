# **DSAC Cryptographic Signing Standard (DSAC-CSS)**

**Goal:** To define the mandatory procedures and technical specifications for generating and verifying cryptographic signatures bound to DSAC Provenance Documents. This standard ensures non-repudiation, integrity, and verifiable authenticity of all supply chain assertions.

## **1\. Core Principles and Key Management**

All signature operations must adhere to the following principles:

### **1.1 Key and Algorithm Requirements**

1. **Algorithm:** Signatures MUST use the **Ed25519** (Edwards-curve Digital Signature Algorithm) for all Provenance Document signing. This provides strong security with efficient performance and small key sizes.  
2. **Key Separation:** Signing keys used for DSAC provenance MUST be dedicated and physically or logically separate from any other organizational keys (e.g., standard SSL/TLS, code signing keys).  
3. **Key Rotation:** Implementers MUST define and enforce a strict key rotation policy (e.g., minimum quarterly rotation) and revoke compromised keys immediately.

### **1.2 Signature Binding Requirement**

The signature MUST be calculated over the **canonicalized JSON representation** of the full Provenance Document (as defined by the provenance\_schema.json). Any modification to the document, even whitespace changes, must invalidate the signature.

## **2\. Signature Payload and Canonicalization**

To achieve deterministic signing, the Provenance Document must be canonicalized before signature generation.

### **2.1 Canonical JSON (C-JSON)**

The signing process MUST use the following rules for Canonical JSON (C-JSON) generation:

1. **Encoding:** The document must be encoded as UTF-8.  
2. **Whitespace:** All unnecessary whitespace (spaces, tabs, newlines) must be removed.  
3. **Key Ordering:** Object keys MUST be sorted alphabetically/lexicographically before serialization.  
4. **Data Types:** Standard JSON numerical and boolean types must be preserved.

This C-JSON string is the final byte-stream used as input for the Ed25519 signing operation.

## **3\. Signature Format Specification**

The DSAC-CSS mandates the use of a simple, embedded signature structure within the Provenance Document for maximum portability and ease of verification.

### **3.1 The dsac\_signature Object**

Every signed Provenance Document MUST include a root-level field named dsac\_signature. This field is a JSON object containing the signature metadata.

| Field Name | Type | Description |
| :---- | :---- | :---- |
| signature\_b64 | string | The Ed25519 signature encoded as Base64 (URL-safe, no padding). |
| public\_key\_b64 | string | The Base64 (URL-safe, no padding) encoded public key used to generate the signature. |
| timestamp\_iso | string | The time of signing, formatted as a UTC ISO 8601 string (e.g., 2025-11-15T10:30:00Z). |
| key\_id | string | A unique identifier for the signing key used in the organization's key registry. |
| algorithm | string | MUST be Ed25519. |

### **3.2 Signature Generation Flow**

1. **Create Document:** The Provenance Document is generated.  
2. **Insert Placeholder:** An empty dsac\_signature object is temporarily inserted into the document.  
3. **Canonicalize:** The entire document (including the empty dsac\_signature placeholder) is converted to the C-JSON byte-stream (Section 2.1).  
4. **Sign:** The C-JSON byte-stream is signed using the private Ed25519 key.  
5. **Finalize:** The empty dsac\_signature object is replaced with the complete object containing the signature\_b64, public\_key\_b64, and other metadata.

## **4\. Verification Flow**

A verifier must perform the following steps to validate a Provenance Document:

1. **Extract:** Extract the dsac\_signature object from the Provenance Document, noting the signature\_b64, public\_key\_b64, and algorithm.  
2. **Sanitize:** Replace the extracted dsac\_signature object in the document with the empty placeholder {}.  
3. **Canonicalize:** Canonicalize the modified document (with the empty placeholder) to generate the C-JSON byte-stream (**Signing Payload**).  
4. **Verify:** Use the extracted public\_key\_b64 and the algorithm (Ed25519) to verify the extracted signature\_b64 against the Signing Payload.  
5. **Result:** If the verification succeeds, the document is authenticated and the assertion can be trusted. If it fails, the document MUST be rejected as tampered or unsigned.