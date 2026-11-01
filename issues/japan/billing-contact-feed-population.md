# Billing contact information absent from broker output

**Country:** Japan\
**Brands:** NEC\
**Status:** Billing fields populated after store-setting change in UAT\
**Contribution:** Validation record and investigation synthesis from owner-provided workbook

## Issue and business impact

The initial UAT broker feed lacked billing names and address data for same-address and different-address examples.

## Expected behavior and requirement

Capture the order billing information according to store configuration and retain correct Bill To fields independently of Ship To edits.

## RCA and evidence

Broker Feed Comparison records previously blank billing fields becoming populated after a product-store setting update. The Rollback plan identifies SAVE_BILL_TO_INF as the reversible setting. Source addresses, names, and phone numbers are omitted here.

## Documented actions

1. The workbook compared production and UAT billing-field output.
2. It records the product-store setting update and populated output for both address configurations.
3. The rollback notes describe how to restore the old setting if necessary; no rollback was performed for this portfolio.

## Outcome and remaining work

Source-recorded UAT correction is available. Production acceptance is not established.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Verify billing contact creation as well as final broker fields.
- Test same and distinct billing/shipping addresses.
- Confirm later shipping edits leave captured billing details unchanged.

## Evidence basis

[New Era validation workbook](https://docs.google.com/spreadsheets/d/1imU-emS67yW7hHUxPVRot7L7JBZENkGhJadfAoVDm-w/edit?usp=sharing), XLSX export reviewed November 2, 2026. Results below are recorded UAT observations, not newly executed tests.
