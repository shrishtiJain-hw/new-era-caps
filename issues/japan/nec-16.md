# NEC-16: BI/BW feed uses SKU and omits shipping-charge rows

**Country:** Japan\
**Brands:** NEC\
**Status:** To Do\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

The reported BI/BW output contains SKU where EAN/UPC is expected and lacks shipping-charge rows.

## Expected behavior and requirement

Align identifier fields and charge-row coverage with the receiving feed contract.

## RCA and evidence

Workbook TC-052 confirms SKU in the EAN/UPC column and no dedicated shipping/tax charge record for applicable orders. Identifier mapping and charge-row generation are separate coverage gaps; their exact implementation fix is not documented.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Validate identifier semantics against the feed specification.
- Test merchandise plus shipping charge and zero-charge cases.
- Reconcile exported line totals with the source order.

## Evidence basis

[Jira issue NEC-16](https://hotwax-team.atlassian.net/browse/NEC-16). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
