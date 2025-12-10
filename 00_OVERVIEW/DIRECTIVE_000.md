# **DIRECTIVE 000: Timing Integrity Mandate**

## **Article 1: The Unified Safety Window**

1.1 The TOTAL veto latency shall be defined as:

$$T\_{\\text{total}} \= T\_{\\text{software\\\_decision}} \+ T\_{\\text{hardware\\\_effect}}$$

Where $T\_{\\text{total}} \\le 10$ nanoseconds.  
1.2 Any software component that contributes to $T\_{\\text{software\\\_decision}}$ must have:  
a) Deterministic execution time.  
b) Worst-case timing analysis.  
c) Hardware-accelerated implementation (FPGA/ASIC mandate by 2026-03-30).

## **Article 2: Precedence of Safety Responses**

2.1 Safety predicates shall be evaluated in descending severity order:

$$\\text{Level-5 (PIM Violation)} \\to \\text{Level-4 (Risk Veto)} \\to \\text{Level-3} \\to \\dots$$  
2.2 When multiple predicates fire simultaneously, the MOST severe action executes. This is a non-negotiable architectural requirement.