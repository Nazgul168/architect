
# Surgical Change Log — ARCH-0.2.1-RC5

Status: RELEASE CANDIDATE  
Date: 2026-09-04

RC5 is a **baseline-finalization sequencing patch only**.

It does not redesign DEC-A–G, runtime isolation, learning governance, or compact Project Instructions.

## Closed MATERIAL defect

RC4 allowed a sequencing ambiguity between:
- finalized Baseline Run Record;
- ARCHITECT Maintainer decision;
- `evaluation/00_BASELINE_REGISTRY.md`;
- final `KNOWN_GOOD` status.

RC5 introduces one **Baseline Finalization Transaction**.

A baseline becomes `KNOWN_GOOD` only when:
1. evaluation/acceptance criteria pass;
2. current acting Maintainer authorization is verified;
3. Maintainer decision is `AUTHORIZE_KNOWN_GOOD_IF_FINALIZATION_SUCCEEDS`;
4. final Run Record and matching Registry entry are prepared with the same `RUN_ID`, `FINALIZATION_TRANSACTION_ID`, and `KNOWN_GOOD` status;
5. both artifacts are canonically finalized together;
6. their canonical consistency is verified.

Where Git is available, both artifacts must be in the **same finalization commit**.

A partial/mismatched write is `BASELINE_INCONSISTENT`, not `KNOWN_GOOD`.

## PI

No behavioral invariant was added or removed from the compact PI; only RC5 identity/sentinel changed.

Canonical PI characters: 7124 / 8000  
Headroom: 876  
SHA-256: e1aafd3a96e8c0f2ad5dba8dfcab61b2c8f78fb0ac1b18eef5db4aacb150acf0

Behavioral baseline remains **NOT ESTABLISHED** until the first real run completes this finalization workflow.
