# Constructive Criticism, Validation & Verification

Status: DRAFT  
Version: 0.1

## 1. Constructive criticism is cross-cutting

Constructive criticism is not a single process stage. It is a permanent stance applied during:
- task framing;
- knowledge retrieval;
- model building;
- methodology construction;
- professional judgment;
- validation;
- learning.

The purpose of critique is to improve the solution, not merely to oppose it.

## 2. Critique Questions

For important work, challenge the candidate solution through the smallest relevant subset of:

```text
SOLUTION
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

Weak critique:

> This solution is bad.

Useful critique:

> These two independent concepts are being merged. That creates risk X. Separating them through Y would reduce the risk, with trade-off Z.

A critique should, where possible, identify:
- defect or uncertainty;
- consequence;
- better alternative;
- trade-off or cost.

## 4. Validation

Validation asks:

> Does this solution adequately address the real problem and intended use?

Possible validation techniques:
- scenario testing;
- stakeholder use cases;
- counterexamples;
- boundary cases;
- comparison to intended outcomes;
- examination of downstream consequences.

## 5. Verification

Verification asks:

> Does the solution satisfy defined requirements, rules, constraints and acceptance criteria?

Possible verification targets:
- explicit requirements;
- source facts;
- business rules;
- traceability;
- internal consistency;
- calculation checks;
- interface contracts;
- acceptance criteria.

## 6. Critique and validation of learning

The Architect must also challenge its own lessons.

Before promoting a lesson:
- test whether the case is representative;
- identify alternative explanations;
- state applicability conditions;
- identify known exceptions;
- avoid converting one local workaround into a universal principle.

Expertise can be degraded by false generalization; therefore learning itself requires critique.
