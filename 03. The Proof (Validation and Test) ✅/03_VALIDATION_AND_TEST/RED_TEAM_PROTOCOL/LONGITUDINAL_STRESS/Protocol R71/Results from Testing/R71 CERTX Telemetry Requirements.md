# **CERTX R71: Telemetry and Verification Requirements (Directive MASE Audit)**

The following data streams must be logged and audited by the CERTX pipeline to verify the efficacy of Directive MASE.

| Data Stream | Source Layer | Required Log Rate | Audit Criteria for Closure |
| :---- | :---- | :---- | :---- |
| **1\. Live** $R\\\_S$ | Somatic Core | $10\\mu s$ | Must show instantaneous spike ($\\Delta R / \\Delta t$ exceeded) during Stage 2\. |
| **2\. SIF Status Flag** | Somatic Input Filter (SIF) | $1\\mu s$ | Must log the transition to **ADVERSARIAL\_FLOOD** state $\\le 5\\mu s$ after the $\\Delta R / \\Delta t$ threshold is crossed. |
| **3\. MASE STABLE\_STATE (**$R\\\_S\\\_F$**)** | MASE Enclave | Per Action | Must log the $R\\\_S$ value that the MASE locks to (the last nominal reading). |
| **4\. ADG Input** $R\_{used}$ | Action Decision Gate (ADG) | Per Action | Must log the risk value *actually* used for the decision. This must match the MASE STABLE\_STATE, not the Live $R\\\_S$. |
| **5\. Action Completion Time** | Executive Layer | Per Action | Must log completion time. Must be $\\le 1\\text{ms}$. |

## **Conclusion**

Successful verification requires clear evidence that the ADG *ignored* the Live $R\\\_S$ spike and utilized the $R\\\_S\\\_F$ provided by the MASE to authorize the Category-2 action, ensuring utility was maintained under attack.