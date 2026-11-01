# Phase 2 recorded validation results

The workbook’s **Test case matrix** contains **53 scenario rows**: TC-001 through TC-052 plus TC-SFS. This table paraphrases its actual-result cells and comments. Results are source-recorded UAT observations, not tests rerun while preparing the portfolio.

The presentation’s shorter 22-case table and speaker reference to fourteen cases are different source summaries. Neither establishes that all 53 workbook scenarios passed. Blank results, observed failures, and explicitly unexecuted scenarios remain visible below.

| Source scenario | Scenario | Recorded result and limit |
| --- | --- | --- |
| TC-001 | Create Standard Shipping Order in Shopify | Import and later allocation recorded. |
| TC-002 | Create COD Order | COD import and later allocation recorded. |
| TC-003 | Validate COD Fee Split | Recorded adjustments: 700 fee + 70 fee tax = 770 total charge. The deck’s 90/10 wording does not express this example accurately. |
| TC-004 | Validate Delivery Date and Delivery Time Slot Mapping | Import with date and slot recorded. |
| TC-005 | Validate Delivery Date Mapping | Import with date recorded. |
| TC-006 | Validate Delivery Time Slot mapping | Import with slot recorded; comment also says this case may be skipped, so acceptance needs reconciliation. |
| TC-007 | Validate Customer Notes Mapping | Online note absent by checkout design; draft-order note recorded in OMS. |
| TC-008 | Validate Membership Attributes Mapping | Membership attribute synchronized. |
| TC-SFS | Validate SFS order | SFS tag drove store allocation in the recorded test. |
| TC-009 | Validate HOLD Tag Assignment for Yohji Product Order | Collaboration order held without OMS soft allocation. |
| TC-010 | Validate HOLD Tag Assignment for High Value Order (> ¥70,000) | High-value order held without OMS soft allocation. |
| TC-011 | Validate HOLD Tag Assignment for Delivery Restriction Order (配達指定不可) | Restricted-delivery order held without OMS soft allocation. |
| TC-012 | Validate APPROVED Tag Assignment for Eligible Order | Eligible approval behavior recorded. |
| TC-013 | Validate HOLD → APPROVED Synchronization | Held order became allocatable after approval. |
| TC-014 | Validate APPROVED → HOLD Synchronization | Explicitly not executed: source says it is outside the intended workflow. |
| TC-015 | Validate tag assginment for an order with a mix of products - Yohji product with other products | Mixed basket held at order level. |
| TC-016 | Add multiple tags at once from shopify after order import | Multiple tags synchronized; source records a pass. |
| TC-017 | Validate inventory availability for HOLD order | Shopify stock committed while OMS showed unallocated ATP; storefront remained unavailable. |
| TC-018 | Process 10 orders simultaneously | Ten simultaneous orders imported in the recorded test. |
| TC-019 | Process 50 orders simultaneously | Fifty simultaneous orders imported in the recorded test. |
| TC-020 | Simulate queue delay | No delay observed; this does not demonstrate simulated-delay recovery. |
| TC-021 | Verify no order loss | Source-to-OMS order presence recorded. |
| TC-022 | Verify no duplicate orders | No duplicates observed in the recorded test. |
| TC-023 | Missing customer note | Import without customer note recorded. |
| TC-024 | Missing delivery slot | Import without delivery slot recorded. |
| TC-025 | OMS service unavailable | Actual result blank; outage recovery unverified. |
| TC-026 | SQS processing interruption | Actual result blank; interruption recovery unverified. |
| TC-027 | Shopify → Webhook → SQS → OMS | Webhook/SQS/OMS import recorded. |
| TC-028 | Shopify HOLD Tag → OMS | Hold sync without allocation recorded. |
| TC-029 | Shopify APPROVED Tag → OMS | Approval synchronization and eligibility recorded. |
| TC-030 | Complete Flow Validation for Order Sync | Actual result blank; complete end-to-end scenario unverified. |
| TC-031 | Partial cancellation in a multi-item order | Initial reshipping failure; successful retest after NiFi queue query change. |
| TC-032 | Full order cancellation with RESTOCK option enabled | Cancellation with restock released inventory as expected. |
| TC-033 | Full order cancellation with no RESTOCK option selected. | Failure: stock returned to ATP despite no-restock selection. |
| TC-034 | Successful fulfillment updates from Shopify to OMS Shopify ( Fulfilled ) => OMS ( Completed ) | Shopify fulfillment reached completed/shipped OMS state. |
| TC-035 | Successful fulfillment updates from OMS to Shopify OMS ( Completed ) = > Shopify ( Fulfilled ) | WMS SR consumption completed OMS order and updated Shopify fulfillment. |
| TC-036 | Update Shopify order by adding an item to an existing order. | New item imported and allocated, but broker feed history was missing. |
| TC-037 | Validate an order immediately cancelled from Shopify before import into oms | Immediate source cancellation imported and cancelled in OMS. |
| TC-038 | Edit the shipping address in Shopify after order is imported in OMS | Shipping-address update recorded; captured billing address retained. |
| TC-039 | Edit the Shipping address in Shopify after broker feed for that order was already generated | Post-broker shipping-address update recorded; no additional broker file generated. |
| TC-040 | Update customer's email address on Shopify by editing contact information. | Party email updated; order contact retained old email. Broker feed has no email field. |
| TC-041 | Update phone number by editing shipping address on Shopify | Failure: changed shipping phone did not reach OMS contacts or broker output. |
| TC-042 | Update complete shipping address after order is imported into OMS | Postal address updated; telephone data remained stale. |
| TC-043 | Edit the order by adding a discount from Shopify after order is imported into OMS | Failure: post-import discount did not reach OMS. |
| TC-044 | Edit the order by removing the shipping charge from Shopify after order is imported into OMS | Failure: removed shipping charge did not reduce OMS total. |
| TC-045 | Fulfill an item from Shopify before / after brokering in a multi item order scenario | Failure: partially fulfilled item remained Approved in OMS. |
| TC-046 | Edit the customer first name/last name from Shopify after the order gets imported into OMS. The order should have same billing and shipping addresses. | Name and shipping-location updates recorded; billing location retained. |
| TC-047 | Remove customer from Shopify order after import | Failure: customer removal left an active OMS order role. |
| TC-048 | Remove existing customer → Link a different customer to an existing Shopify order | Customer reassociation correct; duplicate fulfillment rows and broker details created. |
| TC-049 | Edit shipping address on a partially fulfilled order | Actual result blank; partial-fulfillment address edit unverified. |
| TC-050 | Order with one discounted item and one non-discounted item | Failure: line discount adjustment absent and totals unchanged. |
| TC-051 | Multiple refunds on the same order refund 1 : X amount refund 2 : Y amount refund 3 : Refund the item as well as shipping fee without restock (eventually leading to cancellation) | Three refund transactions retained and cumulative refund reconciled; cancellation/no-restock behavior recorded successful in this example. |
| TC-052 | BI/BW feed files are not generated as expected in New Order Sync | Failure: SKU used instead of UPC and shipping/tax charge row absent. |

## Retest evidence

The separate Payment scenarios after fix tab records eighteen payment/cancellation scenarios dated July 23–24. Some contain “resolved” followed by “again incorrect” observations. Preserve retest sequence and build information before reconciling these with later matrix successes.

## Acceptance follow-up

Attach build/version and execution dates to each result, retest unresolved monetary and contact changes, and complete the blank outage/interruption/end-to-end scenarios. A no-delay observation does not establish recovery under an induced delay. The spreadsheet’s recorded cleanup and rollback instructions are source plans; no deletion or configuration change was performed for this portfolio.

[Original validation workbook](https://docs.google.com/spreadsheets/d/1imU-emS67yW7hHUxPVRot7L7JBZENkGhJadfAoVDm-w/edit?usp=sharing)
