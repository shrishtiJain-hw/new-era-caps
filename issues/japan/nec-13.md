# NEC-13: Post-import order discount edits do not synchronize

**Country:** Japan\
**Brands:** NEC\
**Status:** To Do\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

A discount changed in Shopify after initial import remains unchanged in OMS.

## Expected behavior and requirement

Propagate supported post-import discount changes while keeping order totals reconcilable.

## RCA and evidence

Workbook TC-043 and TC-050 record unchanged totals after Shopify discount edits. The mixed-line example has no discount OrderAdjustment and leaves the discounted line unchanged. This narrows the observed failure to monetary-edit propagation or recalculation; the exact missing handler is not proven.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Compare original and edited discount allocations.
- Trace update ingestion and total recalculation.
- Test item and order-level discounts without double application.

## Evidence basis

[Jira issue NEC-13](https://hotwax-team.atlassian.net/browse/NEC-13). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
