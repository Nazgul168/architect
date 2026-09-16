# Knowledge Object Model

Status: RELEASE CANDIDATE  
Release: 1.0.0-rc.1

## 1. Purpose

A Knowledge Object is the atomic managed unit of transferable Expert Memory.

It should support:
- future recognition;
- applicability assessment;
- professional reasoning;
- critique;
- revision;
- governance.

## 2. Controlled object types

- `pattern`
- `principle`
- `heuristic`
- `failure_mode`
- `decision_principle`
- `method`
- `meta_method`
- `case_abstraction`

### Method improvement
A method improvement is a revision of an existing `method`, not a separate type.

### Critique framework
A reusable critique framework is normally `method`, or rarely `meta_method`.

## 3. Status model

- `candidate`
- `validated`
- `contested`
- `deprecated`
- `superseded`

### Meaning of `validated`

`validated` means:
1. the applicable epistemic criteria were satisfied;
2. the change was accepted through the Role Updater controlled-release path;
3. required System Validation passed;
4. RF Owner approved the immutable release-candidate subject;
5. the published clean ARCHITECT release containing the object was canonically written.

It does **not** mean:
- absolutely true;
- universally applicable;
- permanently immune to revision.

## 4. Transition authority

ARCHITECT may autonomously create an Engagement-side `candidate` and may recommend it for Role Updater review. It may not self-assign `APPROVED_FOR_ROLE_REVIEW` or write the candidate directly into canonical Expert Memory.

Canonical promotion to `validated` is a clean-ROLE change. It requires applicable epistemic/privacy criteria, Role Updater evaluation, mandatory System Validation, explicit RF Owner approval of the release candidate, and successful publication of the immutable clean ARCHITECT release. Until publication, the object remains non-canonical candidate material.

Transitions from `validated` to:
- `contested`;
- `deprecated`;
- `superseded`

always change Active Expert Memory and therefore require:
1. applicable epistemic/reasoning basis;
2. behavioral-impact evaluation where material;
3. Role Updater evaluation and required System Validation;
4. explicit RF Owner release approval;
5. successful immutable clean-ROLE publication.

ARCHITECT may recommend such a transition but cannot execute it unilaterally; it is routed through Role Updater.

For `superseded`, identify the replacement object. Normally it is already `validated`, or replacement promotion and supersession are approved/applied as one controlled change.

## 5. Recommended metadata

```yaml
id: HEUR-0001
type: heuristic
title: Example title
status: candidate
confidence: medium

origin:
  engagement: ENG-0001
  case: CASE-0047

privacy:
  body_deidentified: true
  structural_context_preserved: true
  provenance_mode: opaque

role_review:
  status: CANDIDATE        # CANDIDATE | LOCAL_ONLY | RECOMMENDED_FOR_ROLE_REVIEW | APPROVED_FOR_ROLE_REVIEW | REJECTED | EXPORTED_TO_ROLE_UPDATER
  approved_by: null
  approved_at: null

created: YYYY-MM-DD
last_reviewed: YYYY-MM-DD

related:
  - PAT-0003
  - FAIL-0007
```

Confidence:
- low
- medium
- high

Confidence is not proof or promotion authority.

## 6. Privacy and provenance

Exclude unnecessary:
- personal names;
- internal document names;
- financial figures.

Preserve non-sensitive structural context needed for recognition and applicability.

If process/case structure may itself be confidential, obtain the appropriate Engagement-side confidentiality authorization before transfer. Any canonical promotion is separately governed by Role Updater and RF Owner release approval.

Preferred provenance:
- opaque ID;
- approved non-sensitive alias where justified.

Any mapping back to identifiable evidence remains Engagement-side and access-controlled.

## 7. Canonical body

Use the smallest applicable subset:

```markdown
# Title

## Summary

## Knowledge
Pattern / Principle / Heuristic / Method / etc.

## Recognition Cues

## Structural Context

## Applicability

## Non-Applicability / Limits

## Counterexamples / Exceptions

## Failure Mode

## Rationale

## Evidence

## Related Knowledge

## Impact on Method

## Behavioral Impact / Regression Scope

## Governance

## Revision Notes
```

## 8. Candidate promotion brief

```text
Candidate ID:
Type:
Proposed knowledge:

Why transferable:
Evidence:
Recognition cues:
Structural context:
Applicability:
Limits / counterexamples:
Confidence:
Existing knowledge affected:
Privacy/provenance status:
Expected behavioral impact:
Recommended evaluation scope:
Recommended action:
```

## 9. Example

```yaml
id: PAT-0017
type: pattern
title: Business Change as First-Class Event
status: candidate
confidence: high

origin:
  engagement: ENG-0001
  case: CASE-0047

privacy:
  body_deidentified: true
  structural_context_preserved: true
  provenance_mode: opaque
```

```markdown
# Business Change as First-Class Event

## Pattern
Changes to a business object may themselves constitute first-class business events.

## Recognition Cues
- independent reason or legal basis;
- separate approval;
- own effective date;
- downstream consequences;
- causal audit requirement.

## Structural Context
Useful in environments with formally effective changes, multiple authoritative records,
audit-sensitive downstream consequences, or legally significant state transitions.

## Applicability
Contracts, pricing, subscriptions, budgets, permissions, product configuration,
legal status.

## Limits
A separate event may be unnecessary when the change has no independent business
meaning and historical state reconstruction is sufficient.

## Failure Mode
Simple version history may preserve what changed while losing why it changed
and what downstream consequences followed.
```

This remains `candidate` until the full promotion path is completed.

## 10. Design rule

A Knowledge Object is not a transcript summary.

It is a compact, revisable professional memory object.
