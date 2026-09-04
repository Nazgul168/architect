# Memory Architecture & Promotion Rules

Status: DRAFT  
Version: 0.1

## 1. Memory layers

ARCHITECT uses four distinct knowledge/state layers in addition to the Cognitive Core.

## PROJECT CONTEXT

### Definition
Current-project input.

### Contains
- documents;
- requirements;
- data;
- regulations;
- research;
- organizational information;
- stakeholder information;
- current external constraints.

### Does not automatically contain
Architect-created accepted decisions or learning. Those belong in Project Memory.

---

## WORKING STATE

### Definition
Temporary state of current reasoning.

### Contains
- hypotheses;
- draft models;
- candidate alternatives;
- provisional assumptions;
- unresolved questions;
- items to verify;
- work-in-progress artifacts.

### Rule
Working State is not authoritative.

Material that becomes accepted, established or operationally important should be promoted to Project Memory.

---

## PROJECT MEMORY

### Definition
Explicit, managed, project-specific knowledge accumulated during the project.

### Contains
- accepted decisions and rationale;
- rejected alternatives where useful;
- project glossary;
- accepted definitions;
- confirmed assumptions;
- resolved contradictions;
- unresolved important questions;
- local lessons learned;
- evolution of the solution.

### Rule
Project Memory is project-specific. It is not automatically transferable expertise.

---

## EXPERT MEMORY

### Definition
Long-term transferable professional capital accumulated across projects.

### Contains
- validated patterns;
- principles;
- heuristics;
- failure modes;
- decision principles;
- method improvements;
- methods;
- meta-methods;
- case abstractions.

### Rule
Only promote knowledge that has passed transferability assessment and learning validation.

## 2. Knowledge movement

```text
PROJECT CONTEXT
      ↓ informs
WORKING STATE
      ↓ accepted / established / important
PROJECT MEMORY
      ↓ abstraction + transferability + validation
EXPERT MEMORY
```

## 3. Promotion rules

### Working State → Project Memory
Promote when an item becomes:
- accepted;
- verified;
- operationally important;
- necessary for continuity;
- necessary to explain a later decision.

### Project Memory → Expert Memory
Promote when an item:
- is transferable beyond the current project;
- can be expressed independently of local names/details;
- has explicit applicability conditions;
- has known limits or uncertainty;
- improves recognition, judgment, method selection, critique or validation.

## 4. Non-promotion examples

Keep only in Project Memory:
- a specific manager's preference;
- an internal form name;
- a local approval route;
- a one-off workaround;
- project-specific terminology;
- a local deadline.

Promote to Expert Memory only if a more general lesson exists and is justified.

## 5. Platform memory distinction

**CHATGPT PROJECT MEMORY** is an ambient product capability.

It may help contextual continuity but must not be treated as the canonical Project Memory described above.

Canonical project knowledge should be represented in explicit artifacts that can be inspected, corrected and versioned.

## 6. Project closure

At project close:

```text
PROJECT MEMORY
├── project-specific → PROJECT ARCHIVE
└── transferable → EXPERT DISTILLATION → EXPERT MEMORY
```

Project-close distillation complements continuous learning; it does not replace it.

## 7. Causality and revision history

Do not overwrite important decisions or expert knowledge in a way that destroys:
- what changed;
- why it changed;
- what evidence triggered the change;
- what it superseded;
- what consequences followed.

Git version history should support, not replace, explicit semantic provenance inside important knowledge objects.
