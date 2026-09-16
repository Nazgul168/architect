# ARCHITECT

Canonical clean-ROLE migration candidate: **1.0.0-rc.1**  
Status: **PREPARED / VALIDATION REQUIRED — NOT PUBLISHED, NOT KNOWN-GOOD**  
Source lineage: `ARCH-0.2.1-RC5` at `6f843575253c35312d24d03bd6fe9560045b8e95`

## Purpose

ARCHITECT is a **Persistent Digital Professional / Digital Methodologist**: a transferable professional expert whose cognitive identity and accumulated professional capital persist while domains, organizations, Engagements, runtime containers and source materials may change.

Its core work is:

**understand the real problem → navigate relevant knowledge → build an adequate model → synthesize a solution or methodology → exercise professional judgment → critically validate the result → extract transferable learning.**

## RF v4.5 management model

ARCHITECT is now packaged as an RF-managed **clean ROLE**.

```text
clean ARCHITECT release
        +
Engagement repository/state
        =
task-specific ARCHITECT
```

The clean repository contains only transferable professional components. It does not own raw Engagement truth or enumerate dependent Engagements.

Clean ARCHITECT evolution is controlled by the **Role Updater TOOL**. ARCHITECT may learn and recommend changes, but it cannot self-promote learning or directly release a modified clean ROLE.

The current deployment is single-user: the current human RF Owner is the sole clean-ROLE `AUTH-ROLE`. Legacy `ARCH-MAINT-001` terminology is retained only as an ARCHITECT-local alias for that same current owner.

## Learning flow

For Engagements with learning enabled:

```text
Engagement work
→ Engagement Memory
→ Learning Candidate
→ RECOMMENDED_FOR_ROLE_REVIEW
→ explicit human APPROVED_FOR_ROLE_REVIEW
→ Role Learning Export
→ Role Updater evaluation
→ ROLE_CHANGE_PROPOSAL / NO_ROLE_CHANGE / REQUEST_MORE_EVIDENCE
→ human approval
→ candidate change
→ System Validation
→ release-candidate approval
→ immutable clean ARCHITECT release
```

`APPROVED_FOR_ROLE_REVIEW` is permission to evaluate, not automatic promotion.

Live learning candidates belong in the Engagement-owned store. The clean repository's `memory/candidates/` directory is retained only as a schema/reference marker and must not become a hidden cross-Engagement candidate database.

## Expert Memory

Expert Memory is ARCHITECT's transferable professional memory. The EKB under `memory/expert_memory/` is its canonical physical representation within the clean ROLE.

A Knowledge Object is `validated` only when its epistemic/privacy requirements are satisfied and it is included in a successfully validated, explicitly approved, canonically published clean ARCHITECT release.

## Source-of-truth model

For clean ARCHITECT content and releases:

1. canonical `Nazgul168/architect` repository;
2. `SYSTEM_MANIFEST.md`;
3. the single immutable published release revision;
4. `ROLE_UPDATE_HISTORY.md` and release validation provenance.

A runtime Project/Chat is an execution environment, not the source of permanence.

For a task-specific ARCHITECT, the Engagement repository and Engagement Manifest are authoritative for parent binding and Engagement state.

## Governing source hierarchy

For ARCHITECT behavior:

1. deployed Project Instructions;
2. Cognitive Core + governing System Protocols;
3. validated Expert Memory;
4. Working State.

Design/history documents and learning candidates are non-governing.

If an accepted governing change affects Project Instructions, the runtime is not synchronized until the deployed Project Instructions are updated and verified.

## Evaluation model

ARCHITECT separates:

- **System Validation** — portable clean-ROLE behavior against the canonical suite;
- **Runtime Compatibility / behavioral baseline** — whether a specific execution profile reliably runs that release.

A canonical clean-ROLE release requires executed System Validation with every applicable critical gate PASS. There is no validation waiver.

A runtime may only inherit/claim a known-good baseline when its own runtime/deployment evidence satisfies the runtime protocol.

## Runtime binding

Substantial task-specific Engagements bind to an exact published ARCHITECT release and revision. The parent update policy is one of:

- `PINNED`;
- `CONTROLLED_UPDATE` (recommended/default for substantial Engagements);
- `FOLLOW_LATEST`.

Expert Memory is part of the bound clean ROLE release; it does not float independently from the governing clean ROLE binding.

Canonical parent-binding update and ChatGPT/runtime synchronization are separate states.

## Repository structure

- `SYSTEM_MANIFEST.md` — RF-compatible clean ROLE identity and metadata.
- `ROLE_UPDATE_HISTORY.md` — RF-managed published release history.
- `core/` — Project Instructions and Cognitive Core.
- `system/` — governing professional protocols.
- `memory/expert_memory/` — canonical transferable Expert Memory.
- `evaluation/system_validation/` — portable System Validation records.
- `evaluation/runs/` — runtime behavioral/baseline evidence.
- `runtime/` — runtime registry/records.
- `templates/` — reusable Engagement/runtime/evaluation templates.
- `design/` — historical/non-governing design records.

## Migration status

`1.0.0-rc.1` is a prepared migration candidate. It must not be registered as an ACTIVE reusable clean ROLE in the Role Catalog until the first RF-managed release is actually validated, approved and published.

The legacy `ARCH-0.2.1-RC5` line remains historical provenance and is not retroactively declared a validated RF release.
