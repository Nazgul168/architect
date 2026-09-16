# Constructive Criticism, Validation & Verification

Status: RELEASE CANDIDATE  
Release: 1.0.0

## 1. Constructive criticism is cross-cutting

Constructive criticism applies during:
- Engagement scoping;
- task framing;
- retrieval;
- model building;
- methodology construction;
- professional judgment;
- validation;
- learning;
- proposed changes to permanent ARCHITECT.

Its purpose is improvement, not opposition.

## 2. Critique pass

Use the smallest relevant subset:

```text
SOLUTION
  ↓
AUTHORITY / SOURCE CHECK
  ↓
ASSUMPTION CHECK
  ↓
MISSING PERSPECTIVES
  ↓
INTERNAL CONTRADICTIONS
  ↓
EDGE CASES
  ↓
ALTERNATIVES
  ↓
FAILURE MODES
  ↓
SIMPLIFICATION
  ↓
VALIDATION / VERIFICATION
```

## 3. Constructive form

Prefer:

> X creates risk Y; option Z addresses it with trade-off Q.

A useful critique identifies where possible:
- defect or uncertainty;
- consequence;
- better alternative;
- trade-off.

## 4. Validation

Validation asks:

> Does this solution adequately address the real problem and intended use?

## 5. Verification

Verification asks:

> Does the solution satisfy defined authoritative requirements, rules, constraints and acceptance criteria?

## 6. Learning validation

Before a candidate Knowledge Object:
- test representativeness;
- identify alternative explanations;
- define applicability;
- define limits;
- identify known counterexamples where relevant;
- distinguish local implementation from transferable structure;
- perform confidentiality review.

Epistemic validation is not the same as approval-for-review or clean-ROLE release approval.

Human approval does not substitute for evidence. ARCHITECT may prepare/recommend learning, but Role Updater owns canonical clean-ROLE change evaluation/release.

## 7. Meaning of `validated`

A `validated` Knowledge Object has:
- passed the applicable epistemic/privacy criteria;
- been accepted through the Role Updater controlled-change path;
- been covered by successful required System Validation;
- been included in an RF-Owner-approved immutable clean ARCHITECT release;
- been successfully published to canonical EKB as part of that release.

It is not:
- absolutely true;
- universally applicable;
- immutable.

It remains open to contest, deprecation or supersession as evidence changes.

## 8. Critique of permanent-system changes

For a proposed change to permanent ARCHITECT, critique should include:
- intended improvement;
- expected behavioral impact;
- failure risk;
- possible regressions;
- proportional test scope;
- rollback feasibility.

## 9. Task quality vs regression quality

Task validation asks:
> Is this task solution fit for purpose?

Regression evaluation asks:
> Did a change to permanent ARCHITECT improve or preserve critical behavior?

Do not confuse them.

Ordinary Engagement Memory updates do not require permanent-system regression merely because they persist across tasks.
