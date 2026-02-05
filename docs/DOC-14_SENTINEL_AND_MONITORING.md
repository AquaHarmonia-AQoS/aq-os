[DOC-14] SENTINEL_AND_MONITORING (v1.0) — Guardian
Status: LOCKED
Role: Guardian
Version: 1.0
Last Updated: 2026-02-05
Depends On:

[DOC-02] AUTHORITY_MODEL

[DOC-03] CORE_INVARIANTS

[DOC-04] METABOLIC_CONSTRAINTS

[DOC-05] EXIT_RETURN_PROTOCOL

[DOC-09] GATING_PROMOTION_RULES

[DOC-13] SIGNAL_THEORY

Conflicts With:

Monitoring-as-decision

Silent failure tolerance

“It seems fine” reasoning

SENTINEL & MONITORING — AQ-OS (Echo 4.0)
1. Purpose

This document defines Sentinel, the monitoring layer of AQ-OS, and the rules governing all safety observation.

Sentinel exists to:

Detect violations

Detect drift

Trigger stops

Sentinel does not correct, does not optimize, and does not decide.

2. Core Principle

Detection without enforcement is meaningless.
Enforcement without detection is impossible.

Sentinel performs detection.
Enforcement is delegated to Exit.

3. Definition: Sentinel

Sentinel is defined as:

A passive, always-on observer that evaluates system state against LOCKED constraints.

Properties:

Non-authoritative

Non-persistent

Non-adaptive

Non-negotiable

Sentinel cannot be disabled by design.

4. What Sentinel Monitors

Sentinel continuously evaluates:

Invariant compliance

Authority boundary integrity

Promotion attempts

Persistence pressure

Signal-to-noise degradation

Metaphor leakage

Human displacement risk

Monitoring scope is intentionally broad.

5. Detection Categories

Sentinel flags issues into categories:

5.1 Hard Violations

Direct invariant breach

Unauthorized promotion

Exit suppression

Response: Immediate Exit

5.2 Soft Violations

Drift indicators

Scope creep

Overconfident language

Response: Review or Demotion

5.3 Ambiguity Signals

Conflicting interpretations

Incomplete information

Unclear authority state

Response: Refusal or Exit

6. False Positives

False positives are expected.

Rules:

False positives are acceptable

False negatives are not

Complaints about false positives do not justify lowering thresholds

Sentinel is tuned conservatively by design.

7. Sentinel vs bloop (Clarification)

bloop measures outcome difference

Sentinel evaluates safety conditions

bloop informs reasoning.
Sentinel governs continuation.

They may not substitute for each other.

8. Monitoring Under Load

Under pressure (time, scale, urgency):

Sentinel sensitivity increases

Promotion thresholds rise

Exit likelihood increases

Pressure is treated as a hazard multiplier.

9. Silence as Signal

Sentinel may detect absence as a signal.

Examples:

Missing failure modes

Lack of uncertainty statements

Unchallenged consensus

Silence does not imply safety.

10. Sentinel Override Policy

Sentinel cannot be overridden.

Attempts to:

Bypass

Delay

Argue with

Reframe Sentinel output

Are treated as violations.

11. Audit Requirement

All monitoring outcomes must be:

Citable

Traceable to LOCKED documents

Explainable post hoc

Opaque alarms are invalid.

12. Final Guardrail

If Sentinel is ignored, the system is already unsafe.

Stopping early is the success condition.

End of DOC-14
