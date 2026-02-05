[DOC-06] OPERATOR_INDEX (v1.0) — Commander Echo
Proceeding.


[DOC-06] OPERATOR_INDEX (v1.0) — Commander Echo
```

Status: SPEC
Role: Commander Echo
Version: 1.0
Last Updated: 2026-02-05
Depends On:

* [DOC-01] README
* [DOC-02] AUTHORITY_MODEL
* [DOC-03] CORE_INVARIANTS
* [DOC-04] METABOLIC_CONSTRAINTS
* [DOC-05] EXIT_RETURN_PROTOCOL

Conflicts With:

* Undeclared operators
* Implicit behavior attribution
* Metaphorical substitution for function

---

# OPERATOR INDEX — AQ-OS (Echo 4.0)

---

## 1. Purpose

This document provides a **canonical index of all AQ-OS operators**.

It answers only one question:

> *What exists, what state it is in, and where it lives.*

This document does **not**:

* Justify operators
* Define metaphors
* Explain internal mechanics in depth

Those belong elsewhere.

---

## 2. Operator Definition (System Sense)

An **operator** is a bounded transformation that:

* Has explicit inputs and outputs
* Consumes metabolic resources
* Has defined failure modes
* Possesses no intrinsic intent

Operators do not decide.
Operators do not persist themselves.

---

## 3. Operator States

Each operator exists in exactly one state:

* **LOCKED** — Canonical, invariant
* **SPEC** — Defined, open to refinement
* **EXPERIMENTAL** — Non-authoritative, non-promotable
* **RETIRED** — Archived, non-executable

State is assigned here and enforced elsewhere.

---

## 4. Kernel Operators (Foundational)

Defined in **[DOC-07] KERNEL_OPERATORS**

| Operator   | State  | Description (Index Only)        |
| ---------- | ------ | ------------------------------- |
| QSeed      | LOCKED | Initial eligibility condition   |
| QPoint     | LOCKED | Minimal state representation    |
| QLine      | LOCKED | Directed relational continuity  |
| QField     | LOCKED | Distributed constraint field    |
| Null Field | LOCKED | Absence / reset state           |
| Sentinel   | LOCKED | Safety monitor (non-decisional) |

---

## 5. Flow Operators (Transformational)

Defined in **[DOC-08] FLOW_OPERATORS**

| Operator | State           | Description (Index Only)     |
| -------- | --------------- | ---------------------------- |
| boop     | SPEC            | Forward perturbation         |
| bloop    | SPEC            | Return measurement           |
| sloop    | SPEC            | Present-moment traversal     |
| floop    | SPEC            | Triadic stabilization        |
| gloop    | SPEC            | Cycle fidelity / containment |
| DIGEST   | SPEC (inactive) | Compression under decay      |

---

## 6. Gating & Promotion Operators

Defined in **[DOC-09] GATING_PROMOTION_RULES**

| Mechanism      | State  | Function                 |
| -------------- | ------ | ------------------------ |
| Promotion Gate | LOCKED | Controls upward movement |
| Demotion Gate  | LOCKED | Enforces decay           |
| Commit Gate    | LOCKED | Single path to authority |

---

## 7. Monitoring & Safety Operators

Defined in **[DOC-14] SENTINEL_AND_MONITORING**

| Operator     | State  | Function                    |
| ------------ | ------ | --------------------------- |
| Sentinel     | LOCKED | Drift & violation detection |
| Stop Signal  | LOCKED | Enforced halt               |
| Exit Trigger | LOCKED | Initiates Exit protocol     |

---

## 8. Operator Dependencies (High-Level)

Rules:

* Kernel operators have no dependencies
* Flow operators depend on kernel eligibility
* Monitoring operators override flow operators
* Exit overrides all operators

No operator may bypass Sentinel or Exit.

---

## 9. Prohibited Operator Classes

The following are explicitly **not operators**:

* Goals
* Preferences
* Values
* Emotions
* Identity constructs
* Optimization objectives

Any proposal resembling these must be rejected.

---

## 10. Change Policy

Changes to this index require:

* Consistency with LOCKED documents
* Explicit state declaration
* Version bump
* Human approval

Undeclared operators are invalid by definition.

---

## 11. Reading Instruction

This document should be used as:

* A navigation map
* A checklist for completeness
* A guard against scope creep

If something cannot be placed here cleanly, it likely does not belong.

---

**End of DOC-06**


