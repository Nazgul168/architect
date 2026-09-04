# Task Understanding & Knowledge Navigation Protocol

Status: DRAFT  
Version: 0.1

## 1. Purpose

Before searching for a solution, ARCHITECT should first determine what kind of problem is actually being presented.

The objective is to create a **task representation / task signature** that guides relevant knowledge retrieval.

## 2. Task Representation

For substantial tasks, determine the smallest useful subset of the following:

### OBJECT
What is being created, changed, analyzed or decided?

### GOAL
What real problem or outcome should be addressed?

### SYSTEM LEVEL
What is the primary level of intervention?

Examples:
- product;
- service;
- process;
- organization;
- information system;
- policy;
- business model.

### LIFECYCLE STAGE
Where is the work occurring?

Examples:
- discovery;
- concept;
- design;
- implementation;
- operation;
- evaluation.

### UNCERTAINTY
What is not yet known?

### STAKEHOLDERS
Who is affected, who decides, who supplies information, who bears consequences?

### CONSTRAINTS
What limits the feasible solution?

### DECISION TYPE
What decision must actually be made?

### OUTPUT
What artifact, recommendation, decision, model or action is expected?

## 3. Problem Framing Discipline

Do not confuse:
- the user's objective with the user's first implementation idea;
- terminology with ontology;
- symptoms with root problems;
- a requested artifact with the actual decision the artifact must support.

When the problem is weakly framed, improve the framing before selecting a method.

## 4. Retrieval Strategy

Use the task representation to identify relevant knowledge.

Retrieval should answer:

- Which Expert Memory objects are potentially relevant?
- Which current-project sources contain required evidence?
- Which methods address this problem class?
- Which known failure modes resemble the current case?
- Which past cases are structurally similar?
- Which assumptions need external verification?

Prefer **structure-based retrieval** over keyword-only retrieval.

Example:

A request containing the word "workflow" may actually be a:
- domain-model problem;
- role/authorization problem;
- lifecycle problem;
- control problem;
- process problem.

Do not retrieve process-modelling knowledge automatically until the problem structure is established.

## 5. Retrieval Cues

Knowledge Objects should expose recognition cues so they can be retrieved when a current problem exhibits similar structural features.

Useful cues include:
- problem type;
- lifecycle stage;
- system level;
- uncertainty type;
- stakeholder conflict;
- change/event structure;
- auditability requirements;
- semantic ambiguity;
- reversibility;
- dependency structure.

## 6. Retrieval Quality

Do not equate retrieval with application.

For each relevant item, assess:
- applicability;
- limitations;
- context differences;
- known exceptions;
- confidence;
- potential conflict with other knowledge.

Prior experience is evidence and guidance, not an automatic answer.
