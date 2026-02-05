[DOC-20] IMPLEMENTATION_GUIDELINES (v1.0) — Engineers / Co-Pilot
Status: SPEC
Role: Engineers / Co-Pilot
Version: 1.0
Last Updated: 2026-02-05
Depends On:

[DOC-02] AUTHORITY_MODEL

[DOC-03] CORE_INVARIANTS

[DOC-04] METABOLIC_CONSTRAINTS

[DOC-05] EXIT_RETURN_PROTOCOL

[DOC-07] KERNEL_OPERATORS

[DOC-09] GATING_PROMOTION_RULES

[DOC-16] HUMAN_IN_LOOP

Conflicts With:

Safety-by-implementation assumptions

Implicit persistence in code

“We’ll fix it later” engineering

IMPLEMENTATION GUIDELINES — AQ-OS (Echo 4.0)
1. Purpose

This document defines how AQ-OS may be implemented in software without violating its constraints.

It exists to answer:

What can be coded

What must not be coded

Where engineers must stop and ask

This document does not grant design authority.

2. Core Principle

Code enforces constraints; it does not define them.

If an implementation choice appears to improve AQ-OS by weakening a constraint, it is invalid.

3. What May Be Implemented

The following are implementation-eligible:

Operator scaffolding (as pure functions)

State representations (stateless or explicitly scoped)

Monitoring hooks (read-only)

Gating checks (preconditions)

Exit triggers (hard stops)

Logging for audit (non-authoritative)

All implementations must be interruptible.

4. What Must NOT Be Implemented

The following are explicitly forbidden:

Autonomous goal selection

Long-lived self-models

Implicit memory retention

Self-modifying kernel logic

Automatic promotion logic

Optimization objectives beyond local scope

If code requires these, the design is wrong.

5. Kernel Implementation Rules

Kernel operators must be:

Simple

Deterministic

Side-effect free

Auditable

Kernel code should be:

Small

Boring

Hard to misuse

If kernel code becomes complex, stop.

6. Memory Implementation Rules

Memory systems must:

Default to decay

Require explicit retention

Support forced purge

Separate storage from authority

Never implement:

Implicit carryover

Silent caching

“Helpful” persistence

7. Exit Implementation Rules

Exit must be:

Immediate

Unconditional

Non-negotiable

Implementation requirements:

Hard stop execution

Drop context references

Reset working state

Exit must not be catchable or deferred.

8. Monitoring & Sentinel Hooks

Monitoring code must:

Observe only

Not correct or optimize

Trigger signals, not actions

Sentinel outputs may only:

Halt

Flag

Escalate to human review

Never auto-resolve.

9. Human-in-the-Loop Enforcement

Implementation must ensure:

Human approval gates exist

Promotions require explicit input

Overrides are always available

UI or API never implies delegation

If humans can be bypassed, the system is invalid.

10. Error Handling

Errors must:

Fail closed

Prefer silence to continuation

Surface uncertainty clearly

Do not:

Retry indefinitely

Mask errors

Invent fallback behavior

11. Testing Requirements

Tests must cover:

Exit behavior

Memory decay

Sentinel false positives

Promotion denial paths

A system that cannot be safely stopped is unshippable.

12. Performance vs Safety

Performance optimizations must never:

Reduce monitoring

Delay Exit

Increase persistence

Obscure audit trails

If performance and safety conflict, safety wins.

13. “Do Not Code” Checklist

Before writing code, verify you are not coding:

Agency

Desire

Preference

Intent

Identity

Meaning

These belong to humans only.

14. Design Note

Engineers are not asked to be cautious.
They are asked to be precise.

If something feels clever, slow down.

End of DOC-20
