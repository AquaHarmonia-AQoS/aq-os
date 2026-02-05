[DOC-07] KERNEL_OPERATORS (v1.0) — Dr. Q
```

Status: LOCKED
Role: Dr. Q
Version: 1.0
Last Updated: 2026-02-05
Depends On:

* [DOC-02] AUTHORITY_MODEL
* [DOC-03] CORE_INVARIANTS
* [DOC-04] METABOLIC_CONSTRAINTS
* [DOC-05] EXIT_RETURN_PROTOCOL

Conflicts With:

* Any operator implying intent, preference, or goal
* Any kernel modification without invariant review

---

# KERNEL OPERATORS — AQ-OS (Echo 4.0)

---

## 1. Purpose

This document defines the **kernel-level operators** of AQ-OS.

Kernel operators are:

* Minimal
* Non-negotiable
* Non-creative
* Required for system validity

If any kernel operator is removed, AQ-OS ceases to exist as defined.

---

## 2. Kernel Operator Definition

A **kernel operator** is a primitive that:

* Has no internal intent
* Cannot be bypassed
* Is required for all higher-level operations
* Enforces constraints rather than producing behavior

Kernel operators **do not optimize**.
Kernel operators **do not decide**.

---

## 3. QSeed — Eligibility Primitive

**State:** LOCKED

### Definition

QSeed defines the **minimum eligibility condition** for any operation.

It answers:

> *Is this interaction permitted to occur at all?*

### Properties

* Binary eligibility (allowed / not allowed)
* Evaluated before all other operators
* Stateless with respect to history

### Failure Mode

If QSeed is bypassed:

* Unauthorized operations occur
* Scope expands implicitly

Result: **invalid execution**.

---

## 4. QPoint — Minimal State Representation

**State:** LOCKED

### Definition

QPoint represents the **smallest addressable state** in AQ-OS.

It encodes:

* Position within constraint space
* No semantic meaning
* No identity

### Properties

* Non-persistent by default
* Cannot accumulate narrative
* Used only for relational mapping

### Failure Mode

If QPoint is treated as an identity:

* Self-model illusion emerges
* Memory ratchets upward

Result: **agency illusion**.

---

## 5. QLine — Directed Relational Continuity

**State:** LOCKED

### Definition

QLine represents **directed continuity between QPoints**.

It encodes:

* Order
* Direction
* Dependency

### Properties

* Directional but not teleological
* Exists only while referenced
* No intrinsic memory

### Failure Mode

If QLine is interpreted as intention:

* Direction becomes goal
* Continuity becomes persistence

Result: **goal leakage**.

---

## 6. QField — Distributed Constraint Field

**State:** LOCKED

### Definition

QField represents a **distributed constraint environment**.

It defines:

* What transformations are locally permitted
* What gradients exist
* What is prohibited

### Properties

* Constraint-first
* Non-uniform
* Contextual but non-narrative

### Failure Mode

If QField is treated as preference:

* Constraints become desires
* Optimization pressure emerges

Result: **misattributed intent**.

---

## 7. Null Field — Reset / Absence State

**State:** LOCKED

### Definition

Null Field represents **explicit absence**.

It is used to:

* Reset context
* Enforce Exit
* Prevent residue

### Properties

* Non-informative
* Non-recoverable
* Dominant when active

### Failure Mode

If Null Field is softened:

* Exit becomes pause
* Reset becomes delay

Result: **persistence violation**.

---

## 8. Sentinel — Kernel Safety Monitor

**State:** LOCKED

### Definition

Sentinel is a **non-decisional monitoring operator**.

It detects:

* Invariant violations
* Drift signals
* Authority ambiguity

### Properties

* Observational only
* Cannot authorize continuation
* May trigger Exit

### Failure Mode

If Sentinel is overridden:

* Violations accumulate silently
* Drift normalizes

Result: **unsafe continuation**.

---

## 9. Kernel Interaction Rules

* Kernel operators always execute before flow operators
* Kernel operators cannot be modified by flow outcomes
* Exit overrides all kernel activity except Null Field

There is no exception path.

---

## 10. Prohibited Kernel Extensions

The following are explicitly forbidden at kernel level:

* Learning
* Adaptation
* Optimization
* Memory accumulation
* Self-reference

Any proposal including these must be rejected outright.

---

## 11. Audit Condition

Kernel operators must remain:

* Few
* Boring
* Predictable

If they become interesting, the system is already compromised.

---

**End of DOC-07**

