![NEW ERA CAPS engineering portfolio](assets/banner.svg)

# NEW ERA CAPS

Japan-only commerce operations, real-time integration validation, and issue investigations.

**Shrishti Jain** · Product Associate · Business analysis and commerce operations

**24 case studies** · 21 issues and investigations · 3 requirements and delivery records\
Last curated: November 2, 2026

## Coverage and navigation

**Market: Japan only.**

- [Japan issues](issues/japan/README.md)
- [Japan requirements](requirements/japan/README.md)
- [Project resources and source review](resources/README.md)
- [Phase 2 validation matrix](resources/validation-matrix.md)

The supplied board snapshot shows four To Do, two In Progress, seven In Review, and zero Done items. Historical email adds two other issue references. These workflow statuses do not establish production closure.


## Case study register

| Case | Country | Brand scope | Recorded status |
| --- | --- | --- | --- |
| [Billing contact information absent from broker output](issues/japan/billing-contact-feed-population.md) | Japan | NEC | Billing fields populated after store-setting change in UAT |
| [HOLD review status and inventory reservation behavior](issues/japan/hold-allocation-and-reservation.md) | Japan | NEC | Successful HOLD examples recorded; specification clarification needed |
| [NEC-10: COD fees absent from the OMS summary total](issues/japan/nec-10.md) | Japan | NEC | To Do |
| [NEC-11: Updated shipping phone does not reach OMS and broker feed](issues/japan/nec-11.md) | Japan | NEC | In Review |
| [NEC-12: Order contact retains an old customer email](issues/japan/nec-12.md) | Japan | NEC | In Review |
| [NEC-13: Post-import order discount edits do not synchronize](issues/japan/nec-13.md) | Japan | NEC | To Do |
| [NEC-14: Partial fulfillment updates fail to synchronize](issues/japan/nec-14.md) | Japan | NEC | In Review |
| [NEC-15: Customer reassociation duplicates broker detail rows](issues/japan/nec-15.md) | Japan | NEC | In Progress |
| [NEC-16: BI/BW feed uses SKU and omits shipping-charge rows](issues/japan/nec-16.md) | Japan | NEC | To Do |
| [NEC-17: Smaregi inventory reset rejects facility or location identifiers](issues/japan/nec-17.md) | Japan | NEC | In Progress |
| [NEC-2: Draft orders without a shipping address fail import](issues/japan/nec-2.md) | Japan | NEC | In Review |
| [NEC-3: Payment authorization status missing after real-time import](issues/japan/nec-3.md) | Japan | NEC | In Review |
| [NEC-4: Delivery preferences prevent order import](issues/japan/nec-4.md) | Japan | NEC | In Review |
| [NEC-5: Cancellation restores ATP when restocking was disabled](issues/japan/nec-5.md) | Japan | NEC | In Review |
| [NEC-6: Reshipping selection missed rejected-item parking](issues/japan/nec-6.md) | Japan | NEC | In Review in historical mail |
| [NEC-7: Partial cancellation creates a duplicate reject record](issues/japan/nec-7.md) | Japan | NEC | In Review in historical mail |
| [NEC-8: Empty brokered files generated beside valid output](issues/japan/nec-8.md) | Japan | NEC | To Do |
| [Payment and cancellation retests show mixed outcomes](issues/japan/payment-state-regression.md) | Japan | NEC | Open regression observations in payment retest tab |
| [Post-import edits reveal incomplete synchronization](issues/japan/post-import-line-and-customer-updates.md) | Japan | NEC | Mixed results recorded; additional defects remain open |
| [Recovering shipment result processing](issues/japan/shipment-results-recovery.md) | Japan | NEC | Affected orders reprocessed; recurrence investigation open |
| [Imported orders bypassed the intended brokering queue](issues/japan/unexpected-immediate-allocation.md) | Japan | NEC | Recorded Done in workbook issue tracker |
| [Order state aware feed validation](requirements/japan/feed-validation.md) | Japan | NEC | Validation findings and available files shared |
| [Order synchronization and fulfillment workflow knowledge](requirements/japan/order-sync-workflows.md) | Japan | NEC | Documented learning and QA contribution |
| [Phase 2 real-time order synchronization validation](requirements/japan/phase-2-realtime-sync-validation.md) | Japan | NEC | Source overview reports UAT complete; follow-up scenarios remain |

## Reading the record

Each new case separates the issue, expected behavior, RCA, documented actions, outcome, and recommended validation. Earlier cases retain their implementation narrative and explicit RCA/action additions. Proposed checks are not claimed as executed. An open RCA remains open even when a particular order or feed was recovered.

Personal contributions, customer confirmations, and team implementations retain their separate attribution. Cases with unknown brand scope are labelled accordingly. This is a curated record, not automatic mailbox monitoring.

Use the [case template](templates/case-study.md) and [contribution guide](CONTRIBUTING.md) for future additions. Routine employee creation and administrative provisioning are excluded.

This personal portfolio is independently prepared and unaffiliated with the brands. Raw mail, production payloads, credentials, and private customer/contact details are excluded.
