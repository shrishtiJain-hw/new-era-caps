# NEC-4: Delivery preferences prevent order import

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

Orders carrying delivery-date or time-slot preferences fail import.

## Expected behavior and requirement

Map optional delivery date and slot independently and allow supported combinations.

## RCA and evidence

The workbook Execution summary identifies a delivery-details transformation that attempted a plain-value-map conversion, with a proposed change to merge the incoming delivery-details map directly. Test case matrix rows TC-004 through TC-006 later record successful imports with delivery preferences. The board remains In Review, so recorded UAT success is not production closure.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Test date only, slot only, both, and neither.
- Check source attribute names and destination formats.
- Confirm customer notes remain unaffected.

## Evidence basis

[Jira issue NEC-4](https://hotwax-team.atlassian.net/browse/NEC-4). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
