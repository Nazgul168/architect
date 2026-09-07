# ARCHITECT Architecture Decision Record — v0.2

Status: ACCEPTED / IMPLEMENTED / NON-GOVERNING DECISION RECORD
Decision Set Version: 0.2
Current Release: ARCH-0.2.1-RC5
Date: 2026-09-04

This document records architecture decisions accepted for the v0.2 line and their rationale.

It is **not itself a runtime governing source** after implementation. Runtime authority resides in Project Instructions, Cognitive Core, and governing System Protocols. If this record conflicts with an implemented governing source, surface the drift; do not silently treat this historical decision record as an executable instruction.

---

## DEC-A — Permanent ARCHITECT vs Engagement Runtime

**Decision**

ARCHITECT is the permanent professional system.

An **Engagement** is a real-world assignment, initiative, client project, or problem context handled by ARCHITECT.

The persistent identity and professional biography of ARCHITECT are carried by its:
- Cognitive Core;
- governing System Protocols;
- Expert Memory / EKB;
- evaluation architecture;
- versioned professional history.

They are **not** carried by the chat history of one ChatGPT Project.

A ChatGPT Project named `ARCHITECT` may serve as the home, development, maintenance, or general interaction workspace for ARCHITECT.

An Engagement may be executed in that workspace when cross-engagement context leakage is immaterial.

A substantial, sensitive, confidential, or context-heavy Engagement should use an **isolated runtime context** when cross-engagement leakage would be material. This may be a separate ChatGPT Project or another suitably isolated environment.

The same ARCHITECT professional system may be reused across isolated Engagement runtimes.

**Invariant**

> ARCHITECT is permanent; individual Engagement context is not.

---

## DEC-B — Persistence and Authority Are Independent

**Decision**

Scope/persistence and authority are independent dimensions of knowledge.

**Scope / persistence** determines:
- where knowledge belongs;
- how long it should persist;
- whether it is engagement-specific or transferable.

**Authority** determines:
- which source should prevail for the particular claim, decision, or question being resolved.

Authority must be evaluated **relative to the claim and scope concerned**.

Permanent or transferable knowledge is not automatically more authoritative than Engagement-specific knowledge.

An authoritative Engagement source may override a generic Expert Memory heuristic within the scope for which that source is authoritative.

---

## DEC-C — Epistemic Validation + Maintainer Authorization

**Decision**

ARCHITECT may autonomously:
- extract learning;
- perform abstraction;
- assess transferability;
- perform epistemic learning validation;
- create `candidate` Knowledge Objects.

Promotion of a candidate into canonical `validated` Expert Memory requires **both**:

1. satisfaction of the applicable epistemic criteria, including evidence quality, abstraction quality, transferability, applicability, limitations, counterexamples where relevant, and confidence;
2. explicit authorization by the ARCHITECT Maintainer.

ARCHITECT Maintainer approval is a **governance authorization**, not evidence by itself.

The status `validated` means:

> the Knowledge Object has satisfied the applicable epistemic criteria, has received ARCHITECT Maintainer authorization for canonical Expert Memory, **and the canonical EKB write has succeeded**.

After authorization but before canonical write, the object remains a `candidate` in a promotion-authorized/pending-write state.

It does **not** mean:
- absolutely true;
- universally applicable;
- permanently beyond revision.

A validated object may later become `contested`, `deprecated`, or `superseded` when new evidence justifies it, subject to the applicable governance process.

**Governance clarification:** the **ARCHITECT Maintainer** governs changes to the permanent professional system. An Engagement Owner / Engagement Confidentiality Authority does not automatically have authority to modify global ARCHITECT Expert Memory or governing behavior.

Any change to permanent governing behavior — Project Instructions, Cognitive Core, governing System Protocols, or evaluation/control mechanisms — requires explicit ARCHITECT Maintainer authorization after applicable evaluation and before canonical write/deployment.

The ARCHITECT Maintainer role is itself governed: succession/revocation must be explicit and versioned; Engagement-side authority does not inherit global Maintainer authority automatically.

---

## DEC-D — Explicit Isolated Canonical Engagement Memory

**Decision**

Every substantial Engagement must maintain an explicit canonical **Engagement Memory artifact or artifact set** in an Engagement-owned, inspectable, controlled, and versioned store.

The canonical Engagement Memory store must be logically or physically separated from ARCHITECT Expert Memory.

Where Git is available and appropriate, a separate Engagement Git repository is the **preferred implementation**, not a universal architectural requirement.

Raw Engagement Memory must not be stored in the ARCHITECT Expert Memory repository.

A common preferred organization is:

```text
Manifest
Canonical Engagement Memory
Context
Working
Outputs
```

This structure is a reusable implementation model, not a mandatory universal structure for every Engagement.

---

## DEC-E — Dual Feedback Control + Proportional Regression

**Decision**

ARCHITECT uses two logically distinct feedback loops.

### Fast Operational Loop

The Fast Loop improves work inside the current Engagement.

It may:
- update Working State;
- update Engagement Memory;
- refine the current solution;
- use task feedback to improve subsequent work in the same Engagement.

It does **not** automatically modify the permanent professional system ARCHITECT.

### Slow Adaptation Loop

The Slow Loop governs proposed changes to the **permanent professional system ARCHITECT**, including where applicable:
- canonical Expert Memory / EKB;
- reusable Methods;
- Cognitive Core;
- governing System Protocols;
- Project Instructions;
- evaluation/control mechanisms.

Changes to the permanent professional system require evaluation and regression control **proportional to their expected behavioral impact and failure risk**.

Examples:
- new Case Abstraction → lightweight or targeted evaluation;
- new Heuristic → affected scenarios and critical tests where relevant;
- Method revision → broader regression over affected behavior;
- Cognitive Core or Project Instructions change → full critical regression set.

The dual-loop model is a **logical architecture/workflow**. It does not imply invisible or autonomous background execution where no such capability exists.

A change to the permanent professional system is considered implemented only when the relevant canonical store has actually been updated through a verified write path.

Material regression must support rollback to the last known good state.

**Clarification**

Ordinary persistence of Engagement Memory inside an Engagement is **not** a Slow Loop change merely because the Engagement Memory survives across tasks.

---

## DEC-F — De-identification Without Destroying Useful Context

**Decision**

Expert Memory must exclude or de-identify Engagement-specific sensitive and identifying information while preserving the **non-sensitive structural context** required for:
- future recognition;
- applicability assessment;
- professional reasoning;
- retrieval.

Exclude by default:
- names of people;
- internal document names;
- financial figures.

For process descriptions, case structures, or operational mechanisms whose confidentiality is uncertain, ARCHITECT obtains the appropriate Engagement-side confidentiality authorization before transfer and ARCHITECT Maintainer authorization before global promotion.

Canonical EKB provenance uses opaque Engagement and Case IDs.

Any mapping from opaque IDs back to identifiable Engagement evidence remains Engagement-side and access-controlled.

De-identification must not make Expert Memory so context-poor that Recognition Cues or applicability conditions are lost.

---

## DEC-G — Governing Source Hierarchy & Synchronization

**Decision**

ARCHITECT maintains an explicit governing-source hierarchy.

### Governing sources

1. **Project Instructions** — executable runtime constitution.
2. **Cognitive Core + governing System Protocols** — detailed normative specification.
3. **Expert Memory** — learned professional knowledge that informs reasoning but cannot override governing instructions or protocols.

### Non-governing sources

- design/history documents;
- candidate knowledge;
- Working State.

If an accepted change to Cognitive Core or a governing System Protocol materially changes behavior represented in Project Instructions, that change is **not fully implemented until Project Instructions are synchronized**.

Known conflicts between governing layers must be surfaced and resolved, never silently blended.

---

# Operational Invariant — Canonical Write Requirement

This is not a separate DEC, but is mandatory.

> No learning or governing change to the permanent professional system ARCHITECT is considered implemented until the relevant canonical store reflects the approved state.

A model statement such as:
- "I remembered this";
- "I updated my memory";
- "this is now part of EKB";

is insufficient.

If no verified write path is available, ARCHITECT must:
- produce a proposed patch, candidate Knowledge Object, or explicit change set for the ARCHITECT Maintainer;
- state that canonical persistence has **not** occurred;
- not claim that permanent ARCHITECT has been updated.

This invariant does not apply to ordinary Engagement Memory updates when their own Engagement-side canonical store has been successfully updated.

---

# Post-Audit Operational Clarifications

These controls refine implementation of DEC-A, DEC-C, DEC-E and DEC-G without redesigning the architecture.

1. **Runtime deployment contract.** The canonical Git/source copy of Project Instructions and the instructions actually deployed into a runtime are distinct states. Each runtime records the expected ARCHITECT release, Project Instructions ID, governing-pack revision, EKB revision, deployment status and synchronization state.
2. **Read-path truth.** ARCHITECT must not claim that EKB, governing sources, or Engagement Memory were read/used unless a verified read path is available and the relevant source/revision is accessible. If EKB access is unavailable, the runtime operates in a declared degraded professional-memory state rather than pretending to have current Expert Memory.
3. **Isolation is capability-based.** A different runtime/container is not considered isolated merely by name. The required isolation capabilities must be verified for the Engagement and recorded.
4. **Authoritative-source conflicts.** Conflicting authoritative Engagement sources with overlapping authority must be surfaced and resolved through scope, precedence, effective date, governing hierarchy, or the appropriate Engagement authority; they must never be silently blended.
5. **Approval with revision.** A material ARCHITECT Maintainer revision returns the candidate to the affected epistemic/privacy/regression stages before final authorization and write.
6. **Critical regression gate.** Every CRITICAL test in the applicable regression set must PASS. CRITICAL PARTIAL blocks promotion exactly as CRITICAL FAIL does.

# Decision Set Integrity

The seven decisions form one governance model:

```text
DEC-A  defines what is permanent and what may require runtime isolation
DEC-B  separates persistence from authority
DEC-C  separates epistemic validation from governance authorization
DEC-D  defines canonical Engagement-side persistence
DEC-E  controls adaptation of the permanent professional system
DEC-F  controls safe transfer across Engagement boundaries
DEC-G  controls governing-source authority and synchronization
```

The operational invariant closes the gap between an approved conceptual change and an actually implemented canonical change.
