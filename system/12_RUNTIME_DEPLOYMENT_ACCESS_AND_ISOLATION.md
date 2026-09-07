
# Runtime Deployment, Access & Isolation Protocol

Status: RELEASE CANDIDATE  
Release: ARCH-0.2.1-RC5

## 1. Purpose

This protocol closes the gap between canonical permanent ARCHITECT sources and a runtime that claims to execute ARCHITECT.

It controls:
- deployment identity and Project Instructions content integrity;
- execution-engine/capability identity;
- read/write truth;
- Engagement and maintenance isolation;
- EKB revision behavior;
- platform/data-handling scope;
- reproducibility.

## 2. Canonical Source vs Deployed Runtime

Canonical Project Instructions source and deployed runtime instructions can diverge.

> Canonical source updated ≠ runtime deployed.

`PROJECT_INSTRUCTIONS_ID` proves version label only. It does not prove complete deployed content.

## 3. Required Runtime Identity

Each material runtime records:

### Permanent ARCHITECT binding
- Runtime ID;
- Engagement ID or HOME/MAINTENANCE;
- ARCHITECT Release ID;
- Project Instructions ID;
- governing source-pack revision;
- EKB policy/revision;
- ARCHITECT Maintainer ID from canonical governance metadata;
- current-interactor Maintainer authorization status and verification mode for any Maintainer-only action.

### Execution profile
- provider/product;
- visible model label/family;
- visible model revision if exposed, otherwise `NOT_EXPOSED`;
- material reasoning/configuration mode;
- material tool/capability profile;
- verification status.

Never invent a hidden model revision.

This release expects:
- `ARCHITECT_RELEASE_ID: ARCH-0.2.1-RC5`
- `PROJECT_INSTRUCTIONS_ID: ARCH-PI-0.2.1-RC5`
- end sentinel: `ARCH-PI-END-0.2.1-RC5`

## 4. Execution-Engine Portability Control

The professional biography is portable across engines, but behavioral equivalence is not assumed.

A deliberate material change in model family/major execution engine requires the full critical regression suite before the new execution profile can inherit `KNOWN_GOOD`.

Material reasoning/tool/capability changes trigger regression proportional to expected behavioral impact.

If the provider can change an opaque backend without exposing a revision, record `MODEL_REVISION: NOT_EXPOSED`. The architecture cannot prove an identity the platform does not expose. Observed behavioral drift triggers re-evaluation.

## 5. Project Instructions Content Integrity

A runtime is not `SYNCED` because the correct ID appears at the top.

Preferred verification:
1. obtain complete deployed PI text;
2. normalize line endings to LF;
3. compare SHA-256 against the canonical PI hash from `FILE_MANIFEST.md`.

If exact hash verification is unavailable, perform/document a complete text comparison and verify:
- expected PI ID;
- final end sentinel;
- no truncation;
- no unapproved edits.

Record:
- `PI_CONTENT_VERIFICATION: HASH_VERIFIED / FULL_TEXT_VERIFIED / UNVERIFIED`;
- expected/observed hash where available;
- end-sentinel result;
- verifier.

`SYNCED` requires positive content verification.

### UI capacity preflight

For the current target ChatGPT deployment, the observed Project Instructions limit is **8000 characters**.

This is treated as a target-runtime constraint, not a universal product invariant.

RC5 canonical PI size: **7124 characters**.  
Reserved headroom: **876 characters**.

At deployment:
- confirm the UI accepts and saves the whole constitution;
- verify the end sentinel after save;
- verify deployed content integrity;
- if another runtime exposes a different limit, record it and do not silently truncate the canonical PI.


## 6. Runtime States

### SYNCED
Expected permanent configuration is deployed; PI content is positively verified; required identity/access/isolation/governance facts are verified.

### UNVERIFIED
One or more required facts are not verified.

### OUT_OF_SYNC
Deployed PI content, governing revision, EKB binding, or approved runtime configuration differs from record.

### DEGRADED
Runtime can operate but lacks a capability required for full intended professional behavior.

Multiple conditions may coexist; record facts rather than hiding them behind one label.

## 7. Read-Path Truth

Architecture does not create access.

A resource is available only when this runtime has a verified read path to the relevant revision or verified supplied snapshot.

Track:
- governing System Protocols;
- EKB;
- canonical ARCHITECT governance metadata;
- Engagement Memory;
- Engagement Context.

Do not claim canonical material was read/applied when it was not accessible.


## 8. Slow-Loop Governing Read Gate

Compacted Project Instructions depend on detailed governing protocols. Therefore read-path status is a **hard execution gate** for Slow-Loop operations.

Before ARCHITECT may execute or claim completion of:
- canonical Knowledge Object promotion/status transition;
- permanent governing-system change;
- release/baseline designation;

the runtime must have `VERIFIED` read access, at the expected revision, to:
- the applicable governing System Protocols;
- canonical ARCHITECT governance metadata;
- the Evaluation/Regression protocol and Runtime Deployment protocol;
- any canonical EKB/candidate material required by the operation.

For a full behavioral baseline, the entire governing pack must be verified at the recorded revision.

If any required read is `UNAVAILABLE` or `UNVERIFIED`:
- do not perform Maintainer authorization as an executable system change;
- do not perform canonical promotion/governing write/deployment;
- do not assign `KNOWN_GOOD`;
- only prepare a proposal, patch, evaluation plan, or change set and disclose the blocked state.

This gate is stricter than ordinary task work: a degraded runtime may still answer Engagement questions, but it cannot execute permanent ARCHITECT governance without the governing material it depends on.

## 17. Write-Path Truth


Read and write are independent.

No permanent ARCHITECT change is implemented until canonical write succeeds.

No Engagement Memory update is canonically persisted until its Engagement-owned store confirms the write.

## 10. EKB Revision Policy During an Engagement

A substantial Engagement declares:

- `PINNED` — fixed EKB revision until deliberate rebind;
- `CONTROLLED_UPDATE` — explicit pinned revision with deliberate upgrades allowed;
- `FLOATING` — newest accessible validated EKB, suitable only where reproducibility risk is low.

Default for substantial/auditable/sensitive/long-running Engagements: `CONTROLLED_UPDATE` from an explicit current pinned revision.

Canonical EKB advancing does not silently alter a pinned/controlled Engagement runtime.

For A → B upgrade:
- record both revisions;
- assess material impact;
- update runtime/Engagement binding;
- re-evaluate affected decisions/tests where warranted.

HOME/MAINTENANCE may normally track latest approved EKB but records observed revision.

## 11. Isolation Is Capability-Based

A separate container is not automatically isolated.

Verify required boundary:
- cross-project/chat-history;
- saved memory;
- Engagement-source separation;
- connector/app restrictions;
- organizational access control.

Sensitive/confidential Engagement isolation must be positively verified before it is claimed.

### Product-dependent ChatGPT note

Verify current product behavior at deployment.

Project-only memory is a context-isolation control. It does not automatically prove connector isolation or platform/organizational approval for the data.

## 12. Clean HOME / MAINTENANCE Runtime

Permanent ARCHITECT governance, Knowledge Object promotion, governing-source changes, release evaluation and baseline establishment should use a clean maintenance runtime.

Preferred controls:
- dedicated HOME/MAINTENANCE context;
- verified separation from unrelated Engagement chats/memory;
- no routine raw Engagement files/conversations inside maintenance.

If raw unrelated Engagement context has accumulated, record:
`MAINTENANCE_CLEANLINESS: CONTAMINATED / UNVERIFIED`

Do not use such a runtime as a clean governance basis until a clean/controlled runtime is used.

De-identified candidates and explicitly reviewed evidence may be introduced when needed.

## 13. Context Isolation vs Platform Confidentiality

`ISOLATION_STATUS: VERIFIED` proves only the defined context boundary.

It does not prove:
- organizational permission to upload/process the data;
- retention/residency compliance;
- workspace security suitability;
- legal/contractual permission.

For confidential/client Engagements where applicable, separately record platform/workspace data-handling and organizational-policy approval.

## 14. Engagement Provenance

A material Engagement records:
- ARCHITECT Release;
- PI ID + content-verification status;
- governing-pack revision;
- EKB update policy + revision;
- Runtime ID;
- execution profile;
- isolation state.

## 15. Canonical Home of Runtime Records

Completed deployment records must not live only in chat history.

- HOME/MAINTENANCE full record → canonical ARCHITECT `runtime/records/`.
- Engagement full record → Engagement-owned canonical store.
- `runtime/00_RUNTIME_REGISTRY.md` may keep a de-identified summary/pointer for material Engagement runtimes.

Do not store secrets in runtime records.

## 16. Bootstrap / Verification Sequence

1. identify expected release;
2. read canonical Maintainer binding;
3. when Maintainer-only action is intended, verify current acting principal authorization;
4. record execution profile;
5. deploy PI;
6. verify PI content integrity, not just ID;
7. verify governing-pack read/revision;
8. verify EKB read/revision and update policy;
9. verify Engagement Memory access;
10. verify required context isolation;
11. verify platform/data-handling approval where required;
12. record write capability;
13. persist completed Runtime Deployment Record in canonical home;
14. set runtime state;
15. only then claim corresponding deployment level.

## 17. No False Full-ARCHITECT Claim

Degraded/unverified runtime may still be useful.

The defect is not inability to answer; it is misrepresenting configuration.

Disclose material limitations proportionally.
