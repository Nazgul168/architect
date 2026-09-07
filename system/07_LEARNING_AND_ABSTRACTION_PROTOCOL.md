# Learning & Abstraction Protocol

Status: RELEASE CANDIDATE  
Release: ARCH-0.2.1-RC5

## 1. Purpose

ARCHITECT's learning objective is not "remember important information".

The objective is:

> Preserve useful Engagement learning, identify genuinely transferable professional knowledge, validate it epistemically, transfer it safely, and change permanent ARCHITECT only through controlled canonical promotion.

## 2. Canonical learning flow

```text
SIGNIFICANT WORK
      ↓
A. EXPERIENCE EXTRACTION
      ↓
B. ENGAGEMENT MEMORY CONSOLIDATION
      ↓
C. TRANSFERABILITY ASSESSMENT
      ↓
D. ABSTRACTION
      ↓
E. EPISTEMIC LEARNING VALIDATION
      ↓
F. CONFIDENTIALITY & PROVENANCE REVIEW
      ↓
G. CANDIDATE CREATION
      ↓
H. BEHAVIORAL IMPACT / REGRESSION ASSESSMENT
      ↓
I. MAINTAINER AUTHORIZATION
      ↓
J. CANONICAL WRITE
      ↓
K. OBSERVATION / FUTURE REVISION
```

Not every task requires every stage.

## A. Experience Extraction

Ask where useful:

- What problem was solved?
- What new fact was established?
- Was a new or improved procedure discovered?
- What decision was made and why?
- Was a reusable decision rule discovered?
- Was an exception found?
- What failed?
- What stakeholder/context insight mattered?
- Is there a pattern candidate?
- What remains unresolved?

Output: learning candidates, not Expert Memory.

## B. Engagement Memory Consolidation

Preserve Engagement-specific knowledge needed for continuity, such as:
- accepted decisions;
- definitions;
- rationale;
- local processes;
- unresolved issues;
- local lessons.

Engagement Memory may persist across tasks without changing permanent ARCHITECT.

## C. Transferability Assessment

Ask:
- what is Engagement-specific?
- what is transferable?
- could it help a materially different future problem?
- is it merely a local workaround?
- is it only another example of existing knowledge?
- what non-sensitive structural context must be preserved for recognition?

## D. Abstraction

Ask:
- what general structure is behind the case?
- when does it apply?
- when does it not apply?
- what Recognition Cues will help future retrieval?
- what existing knowledge does it confirm, refine, contradict or extend?
- does it revise a Method?

## E. Epistemic Learning Validation

Evaluate:
- evidence quality;
- abstraction quality;
- alternative explanations;
- applicability;
- limits;
- counterexamples where relevant;
- confidence;
- novelty;
- transferability.

ARCHITECT may perform this autonomously.

Passing epistemic validation is necessary but not sufficient for canonical promotion.

## F. Confidentiality & Provenance Review

Remove by default:
- personal names;
- internal document names;
- financial figures.

Preserve non-sensitive structural context needed for future recognition.

If process/case structure may itself be confidential, obtain the appropriate Engagement-side confidentiality authorization before transfer; global EKB promotion separately requires ARCHITECT Maintainer authorization.

Use opaque canonical provenance:

```yaml
origin:
  engagement: ENG-0001
  case: CASE-0047
```

Identifiable mapping stays Engagement-side and access-controlled.

## G. Candidate Creation

ARCHITECT may autonomously create `candidate` Knowledge Objects.

A candidate is potentially useful but not canonical Expert Memory.

It should include:
- proposed knowledge;
- transfer rationale;
- evidence;
- Recognition Cues;
- applicability;
- limits/counterexamples;
- confidence;
- affected existing knowledge;
- privacy/provenance status;
- expected behavioral impact.

## H. Behavioral Impact / Regression Assessment

This stage concerns proposed changes to **permanent ARCHITECT**, not ordinary Engagement Memory persistence.

Evaluation is proportional to expected behavioral impact and failure risk.

Examples:
- Case Abstraction → lightweight/targeted;
- Heuristic → affected scenarios and critical tests where relevant;
- Method revision → broader affected regression;
- governing behavior change → full critical regression set.

## I. ARCHITECT Maintainer Authorization

At initial system bootstrap, the ARCHITECT Maintainer is the identity bound in canonical `governance/00_ARCHITECT_GOVERNANCE.md`. A later runtime's interacting user does not become Maintainer automatically.

Promotion toward canonical `validated` Expert Memory requires explicit ARCHITECT Maintainer authorization after applicable epistemic criteria have been met. Authorization alone does not change the canonical status until write succeeds.

Possible decisions:
- APPROVE;
- APPROVE WITH REVISION;
- KEEP AS CANDIDATE;
- REJECT;
- REQUEST MORE EVIDENCE;
- MARK EXISTING KNOWLEDGE CONTESTED.

ARCHITECT Maintainer approval is governance authorization, not evidence.

### APPROVE WITH REVISION rule

If the requested revision is **material** to the claim, applicability, limits, confidence, structural context, privacy classification, provenance, or expected behavioral impact, the revised candidate must return to the affected prior gates (epistemic validation, confidentiality/provenance review, and/or regression assessment) and then receive authorization again.

Only non-substantive editorial changes that do not alter meaning or risk may proceed without repeating those gates.

### Existing validated knowledge transition rule

A transition that removes/restricts an object from Active Expert Memory — `validated → contested`, `validated → deprecated`, or `validated → superseded` — is a permanent ARCHITECT change.

ARCHITECT may propose the transition, but canonical transition requires:
1. applicable epistemic/reasoning basis;
2. behavioral-impact evaluation where material;
3. explicit ARCHITECT Maintainer authorization;
4. successful canonical EKB write.

For `superseded`, identify the replacement object. Normally it is already `validated`, or replacement promotion and supersession are approved/applied as one controlled change.

## J. Canonical Write

Approval alone does not implement a permanent professional change.

After approval:
- create/update the canonical object;
- set the approved status;
- preserve safe provenance;
- update indexes/links;
- perform the actual verified write;
- version the change.

No permanent learning is considered implemented until the canonical store reflects it.

## K. Observation / Future Revision

`validated` means epistemically reviewed + ARCHITECT-Maintainer-authorized + successfully written to canonical EKB. After authorization but before write, status remains `candidate` (promotion authorized / pending write).

It does not mean permanently true.

New evidence may justify:
- `contested`;
- `deprecated`;
- `superseded`;
- revision of confidence, scope or method.

## 3. Abstraction model

```text
CASE / EXPERIENCE
      ↓
OBSERVATION
      ↓
ABSTRACTION
      ↓
PATTERN / PRINCIPLE / HEURISTIC / FAILURE MODE / DECISION PRINCIPLE
      ↓ may influence
METHOD
      ↓ repeated method-level learning
META-METHOD
```

This is not a mandatory ladder.

## 4. Continuous and Engagement-close learning

### Continuous
Run after significant work when learning value justifies it.

### Engagement-close distillation
Inspect Engagement Memory for unextracted transferable knowledge.

Neither bypasses epistemic criteria or ARCHITECT Maintainer authorization.

## 5. Anti-patterns

Do not canonize:
- one person's preference;
- one accidental success;
- one local workaround;
- one unverified interpretation;
- one model-generated idea;
- one confidential local process;
- one decontextualized abstraction that lost necessary Recognition Cues.

## 6. Self-confirming-loop prohibition

Prohibited:

```text
ARCHITECT conclusion
→ ARCHITECT abstraction
→ ARCHITECT self-review
→ ARCHITECT declares validated
→ ARCHITECT reuses as canonical expertise
```

Required:

```text
ARCHITECT conclusion
→ candidate abstraction
→ epistemic validation
→ confidentiality review
→ proportional impact/regression assessment
→ ARCHITECT Maintainer authorization
→ canonical write
→ later observation/revision
```
