# GreenLeaf Grocers — Checkout Test Cases

## TC-GL-01: Verify Guest Checkout Without Signing In

| Field | Details |
|---|---|
| Test Case ID | TC-GL-01 |
| Linked Story | GL-101 |
| Preconditions | Storefront is accessible, shopper is not signed in, and product is available. |

**Test Steps**

| Step | Action | Expected Result |
|---|---|---|
| 1 | Open the storefront. | Storefront should load successfully. |
| 2 | Add a product to the cart. | Product should be added to the cart. |
| 3 | Open the cart. | Cart should display the selected product. |
| 4 | Proceed to checkout. | Checkout page should open. |
| 5 | Enter all required details. | Checkout details should be accepted. |
| 6 | Click Submit Order. | Order should be submitted successfully. |
| 7 | Observe the confirmation page. | Confirmation page should display the order total and success message. |

---

## TC-GL-02: Verify Required Checkout Field Validation

| Field | Details |
|---|---|
| Test Case ID | TC-GL-02 |
| Linked Story | GL-103 |
| Preconditions | A product is available in the cart, checkout page is open, and required fields are empty. |

**Test Steps**

| Step | Action | Expected Result |
|---|---|---|
| 1 | Leave all required fields empty. | Required fields should remain empty. |
| 2 | Click Submit Order. | Validation should be triggered. |
| 3 | Observe the validation messages. | Messages should identify the missing required fields. |
| 4 | Check whether the confirmation page appears. | Order should not be submitted and confirmation page should not appear. |

---

## TC-GL-03: Verify Invalid Promo Code Handling

| Field | Details |
|---|---|
| Test Case ID | TC-GL-03 |
| Linked Story | GL-102 |
| Preconditions | A product is available in the cart, checkout page is open, and no promo code has been applied. |

**Test Steps**

| Step | Action | Expected Result |
|---|---|---|
| 1 | Note the original order total. | Original order total should be recorded. |
| 2 | Enter the invalid promo code `promo123`. | Promo code should be entered. |
| 3 | Click Apply Promo. | System should validate the promo code. |
| 4 | Observe the validation message. | An appropriate invalid promo code message should appear. |
| 5 | Check the order total. | Order total should remain unchanged. |
