# Post-import edits reveal incomplete synchronization

**Country:** Japan\
**Brands:** NEC\
**Status:** Mixed results recorded; additional defects remain open\
**Contribution:** Validation record and investigation synthesis from owner-provided workbook

## Issue and business impact

Adding an item, removing a customer, or editing monetary fields can produce different downstream gaps after initial import.

## Expected behavior and requirement

Apply each supported edit to the intended entity and regenerate only the required downstream outputs.

## RCA and evidence

The matrix records a newly added line that allocated but lacked broker history, a removed customer whose active order role remained, and discount/shipping-charge edits that did not change OMS totals. Reassociation correctly changed the active customer but produced duplicate fulfillment records. These are distinct paths and should not share an invented single RCA.

## Documented actions

1. Compared each edit’s expected behavior against the workbook’s actual result.
2. Separated customer-role changes, item export history, and financial adjustment gaps.
3. Linked related cases to the contact, discount, and duplicate-feed tickets.

## Outcome and remaining work

Several synchronization defects remain evidenced by the workbook. Successful customer-name and address examples do not close the failing edit scenarios.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Test item addition through allocation and broker-history creation.
- Verify active/historical customer roles after removal and reassociation.
- Reconcile totals after discount and shipping-charge changes.

## Evidence basis

[New Era validation workbook](https://docs.google.com/spreadsheets/d/1imU-emS67yW7hHUxPVRot7L7JBZENkGhJadfAoVDm-w/edit?usp=sharing), XLSX export reviewed November 2, 2026. Results below are recorded UAT observations, not newly executed tests.
