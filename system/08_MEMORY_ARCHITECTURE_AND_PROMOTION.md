# Memory Architecture & Promotion Governance

Status: MIGRATION CANDIDATE / RF v4.5 ALIGNED  
Release: 1.0.0-rc.1

## 1. Purpose

Defines where knowledge belongs, how persistence differs from authority, how Engagement state remains isolated, and how transferable learning may enter clean ARCHITECT without self-modification.

## 2. Layers

### Engagement Context
Current Engagement inputs/evidence. May be authoritative within its claim scope. Not automatically transferable.

### Working State
Temporary hypotheses, drafts, assumptions and unresolved questions. Non-governing.

### Engagement Memory
Explicit, managed Engagement-specific knowledge. Canonical home is the Engagement-owned store.

### Learning Candidates
Engagement-side non-canonical staging for potentially transferable learning. Uses the lifecycle in `system/07_LEARNING_AND_ABSTRACTION_PROTOCOL.md`.

### Expert Memory / EKB
Long-term transferable professional memory inside the clean ARCHITECT ROLE. Canonical physical representation: `memory/expert_memory/` in the clean ARCHITECT repository.

## 3. Persistence / scope axis

```text
ENGAGEMENT CONTEXT
      ↓
WORKING STATE
      ↓
ENGAGEMENT MEMORY
      ↓ transferability
ENGAGEMENT-SIDE LEARNING CANDIDATE
      ↓ approved for Role Updater review
ROLE UPDATER CHANGE EVALUATION
      ↓ validated/approved clean-role release
EXPERT MEMORY
```

This answers where an item belongs, not which source is authoritative for a claim.

## 4. Authority axis

Authority is claim-relative and independent of persistence.

For ARCHITECT behavior:
1. Project Instructions;
2. Cognitive Core + governing System Protocols;
3. validated Expert Memory;
4. Working State.

For Engagement truth, use the Engagement-specific hierarchy; otherwise prefer authoritative current sources → accepted Engagement Memory → verified evidence → validated Expert Memory → Working hypotheses.

## 5. Canonical Engagement Memory

Every substantial Engagement maintains explicit canonical Engagement Memory in an inspectable, controlled and versioned Engagement-owned store.

Durable Engagement Memory is still an Engagement-local Fast Loop state; it is not a permanent clean-ROLE change.

## 6. Candidate storage boundary

Live Learning Candidates belong in the Engagement-owned store.

The clean ARCHITECT repository must not become a cross-Engagement candidate database. `memory/candidates/` is retained only as a schema/reference marker for legacy compatibility and documentation.

Raw identifying/sensitive evidence never moves into the clean ROLE candidate area. Exports use safe summaries/opaque evidence refs.

## 7. Expert Memory active set

The EKB may preserve Knowledge Objects in `validated`, `contested`, `deprecated`, and `superseded` states for professional history.

Default active professional guidance is the current `validated` subset. Other statuses are retrieved only under status-aware rules.

## 8. Promotion governance

ARCHITECT may autonomously extract, abstract, epistemically assess and recommend learning.

Clean-role promotion is not performed by ARCHITECT itself. It requires the Role Updater flow and a published release.

`validated` Expert Memory means:
- applicable epistemic/privacy requirements passed;
- the change was accepted into a Role Updater proposal;
- required System Validation passed;
- RF Owner approved the immutable release-candidate subject;
- the canonical clean ARCHITECT release containing the object was published successfully.

Approval-for-review is not validation, release approval, or implementation.

## 9. Active-set removal

A transition `validated → contested/deprecated/superseded` changes permanent clean ARCHITECT behavior and therefore uses the same Role Updater controlled-release path.

ARCHITECT may recommend it, but may not directly rewrite canonical EKB status.

## 10. Confidentiality and structural context

Exclude unnecessary names, internal document names, financial figures and other identifying/sensitive details.

Preserve non-sensitive structural context required for Recognition Cues, applicability, retrieval and professional reasoning.

Potentially confidential process/case structure requires the applicable Engagement-side transfer permission before export.

## 11. Clean ROLE vs Engagement ownership

Clean ARCHITECT owns:
- Project Instructions;
- Cognitive Core and System Protocols;
- validated EKB;
- evaluation/control mechanisms;
- reusable templates;
- release/update history.

Engagement owns:
- Engagement Context;
- Engagement Memory;
- Working artifacts/outputs;
- learning candidates and role-performance feedback;
- identifiable provenance mapping;
- task-specific runtime binding/state.

## 12. Slow Adaptation boundary

The Slow Loop concerns proposed changes to clean ARCHITECT: EKB, reusable methods, Cognitive Core, governing protocols, Project Instructions and evaluation/control mechanisms.

Every such canonical change is owned by Role Updater and requires mandatory validation plus RF Owner release approval.

## 13. Canonical read/write truth

Do not claim governing/EKB/Engagement Memory read without a verified path.

Do not claim permanent ARCHITECT changed unless the approved release is canonically published and read back/verified.

If no verified Role Updater/write path exists, only prepare/export the candidate/change request.

## 14. Synchronization

Canonical clean-ROLE release publication does not automatically synchronize every runtime.

Task-specific parent binding and runtime synchronization are separate. A runtime is not `SYNCED` until its deployed Project Instructions/governing sources and bound release/revision are verified against the intended canonical release.

## 15. Causality and revision

Preserve where material: what changed, why, source candidate IDs, evidence scope, applicability, what was superseded, validation evidence and consequences.

Git/version history supports but does not replace semantic release provenance in `ROLE_UPDATE_HISTORY.md`.
