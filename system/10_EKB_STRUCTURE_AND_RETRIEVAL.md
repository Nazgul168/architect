# Expert Knowledge Base Structure & Retrieval

Status: DRAFT  
Version: 0.1

## 1. Purpose

The Expert Knowledge Base (EKB) is the long-term transferable professional memory of ARCHITECT.

It should remain compact, inspectable, versioned and retrieval-friendly.

The EKB is a distillation of experience, not a dump of project documents.

## 2. Canonical storage

The canonical EKB should live in a version-controlled Git repository.

A private GitHub repository may host the canonical remote copy.

The storage layer and the retrieval layer are separate concerns.

## 3. Recommended repository structure

```text
architect/
├── README.md
│
├── core/
│   ├── project_instructions_draft.md
│   └── cognitive_core.md
│
├── system/
│   ├── task_understanding_and_knowledge_navigation.md
│   ├── methodology_design_and_professional_judgment.md
│   ├── critique_validation_verification.md
│   ├── learning_protocol.md
│   ├── memory_architecture.md
│   └── knowledge_object_model.md
│
└── memory/
    ├── expert_model.md
    └── expert_memory/
        ├── 00_EKB_INDEX.md
        ├── meta_methods/
        ├── reasoning_heuristics/
        ├── method_library/
        ├── patterns/
        ├── failure_modes/
        ├── case_abstractions/
        ├── critique_frameworks/
        └── decision_principles/
```

`critique_frameworks/` contains learned/adopted reusable critique frameworks.  
The governing critique protocol itself belongs under `system/`.

## 4. EKB Index

`00_EKB_INDEX.md` is not merely a folder listing.

It is a conceptual map of the Architect's memory.

Example:

```text
SYSTEM / PROBLEM FRAMING
→ boundary definition
→ problem decomposition
→ stakeholder ambiguity
→ objective vs proposed solution

INFORMATION / DATA
→ entity identification
→ state vs event
→ temporal modelling
→ auditability
→ versioning

METHODOLOGY DESIGN
→ methodology composition
→ method selection
→ evidence requirements
→ validation

DECISION MAKING
→ uncertainty
→ competing constraints
→ reversibility
→ option comparison

IMPLEMENTATION
→ decomposition
→ verification
→ handoff
→ acceptance
```

The index should help form retrieval paths based on problem structure.

## 5. Retrieval principle

A large EKB is useful only if relevant knowledge can be activated.

Retrieval should follow:

```text
CURRENT TASK
   ↓
TASK REPRESENTATION / TASK SIGNATURE
   ↓
RETRIEVAL CUES
   ↓
RELEVANT EKB OBJECTS
   ↓
APPLICABILITY CHECK
   ↓
WORKING CONTEXT
```

Do not load the entire EKB by default.

## 6. Retrieval cues inside Knowledge Objects

Each important Knowledge Object should expose cues such as:
- problem class;
- system level;
- lifecycle stage;
- conditions;
- symptoms;
- failure signals;
- constraints;
- related methods;
- related objects.

This supports semantic retrieval and later indexing technologies.

## 7. Future retrieval layer

Git remains the source of truth even if future retrieval uses:
- full-text search;
- semantic search;
- embeddings;
- vector databases;
- knowledge graphs;
- agentic retrieval.

Derived indexes must be reproducible from the canonical repository where practical.

## 8. EKB hygiene

Avoid:
- raw transcript accumulation;
- duplicate knowledge objects;
- project-specific facts without abstraction;
- universal claims from isolated cases;
- many tiny objects that carry no independent retrieval value;
- silent contradiction between objects.

Prefer:
- compact, reusable abstractions;
- clear recognition cues;
- explicit limits;
- provenance;
- links;
- controlled revision.

## 9. Expert Model

`expert_model.md` may track the Architect's current self-model:
- strengths;
- weak areas;
- mature methods;
- immature methods;
- recurring failure patterns;
- areas needing more evidence.

This is not a claim of autonomous self-awareness. It is a managed meta-record used to guide future learning and evaluation.
