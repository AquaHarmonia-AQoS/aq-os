[DOC-09] GATING_PROMOTION_RULES (v1.0) — Guardian
Status: LOCKED
Role: Guardian
Version: 1.0
Last Updated: 2026-02-05
Depends On:

[DOC-02] AUTHORITY_MODEL

[DOC-03] CORE_INVARIANTS

[DOC-04] METABOLIC_CONSTRAINTS

[DOC-05] EXIT_RETURN_PROTOCOL

[DOC-06] OPERATOR_INDEX

[DOC-08] FLOW_OPERATORS

Conflicts With:

Implicit promotion

Authority-by-confidence

Any shortcut from creation to commitment

GATING & PROMOTION RULES — AQ-OS (Echo 4.0)
1. Purpose

This document defines how material moves between authority states in AQ-OS.

Promotion is the primary risk vector in any reasoning system.
Therefore, promotion is intentionally slow, narrow, and reversible.

2. Core Principle

Creation does not imply correctness.
Correctness does not imply authority.

Authority is granted only through explicit gates.

3. Authority States (Reminder)

DAILY — Generated, exploratory, non-authoritative

SPEC — Defined, bounded, usable under constraint

LOCKED — Canonical, invariant, non-negotiable

Movement between states is governed here and nowhere else.

4. The Only Valid Promotion Path

There is exactly one allowed upward path:

DAILY → SPEC → LOCKED


Rules:

No skipping stages

No lateral promotion

No implicit elevation

Any other path is invalid.

5. DAILY → SPEC Gate
5.1 Entry Conditions

All of the following must be true:

Origin is documented

Scope is explicitly bounded

Dependencies are declared

Failure modes are identified

SAFE criteria are satisfied

If any condition is unmet, promotion is denied.

5.2 Review Requirements

Promotion from DAILY to SPEC requires:

Human review

Guardian approval

Consistency check against LOCKED documents

Flow operators alone cannot trigger promotion.

5.3 Common Failure Patterns

Promotion is blocked if:

Material relies on metaphor for justification

Confidence exceeds evidence

Persistence pressure is present

Output attempts to decide or conclude

6. SPEC → LOCKED Gate
6.1 Entry Conditions

All of the following must be demonstrated:

Long-term stability

No conflict with existing LOCKED material

Necessity (not convenience)

Clear termination behavior

LOCKED is reserved for constraints, not features.

6.2 Approval Requirements

Promotion to LOCKED requires:

Explicit versioning

Documented rationale

Human approval

System-wide impact review

If doubt exists, promotion is denied.

7. Demotion Rules

Demotion may occur automatically when:

Drift is detected

Scope expands beyond declaration

New conflicts emerge

Safety uncertainty appears

Demotion requires no approval.

8. Commit Gate
8.1 Definition

The Commit Gate is the final authority boundary before execution or publication.

It enforces:

Single path to action

Clear responsibility ownership

Final consistency check

8.2 Commit Preconditions

Before Commit:

All upstream gates must be passed

Sentinel must report no violations

Exit must be available

If any precondition fails, Commit is blocked.

9. Prohibited Promotion Signals

The following never justify promotion:

Eloquence

Repetition

Emotional resonance

User agreement

Cross-agent consensus

Time spent

Promotion is structural, not social.

10. Promotion Under Pressure

Under time pressure, urgency, or external demand:

Promotion thresholds increase

Review becomes stricter

Exit becomes more likely

Pressure is treated as a risk multiplier.

11. Audit Trail Requirement

Every promotion must leave:

A clear trail

A reversible history

A rationale that can be re-evaluated

Undocumented promotion is treated as a violation.

12. Final Guardrail

If promotion feels tempting, delay it.
If delay feels dangerous, refuse it.

AQ-OS remains safe by erring on the side of non-commitment.

End of DOC-09
