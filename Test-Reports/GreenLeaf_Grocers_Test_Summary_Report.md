# Test Summary Report — GreenLeaf Grocers Checkout Overhaul

## Executive Summary

The GreenLeaf Grocers checkout overhaul project covered guest checkout test design, exploratory UI and API testing, Playwright automation, SQL backend validation, and defect reporting.

Two critical defects remain open. The Playwright guest checkout happy-path test passed, and SQL validation confirmed that the order was successfully persisted.

**Release Recommendation: No-Go** until both critical defects are fixed and verified.

## Scope Tested

- Guest checkout workflow
- Required checkout field validation
- Invalid promo code handling
- Mobile checkout UI
- Promo validation API
- Playwright guest checkout automation
- SQL order persistence validation

## Critical Defects

| Defect ID | Description | Severity | Status |
|---|---|---|---|
| GL-B01 | Apply Promo overlaps Submit Order on mobile viewports below 768px | Critical | Open |
| GL-B02 | Expired promo code `EXPIRED20` causes HTTP 500 from `POST /api/promo/validate` instead of a controlled error response | Critical | Open |

## Automation Results

- Playwright guest checkout happy-path test: **1 passed**
- The test used `capstone.guest@example.test`.
- No promo code was applied during this test.

## Backend Validation

SQL validation confirmed a persisted order for `capstone.guest@example.test`:

- Order status: `placed`
- Total amount: `4.99`
- Promo applied: `0`

## Defect and Traceability

The local Git workflow created a pull request linked to Jira story `GL-101`. Its recorded status was **In Review**.

## Release Recommendation

**No-Go**

Although the guest checkout automation passed and backend persistence was confirmed, both critical defects remain unresolved. Production release should be reconsidered only after GL-B01 and GL-B02 are fixed and regression testing passes.
