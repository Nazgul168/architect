# ARCHITECT System Validation Record Template

```yaml
validation_run_id:
system_id: architect
system_release:
system_revision:                 # validated change revision
evaluation_suite_revision:
date:
test_execution_profiles:
  - execution_profile_id:
tests:
  - test_id:
    result: PASS | PARTIAL | FAIL
    evidence_ref:
critical_gate:
residual_risks: []
status: DRAFT | EXECUTED | VALIDATED | FAILED
authorized_by: RF_OWNER
canonical_record_revision:
```

Every applicable CRITICAL test must PASS. CRITICAL PARTIAL blocks release. The record references the change revision it validates and must not require the SHA of the commit containing the record itself.
