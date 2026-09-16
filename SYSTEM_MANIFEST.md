# ARCHITECT SYSTEM MANIFEST

```yaml
system_id: architect
name: ARCHITECT
type: CLEAN_ROLE
release: 1.0.0-rc.1
status: PREPARED / VALIDATION_REQUIRED
canonical_repository: Nazgul168/architect

system_traits:
  domains:
    - cross-domain problem solving
    - methodology design
    - systems analysis
    - decision support
    - knowledge architecture
  primary_functions:
    - problem framing
    - knowledge navigation
    - model building
    - methodology synthesis
    - professional judgment
    - critique and validation
    - transferable learning extraction
  decision_types:
    - architecture and design decisions
    - methodology selection and adaptation
    - evidence/authority resolution
    - risk/trade-off decisions
    - knowledge transferability decisions
  cognitive_functions:
    - understand
    - retrieve
    - model
    - synthesize
    - judge
    - critique
    - validate
    - learn
  class_tags:
    - digital-methodologist
    - transferable-professional
    - systems-architect
    - cross-domain

engagement_learning_policy:
  supported: true
  default_for_new_engagements: ENABLED
  user_can_override: true

paths:
  governing_instructions: core/01_PROJECT_INSTRUCTIONS_v1.0.0_RC1.md
  professional_profile: README.md
  cognitive_core: core/03_COGNITIVE_CORE.md
  protocols:
    - system/02_SYSTEM_MODEL.md
    - system/04_TASK_UNDERSTANDING_AND_KNOWLEDGE_NAVIGATION.md
    - system/05_METHODOLOGY_DESIGN_AND_PROFESSIONAL_JUDGMENT.md
    - system/06_CONSTRUCTIVE_CRITICISM_VALIDATION_VERIFICATION.md
    - system/07_LEARNING_AND_ABSTRACTION_PROTOCOL.md
    - system/08_MEMORY_ARCHITECTURE_AND_PROMOTION.md
    - system/09_KNOWLEDGE_OBJECT_MODEL.md
    - system/10_EKB_STRUCTURE_AND_RETRIEVAL.md
    - system/11_EVALUATION_AND_REGRESSION_SUITE.md
    - system/12_RUNTIME_DEPLOYMENT_ACCESS_AND_ISOLATION.md
  expert_memory: memory/expert_memory/
  evaluation_suite: system/11_EVALUATION_AND_REGRESSION_SUITE.md
  system_validation_records: evaluation/system_validation/
  runtime_compatibility_records: runtime/records/

clean_role_update:
  owner_tool: role-updater
  role_updater_contract: role-factory/tool_contracts/ROLE_UPDATER_CONTRACT.md
  auth_role: RF_OWNER
  self_update_allowed: false

release_model:
  versioning: SEMVER
  immutable_self_contained_release: true
  validation_required: true
  validation_waiver: false

runtime_requirements:
  - complete governing-source read path for Slow-Loop operations
  - explicit clean-role release/revision binding
  - Project Instructions content verification for synchronized runtime claims
  - Engagement isolation verification where material
  - no false read/write/sync claims

generation_provenance:
  role_factory_release: "4.5"
  role_factory_revision: UNVERIFIED
  migration_mode: MANUAL_RF45_COMPATIBILITY_MIGRATION
  source_system_release: "ARCH-0.2.1-RC5"
  source_system_revision: "6f843575253c35312d24d03bd6fe9560045b8e95"
  blueprint_versions:
    clean_role_base: "1.5"
    engagement_module: "1.5"
    system_manifest: "1.4"
    evaluation_evidence: "1.2"
    role_update_history: "1.1-static-patch-1"
  schema_version: "1.5"

design_decisions:
  local:
    - decision: Preserve ARCHITECT professional cognition/methodology; migrate only lifecycle, learning, release and RF-integration controls.
      why_local: Does not alter external RF governance and minimizes professional-behavior drift.
    - decision: Keep ARCHITECT Maintainer terminology as a local legacy alias for the same current human RF Owner, without creating separate release authority.
      why_local: Preserves existing terminology while clean-ROLE authority remains governed by RF4-039/040.
  governed:
    - decision: Clean ROLE changes are owned by Role Updater; RF Owner is sole AUTH-ROLE.
      source: RF4-039/040 and ROLE_UPDATER_CONTRACT 0.4
    - decision: Published releases are one immutable self-contained revision.
      source: RF4-041
    - decision: Validation is mandatory with no waiver.
      source: RF4-042
    - decision: Clean ROLE releases use SemVer.
      source: RF4-043
    - decision: Generated-system normative boundary applies.
      source: RF4-045
    - decision: Evaluation is invariant-based and adversarial.
      source: RF4-046
  pending_normative: []
```

## Migration status

This manifest describes a **migration candidate**, not a published/validated clean ROLE release. The previous repository head `6f843575253c35312d24d03bd6fe9560045b8e95` was `ARCH-0.2.1-RC5`, a release candidate whose behavioral baseline had not been established.

The first RF-managed published ARCHITECT release must be created only after required System Validation passes and the RF Owner approves the exact immutable release-candidate subject.
