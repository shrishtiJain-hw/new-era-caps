# Imported orders bypassed the intended brokering queue

**Country:** Japan\
**Brands:** NEC\
**Status:** Recorded Done in workbook issue tracker\
**Contribution:** Validation record and investigation synthesis from owner-provided workbook

## Issue and business impact

UAT orders were assigned directly to the configured warehouse instead of first entering the brokering queue.

## Expected behavior and requirement

Resolve import allocation according to the intended order type and queue policy.

## RCA and evidence

The Execution summary traces fallback to the product store default inventory facility. It proposes setting the queue as the default, or changing the resolution branch. The Issue Tracker marks the allocation issue Done, but does not isolate which alternative was actually applied.

## Documented actions

1. The source investigation compared the transformation fallback with the product-store setting.
2. The workbook records the issue as Done. Its proposed code/config alternatives are retained as analysis rather than both being claimed executed.

## Outcome and remaining work

The workbook supports a recorded UAT closure. It does not establish a subsequent production deployment.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Test standard online, cash-sale, mixed POS, and send-sale allocation separately.
- Verify the configured fallback rather than forcing every order into one facility.

## Evidence basis

[New Era validation workbook](https://docs.google.com/spreadsheets/d/1imU-emS67yW7hHUxPVRot7L7JBZENkGhJadfAoVDm-w/edit?usp=sharing), XLSX export reviewed November 2, 2026. Results below are recorded UAT observations, not newly executed tests.
