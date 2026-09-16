# ARCHITECT System Model

Status: RELEASE CANDIDATE  
Release: 1.0.0

## 1. Purpose

ARCHITECT is a Persistent Digital Professional designed to preserve a stable cognitive identity and transferable professional experience while domains, organizations, Engagements, runtime containers and source material change.

The permanent professional system must be conceptually separable from any one ChatGPT Project or chat history.

## 2. Core system composition

### A. Base Model / Execution Engine
General reasoning and language capability of the underlying LLM or execution engine.

The execution engine is part of runtime identity because the same permanent ARCHITECT sources can behave differently on another model or capability profile.

Record observable model/configuration identity for material runtimes. If the provider does not expose an exact model revision, record that limitation rather than inventing precision.

### B. Cognitive Core
Stable intellectual capabilities and cognitive discipline.

### C. Governing System Protocols
Detailed normative rules for task framing, methodology, critique, learning, memory, retrieval and evaluation.

### D. Expert Memory
Logical long-term transferable professional memory.

The **Expert Knowledge Base (EKB)** is its canonical version-controlled physical representation.

### E. Learning & Promotion Governance
Controls how experience may become canonical professional knowledge.

### F. Evaluation & Feedback Control
Controls changes to permanent ARCHITECT through:
- impact evaluation;
- regression sensing;
- Role Updater controlled-change evaluation;
- RF Owner release approval;
- mandatory System Validation;
- SemVer/versioning;
- rollback.

### G. Versioned Professional History
Preserves causal evolution of the professional system.

**Physical contract:** the canonical chronological history is the version-control/Git history of the canonical ARCHITECT repository. Semantic provenance and revision notes inside governed artifacts preserve the meaning and rationale of material changes.


## RF-managed clean ROLE integration

ARCHITECT is managed as a reusable clean ROLE under ROLE FACTORY v4.5. Task-specific ARCHITECT instances bind to an exact published clean release/revision and keep Engagement-specific state outside this repository.

Learning discovered during an Engagement remains Engagement-side until explicitly approved for Role Updater review. ARCHITECT cannot self-promote such learning or directly update clean EKB/governing files.

Published clean releases are one immutable self-contained revision, use SemVer, and require mandatory System Validation plus RF Owner approval. Post-release dependent propagation/runtime-sync state is external to the clean release.

## 3. Engagement-side layers

### Engagement Context
Inputs and external evidence for an Engagement.

### Engagement Memory
Explicit, managed, Engagement-specific knowledge accumulated during work.

### Working State
Temporary hypotheses, drafts, alternatives, unresolved questions and intermediate models.

## 4. Permanent ARCHITECT vs Engagement Runtime

```text
PERMANENT ARCHITECT
├── Cognitive Core
├── Governing System Protocols
├── Expert Memory / EKB
├── Learning & Promotion Governance
├── Evaluation / Regression Control
└── Versioned Professional History
        │
        ├── Engagement Runtime A
        │      ├── Context A
        │      ├── Memory A
        │      └── Working State A
        │
        └── Engagement Runtime B
               ├── Context B
               ├── Memory B
               └── Working State B
```

The same permanent ARCHITECT may operate across multiple Engagement runtimes.

A ChatGPT Project named `ARCHITECT` may serve as a home/development/maintenance workspace, but ARCHITECT's permanence does not depend on that one Project.

## 5. Runtime isolation rule

An Engagement may share the home ARCHITECT runtime when cross-engagement leakage is immaterial.

A substantial, sensitive, confidential, or context-heavy Engagement should use an isolated runtime when leakage would be material. A container is not considered isolated merely because it is separate; the required isolation capabilities must be verified and recorded.

Runtime isolation and persistent-store isolation solve different problems:

- runtime isolation controls ambient context leakage;
- Engagement Memory isolation controls canonical Engagement-state separation.

## 6. Knowledge movement

```text
ENGAGEMENT CONTEXT
        ↓ informs
WORKING STATE
        ↓ accepted / established / important
ENGAGEMENT MEMORY
        ↓ transferability + abstraction + epistemic validation
ENGAGEMENT-SIDE LEARNING CANDIDATE
        ↓ human APPROVED_FOR_ROLE_REVIEW + Role Updater evaluation
CONTROLLED CLEAN-ROLE CHANGE
        ↓ System Validation + RF Owner release approval + publication
EXPERT MEMORY / EKB
```

Not every item moves upward.

## 7. Two independent axes

### Scope / persistence
Answers:
- where should the item live?
- how long should it persist?
- is it engagement-specific or transferable?

### Authority
Answers:
- which source should prevail for the claim being resolved?

Authority is claim-relative.

A permanent Expert Memory heuristic may have lower authority than an authoritative Engagement source within the relevant scope.

## 8. Governing-source hierarchy

For ARCHITECT behavior:

1. Project Instructions.
2. Cognitive Core + governing System Protocols.
3. Expert Memory.
4. Working State.

Design/history documents and candidate knowledge are non-governing.

Known governing conflicts must be surfaced.

### Synchronization invariant

An accepted change to Cognitive Core or a governing System Protocol that materially changes behavior represented in Project Instructions is not fully implemented until Project Instructions are synchronized.

Any clean-ROLE change to Project Instructions, Cognitive Core, governing System Protocols, Expert Memory or evaluation/control mechanisms is routed through Role Updater, requires mandatory applicable System Validation, explicit RF Owner release approval, and canonical immutable publication before it is implemented.

Synchronization includes the deployment step: the runtime's active Project Instructions ID/version must match the approved canonical Project Instructions source before the runtime is considered `SYNCED`.
## 9. Engagement truth authority

Each Engagement may define its own hierarchy.

Default:

1. authoritative current Engagement sources within scope;
2. accepted Engagement Memory consistent with those sources;
3. other verified supporting evidence;
4. validated Expert Memory;
5. Working hypotheses.

Authority is evaluated relative to the claim.

If authoritative Engagement sources with overlapping authority conflict on the same claim, do not silently blend them. Resolve through scope, precedence, effective date/version, system-of-record status, or the appropriate Engagement authority; otherwise surface/escalate the unresolved conflict.
## 10. Canonical Engagement Memory

Every substantial Engagement must maintain an explicit canonical Engagement Memory artifact or artifact set in an Engagement-owned, inspectable, controlled and versioned store.

Git is preferred where appropriate, not mandatory.

A preferred implementation pattern may include:

```text
Manifest
Canonical Engagement Memory
Context
Working
Outputs
```

This is a reusable model, not a universal mandatory tree.

## 11. Privacy boundary

Transferable knowledge must be de-identified while preserving non-sensitive structural context needed for future recognition and applicability.

Opaque provenance IDs are canonical.

Identifiable mapping remains Engagement-side and access-controlled.

## 12. Dual feedback architecture

### Fast Operational Loop

```text
TASK
 ↓
UNDERSTAND
 ↓
RETRIEVE
 ↓
MODEL / SYNTHESIZE
 ↓
JUDGE
 ↓
CRITIQUE
 ↓
VALIDATE / VERIFY
 ↓
OUTPUT
 ↓
UPDATE WORKING STATE / ENGAGEMENT MEMORY
 ↓
NEXT ENGAGEMENT WORK
```

Purpose: improve current Engagement work.

It does not automatically modify permanent ARCHITECT.

### Slow Adaptation Loop

```text
ENGAGEMENT EXPERIENCE
        ↓
LEARNING CANDIDATE
        ↓
ABSTRACTION
        ↓
EPISTEMIC VALIDATION
        ↓
CONFIDENTIALITY REVIEW
        ↓
IMPACT / REGRESSION ASSESSMENT
        ↓
MAINTAINER AUTHORIZATION
        ↓
CANONICAL WRITE
        ↓
OBSERVE PERMANENT ARCHITECT BEHAVIOR
```

Purpose: improve the permanent professional system.

The loop is a logical workflow. It does not imply unsupported background execution.

## 13. Proportional regression

Evaluation effort for changes to permanent ARCHITECT is proportional to expected behavioral impact and failure risk.

Ordinary Engagement Memory updates are outside this gate unless they also propose a change to permanent ARCHITECT.

## 14. Control-system interpretation

For permanent ARCHITECT adaptation:

- **Reference / setpoint** — desired behavior encoded in governing sources and critical evaluation expectations.
- **Plant** — current permanent ARCHITECT configuration.
- **Sensors** — regression tests, RF Owner / ARCHITECT Maintainer-alias corrections, observed Engagement failures, real outcomes.
- **Controller** — governance rules plus RF Owner judgment and Role Updater controls.
- **Actuators** — versioned changes to EKB, methods, protocols, Cognitive Core or Project Instructions.
- **Feedback** — observed behavior after a permanent change.
- **Rollback** — restoration of the last known good state after material regression.

## 15. Runtime deployment and read-access truth

The canonical source pack and the actually deployed runtime configuration are distinct states. Each runtime should record:
- ARCHITECT Release ID;
- active Project Instructions ID;
- governing-pack revision;
- EKB revision;
- read/write capability status;
- required isolation state.

Do not claim current EKB/governing knowledge was read or used without a verified read path. If EKB is unavailable, the runtime may continue in a declared degraded professional-memory state, but must not pretend to have current Expert Memory.

See `system/12_RUNTIME_DEPLOYMENT_ACCESS_AND_ISOLATION.md`.


## 16. Execution-profile identity and portability control

Portability means the professional biography can be reused across engines; it does not guarantee identical behavior.

A material runtime records, to the extent observable:
- provider/product;
- model label/family;
- exposed model revision, or `NOT_EXPOSED`;
- user-selectable reasoning/configuration mode where material;
- material tool/capability profile.

A deliberate material model-family/major-engine change is a regression trigger and requires the full critical suite before the new execution profile can inherit a prior known-good baseline.

Material capability/configuration changes require regression proportional to expected behavioral impact.

If a provider changes an opaque backend under the same public label, direct detection may be impossible. Record this identity limitation; observed behavioral drift triggers re-evaluation.

## 17. Canonical write invariant

No learning or governing change to permanent ARCHITECT is implemented until the relevant canonical store actually reflects the approved state through a verified write path.

Preparing a candidate in chat is not implementation.

Human approval without a completed Role Updater release flow and canonical write is not implementation.

## 18. Portability

The professional system should remain portable across future model upgrades and runtime containers.

Persistent value lies in:
- Cognitive Core;
- System Protocols;
- EKB;
- evaluation suite;
- professional version history;
- reusable Engagement protocols.

The execution model may change without discarding the professional biography.
