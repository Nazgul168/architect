
# ARCHITECT Behavioral Baseline Registry

Status: RELEASE CANDIDATE  
Release line: ARCH-0.2.1-RC5

## Purpose

Canonical index of executed behavioral regression runs and accepted known-good baselines for permanent ARCHITECT.

A chat transcript or unpersisted test result is not a canonical baseline record.

## Status vocabulary

- `DRAFT`
- `EXECUTED_NOT_APPROVED`
- `CANDIDATE_BASELINE`
- `KNOWN_GOOD`
- `WITHDRAWN`
- `SUPERSEDED`
- `BASELINE_INCONSISTENT`

## Finalization rule

A `KNOWN_GOOD` Registry entry is valid only when the matching full Run Record:
- has the same `RUN_ID`;
- has the same `FINALIZATION_TRANSACTION_ID`;
- has status `KNOWN_GOOD`;
- contains the corresponding Maintainer decision;
- was canonically finalized in the same controlled transaction.

Where Git is used, finalize the Registry entry and full Run Record in the same commit.

Any mismatch is `BASELINE_INCONSISTENT`, not `KNOWN_GOOD`.

## Registry

_No behavioral runs recorded yet._

| Baseline/Run ID | Finalization Tx | Status | ARCHITECT Release | Execution Profile | Governing Revision | EKB Revision | Runtime Record | Critical Result | Maintainer Authorization | Full Record |
|---|---|---|---|---|---|---|---|---|---|---|
