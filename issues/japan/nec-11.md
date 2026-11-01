# NEC-11: Updated shipping phone does not reach OMS and broker feed

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

A source phone correction remains stale in OMS and the broker input feed.

## Expected behavior and requirement

Propagate the updated shipping contact without retaining stale active associations.

## RCA and evidence

Workbook TC-041 and TC-042 record a stale phone in OMS, TelecomNumber-linked contacts, and the broker phone field even when postal-address updates succeed. That distinguishes telephone synchronization from postal-address synchronization. The specific service defect and production correction remain unconfirmed.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Compare source shipping contact and active OMS contact associations.
- Trace the emitted broker record after a source edit.
- Test updates both before and after allocation.

## Evidence basis

[Jira issue NEC-11](https://hotwax-team.atlassian.net/browse/NEC-11). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
