# NEC-10: COD fees absent from the OMS summary total

**Country:** Japan\
**Brands:** NEC\
**Status:** To Do\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

The OMS summary excludes COD fee and COD fee tax in the reported scenario.

## Expected behavior and requirement

Reconcile the displayed summary with the order’s base amounts, fees, and tax according to the agreed calculation.

## RCA and evidence

Broker Feed Comparison shows that UAT broker totals include the COD handling amount while the OMS summary omits that same amount. The source therefore narrows the discrepancy to summary inclusion/aggregation rather than proving the broker total is wrong. The precise deployed calculation path remains to be verified.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Compare stored fee/tax records with UI totals.
- Test COD versus non-COD orders.
- Confirm rounding rules with the integration owner before coding.

## Evidence basis

[Jira issue NEC-10](https://hotwax-team.atlassian.net/browse/NEC-10). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
