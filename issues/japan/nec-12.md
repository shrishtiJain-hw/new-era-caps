# NEC-12: Order contact retains an old customer email

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

A Shopify customer email change leaves the old email in order contact data.

## Expected behavior and requirement

Apply the agreed customer-to-order update semantics and choose the intended contact association.

## RCA and evidence

Workbook TC-040 records the new email in the UI and party contact, while OrderContactMech retains the original value. The case also notes that the broker feed has no email field, so broker email propagation was not a valid verification target. The mail references a bridge PR, without proving deployment.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Clarify which existing orders should update.
- Check contact association validity and feed selection.
- Verify an email update does not create multiple active contacts.

## Evidence basis

[Jira issue NEC-12](https://hotwax-team.atlassian.net/browse/NEC-12). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
