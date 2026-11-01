# NEC-5: Cancellation restores ATP when restocking was disabled

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

OMS restores availability after Shopify cancellation even when the user did not request restocking.

## Expected behavior and requirement

Follow the business-approved restock behavior and preserve separate cancellation and inventory effects.

## RCA and evidence

A restock-intent mismatch is the documented defect. The notification references a connector PR; final production verification is unavailable.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Compare cancellation refund/restock input with inventory events.
- Test restock enabled and disabled.
- Replay the event and check that inventory changes only once.

## Evidence basis

[Jira issue NEC-5](https://hotwax-team.atlassian.net/browse/NEC-5). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader.
