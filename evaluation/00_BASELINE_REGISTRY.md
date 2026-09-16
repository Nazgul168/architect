# ARCHITECT Runtime Behavioral Baseline Registry

Status: MIGRATION CANDIDATE  
Clean ROLE line: 1.0.0-rc.1

## Purpose

Canonical index of executed Runtime Compatibility / behavioral regression runs for specific ARCHITECT execution profiles.

Portable clean-ROLE System Validation records live under `evaluation/system_validation/` and are governed separately.

A chat transcript or unpersisted test result is not a canonical runtime baseline record.

## Status vocabulary

- `DRAFT`
- `EXECUTED_NOT_APPROVED`
- `CANDIDATE_BASELINE`
- `KNOWN_GOOD`
- `WITHDRAWN`
- `SUPERSEDED`
- `BASELINE_INCONSISTENT`

## Finalization rule

A `KNOWN_GOOD` runtime Registry entry is valid only when the matching full Run Record has the same Run ID, Finalization Transaction ID and status and both artifacts are canonically finalized together.

`KNOWN_GOOD` does not replace or imply clean-ROLE System Validation. A published clean release must already have its own System Validation evidence.

## Registry

_No behavioral runtime runs recorded yet._

| Baseline/Run ID | Finalization Tx | Status | ARCHITECT Release | Published Revision | Execution Profile | Runtime Record | Critical Result | Human Authorization | Full Record |
|---|---|---|---|---|---|---|---|---|---|
