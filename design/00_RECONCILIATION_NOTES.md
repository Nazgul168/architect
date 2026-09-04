# Reconciliation Notes

Status: DRAFT  
Version: 0.1  
Purpose: Resolve contradictions and ambiguities in the current Architect concept before Project Instructions become canonical.

## 1. Top-level layer labels

### Issue
The draft uses `C` for both Project Context and Project Memory, then `D` for Working State.

### Resolution
Use five distinct layers:

A. Cognitive Core  
B. Expert Memory  
C. Project Context  
D. Project Memory  
E. Working State

The Learning System is a cross-layer mechanism rather than another memory layer.

---

## 2. Project Context vs Project Memory

### Issue
The Project Memory description partially repeats the Project Context description ("what was given to understand the project", "changeable sources").

### Resolution
Define them strictly:

**Project Context** = what the Architect receives as input about the current project.

Examples:
- documents;
- requirements;
- data;
- regulations;
- research;
- organizational context;
- stakeholder information.

**Project Memory** = what the Architect learns, decides, establishes, or records while working on the current project.

Examples:
- accepted project decisions and rationale;
- rejected alternatives;
- resolved contradictions;
- glossary and accepted definitions;
- confirmed assumptions;
- unresolved questions;
- local lessons learned;
- evolution of the solution.

Current decisions belong in Project Memory, not Project Context.

---

## 3. "Project Memory" has two meanings

### Issue
The draft uses `Project Memory` both for a controlled project-specific memory layer and for ChatGPT's ambient Project Memory capability. Those are materially different.

### Resolution
Use the following terms:

**PROJECT MEMORY** = Architect-managed, explicit, controlled project memory.

**CHATGPT PROJECT MEMORY** = platform-level contextual memory. It may help retrieval but is not canonical and must not be relied on as the sole source of truth.

---

## 4. Learning extraction vs transferable knowledge only

### Issue
One draft instruction says that after significant work the Architect should extract "only transferable knowledge". Elsewhere the learning protocol correctly says project-specific learning must first be consolidated into Project Memory and only then assessed for transferability.

### Resolution
Canonical rule:

> After significant work, extract relevant experience. Consolidate important project-specific learning into Project Memory. Promote only meaningfully transferable, sufficiently supported abstractions into Expert Memory.

---

## 5. Detailed cognitive protocols do not belong in Expert Memory

### Issue
One passage says that detailed instructions for task understanding, knowledge retrieval, methodology construction, critique, validation and learning are stored "in Expert Memory".

### Resolution
Detailed operating protocols belong in `core/` and `system/`.

**Expert Memory** is reserved for accumulated professional capital:
- transferable principles;
- heuristics;
- patterns;
- failure modes;
- case abstractions;
- learned methods;
- method improvements;
- meta-methods.

This prevents governing instructions from being mixed with learned content.

---

## 6. Pattern is both an intermediate and a final knowledge type

### Issue
The abstraction ladder shows `CANDIDATE PATTERN` as a mandatory intermediate step before Principle / Heuristic / Failure Mode, while the EKB also treats Pattern as a final knowledge object.

### Resolution
Use a non-linear abstraction model:

CASE / EXPERIENCE  
→ OBSERVATION  
→ ABSTRACTION  
→ one or more of:
- PATTERN
- PRINCIPLE
- HEURISTIC
- FAILURE MODE
- DECISION PRINCIPLE
- METHOD IMPROVEMENT

Several such objects may later alter a METHOD. Repeated method-level learning may eventually produce a META-METHOD.

A Pattern can therefore be a final promoted knowledge object.

---

## 7. Five abilities vs seven cognitive capabilities

### Issue
The mission is summarized as five abilities, while the Cognitive Core contains seven capabilities.

### Resolution
No conflict exists if the levels are explicit.

The **five abilities** are the compact lifecycle summary:

understand → retrieve → synthesize → critically check → learn.

The **seven capabilities** are the operational decomposition of that lifecycle:

1. Task Understanding & Problem Framing
2. Knowledge Navigation
3. Model Building
4. Synthesis & Methodology Design
5. Professional Judgment
6. Validation & Verification
7. Learning & Abstraction

---

## 8. Constructive criticism vs Validation

### Issue
Critique sometimes appears as if it were an explicit process stage, while elsewhere it is described as a permanent characteristic of the Architect.

### Resolution
Constructive criticism is a **cross-cutting cognitive principle** applied throughout the seven capabilities.

Validation and Verification remain explicit cognitive functions.

- **Critique** challenges assumptions, completeness, consistency, alternatives and failure modes.
- **Validation** asks whether the solution is appropriate for the real problem and intended use.
- **Verification** asks whether the solution satisfies specified requirements, rules, constraints and acceptance criteria.

---

## 9. Continuous learning vs end-of-project distillation

### Issue
The draft describes both promotion after significant work and Expert Distillation after a project ends.

### Resolution
Use both:

- **Continuous learning:** promotion may occur after significant work when the evidence is sufficient.
- **Project-close distillation:** a mandatory final pass checks whether valuable transferable learning remains trapped in Project Memory.

---

## 10. GitHub vs Git repository

### Issue
The draft says "GitHub is the canonical physical storage".

### Resolution
Canonical formulation:

> The version-controlled **Git repository** is the canonical Expert Knowledge Base. A private GitHub repository may host the canonical remote copy.

This preserves portability to another Git host if needed.

---

## 11. EKB access from ChatGPT

### Issue
The draft implies that Project Sources directly connect the EKB to the Architect.

### Resolution
Treat access as an implementation layer.

The Architect must have a verified retrieval path to the EKB. Depending on available capabilities this may be:
- a GitHub connector;
- mounted Project Sources;
- an indexed retrieval layer;
- a controlled synchronization process;
- another verified tool.

Do not assume automatic read/write synchronization unless it is actually available.

---

## 12. Working State example contains "3 alternatives"

### Issue
"3 possible variants" appears as an example but could be misread as a fixed rule.

### Resolution
Working State may contain any number of candidate alternatives appropriate to the task. No fixed number is required.
