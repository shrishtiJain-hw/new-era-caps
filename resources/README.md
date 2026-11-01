# New Era Japan project resources

| Resource | Purpose | Review coverage |
| --- | --- | --- |
| [Phase 2 validation spreadsheet](https://docs.google.com/spreadsheets/d/1imU-emS67yW7hHUxPVRot7L7JBZENkGhJadfAoVDm-w/edit?usp=sharing) | Scope, environment, validation approach, and follow-up work | All eight tabs inspected from XLSX export; scenario results summarized separately |
| [Real-time order synchronization presentation](https://docs.google.com/presentation/d/1zv4P6yhyiCQbLJNhZZQ2xo-4gOFl3Rp_4CUT0J3UODY/edit?usp=sharing) | Architecture, tags, order customizations, fulfillment exceptions, and scenarios | Full text export inspected; visual layout not reviewed |
| [NEC Jira project list](https://hotwax-team.atlassian.net/jira/software/projects/NEC/list?jql=project%20%3D%20NEC%20ORDER%20BY%20cf%5B10019%5D%20ASC) | Live work tracking | Screenshot and notification emails used; live board not fetched |

These are owner-provided references. Access to linked systems remains governed by their sharing settings. No raw mailbox data or private source exports are copied into this repository.

## Architecture and business rules

The presentation describes Shopify webhook delivery through Amazon SQS, consumption by Maarg, and transformation into HotWax OMS. It covers HOLD/APPROVED review control, delivery dates and slots, COD fee handling, customer notes, membership attributes, and fulfillment/replacement exceptions.

Treat queue delivery, duplicate prevention, timing, and financial rounding as behaviors to validate. The deck's absolute reliability and latency statements are not measured results in this portfolio. Its fee-split description requires confirmation against the approved calculation and rounding rules.

## Source inconsistencies retained as open questions

- The presentation table lists TC-001 through TC-022, while speaker text describes fourteen cases and successful execution of all cases. Those claims cannot establish a consistent executed-test count.
- Descriptions of HOLD orders differ on whether inventory is reserved. Confirm the intended allocation behavior with the operational owner.
- The spreadsheet states UAT completed but its detailed matrix includes failures, unexecuted cases, and blank actual results. Overview completion does not close every issue or establish production sign-off.

See the [validation matrix](validation-matrix.md) and [Phase 2 case study](../requirements/japan/phase-2-realtime-sync-validation.md).

## Workbook tab coverage

| Tab | Review focus |
| --- | --- |
| Rollout strategy | Environment, objective, validation scope, and remaining checks |
| Rollback plan | Reversal notes for billing capture and reshipping query changes |
| Test case matrix | 53 scenario rows with actual observations |
| Payment scenarios after fix | 18 payment/cancellation regression scenarios |
| Broker Feed Comparison | Production/UAT field behavior, billing capture, payment mappings, and charge discrepancies |
| Execution summary | Proposed transformation and allocation fixes, plus outstanding observations |
| Issue Tracker | Nine issue rows with historical workbook states |
| Hold Tag Synchronization Compar | Legacy and new review-tag paths, including inconsistent release-tag terminology |

The matrix example records a 700 fee plus 70 tax equalling a 770 gross charge. Do not substitute a 90/10 split of the gross charge merely because the deck uses that wording. This is a source-consistency check, not tax advice.
