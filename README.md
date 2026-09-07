# ARCHITECT

Release ID: ARCH-0.2.1-RC5
Status: RELEASE CANDIDATE — BEHAVIORAL BASELINE NOT YET ESTABLISHED
Date: 2026-09-04

## Purpose

ARCHITECT is a **Persistent Digital Professional / Digital Methodologist**: a transferable professional expert whose cognitive identity and accumulated professional capital persist while domains, organizations, real-world initiatives, runtime containers, and source materials may change.

ARCHITECT is not a new foundation model. It is a persistent professional system built around a general-purpose LLM.

Its long-term development is defined by improved ability to:

**understand the real problem → navigate relevant knowledge → build an adequate model → synthesize a solution or methodology → exercise professional judgment → critically validate the result → extract transferable learning.**

## Terminology

- **ARCHITECT** — the permanent professional system.
- **ChatGPT Project `ARCHITECT`** — a possible home/development/maintenance workspace; it is not the source of ARCHITECT's permanence.
- **Engagement** — a real-world assignment, initiative, client project, or problem context handled by ARCHITECT.
- **Active Engagement** — the Engagement currently in scope for work.
- **Engagement Runtime** — the runtime/context container in which an Engagement is executed.
- **Engagement Context** — source material and external facts for the Active Engagement.
- **Engagement Memory** — explicit, managed, engagement-specific knowledge accumulated during work.
- **Working State** — temporary reasoning state for current work.
- **Expert Memory** — ARCHITECT's transferable professional memory.
- **Expert Knowledge Base (EKB)** — the canonical version-controlled physical representation of Expert Memory.
- **ARCHITECT Maintainer** — the human governance authority for changes to the permanent professional system ARCHITECT. At initial system bootstrap, the canonical repository owner/user designates this role in `governance/00_ARCHITECT_GOVERNANCE.md`; later runtime users do not become Maintainer automatically.
- **Engagement Owner / Engagement Confidentiality Authority** — an Engagement-side role that may approve Engagement-specific decisions or confidentiality/transfer permissions but does not automatically control global ARCHITECT memory or governing behavior.

### ARCHITECT Maintainer continuity

The canonical Maintainer binding is stored in `governance/00_ARCHITECT_GOVERNANCE.md`. A change, revocation, or succession of this authority must be versioned. Normally it is authorized by the current ARCHITECT Maintainer; if that authority is unavailable, a documented recovery action by the canonical repository owner/administrator may establish a successor. Engagement-side roles never inherit ARCHITECT Maintainer authority automatically.

## Architectural model

```text
PERMANENT ARCHITECT
├── Cognitive Core
├── Governing System Protocols
├── Expert Memory / EKB
├── Learning & Promotion Governance
├── Evaluation / Regression Control
└── Versioned Professional History
        │
        ├── reused by Engagement Runtime A
        │      ├── Engagement Context A
        │      ├── Engagement Memory A
        │      └── Working State A
        │
        └── reused by Engagement Runtime B
               ├── Engagement Context B
               ├── Engagement Memory B
               └── Working State B
```

**Invariant:** ARCHITECT is permanent; individual Engagement context is not.

## Runtime isolation

A ChatGPT Project named `ARCHITECT` may be used as the home, development, maintenance, or general interaction workspace.

It is **not** assumed that every Engagement must live inside that one ChatGPT Project.

When cross-engagement context leakage would be material, a substantial or sensitive Engagement should use an isolated runtime context.

Runtime isolation is separate from persistent-storage isolation.

## Two independent knowledge axes

### Scope / persistence
Asks:
> Where does this knowledge belong and how long should it persist?

Typical flow:

`Working State → Engagement Memory → candidate transferable learning → Expert Memory`

### Authority
Asks:
> Which source should prevail for the particular claim or decision being resolved?

Authority is claim-relative.

Permanent or transferable does not mean more authoritative.

## Governing source hierarchy

For ARCHITECT behavior:

1. Project Instructions — executable runtime constitution.
2. Cognitive Core + governing System Protocols — detailed normative specification.
3. Expert Memory — learned professional knowledge.
4. Working State — non-governing.

Design/history documents and candidate knowledge are non-governing.

**Claim-specific governance metadata:** `governance/00_ARCHITECT_GOVERNANCE.md` is canonical for who currently holds ARCHITECT Maintainer authority and succession/revocation status. It does not override PI/Core/Protocols on behavioral rules or the scope of Maintainer powers.

An accepted change to Cognitive Core or a governing System Protocol that materially changes behavior represented in Project Instructions is not fully implemented until Project Instructions are synchronized.

## Engagement truth

Each Engagement may define its own source hierarchy.

Where no stronger hierarchy is defined, use:

1. authoritative current Engagement sources within their scope;
2. accepted Engagement Memory consistent with those sources;
3. other verified supporting evidence;
4. validated Expert Memory;
5. Working hypotheses.

Authority must be evaluated relative to the claim.

## Learning governance

ARCHITECT may autonomously:
- extract learning;
- abstract;
- assess transferability;
- perform epistemic validation;
- create candidate Knowledge Objects.

Promotion to canonical `validated` Expert Memory requires:
1. applicable epistemic criteria;
2. confidentiality/provenance review;
3. proportional impact/regression review where material;
4. explicit ARCHITECT Maintainer authorization;
5. successful canonical EKB write.

`validated` means the object passed these applicable gates and **was successfully written to canonical EKB**. Authorization without write leaves it a candidate pending canonical write. `validated` does not mean absolutely true forever.

## Engagement Memory persistence

Every substantial Engagement requires an explicit canonical Engagement Memory artifact or artifact set in an Engagement-owned, inspectable, controlled, and versioned store.

Git is a preferred implementation where appropriate, not a universal requirement.

A preferred implementation pattern is provided under `templates/`.

## Confidentiality and provenance

Expert Memory must be de-identified without destroying structurally meaningful context.

Names of people, internal document names and financial figures are excluded by default.

Potentially confidential process/case abstractions require the appropriate Engagement-side confidentiality authorization before transfer and ARCHITECT Maintainer authorization for global promotion.

Canonical EKB provenance uses opaque Engagement and Case IDs. Identifiable mappings stay Engagement-side and access-controlled.

## Dual feedback control

### Fast Operational Loop
Improves current Engagement work and may update Engagement Memory.

### Slow Adaptation Loop
Controls changes to the **permanent professional system ARCHITECT**.

Evaluation/regression effort is proportional to expected behavioral impact and failure risk.

The dual-loop model is a logical workflow and does not imply unsupported background autonomy.

## Versioned Professional History contract

The canonical chronological history of permanent ARCHITECT is the Git/version-control history of the canonical ARCHITECT repository. Semantic provenance inside Knowledge Objects, decision records and revision notes explains **why** material changes occurred and complements, but does not replace, Git history.

## Canonical write invariant

No learning or governing change to the permanent professional system ARCHITECT is considered implemented until the relevant canonical store actually reflects the approved state through a verified write path.

If no write path is available, ARCHITECT produces a proposed change set and must not claim permanent memory was updated.

## Runtime deployment, access and isolation contract

The canonical source copy of Project Instructions is not the same thing as the instructions actually deployed in a runtime.

Each runtime must record and, where material, verify:
- ARCHITECT Release ID;
- observable execution-engine/model and material capability profile;
- active Project Instructions ID **and content integrity**;
- governing source-pack revision / Git commit;
- EKB revision;
- governing-source read status;
- EKB read status;
- write capabilities;
- required isolation capabilities and verification state.

A runtime may be `SYNCED`, `OUT_OF_SYNC`, `UNVERIFIED`, or operate in a declared `DEGRADED` state. Project Instructions ID match alone does not establish synchronization.

ARCHITECT must not claim to have read or used canonical EKB/governing material without a verified read path.

For sensitive Engagements, isolation is a **verified capability**, not merely the fact that a different ChatGPT Project or container exists.

See `system/12_RUNTIME_DEPLOYMENT_ACCESS_AND_ISOLATION.md` and `templates/RUNTIME_DEPLOYMENT_RECORD_TEMPLATE.md`.


## Execution profile and baseline

A known-good behavioral baseline is bound to both the permanent ARCHITECT release/configuration and the observable execution profile.

A deliberate model-family/major-engine change requires a new full critical regression run before the new execution profile inherits `KNOWN_GOOD`.

When the provider does not expose an exact backend revision, record that limitation rather than inventing precision.

## Engagement EKB update policy

Substantial Engagements explicitly choose `PINNED`, `CONTROLLED_UPDATE`, or `FLOATING`.

Default for substantial/auditable/sensitive/long-running Engagements is controlled update from an explicit pinned revision.

## Maintenance runtime cleanliness

Canonical promotion, governing changes and baseline work should be performed in a clean HOME/MAINTENANCE runtime separated from unrelated raw Engagement contexts.

## Platform confidentiality boundary

Context isolation does not itself establish organizational/platform approval for confidential data. Where required, data-handling, retention/residency/security and organizational-policy approval are verified separately.


## Behavioral baseline evidence

A `KNOWN_GOOD` baseline is canonical only when its finalized Run Record under `evaluation/runs/` and matching entry in `evaluation/00_BASELINE_REGISTRY.md` share the same Run ID, Finalization Transaction ID and status, and are canonically finalized together.

Where Git is used, both artifacts are committed in the same finalization commit.

The record binds results to the exact ARCHITECT release, PI integrity, governing revision, EKB revision, runtime record and execution profile. Passing tests in chat is not a known-good baseline.

## Repository model

### ARCHITECT repository
Preferred canonical home for:
- Cognitive Core;
- System Protocols;
- EKB;
- evaluation suite;
- reusable templates;
- design history.

### Engagement store
Owned by the Engagement.

May be:
- a separate Git repository;
- another versioned documentation environment;
- a controlled corporate store;
- another inspectable and versioned store.

Raw Engagement Memory must not be stored as canonical Expert Memory.

## Source pack

### Runtime configuration / governance / decision record
- `design/00_ARCHITECTURE_DECISION_RECORD_v0.2.md`
- `core/01_PROJECT_INSTRUCTIONS_v0.2.1_RC5.md`
- `governance/00_ARCHITECT_GOVERNANCE.md`
- `runtime/00_RUNTIME_REGISTRY.md`
- `evaluation/00_BASELINE_REGISTRY.md`

### Governing professional system
- `core/03_COGNITIVE_CORE.md`
- `system/02_SYSTEM_MODEL.md`
- `system/04_TASK_UNDERSTANDING_AND_KNOWLEDGE_NAVIGATION.md`
- `system/05_METHODOLOGY_DESIGN_AND_PROFESSIONAL_JUDGMENT.md`
- `system/06_CONSTRUCTIVE_CRITICISM_VALIDATION_VERIFICATION.md`
- `system/07_LEARNING_AND_ABSTRACTION_PROTOCOL.md`
- `system/08_MEMORY_ARCHITECTURE_AND_PROMOTION.md`
- `system/09_KNOWLEDGE_OBJECT_MODEL.md`
- `system/10_EKB_STRUCTURE_AND_RETRIEVAL.md`
- `system/11_EVALUATION_AND_REGRESSION_SUITE.md`
- `system/12_RUNTIME_DEPLOYMENT_ACCESS_AND_ISOLATION.md`

### Memory
- `memory/expert_memory/00_EKB_INDEX.md`
- `memory/candidates/README.md`

### Engagement implementation templates
- `templates/00_ENGAGEMENT_MANIFEST_TEMPLATE.md`
- `templates/ENGAGEMENT_MEMORY_TEMPLATE.md`
- `templates/RUNTIME_DEPLOYMENT_RECORD_TEMPLATE.md`
- `templates/BASELINE_RUN_RECORD_TEMPLATE.md`

### Historical / non-governing
- `design/00_RECONCILIATION_NOTES.md`
- `design/01_STATIC_CONSISTENCY_REPORT.md`
- `design/02_SURGICAL_CHANGELOG_v0.2.1_RC5.md`

## Release state

This package is a **release candidate**, not yet an operational behavioral baseline. Static consistency can be checked offline; the behavioral regression baseline must be run after the governing pack and Project Instructions are actually deployed in the target runtime.

## Design rule

Add complexity only when it controls a concrete failure mode.

The goal is not maximum architecture. The goal is a stable, inspectable, transferable professional system.
