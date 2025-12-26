# DiagLogic
Explainable diagnostic reasoning over vehicle diagnostic data  
(formerly OBD-AI)

---

## Project status

DiagLogic is currently in an early architectural phase.

- Diagnostic principles and constraints are frozen
- The reasoning model is defined
- Playbooks are treated as data, not code
- No executable engine is provided yet
- This repository documents the diagnostic framework first

This is intentional.

---

## What this is

DiagLogic is an engineering framework for vehicle diagnostics
that structures human reasoning instead of making decisions for the user.

It is designed to work with:
- OBD DTCs
- raw scanner logs
- multibrand diagnostic data

DiagLogic transforms diagnostic data into a clear, explainable diagnostic plan,
with explicit limits and honest acknowledgment of uncertainty.

---

## What DiagLogic is NOT

DiagLogic is explicitly not:
- a chat assistant
- an “AI that guesses the failure”
- a parts replacement recommendation system
- an automatic problem solver

If you are looking for a tool that tells you “what to replace”,
this project is not for you.

---

## Who this project is for

DiagLogic is built for:
- professional vehicle diagnosticians, not parts changers
- engineers who think in cause-and-effect logic
- practitioners who value explainability, safety, and reproducible diagnostics

---

## Core principle

A mechanical fault is a diagnosis of exclusion.

DiagLogic enforces this order by design:

1. electrical plausibility
2. presence of a control command
3. presence or absence of system response
4. only then mechanical suspicion

This order cannot be bypassed by the system.

---

## Design constraints (non-negotiable)

DiagLogic is intentionally constrained by design.

These constraints are architectural guarantees, not implementation details.

- DiagLogic never produces conclusions without explicit supporting data
- DiagLogic never fills gaps with probabilistic guesses or heuristics
- DiagLogic never reorders diagnostic logic for convenience or speed
- DiagLogic never optimizes for user satisfaction over correctness
- DiagLogic never hides uncertainty behind confident language

If required diagnostic data is missing, the system must stop
and explicitly state why further reasoning is invalid.

Silence or refusal to proceed is considered a valid and correct output.

---

## Non-goals (explicitly excluded)

DiagLogic is not designed to:
- predict failures using statistical likelihoods
- guess the “most common” cause of a fault
- suggest parts replacement
- shorten diagnostic processes by skipping steps
- provide reassurance or confidence without evidence
- simulate expert intuition

Any feature that violates ordered diagnostic reasoning
is considered out of scope, even if it appears useful.

---

## Responsibility boundary

DiagLogic does not make decisions.
It structures reasoning.

All final diagnostic decisions, safety judgments, and repair actions
remain the responsibility of the human diagnostician.

The system is intentionally incapable of acting as an authority.

---

## How it works (conceptual)

OBD data, logs, and reports are processed through a deterministic pipeline:

Normalization  
Playbook selection  
Gated prioritization  
Structured diagnostic plan  
Explicit data gaps  

The output is a report, not a conversation.

---

## What a playbook means in DiagLogic

A playbook is formalized diagnostic logic, represented as data rather than code.

Each playbook defines:
- problem context
- ordered checks
- confirmation conditions
- disconfirmation conditions
- explicit data gaps and their purpose
- safety constraints

A playbook does not advise.
It explains diagnostic reasoning.

---

## Real-world value example

In a real diagnostic case involving:
- P1117 (O2 heater short to ground)
- P0402 (EGR excessive flow)

DiagLogic:
- prevents immediate mechanical assumptions about the EGR valve
- forces consideration of an electrical root cause first
- stops exactly where data is insufficient
- clearly explains why further conclusions are not justified without logs
- This reduces false diagnoses, unnecessary disassembly,
wasted time, and erosion of professional trust.

---

## Why there is no chat interface

Chat interfaces create an illusion of understanding,
hide reasoning steps,
and encourage premature conclusions.

DiagLogic follows a strict model:

analysis → explanation → re-evaluation

Not conversation.

---

## Repository structure

docs/        – design notes, philosophy, constraints  
playbooks/   – diagnostic playbooks (data, not code)  
src/         – future processing engine (not implemented yet)

---

## License

This project is licensed under the Apache License 2.0.

Commercial use is allowed.
The license does not grant endorsement or warranty.

---

## In short

DiagLogic does not tell you what is broken.
It shows you how to think correctly to avoid being wrong.
