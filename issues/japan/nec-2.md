# NEC-2: Draft orders without a shipping address fail import

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

A draft order created without shipping details does not reach OMS.

## Expected behavior and requirement

Handle required address fields explicitly according to order type; an absent address should produce either a supported import or a clear validation result.

## RCA and evidence

The title establishes the missing-address trigger. The exact failing expression is unavailable. A related PR is referenced in the email notifications.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Reproduce address-present and address-absent drafts.
- Trace validation and transformation behavior before order creation.
- Verify existing supported draft scenarios remain importable.

## Evidence basis

[Jira issue NEC-2](https://hotwax-team.atlassian.net/browse/NEC-2). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader.
