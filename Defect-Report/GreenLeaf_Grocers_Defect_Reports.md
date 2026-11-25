# GreenLeaf Grocers — Defect Reports

## GL-B01: Mobile Checkout UI Overlap

| Field | Details |
|---|---|
| Defect ID | GL-B01 |
| Title | Apply Promo overlaps Submit Order on mobile checkout |
| Severity | Critical |
| Status | Open |
| Area | Checkout — UI |
| Environment | Chrome, mobile viewport below 768px |

**Description**

On mobile checkout, the Apply Promo control overlaps the Submit Order button, creating a usability issue that may interfere with order submission.

**Steps to Reproduce**

| Step | Action |
|---|---|
| 1 | Open the GreenLeaf Grocers storefront in Chrome. |
| 2 | Set the viewport width to 375px. |
| 3 | Add a product to the cart. |
| 4 | Open the checkout page. |
| 5 | Observe the Apply Promo and Submit Order controls. |

**Expected Result**

Apply Promo and Submit Order controls should be properly positioned, clearly visible, and independently usable without overlapping.

**Actual Result**

Apply Promo overlaps the Submit Order button at mobile viewport widths below 768px.

---

## GL-B02: Promo API Returns HTTP 500 for Expired Code

| Field | Details |
|---|---|
| Defect ID | GL-B02 |
| Title | Promo validation API returns HTTP 500 for expired promo code |
| Severity | Critical |
| Status | Open |
| Area | Promo Validation — API |
| Endpoint | `POST /api/promo/validate` |
| Test Data | `EXPIRED20` |

**Description**

When the expired promo code `EXPIRED20` is submitted for validation, the API returns HTTP 500 instead of handling the expired code with a controlled client error response.

**Steps to Reproduce**

| Step | Action |
|---|---|
| 1 | Send a POST request to `/api/promo/validate`. |
| 2 | Set the request Content-Type to `application/json`. |
| 3 | Submit the request body containing the code `EXPIRED20`. |
| 4 | Observe the API response status code. |

**Request Body**

```json
{
  "code": "EXPIRED20"
}
```

**Expected Result**

The API should handle the expired promo code gracefully and return a controlled HTTP 400 response with an appropriate error message.

**Actual Result**

The API returns HTTP 500 for the expired promo code.

---

## Defect Summary

| Defect ID | Defect | Severity | Status |
|---|---|---|---|
| GL-B01 | Mobile checkout UI overlap | Critical | Open |
| GL-B02 | Promo API HTTP 500 error | Critical | Open |
