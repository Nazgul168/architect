# ARCHITECT → RF v4.5 Migration Changeset

Source repository: `Nazgul168/architect`
Verified supplied local source head: `6f843575253c35312d24d03bd6fe9560045b8e95` (`ARCH-0.2.1-RC5`).
Proposed first RF-managed release: `1.0.0` (candidate remains unpublished until validation + approval).

## Status

- PREPARED / STATICALLY CONSISTENT
- NOT SYSTEM-VALIDATED
- NOT PUBLISHED
- NOT KNOWN-GOOD
- Do not register as ACTIVE in ROLE_CATALOG yet.

## ADD
- `ROLE_UPDATE_HISTORY.md`
- `SYSTEM_MANIFEST.md`
- `core/01_PROJECT_INSTRUCTIONS_v1.0.0.md`
- `design/03_RF45_MIGRATION_DECISION_RECORD.md`
- `evaluation/system_validation/README.md`
- `templates/SYSTEM_VALIDATION_RECORD_TEMPLATE.md`

## REPLACE
- `FILE_MANIFEST.md`
- `README.md`
- `core/03_COGNITIVE_CORE.md`
- `evaluation/00_BASELINE_REGISTRY.md`
- `governance/00_ARCHITECT_GOVERNANCE.md`
- `memory/candidates/README.md`
- `memory/expert_memory/00_EKB_INDEX.md`
- `runtime/00_RUNTIME_REGISTRY.md`
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
- `templates/00_ENGAGEMENT_MANIFEST_TEMPLATE.md`
- `templates/BASELINE_RUN_RECORD_TEMPLATE.md`
- `templates/RUNTIME_DEPLOYMENT_RECORD_TEMPLATE.md`

## DELETE / RENAME
- `core/01_PROJECT_INSTRUCTIONS_v0.2.1_RC5.md`

## Key migration controls

- Live learning candidates are Engagement-side; clean `memory/candidates/` is reference-only.
- `APPROVED_FOR_ROLE_REVIEW` is review permission, not promotion.
- Clean ROLE updates, including EKB changes, go through Role Updater.
- Current human RF Owner is sole clean-ROLE AUTH-ROLE; `ARCH-MAINT-001` is only a local legacy alias for the same human owner.
- Clean releases: SemVer, mandatory System Validation, one immutable self-contained release revision, no waiver.
- Task-specific ARCHITECT binds the whole clean ROLE release/revision; EKB does not float independently.
- Portable System Validation is separated from runtime compatibility/baseline evidence.
- RF4-045 normative boundary is incorporated.

## Preserved professional behavior

- Cognitive Core is substantively unchanged.
- Task framing / knowledge navigation / methodology design / professional judgment protocols are preserved except release metadata and RF-boundary alignment.
- Historical design files are retained unchanged and remain non-governing.

## Deployment rule

Apply this changeset on a dedicated migration branch, not directly as a published release. Do not merge/tag/publish final `1.0.0` until Role Updater is usable, the required System Validation has executed with all applicable critical tests PASS, and the RF Owner explicitly approves the immutable release candidate.

The next phase is the actual task-specific ARCHITECT Engagement migration. It should bind to the first published clean ARCHITECT release, only after `1.0.0` is actually validated, approved and published.
