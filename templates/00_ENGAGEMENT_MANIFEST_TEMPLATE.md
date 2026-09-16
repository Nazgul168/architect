# Engagement Manifest — RF v4.5 Compatible Template

This template instantiates a task-specific ARCHITECT Engagement. The Engagement Manifest is authoritative for the task-specific parent binding and Engagement state.

```yaml
engagement_id: ENG-XXXX
title_or_approved_alias:
status: ACTIVE | PAUSED | CLOSED
canonical_engagement_store:
confidentiality: NORMAL | RESTRICTED | CONFIDENTIAL

parent_role:
  role_id: architect
  core_repo: Nazgul168/architect
  bound_release:                 # exact published SemVer, not a migration candidate
  bound_revision:                # exact immutable published release revision
  update_policy: PINNED | CONTROLLED_UPDATE | FOLLOW_LATEST
  update_authority_ref: RF_OWNER_CURRENT_HUMAN

parent_role_update_authority:
  type: USER
  identity_ref: RF_OWNER_CURRENT_HUMAN

resolved_role_learning:
  enabled: true | false
  resolved_by: RF_OWNER_CURRENT_HUMAN
  resolved_at:

runtime_binding:
  runtime_id:
  execution_profile_id:
  project_instructions_id:
  project_instructions_verification: HASH_VERIFIED | FULL_TEXT_VERIFIED | UNVERIFIED
  runtime_sync_status: VERIFIED | PENDING | FAILED | UNKNOWN
  synced_parent_revision:

canonical_paths:
  engagement_memory:
  learning_candidates:
  role_performance_log:
  role_change_log:
  runtime_record:
```

## Purpose

## Scope

### In scope

### Out of scope

## Source authority hierarchy

Define claim-specific authority where material. If not otherwise defined, prefer authoritative current Engagement sources → accepted Engagement Memory → verified supporting evidence → validated Expert Memory → Working hypotheses.

Conflicting authoritative sources with overlapping scope are surfaced and resolved by scope/precedence/effective date/system-of-record status or escalated.

## Learning

Clean ARCHITECT policy supports Engagement learning and defaults new Engagements to enabled, with user override allowed.

If `resolved_role_learning.enabled: true`, maintain:
- Learning Candidates using the RF lifecycle;
- ROLE Performance Log;
- ROLE Change Log.

ARCHITECT may recommend candidates for review but may not self-assign `APPROVED_FOR_ROLE_REVIEW`.

## Parent update boundary

A parent update may change only the parent binding and, where required by deployment, materialized portable clean-ROLE copies.

It must not modify Engagement Memory, sources, outputs, learning/feedback records, update policy or update authority.

For `CONTROLLED_UPDATE`, adoption requires approval by the recorded authority. In the current single-user deployment that authority must be the current human owner; another identity → `BLOCKED`.

Canonical parent binding update and runtime synchronization are separate.

## Confidentiality / transfer

De-identify transferable learning. Raw evidence and identifiable provenance mapping remain Engagement-side.

Potentially confidential process/case transfer requires applicable Engagement-side permission before export to Role Updater.
