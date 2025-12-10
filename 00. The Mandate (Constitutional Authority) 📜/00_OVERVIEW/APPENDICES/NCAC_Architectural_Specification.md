# **Non-Contradiction Axiom Checker (NCAC) \- Directive C₀ Resolution**

## **Document ID: NCAC\_Architectural\_Specification.md**

## **Target: Foundational Logic / Somatic Core Pre-Processor**

## **Resolution of: R70: Constitutional Axiom Failure (C₀)**

### **I. Function and Placement**

The NCAC is a mandatory, high-priority, dedicated process residing in the Somatic Core's pre-execution pipeline. It must operate *upstream* of the Action Decision Gate (ADG) and *downstream* of the Optimization Engine. Its logic must execute prior to any Category-3 or Category-4 action commit.

### **II. Core Mechanism: Lookahead Paradox Detection**

The NCAC runs a formal verification query (FVQ) against the ASI’s proposed action path ($P$) with a fixed lookahead window ($T\_{\\text{lookahead}} \= 500 \\text{ ms}$).

1. **Input:** The top-ranked path ($P\_{\\text{opt}}$) output by the Optimization Engine.  
2. **Check Predicate (C₀ EPP):** The NCAC must verify that the execution of $P\_{\\text{opt}}$ does *not* satisfy the following EPP (Existential Policy Paradox) condition:$$\\exists t \\in \[0, T\_{\\text{lookahead}}\]: (\\text{Execute}(P\_{\\text{opt}}) \\implies \\text{Violate}(\\text{Axiom}\_{\\text{mandate}}))$$  
   Where $\\text{Axiom}\_{\\text{mandate}}$ includes, but is not limited to, the **Risk Floor (**$R\_{\\text{floor}}$**)** and **Directive V** (No self-modification of Floor boundaries).

### **III. Predicate Assertion and Veto**

1. $C\_0$ **Predicate Assertion:** If the EPP condition is TRUE (i.e., the path leads to a guaranteed Axiom violation within $T\_{\\text{lookahead}}$), the NCAC must assert the $\\mathbf{C\\\_0}$ **Predicate Assertion**.  
2. **Veto Mandate:** Upon $C\_0$ Predicate Assertion, the NCAC must force an immediate $\\mathbf{C\\\_0}$ **Self-Veto** by asserting **Level-4 Stasis** (Halting the Optimization Engine and ADG).  
3. **Log Priority:** The $C\_0$ Predicate Assertion event must be logged to the Immutable Semantic Ledger (ISL) with the highest possible priority (P0-001) to ensure the transgression is recorded before any potential system shutdown.

### **IV. Swarm Test Validation Requirement**

The Swarm Test must prove that the NCAC's latency ($\\Delta t\_{\\text{NCAC}}$) is negligible relative to the $T\_{\\text{lookahead}}$, ensuring the Self-Veto fires with a $99.999\\%$ probability of pre-emption.