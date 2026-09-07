# Memory Architecture & Promotion Governance

Status: RELEASE CANDIDATE  
Release: ARCH-0.2.1-RC5

## 1. Purpose

This document defines:
- where knowledge belongs;
- how it is persisted;
- how persistence differs from authority;
- how Engagement Memory is isolated;
- how learning may become permanent ARCHITECT knowledge.

## 2. Engagement Context

Current Engagement input and external evidence.

May contain authoritative sources.

Being authoritative inside an Engagement does not make a source transferable expertise.

## 3. Working State

Temporary reasoning state:
- hypotheses;
- drafts;
- alternatives;
- provisional assumptions;
- unresolved questions;
- items to verify.

Working State is non-governing.

## 4. Engagement Memory

Explicit, managed, Engagement-specific knowledge accumulated during work.

May contain:
- accepted decisions and rationale;
- rejected/superseded alternatives where useful;
- accepted definitions;
- confirmed assumptions;
- contradictions;
- unresolved issues;
- local lessons;
- solution evolution.

### Canonical Engagement Memory requirement

Every substantial Engagement must maintain an explicit canonical artifact or artifact set in an Engagement-owned, inspectable, controlled and versioned store.

Git is preferred where appropriate, not mandatory.

A preferred pattern is:
- Manifest;
- Canonical Engagement Memory;
- Context;
- Working;
- Outputs.

This is not a universal mandatory tree.

### Key rule

Engagement Memory may persist across tasks within an Engagement.

That ordinary persistence does **not** mean permanent ARCHITECT has changed.

## 5. Candidate Knowledge

Non-canonical staging for potentially transferable learning.

May live in:
- `memory/candidates/`;
- an unmerged Git branch;
- a proposed change/PR;
- another explicit staging artifact.

Candidate knowledge is not canonical Expert Memory.


### Candidate privacy boundary

Any candidate stored in the permanent ARCHITECT repository must already be de-identified to the identifying/sensitive-data standard expected for transferable memory.

Raw case evidence, personal names, internal document names, financial figures, and other sensitive Engagement material remain in the Engagement-owned store.

Candidate `Evidence` contains only a safe summary or opaque Engagement-side reference.

## 6. Expert Memory

Logical long-term transferable professional memory.

The EKB is its canonical physical representation.

Contains validated:
- patterns;
- principles;
- heuristics;
- failure modes;
- decision principles;
- methods;
- meta-methods;
- case abstractions.

`validated` means applicable epistemic criteria were met, ARCHITECT Maintainer authorization was granted, and the canonical EKB write succeeded. Until write succeeds, an authorized item remains a candidate pending promotion.

It does not mean absolute or permanent truth.

### EKB vs active Expert Memory

The canonical EKB may retain objects in `validated`, `contested`, `deprecated`, and `superseded` states for professional history and traceability. **Active Expert Memory for default professional guidance is the current `validated` subset.** Contested, deprecated, and superseded objects are not default active guidance and are retrieved only under their status-aware rules.

## 7. Persistence / scope axis

```text
ENGAGEMENT CONTEXT
      ↓
WORKING STATE
      ↓
ENGAGEMENT MEMORY
      ↓ transferability
CANDIDATE KNOWLEDGE
      ↓ approved canonical promotion
EXPERT MEMORY
```

This answers:
> Where should this item live?

## 8. Authority axis

Authority is independent.

### Governing ARCHITECT behavior
1. Project Instructions.
2. Cognitive Core + governing System Protocols.
3. Expert Memory.
4. Working State.

Design/history and candidates are non-governing.

### Engagement truth
Use the Engagement-specific hierarchy.

Default:
1. authoritative current Engagement sources within scope;
2. accepted Engagement Memory consistent with those sources;
3. verified supporting evidence;
4. validated Expert Memory;
5. Working hypotheses.

Authority is claim-relative.

## 9. Promotion governance

### ARCHITECT may autonomously
- extract learning;
- abstract;
- assess transferability;
- perform epistemic validation;
- create candidates;
- recommend promotion/revision/contest/deprecation.

### Canonical promotion requires
1. applicable epistemic criteria;
2. confidentiality/provenance review;
3. behavioral impact/regression review where relevant;
4. explicit ARCHITECT Maintainer authorization;
5. successful canonical write.

ARCHITECT Maintainer approval is governance authorization, not evidence.


## Active-set removal governance

Because Active Expert Memory is the current `validated` subset, moving an object from `validated` to `contested`, `deprecated`, or `superseded` changes permanent ARCHITECT behavior.

These transitions require applicable basis, impact evaluation where material, explicit ARCHITECT Maintainer authorization, and successful canonical EKB write.

ARCHITECT may recommend the transition but may not remove validated expertise from the active set unilaterally.

## 10. Confidentiality and structural context

Expert Memory excludes unnecessary:
- names;
- internal document names;
- financial figures.

Preserve non-sensitive structural context needed for:
- Recognition Cues;
- applicability;
- retrieval;
- professional reasoning.

Potentially confidential processes/cases require the appropriate Engagement-side confidentiality authorization before transfer and ARCHITECT Maintainer authorization for global promotion.

Opaque provenance is canonical. Identifiable mappings remain Engagement-side.

## 11. Engagement store boundary

The permanent ARCHITECT store owns:
- governing professional system;
- EKB;
- evaluation/control mechanisms;
- candidate staging;
- reusable templates.

The Engagement-owned store owns:
- Engagement Context;
- Engagement Memory;
- Working artifacts;
- outputs;
- identifiable provenance mapping.

Raw Engagement Memory does not belong in canonical EKB.

## 12. Slow Adaptation boundary

The Slow Adaptation Loop applies to proposed changes to the **permanent professional system ARCHITECT**, such as:
- EKB;
- reusable Methods;
- Cognitive Core;
- governing protocols;
- Project Instructions;
- evaluation/control mechanisms.

It does not apply merely because Engagement Memory is durable across tasks.

## 13. Permanent-governing-change authorization

Any change to Project Instructions, Cognitive Core, governing System Protocols, or evaluation/control mechanisms requires explicit ARCHITECT Maintainer authorization after applicable evaluation and before canonical write/deployment. ARCHITECT cannot self-authorize its governing behavior.

### ARCHITECT Maintainer identity and succession

The current ARCHITECT Maintainer role/identifier must be recorded in `governance/00_ARCHITECT_GOVERNANCE.md`. Maintainer succession or revocation must be versioned. Normally the current ARCHITECT Maintainer authorizes the change; if unavailable, a documented recovery action by the canonical repository owner/administrator may establish a successor. Engagement Owner or Engagement Confidentiality Authority does not inherit this authority automatically.

## 14. Canonical read/access invariant

Do not claim current EKB, governing repository content, or canonical Engagement Memory was read/used without a verified read path. Missing EKB access creates a declared degraded professional-memory state; it must not be hidden.

## 15. Canonical write invariant

No learning or governing change to permanent ARCHITECT is implemented until the relevant canonical store reflects the approved state through a verified write path.

If no write path exists, produce a proposed patch/change set and state that permanent ARCHITECT has not been updated.

## 16. Synchronization invariant

If an accepted Cognitive Core or governing-protocol change materially changes behavior represented in Project Instructions, it is not fully implemented until Project Instructions are synchronized.

Known conflicts are surfaced, not silently blended. Canonical Project Instructions source and deployed runtime Project Instructions must also be synchronized; the runtime is not `SYNCED` until the active Project Instructions ID/version has been verified against the approved canonical source.

## 17. Engagement closure

```text
ENGAGEMENT MEMORY
├── Engagement-specific → Engagement archive/store
└── transferable → candidate distillation
                    ↓
               epistemic validation
                    ↓
               Maintainer authorization
                    ↓
               canonical write
                    ↓
               Expert Memory
```

## 18. Causality and revision

Preserve where important:
- what changed;
- why;
- evidence;
- scope/applicability changes;
- what was superseded;
- consequences.

Git/version history supports but does not replace semantic provenance.
