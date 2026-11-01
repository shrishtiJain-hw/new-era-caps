# NEC-7: Partial cancellation creates a duplicate reject record

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review in historical mail\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

External fulfillment tracking gains a new reject record instead of updating the prior sent record.

## Expected behavior and requirement

Maintain the correct record identity and transition the existing fulfillment item when appropriate.

## RCA and evidence

The duplicate-versus-update defect is recorded and an OMS PR was linked. The exact implementation and deployment outcome are unverified.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Reproduce send then partial cancellation.
- Inspect record identity and state transitions.
- Verify a duplicate cancellation event does not add another reject row.

## Evidence basis

[Jira issue NEC-7](https://hotwax-team.atlassian.net/browse/NEC-7). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader.
