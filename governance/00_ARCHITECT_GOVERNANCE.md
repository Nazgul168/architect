
# ARCHITECT Governance Registry

Status: RELEASE CANDIDATE  
Release: ARCH-0.2.1-RC5

## Purpose

This file is the canonical governance metadata for authority over the **permanent professional system ARCHITECT**.

It binds Maintainer authority independently of whichever user happens to interact with a runtime.

## Claim-relative authority

This registry is the canonical authority for claims about:
- current ARCHITECT Maintainer ID/status;
- Maintainer succession/revocation/recovery;
- the principal-binding method for Maintainer-only authorization.

It is **not** a behavioral instruction source. Project Instructions and governing Core/Protocols remain authoritative for what the Maintainer may authorize and how ARCHITECT must behave.

If sources conflict:
- Maintainer identity/status claim → this Governance Registry prevails;
- behavioral rule/scope-of-power claim → governing behavior hierarchy prevails.

## Current ARCHITECT Maintainer

ARCHITECT_MAINTAINER_ID: ARCH-MAINT-001  
ROLE: Primary ARCHITECT Maintainer  
STATUS: ACTIVE  
PRINCIPAL_BINDING_METHOD: SINGLE_USER_CONTROLLED_RUNTIME / PLATFORM_IDENTITY / EXTERNAL_AUTHORIZATION  
PRINCIPAL_REFERENCE: Canonical repository owner at initial bootstrap  
CRYPTOGRAPHIC_IDENTITY_VERIFICATION: NOT_PROVIDED_BY_ARCHITECT

### Initial binding

`ARCH-MAINT-001` is the Maintainer designated at the **initial system bootstrap of ARCHITECT** by the owner of the canonical ARCHITECT repository.

A new runtime, Engagement, ChatGPT Project, session, or interacting user does **not** create or replace the ARCHITECT Maintainer.

A runtime must read this canonical binding, or receive an explicitly verified snapshot of it, before relying on Maintainer authority.

Reading the binding proves **who is designated**, not that the current interlocutor is that person/principal.

Before a Maintainer-only action, the runtime must record one of:
- `CURRENT_INTERACTOR_MAINTAINER_STATUS: VERIFIED`;
- `CURRENT_INTERACTOR_MAINTAINER_STATUS: NOT_MAINTAINER`;
- `CURRENT_INTERACTOR_MAINTAINER_STATUS: UNVERIFIED`.

Verification may rely on a platform identity control, a controlled single-user runtime, or an external authorization mechanism. If none is available, Maintainer-only actions are blocked; ARCHITECT may only prepare a proposal/change set.

## Authority scope

The ARCHITECT Maintainer authorizes, where applicable:

- promotion of candidate Knowledge Objects into canonical validated Expert Memory;
- transitions that remove/restrict validated objects from Active Expert Memory;
- permanent governing-system changes;
- evaluation-scope acceptance for permanent ARCHITECT changes;
- release / known-good baseline designation;
- Maintainer succession, revocation, or recovery.

Engagement Owner and Engagement Confidentiality Authority are separate roles and do not inherit this authority.

## Succession / revocation

A Maintainer change must be:

1. explicitly authorized by the current ARCHITECT Maintainer; or
2. if unavailable, performed through a documented recovery action by the canonical repository owner/administrator or another pre-authorized recovery authority.

The change must be versioned in the canonical repository.

No Engagement-side role or current interacting user becomes ARCHITECT Maintainer implicitly.

## Recovery authority

BOOTSTRAP_RECOVERY_AUTHORITY: Canonical ARCHITECT repository owner/administrator  
RECOVERY_STATUS: ACTIVE

Do not store credentials, passwords, tokens, or secrets here.

## Change history

RC4 clarifies claim-relative authority and separates designated Maintainer identity from verification of the current acting principal.
