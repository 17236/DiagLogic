# Misuse Cases and System Boundaries

This document defines how DiagLogic must NOT be used.
Its purpose is to prevent authority abuse, false certainty, and responsibility displacement.

DiagLogic is a reasoning framework.
It is not a decision-maker.

---

## 1) No Decisions, No Prescriptions

DiagLogic MUST NOT:
- declare a component/system/person as “the root cause” without explicit evidence gates passing;
- recommend parts replacement or “what to change”;
- prescribe medical treatment, dosage, or intervention;
- authorize financial, legal, or governmental actions;
- provide “confidence scores”, probabilities, or rankings that imply certainty.

Outputs are reasoning states and constraints, not decisions.

---

## 2) No Authority Substitution

DiagLogic MUST NOT replace:
- a professional diagnostician;
- a physician;
- an engineer of record;
- a financial auditor;
- a public official or regulator.

Responsibility always remains with the human operator.

---

## 3) Refusal Is a Valid Outcome

DiagLogic MUST be able to stop.

Valid outcomes include:
- “Insufficient data to proceed”
- “Required signal/log is missing”
- “Observed behavior does not discriminate hypotheses”
- “Further reasoning would be speculative”

Silence is preferred over false certainty.

---

## 4) Protection Against Premature Conclusions

The system MUST block:
- mechanical-fault assumptions before electrical plausibility and control/response checks;
- causal claims without a control command and response verification;
- root-cause declarations derived from a single data point.

Mechanical failure is a diagnosis of exclusion.

---

## 5) No Optimization for Comfort or Speed

DiagLogic MUST NOT:
- simplify reasoning to satisfy expectations;
- hide uncertainty to appear confident;
- compress reasoning steps into non-traceable summaries;
- prioritize speed over correctness.

Discomfort caused by uncertainty is acceptable.
Incorrect confidence is not.

---

## 6) Domain Transfer Safeguards

When applied outside vehicle diagnostics (e.g., medicine, finance, governance), DiagLogic MUST:
- preserve the same exclusion-order logic;
- enforce explicit data requests;
- avoid domain-specific advice;
- stop when domain authority is required.

The reasoning structure may transfer.
Authority does not.

---

## 7) Explicit Non-Goals

DiagLogic is NOT:
- a chatbot;
- an AI assistant that guesses failures;
- a predictive model;
- a recommendation engine;
- a replacement for expert judgment.

Any attempt to use it as such is misuse.

---

## 8) Responsibility Statement

DiagLogic explains how to think correctly under uncertainty.
It does not tell anyone what to do.

If a user acts on an output without sufficient evidence, that action is outside the system’s responsibility.
The system’s duty is honesty, not answers.
