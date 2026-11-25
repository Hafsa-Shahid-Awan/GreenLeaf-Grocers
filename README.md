
# GreenLeaf Grocers — Checkout Overhaul

**QA Capstone Project | Microsoft Junior SQA Professional Certificate**

## Project Overview

This project focuses on quality assurance activities for the GreenLeaf Grocers checkout overhaul. It covers QA planning, guest checkout test design, exploratory UI and API testing, Playwright automation, SQL database validation, defect reporting, and release readiness assessment.

## Project Scope

- QA strategy and test planning using Jira
- Guest checkout test design using Zephyr
- Exploratory testing of checkout workflows
- UI and API defect identification and documentation
- Playwright automation of the guest checkout happy path
- SQL validation of persisted checkout orders
- Test summary and release recommendation

## Tools & Technologies

- Jira
- Zephyr
- Playwright
- SQL
- SQLite
- Git

## Key Findings

Two critical defects were identified during testing:

| Defect ID | Description | Severity | Status |
|---|---|---|---|
| GL-B01 | Apply Promo control overlaps Submit Order on mobile viewports below 768px | Critical | Open |
| GL-B02 | Promo validation API returns HTTP 500 for expired promo code `EXPIRED20` | Critical | Open |

## Automation & Database Validation

- Executed one Playwright automated happy-path test for guest checkout.
- Test execution result: **1 Passed**.
- Performed SQL validation to confirm that the guest checkout order was successfully persisted in the database.

## Test Summary

Both critical defects remained unresolved at the time of reporting.

**Release Recommendation: NO-GO**

Production release was not recommended until both critical defects were fixed and successfully verified through regression testing.

## Project Context

This project was completed as part of the Microsoft Junior SQA Professional Certificate capstone.

**Note:** Git and Jira traceability in the capstone used a local simulated workflow, not live cloud-hosted pull requests or Jira tickets.
