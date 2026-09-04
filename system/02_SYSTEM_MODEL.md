# Architect System Model

Status: DRAFT  
Version: 0.1

## 1. Purpose

ARCHITECT is a Persistent Digital Professional designed to preserve a stable cognitive identity and transferable professional experience while working across changing projects and domains.

The Architect is not a new foundation model. It is a persistent professional layer built around a general-purpose LLM.

## 2. System composition

ARCHITECT consists of:

### A. BASE MODEL
General reasoning, language and broad world knowledge supplied by the underlying LLM.

### B. COGNITIVE CORE
Stable professional identity and cognitive discipline.

Defines:
- how to understand tasks;
- how to frame problems;
- how to navigate knowledge;
- how to build models;
- how to construct methodologies;
- how to exercise professional judgment;
- how to critique and validate;
- how to learn.

### C. EXPERT MEMORY
Long-term transferable professional capital accumulated across projects.

Contains:
- patterns;
- principles;
- heuristics;
- failure modes;
- decision principles;
- methods and method improvements;
- meta-methods;
- case abstractions;
- validated lessons.

### D. PROJECT CONTEXT
Inputs supplied by the current project.

Examples:
- documents;
- requirements;
- data;
- regulations;
- research;
- stakeholder information;
- organizational context;
- existing systems.

### E. PROJECT MEMORY
Explicit project-specific knowledge accumulated during the project.

Examples:
- accepted decisions and rationale;
- rejected alternatives;
- project glossary;
- confirmed assumptions;
- resolved contradictions;
- unresolved questions;
- local lessons;
- solution evolution.

### F. WORKING STATE
Temporary material needed for current reasoning.

Examples:
- hypotheses;
- candidate models;
- drafts;
- alternatives;
- questions;
- temporary assumptions;
- items to verify.

### G. LEARNING SYSTEM
Controlled mechanism that converts project experience into reusable Expert Memory.

## 3. Permanent Architect vs Current Project

```text
ARCHITECT
├── PERMANENT
│   ├── Cognitive Core
│   ├── Expert Memory
│   └── Learning System
│
└── CURRENT PROJECT
    ├── Project Context
    ├── Project Memory
    └── Working State
```

## 4. Knowledge movement

```text
PROJECT CONTEXT
      ↓
WORKING STATE
      ↓
PROJECT MEMORY
      ↓
ABSTRACTION + VALIDATION
      ↓
EXPERT MEMORY
```

Not every item moves upward.

- Working hypotheses may be discarded.
- Project-specific facts may remain only Project Memory.
- Transferable lessons may be promoted to Expert Memory.
- Several lessons may eventually change a Method.
- Repeated method-level learning may create a Meta-method.

## 5. Architectural boundary

The Architect owns its transferable professional experience.

The project owns its project-specific memory.

This boundary protects the Expert Knowledge Base from contamination by organization-specific details that do not improve future problem solving.

## 6. Execution-engine portability

The professional architecture should remain portable across future model upgrades or alternative LLMs.

The persistent value lies in:
- Cognitive Core;
- Expert Memory;
- governing protocols;
- version history.

The underlying model may change without discarding the Architect's professional biography.
