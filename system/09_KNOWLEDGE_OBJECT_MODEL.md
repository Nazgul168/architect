# Knowledge Object Model

Status: DRAFT  
Version: 0.1

## 1. Purpose

A Knowledge Object is the atomic managed unit of transferable Expert Memory.

It should preserve not only a conclusion, but enough context for future recognition, application, critique and revision.

## 2. Knowledge Object types

Initial controlled vocabulary:

- `pattern`
- `principle`
- `heuristic`
- `failure_mode`
- `decision_principle`
- `method`
- `meta_method`
- `case_abstraction`

This list may evolve, but new types should be added only when they solve a real modeling problem.

## 3. Canonical metadata

Recommended front matter:

```yaml
id: HEUR-0001
type: heuristic
title: Example title
status: validated
confidence: medium

origin:
  project: PROJECT_ID
  case: CASE_OR_DECISION_ID

created: YYYY-MM-DD
last_reviewed: YYYY-MM-DD

related:
  - PAT-0003
  - FAIL-0007
```

Possible statuses:
- candidate
- validated
- contested
- deprecated
- superseded

Possible confidence levels:
- low
- medium
- high

Confidence is not proof; it records current epistemic assessment.

## 4. Canonical body

Use the smallest applicable subset.

```markdown
# Title

## Summary
One compact statement of the knowledge.

## Pattern / Principle / Heuristic / Method
The substantive knowledge.

## Recognition Cues
How a future Architect can recognize situations where this may be relevant.

## Applicability
Conditions under which it is useful.

## Non-Applicability / Limits
Conditions under which it should not be used mechanically.

## Failure Mode
What may go wrong if the knowledge is ignored or misapplied.

## Rationale
Why the knowledge is believed to hold.

## Origin / Provenance
Where the lesson came from.

## Evidence / Examples
Supporting cases or evidence.

## Related Knowledge
Links to other Knowledge Objects.

## Impact on Method
Whether this changes an existing method or meta-method.

## Revision Notes
Material changes in meaning or confidence.
```

## 5. Example

```yaml
id: PAT-0017
type: pattern
title: Business Change as First-Class Event
status: validated
confidence: high

origin:
  project: NURA_ERP
  case: Funding Agreement Amendment
```

```markdown
# Business Change as First-Class Event

## Pattern
Changes to a business object may themselves constitute first-class business events.

## Principle
When a change has independent business meaning, authorization, effective date,
causal consequences, or audit requirements, consider modelling the change as
a first-class event/entity rather than only as a new version of the affected object.

## Recognition Cues
- independent reason or legal basis;
- separate approval;
- own effective date;
- downstream consequences;
- requirement to reconstruct causality;
- independent audit significance.

## Applicability
Contracts, pricing, subscriptions, budgets, permissions, product configurations,
legal status.

## Non-Applicability / Limits
A separate event may be unnecessary when the change has no independent business
meaning and historical state reconstruction is sufficient.

## Failure Mode
Simple version history may preserve what changed while losing why it changed
and what downstream consequences followed.

## Origin
NURA ERP — Funding Agreement Amendment.

## Related Knowledge
Temporal modelling, auditability, event modelling, versioning, causal history.
```

## 6. Design rule

A Knowledge Object is not a transcript summary.

It is a compact professional memory object designed for future retrieval and application.
