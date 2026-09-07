# Expert Knowledge Base Structure & Retrieval

Status: RELEASE CANDIDATE  
Release: ARCH-0.2.1-RC5

## 1. Purpose

The Expert Knowledge Base (EKB) is the canonical physical representation of ARCHITECT's transferable professional memory.

Expert Memory is the logical layer.  
EKB is its canonical store.

The EKB should remain:
- compact;
- inspectable;
- versioned;
- de-identified;
- structurally informative;
- retrieval-friendly.

## 2. Canonical storage

The preferred canonical implementation is the ARCHITECT Git repository.

A private GitHub repository may host its canonical remote.

Storage and retrieval are separate concerns.

No component may claim EKB was changed unless a verified write succeeded.

## 3. ARCHITECT repository structure

```text
architect/
├── .gitattributes
├── README.md
├── FILE_MANIFEST.md
├── core/
│   ├── 01_PROJECT_INSTRUCTIONS_v0.2.1_RC5.md
│   └── 03_COGNITIVE_CORE.md
├── governance/
│   └── 00_ARCHITECT_GOVERNANCE.md
├── runtime/
│   ├── 00_RUNTIME_REGISTRY.md
│   └── records/
│       └── README.md
├── evaluation/
│   ├── 00_BASELINE_REGISTRY.md
│   └── runs/
│       └── README.md
├── design/
│   ├── 00_ARCHITECTURE_DECISION_RECORD_v0.2.md
│   ├── 00_RECONCILIATION_NOTES.md
│   ├── 01_STATIC_CONSISTENCY_REPORT.md
│   └── 02_SURGICAL_CHANGELOG_v0.2.1_RC5.md
├── system/
│   ├── 02_SYSTEM_MODEL.md
│   ├── 04_TASK_UNDERSTANDING_AND_KNOWLEDGE_NAVIGATION.md
│   ├── 05_METHODOLOGY_DESIGN_AND_PROFESSIONAL_JUDGMENT.md
│   ├── 06_CONSTRUCTIVE_CRITICISM_VALIDATION_VERIFICATION.md
│   ├── 07_LEARNING_AND_ABSTRACTION_PROTOCOL.md
│   ├── 08_MEMORY_ARCHITECTURE_AND_PROMOTION.md
│   ├── 09_KNOWLEDGE_OBJECT_MODEL.md
│   ├── 10_EKB_STRUCTURE_AND_RETRIEVAL.md
│   ├── 11_EVALUATION_AND_REGRESSION_SUITE.md
│   └── 12_RUNTIME_DEPLOYMENT_ACCESS_AND_ISOLATION.md
├── memory/
│   ├── candidates/
│   │   └── README.md
│   └── expert_memory/
│       ├── 00_EKB_INDEX.md
│       ├── meta_methods/
│       ├── methods/
│       ├── principles/
│       ├── reasoning_heuristics/
│       ├── patterns/
│       ├── failure_modes/
│       ├── decision_principles/
│       └── case_abstractions/
└── templates/
    ├── 00_ENGAGEMENT_MANIFEST_TEMPLATE.md
    ├── ENGAGEMENT_MEMORY_TEMPLATE.md
    ├── RUNTIME_DEPLOYMENT_RECORD_TEMPLATE.md
    └── BASELINE_RUN_RECORD_TEMPLATE.md
```

Empty directories may be created when the first object exists.

## 4. Engagement stores are separate

A substantial Engagement must have its own canonical Engagement Memory artifact or artifact set in an Engagement-owned, inspectable, controlled and versioned store.

That store may be:
- a Git repository;
- a corporate versioned documentation environment;
- another auditable versioned store.

Git is preferred where appropriate, not mandatory.

The template tree is a preferred implementation, not a universal requirement.

## 5. Candidate staging

`memory/candidates/` is non-canonical.

A candidate may alternatively exist in:
- branch;
- PR;
- proposed patch;
- explicit staging artifact.

Candidate content is not validated Expert Memory.

Any candidate stored in the permanent ARCHITECT repository must already be de-identified. Raw sensitive/identifying Engagement evidence remains Engagement-side and is represented only by safe summaries or opaque references.

## 6. EKB Index

`00_EKB_INDEX.md` is a conceptual memory map, not just a folder list.

Knowledge areas may include:
- system/problem framing;
- information/data;
- methodology design;
- decision making;
- implementation.

Categories:
- Meta-Methods;
- Methods;
- Principles;
- Heuristics;
- Patterns;
- Failure Modes;
- Decision Principles;
- Case Abstractions.

## 7. Retrieval

```text
ACTIVE ENGAGEMENT
   +
CURRENT TASK
   ↓
TASK SIGNATURE
   ↓
RETRIEVAL CUES
   ↓
RELEVANT VALIDATED EKB OBJECTS
   ↓
AUTHORITY + APPLICABILITY CHECK
   ↓
WORKING CONTEXT
```

Do not load the entire EKB by default.

## 8. Recognition and structural context

Knowledge Objects should expose:
- problem class;
- system level;
- lifecycle stage;
- conditions;
- symptoms;
- failure signals;
- constraints;
- related methods;
- non-sensitive structural context.

De-identification must not destroy retrieval usefulness.

## 9. Canonical EKB vs Active Expert Memory

The canonical EKB stores the versioned professional record, including current and historical states.

**Active Expert Memory** for default guidance is the current `validated` subset.

Objects in `contested`, `deprecated`, or `superseded` states remain in canonical EKB for traceability but are not default active guidance.

## 10. Status-aware retrieval

- `validated` — canonically available, but context-sensitive and revisable.
- `contested` — use cautiously with competing evidence.
- `deprecated` — historical only unless explicitly needed.
- `superseded` — follow the superseding object.
- `candidate` — not canonical expertise.

## 11. Authority-aware retrieval

Retrieval does not imply authority.

Within an Engagement:
- authoritative Engagement truth may override a generic EKB heuristic for the relevant claim;
- authority is claim-relative;
- a conflict may generate a new learning candidate.

## 12. Privacy-aware retrieval

EKB bodies are de-identified while preserving non-sensitive structural context.

Opaque provenance is not automatically resolved into identifiable Engagement evidence.

Identifiable mapping remains Engagement-side and access-controlled.

## 13. Future retrieval layer

Git may remain canonical while retrieval uses:
- full-text search;
- semantic search;
- embeddings;
- vector databases;
- knowledge graphs;
- agentic retrieval.

Derived indexes should be reproducible from canonical sources where practical.

## 14. EKB hygiene

Avoid:
- raw transcript accumulation;
- duplicate objects;
- raw Engagement facts;
- universal claims from isolated cases;
- privacy leakage;
- candidate knowledge silently becoming canonical;
- context-free abstractions that lose Recognition Cues.

Prefer:
- compact abstractions;
- structural cues;
- explicit limits;
- safe provenance;
- controlled revision;
- clear governance.

## 15. Canonical read/access requirement

Repository existence does not imply runtime access.

ARCHITECT must not claim to have used current EKB unless a verified read path exists and the relevant revision is accessible in the current runtime.

If EKB read access is unavailable:
- do not silently substitute model memory for EKB;
- declare the professional-memory limitation when material;
- continue only with actually available governing and Engagement sources.

A runtime deployment record should identify the expected EKB revision and read status.

## 16. Canonical write requirement

No change to permanent ARCHITECT Expert Memory is implemented until the canonical EKB reflects the approved state through a verified write path.

If no write path exists:
- prepare a proposed patch/change set;
- do not claim EKB changed.

## 17. Versioning and rollback

Material permanent-ARCHITECT changes should be versioned.

Regression evaluation is proportional to expected behavioral impact and risk.

If a newly applied change produces material regression:
- flag it;
- rollback or supersede when necessary;
- restore the last known good state;
- analyze before re-promotion.
