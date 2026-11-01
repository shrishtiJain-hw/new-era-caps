# NEC-14: Partial fulfillment updates fail to synchronize

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

Shopify fulfillment can occur before OMS allocation, leaving partial fulfillment updates unsynchronized.

## Expected behavior and requirement

Agree on allocation timing and fulfillment ownership for this edge case.

## RCA and evidence

A team comment explicitly identifies fulfillment before allocation. It proposes location/routing sync plus brokering configuration, or manual fulfillment in both systems. The options are proposals, not deployed fixes.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Reproduce fulfillment-before-allocation ordering.
- Evaluate routing sync and tag-based brokering together.
- Verify item quantities and partial shipment state in both systems.

## Evidence basis

[Jira issue NEC-14](https://hotwax-team.atlassian.net/browse/NEC-14). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader.
