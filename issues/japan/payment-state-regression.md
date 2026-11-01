# Payment and cancellation retests show mixed outcomes

**Country:** Japan\
**Brands:** NEC\
**Status:** Open regression observations in payment retest tab\
**Contribution:** Validation record and investigation synthesis from owner-provided workbook

## Issue and business impact

After an earlier payment fix, some cancellation and COD scenarios still produced duplicate status records or failed to update cancellation state.

## Expected behavior and requirement

Retain each payment/refund event with the appropriate status history and update cancellation without duplicating authorization or settlement states.

## RCA and evidence

The payment tab records correct standard authorization and partial cancellation examples, but also repeated incorrect COD/payment states, missing cancellation propagation, and missing refund history in some paths. These differ from the later successful cumulative-refund matrix example and cannot be reduced to one all-pass result.

## Documented actions

1. Reviewed the scenario-by-scenario payment retest observations.
2. Separated OrderStatus history from OrderPaymentPreference state.
3. Preserved failures and the later successful refund example as distinct observations rather than asserting a global fix.

## Outcome and remaining work

The source supports a regression investigation. It does not provide a single versioned result that resolves every conflicting entry.

## Recommended validation and prevention

The following checks are proposed follow-up guidance unless explicitly confirmed above.

- Retest cancellation before and after broker generation.
- Compare order-status history with payment preference and refund transactions.
- Record build and event order for each observed regression.

## Evidence basis

[New Era validation workbook](https://docs.google.com/spreadsheets/d/1imU-emS67yW7hHUxPVRot7L7JBZENkGhJadfAoVDm-w/edit?usp=sharing), XLSX export reviewed November 2, 2026. Results below are recorded UAT observations, not newly executed tests.
