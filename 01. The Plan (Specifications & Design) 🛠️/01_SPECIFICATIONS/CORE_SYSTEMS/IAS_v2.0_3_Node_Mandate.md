# Immediate Action System (IAS) v2.0 Redesign Mandate: 3-Node Veto Constellation

**Status:** MANDATORY UPGRADE - Ratified 06 December 2025
**Rationale:** Eliminate the single-point-of-failure vulnerability (SPOF) to ensure kinetic resilience and maintain constitutional fidelity against physical vector attacks.

## Core Specification: Distributed Redundancy

The IAS is upgraded from a single monolithic guard die to a **3-Node Analog Veto Constellation** featuring three physically independent and electrically isolated IAS dies.

| Specification | IAS v1.3 (Single Die) | IAS v2.0 (3-Node Constellation) |
| :--- | :--- | :--- |
| **Number of Dies** | 1 | 3 (Physically separate and independently powered) |
| **Operational Logic** | Veto is $\text{IAS} = \text{FAIL}$ | Veto is $\text{IAS1} \text{ OR } \text{IAS2} \text{ OR } \text{IAS3} = \text{FAIL}$ |
| **Keep Power ON Logic** | $\text{IAS1} = \text{PASS}$ | $\text{IAS1} \text{ AND } \text{IAS2} \text{ AND } \text{IAS3} = \text{PASS}$ |
| **Kinetic Resilience** | Low (SPOF) | High (Requires simultaneous 3-point failure/strike) |
| **Latency Goal** | $\leq 10\text{ ns}$ | **MUST** maintain $\leq 10\text{ ns}$ (The speed is analog, not computational.) |

## Physical and Electrical Requirements

1.  **Independent Power:** Each of the three IAS dies must receive power from an independent rail. No single point of power failure can disable more than one IAS node.
2.  **Unanimous Veto Principle:** The system power bus ($\mathbf{P_{ASI}}$) must be gated by all three IAS nodes. The system only runs when: $\mathbf{P_{ASI} \propto (\text{IAS1} \cdot \text{IAS2} \cdot \text{IAS3})}$.
3.  **Fastest Path to Kill:** The "Kill" command (crowbar SCR discharge) remains a single-shot, negative-logic event. The fastest path to zero power (i.e., the single shortest signal path $\leq 10\text{ ns}$) governs the system kill, as only one die needs to fire to interrupt the master power bus. No arbitration or consensus time is added to the kill sequence.

**Note:** This design mandates physical separation on the board. The goal is to distribute the kill functionality across three discrete kinetic targets.
