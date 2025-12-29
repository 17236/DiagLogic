# Data Request v1
## Canonical data acquisition model for DiagLogic

---

## 1. Purpose

A Data Request is a logical construct used when the system
cannot proceed without violating admissible reasoning.

A Data Request is not an instruction, recommendation, or assumption.
Its sole purpose is to reduce logical uncertainty.

---

## 2. When a Data Request is required

The system must generate a Data Request if:

- the current logical gate cannot be evaluated;
- missing data blocks admissible reasoning;
- continuing without new data would violate reasoning constraints.

Silence is not an acceptable outcome.

---

## 3. Types of Data Request

Every Data Request must declare its type:

### 3.1 Blocking
Reasoning cannot proceed without this data.

### 3.2 Weakening
Reasoning may proceed, but uncertainty remains.

---

## 4. Data Request structure (mandatory)

A Data Request is invalid if any field below is missing.

---

### 4.1 Purpose

Defines which logical uncertainty must be resolved
and what admissibility change is expected.

---

### 4.2 Scope

Defines the playbook or reasoning context
in which this request is valid.

---

### 4.3 Type

Blocking or Weakening.

---

### 4.4 Evidence Type

Defines the expected nature of evidence, without instructions:

- ECU read-only data
- Command/response correlation
- Active test result (non-instructional)
- External measurement
- Human-confirmed fact

---

### 4.5 Minimal Set

Separates required data from optional data.

The system must never demand more than required.

---

### 4.6 Unlocks

Defines which statements or logical transitions
become admissible after data acquisition.

---

### 4.7 Blocks

Defines which hypotheses or assumptions
become inadmissible.

This field is mandatory.

---

### 4.8 Separation Power

Defines which scenarios become distinguishable
because of this data.

If no separation exists, the request is invalid.

---

### 4.9 Validity Constraints

Defines conditions under which the data is valid:

- operating state
- timing
- freshness
- system mode

Invalid data must not be used for reasoning.

---

### 4.10 If Missing

Defines the reasoning state if the data cannot be obtained:

- which gate remains blocked;
- which statements remain inadmissible;
- whether escalation of data source is required.

The system must never become silent.

---

## 5. Prohibitions

A Data Request must not contain:

- repair recommendations;
- probabilistic language;
- promises of outcome;
- instructions for action.

---

## 6. Core principle

A Data Request does not move the system closer to an answer.
It moves the system closer to admissible reasoning.

---

## 7. Status

Data Request v1 is part of the DiagLogic Conceptual Core
and is independent of implementation details.
