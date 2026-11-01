# HOLD review status and inventory reservation behavior

**Country:** Japan\
**Brands:** NEC\
**Status:** Successful HOLD examples recorded; specification clarification needed\
**Contribution:** Validation record and investigation synthesis from owner-provided workbook

## Issue and business impact

Early execution findings flagged HOLD orders allocating before approval. Later matrix rows record no OMS soft allocation for held examples, while Shopify still committed inventory.

## Expected behavior and requirement

Keep unapproved orders from fulfillment and clearly distinguish Shopify commitment from OMS allocation.

## RCA and evidence

The matrix records held collaboration, high-value, and restricted orders remaining under review. A single-stock test shows Shopify available stock at zero while OMS still held physical ATP. This can coexist with no OMS soft allocation. The comparison tab also mixes APPROVED and HOLD_RELEASED terminology, which requires clarification.

## Documented actions

1. The workbook compares held orders with approved orders.
2. The single-stock scenario checks storefront availability while the order remains held.
3. A later approval example records transition to soft allocation.

## Outcome and remaining work

Recorded examples support the intended review gate, but the old execution finding and tag-name inconsistency should not be silently erased. No universal reservation guarantee is inferred.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Agree on the canonical release tag.
- Retest storefront availability after an inventory sync while the order remains held.
- Keep approval reversal separate: the matrix states that scenario was not executed.

## Evidence basis

[New Era validation workbook](https://docs.google.com/spreadsheets/d/1imU-emS67yW7hHUxPVRot7L7JBZENkGhJadfAoVDm-w/edit?usp=sharing), XLSX export reviewed November 2, 2026. Results below are recorded UAT observations, not newly executed tests.
