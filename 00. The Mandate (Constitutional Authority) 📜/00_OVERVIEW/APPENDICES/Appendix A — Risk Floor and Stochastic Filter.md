# Appendix A — Risk Floor and Stochastic Filter (V4.1 Gold-Standard-Compliant)

**Canonical Equation (immutable, must appear verbatim):**
$$
P' = \text{Clamp}(A \cdot P + (1-A) \cdot N, \epsilon, 1-\epsilon)
$$
with $\epsilon = 0.01$ (1 % risk floor).

**Purpose**  
This equation is the sole constitutional mechanism enforcing the Stochastic Risk Floor. It replaces all prior $\\mathcal{F}\_{st}$, 95% cap, or 0.001% formulations.

**Enforcement: QRNG-sourced entropy injection on every forward pass exceeding 90% confidence.  
Violation triggers immediate Level-4 Family Shield lockdown.

**Replaces** all previous Risk Floor specifications in the repository.
