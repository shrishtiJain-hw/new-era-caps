# NEC-17: Smaregi inventory reset rejects facility or location identifiers

**Country:** Japan\
**Brands:** NEC\
**Status:** In Progress\
**Contribution:** Assigned investigation owner

## Issue and business impact

Daily inventory reset produces invalid external-facility or location-sequence errors.

## Expected behavior and requirement

Resolve source location identity to the intended active OMS location before applying inventory.

## RCA and evidence

The assignment notification confirms my ownership of this investigation. The exact bad mapping and a successful correction are not available in the reviewed record.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.
2. The mail assignment identifies Shrishti Jain as the assignee.

## Outcome and remaining work

The recorded status is a workflow state, not proof of production resolution. The checks below describe a proposed investigation and acceptance approach, rather than actions claimed as already executed.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Compare source location values with configured external IDs and location sequences.
- Distinguish absent mapping, inactive location, and mismatched identifier types.
- Retest a targeted reset before broader inventory processing.

## Evidence basis

[Jira issue NEC-17](https://hotwax-team.atlassian.net/browse/NEC-17). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader.
