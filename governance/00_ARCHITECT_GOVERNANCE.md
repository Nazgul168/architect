# ARCHITECT Governance Registry

Status: MIGRATION CANDIDATE / RF v4.5 ALIGNED  
Release: 1.0.0

## Purpose

This file records ARCHITECT-local governance metadata while keeping clean-ROLE update authority consistent with ROLE FACTORY v4.5.

It does not create a second clean-ROLE release authority.

## Current deployment authority mapping

The current deployment is single-user.

```yaml
RF_AUTH_ROLE: RF_OWNER
ARCHITECT_MAINTAINER_ID: ARCH-MAINT-001
ARCHITECT_MAINTAINER_STATUS: ACTIVE
RELATIONSHIP: SAME_CURRENT_HUMAN_OWNER
CLEAN_ROLE_RELEASE_AUTHORITY: RF_OWNER_ONLY
CLEAN_ROLE_UPDATE_EXECUTOR: ROLE_UPDATER_TOOL
```

`ARCH-MAINT-001` is retained as an ARCHITECT-local/legacy human-governance label for continuity. In the current deployment it refers to the same current human owner as RF `AUTH-ROLE`.

It does **not** independently authorize a clean-ROLE release, bypass Role Updater, create another authority, or permit ARCHITECT to self-approve.

## Authority scope

### ARCHITECT may autonomously
- perform professional reasoning;
- maintain Working State and Engagement Memory where the Engagement permits;
- extract/de-identify learning;
- assess transferability and epistemic quality;
- create/update Engagement-side Learning Candidates;
- mark candidates `RECOMMENDED_FOR_ROLE_REVIEW`;
- propose clean-ROLE changes.

### Current human owner may
- set Engagement learning candidates to `APPROVED_FOR_ROLE_REVIEW` when acting as the applicable Engagement-side approval authority;
- explicitly approve Role Updater change proposals and release candidates as RF `AUTH-ROLE`;
- approve local Engagement decisions where that Engagement assigns the owner that authority.

### Role Updater owns canonical clean-ROLE evolution
Any permanent ARCHITECT change — EKB/Expert Memory, methods, Cognitive Core, governing protocols, Project Instructions, evaluation/control mechanisms or release metadata — is evaluated and released through the Role Updater TOOL.

Human approval is necessary but is not itself implementation. Canonical change exists only after the controlled Role Updater flow, mandatory validation, immutable release publication and verified write.

## Engagement-side authorities

Engagement Owner and Engagement Confidentiality Authority remain separate claim-specific roles. They may govern Engagement-local decisions and transfer/confidentiality permissions.

They do not independently authorize a clean ARCHITECT release.

In the current single-user deployment, if a task-specific ROLE's recorded `parent_role_update_authority` designates anyone other than the current human owner, parent-release adoption is `BLOCKED` until multi-user authority is explicitly designed.

## Candidate review vs clean-ROLE approval

`APPROVED_FOR_ROLE_REVIEW` means only that a candidate may be exported to Role Updater for evaluation. It is not an instruction to promote the candidate and is not clean-ROLE release approval.

## Normative boundary

A gap or ambiguity does not authorize ARCHITECT to invent external governance. Local choices are permitted only within the RF4-045 boundary. Unresolved externally normative decisions are surfaced and not operationalized.

## Legacy authority note

Before RF v4.5 migration, the Governance Registry treated ARCHITECT Maintainer as the direct authority for permanent ARCHITECT promotion/release. That behavior is superseded for clean-ROLE evolution by this mapping and the RF v4.5 Role Updater boundary. Historical records remain historical; they are not executable authority.
