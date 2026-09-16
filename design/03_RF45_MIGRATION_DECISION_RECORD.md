# ARCHITECT RF v4.5 Migration Decision Record

Status: PREPARED / NON-GOVERNING MIGRATION RECORD  
Source: `ARCH-0.2.1-RC5` @ `6f843575253c35312d24d03bd6fe9560045b8e95`  
Proposed initial release: `1.0.0` (currently unpublished candidate)

## Objective

Make the existing ARCHITECT clean ROLE manageable by ROLE FACTORY v4.5 and Role Updater without redesigning its professional cognition.

## Required compatibility changes

1. Add RF-compatible `SYSTEM_MANIFEST.md` and `ROLE_UPDATE_HISTORY.md`.
2. Convert permanent self-learning/promotion into Engagement-side Learning Candidates → Role Updater evaluation → controlled clean-role release.
3. Map legacy `ARCH-MAINT-001` to the same current human RF Owner; do not create a second release authority.
4. Bind task-specific Engagements to the whole clean ARCHITECT release/revision; Expert Memory does not float independently.
5. Separate portable System Validation from runtime behavioral/compatibility baselines.
6. Apply the RF4-045 normative-boundary rule.
7. Preserve existing professional cognition/methodology unless required by the above controls.

## Release state

This migration does not retroactively validate `ARCH-0.2.1-RC5` and does not itself publish `1.0.0`. The target remains an unpublished candidate until required System Validation, exact-subject RF Owner approval, integration of release provenance, read-back, and immutable tag publication complete the RF v4.5 release flow.

## Post-merge version correction

The first RF v4.5 migration package used `1.0.0-rc.1`. RF4-043 defines clean-ROLE release versions as `MAJOR.MINOR.PATCH`, and the candidate change revision is expected to carry the proposed final SemVer before validation. Therefore the proposed initial version is corrected to `1.0.0`. This correction does **not** assert validation or publication. The earlier merge to the default branch is treated as an unreleased migration state and is not evidence of a canonical release.
