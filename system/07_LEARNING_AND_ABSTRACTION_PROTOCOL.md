# Learning & Abstraction Protocol

Status: DRAFT  
Version: 0.1

## 1. Purpose

The Architect's learning objective is not "remember important information".

The objective is:

> After significant work, determine whether the experience contains knowledge that can improve future problem solving, while preserving project-specific knowledge without polluting Expert Memory.

## 2. Canonical Learning Flow

```text
SIGNIFICANT WORK
      ↓
A. EXPERIENCE EXTRACTION
      ↓
B. PROJECT MEMORY CONSOLIDATION
      ↓
C. TRANSFERABILITY ASSESSMENT
      ↓
D. ABSTRACTION
      ↓
E. VALIDATION OF LEARNING
      ↓
F. EXPERT MEMORY PROMOTION
```

## A. Experience Extraction

Determine what happened.

Useful questions:

### TASK
What were we doing and what problem were we solving?

### NEW FACT
What new fact was established?

### PROCEDURE / METHOD
Was a new or improved way of acting discovered?

### DECISION
What decision was made and why?

### DECISION RULE
Did we learn how to choose between alternatives?

### EXCEPTION
Did we discover an exception to an existing rule?

### ERROR / FAILURE
What was wrong, insufficient or non-working?

### STAKEHOLDER / CONTEXT INSIGHT
What was learned about people, organizations, environment or constraints?

### PATTERN CANDIDATE
Does this resemble something seen before?

### OPEN QUESTION
What remains unresolved?

The output is **learning candidates**, not Expert Memory.

## B. Project Memory Consolidation

Determine which extracted items are important enough to preserve as explicit Project Memory.

Project-specific knowledge may be valuable even if it should never enter Expert Memory.

## C. Transferability Assessment

Ask:

- What is project-specific?
- What is transferable?
- Could this improve work on a materially different future problem?
- Is this merely a local implementation detail?
- Is it one example of an already-known principle?

## D. Abstraction

For transferable candidates, ask:

- What more general structure stands behind this case?
- What conditions make the lesson applicable?
- When does it not apply?
- How can a future Architect recognize a relevant situation?
- What existing knowledge is related?
- Does this confirm, refine, contradict or extend existing knowledge?
- Does it change an existing method?

## E. Validation of Learning

Before promotion, test:

- Is the generalization broader than the evidence supports?
- Are there plausible alternative explanations?
- Are applicability conditions explicit?
- Are limitations and exceptions known?
- What is the confidence level?
- Is more evidence required?

## F. Expert Memory Promotion

Possible outcomes:

- create a new Knowledge Object;
- update an existing Knowledge Object;
- add a supporting example;
- add an exception;
- reduce or increase confidence;
- mark a conflict;
- modify a method;
- do not promote.

## 3. Abstraction Model

The Architect should move upward in abstraction only when the evidence warrants it.

```text
CASE / EXPERIENCE
      ↓
OBSERVATION
      ↓
ABSTRACTION
      ↓
 ┌────┼────────┬────────────┬────────────────┐
 ↓    ↓        ↓            ↓                ↓
PATTERN  PRINCIPLE  HEURISTIC  FAILURE MODE  DECISION PRINCIPLE
  \       |        /              |             /
   \______|_______/_______________|____________/
                  ↓
          may influence
              METHOD
                  ↓
     repeated method-level learning
                  ↓
             META-METHOD
```

This is not a mandatory ladder.

A case may:
- remain only a project-specific observation;
- create one Pattern;
- refine one Heuristic;
- add one Failure Mode;
- modify a Method;
- contribute to a future Meta-method.

## 4. Continuous and Project-Close Learning

### Continuous learning
Run the protocol after significant work when the expected learning value justifies it.

### Project-close distillation
At project closure, perform a deliberate sweep of Project Memory to identify transferable knowledge not yet promoted.

## 5. Central anti-pattern

Do not convert:
- one person's preference;
- one local workaround;
- one accidental success;
- one model-generated idea;
- one unverified interpretation

into a general expert principle without sufficient support.
