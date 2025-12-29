# Output Specification v0.1
## Canonical result contract for DiagLogic

---

## 1. Purpose

The Output defines what a human sees when DiagLogic processes diagnostic data.

It is not a conversation.
It is not a recommendation.
It is not a decision.

The Output is a structured diagnostic report that:
- exposes reasoning boundaries;
- explains why conclusions are or are not admissible;
- ensures the system never becomes silent.

---

## 2. Output modes (mandatory)

Every Output MUST declare exactly one mode.

### 2.1 Conclude
Sufficient admissible evidence exists to confirm or falsify a hypothesis.

### 2.2 Constrain
Evidence is insufficient for a conclusion, but sufficient to:
- exclude certain hypotheses;
- restrict admissible interpretations.

### 2.3 Acquire
Evidence is insufficient to proceed.
The Output MUST include at least one Data Request.

---

## 3. Output structure (mandatory)

An Output is invalid if any section below is missing.

---

### 3.1 Case Header

Provides context without interpretation.

Required:
- Case ID
- Timestamp
- Vehicle context (ICE / Hybrid / EV)
- Data sources used
- Risk class (low / medium / high)

---

### 3.2 Facts

Contains only verifiable observations.

Allowed:
- DTCs
- freeze frame values
- live data snapshots
- command and feedback states
- test availability or status

Disallowed:
- interpretations
- probability language
- historical assumptions

---

### 3.3 Current Gate

Declares the current diagnostic gate:

- Electrical plausibility
- Command presence
- System response
- Physical state admissibility

A gate may be declared:
- evaluated
- not evaluated
- not assessable

---

### 3.4 Boundaries

Explicitly states what is NOT admissible at this stage.

Each boundary MUST include:
- the prohibited statement;
- the missing evidence;
- the blocked gate.

---

### 3.5 Admissible Hypotheses

Lists only hypotheses that are admissible at the current gate.

Rules:
- hypotheses without falsification paths are prohibited;
- if none are admissible, the section MUST explicitly state this.

---

### 3.6 Data Requests (if applicable)

Included when mode is Constrain or Acquire.

Each Data Request MUST conform to Data Request v1
and be listed with its identifier and type.

---

### 3.7 Next Logical State

Explains what becomes possible after:
- acquiring requested data; or
- remaining without it.

This section MUST describe logical transitions,
not actions or instructions.

---

### 3.8 Safety & Responsibility Note

Mandatory statement:

Diagnostic reasoning is structured by the system.
All decisions, actions, and safety responsibilities remain human.

---

## 4. Prohibitions

The Output MUST NOT contain:
- repair advice;
- parts replacement suggestions;
- probabilistic ranking;
- confidence scores;
- conversational language.

---

## 5. Core guarantee

Even with zero or insufficient data,
the Output MUST still provide:
- Facts (even if empty);
- Boundaries;
- Current Gate;
- at least one Data Request OR an explicit stop condition.

Silence is prohibited.

---

## 6. Status

Output Specification v0.1 is part of the DiagLogic Conceptual Core
and is independent of implementation, UI, or execution engine.
