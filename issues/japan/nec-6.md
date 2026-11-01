# NEC-6: Reshipping selection missed rejected-item parking

**Country:** Japan\
**Brands:** NEC\
**Status:** In Review in historical mail\
**Contribution:** Project issue reference; individual implementation not established

## Issue and business impact

Partially cancelled lines move to rejected-item parking while the reshipping flow selects a different parking queue.

## Expected behavior and requirement

Make reshipping eligibility agree with the actual cancellation-routing destination.

## RCA and evidence

The team comment explicitly calls for the NiFi query to use rejected-item parking. It separately notes a broken ViewOrder display despite correct database records.

## Documented actions

1. The issue and its recorded state were reviewed from the supplied board snapshot and available Jira notification emails.

## Outcome and remaining work

Workbook TC-031 records a successful UAT reshipping retest after correcting the outdated NiFi queue selection from general parking to rejected-item parking. The Rollback plan records the query change and its reversal option. This adds executed UAT evidence to the earlier proposal. Production closure and resolution of the separate ViewOrder display defect are not established.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Review cancellation destination and reshipping selection together.
- Validate one partial cancellation followed by replacement.
- Track the UI display defect independently from data correctness.

## Evidence basis

[Jira issue NEC-6](https://hotwax-team.atlassian.net/browse/NEC-6). Board screenshot supplied November 2, 2026; historical notification emails supplement the snapshot. Live Jira content was unavailable through the available web reader. Additional scenario evidence comes from the eight-tab validation workbook.
