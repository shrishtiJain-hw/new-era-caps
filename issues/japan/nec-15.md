# NEC-15: Customer reassociation duplicates broker detail rows

**Country:** Japan\
**Brands:** NEC\
**Status:** In Progress\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

Broker output contains duplicate detail records after a customer reassociation.

## Expected behavior and requirement

Keep each logical order line unique while selecting the intended current customer association.

## RCA and evidence

Workbook TC-048 records two identical ExternalFulfillmentOrderItem rows for one logical order item after customer reassociation, producing two broker detail lines with duplicated quantity. The active customer role and original billing/shipping preservation were correct in that test. Why the duplicate fulfillment rows were created remains unresolved.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Compare join cardinality before and after reassociation.
- Verify one output detail per logical line.
- Test successive reassociations without masking defects through blanket deduplication.

## Evidence basis

[Jira issue NEC-15](https://hotwax-team.atlassian.net/browse/NEC-15). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
