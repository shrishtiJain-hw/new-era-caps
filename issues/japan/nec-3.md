# NEC-3: Payment authorization status missing after real-time import

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

Imported orders lack the expected PAYMENT_AUTHORIZED history entry.

## Expected behavior and requirement

Preserve payment authorization state consistently through the real-time import.

## RCA and evidence

The missing status is documented, and a connector PR was linked. The available records do not prove its deployed behavior.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Compare source payment state, OMS payment records, and order-status history.
- Test authorized, pending, and failed payments.
- Retest message replay without duplicate payment history.

## Evidence basis

[Jira issue NEC-3](https://hotwax-team.atlassian.net/browse/NEC-3). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader.
