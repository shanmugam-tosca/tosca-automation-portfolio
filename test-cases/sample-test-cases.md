# Sample Test Cases

## Overview

This document contains sample functional and regression test cases for a fictional SAP Fiori-style business application.

All test data is fictional and created for portfolio demonstration purposes.

---

## TC-001 – Successful User Login

**Test Type:** Functional / Smoke  
**Priority:** High

### Test Steps

| Step | Action | Expected Result |
|---|---|---|
| 1 | Open the application | Login page is displayed |
| 2 | Enter valid username | Username is accepted |
| 3 | Enter valid password | Password is accepted |
| 4 | Click Login | User is successfully authenticated |
| 5 | Verify home page | Application home page is displayed |

---

## TC-002 – Create Business Transaction

**Test Type:** Functional / E2E  
**Priority:** High

### Test Steps

| Step | Action | Expected Result |
|---|---|---|
| 1 | Login to the application | User is logged in successfully |
| 2 | Navigate to transaction creation | Transaction screen is displayed |
| 3 | Enter valid business data | Data is accepted |
| 4 | Click Submit | Transaction is submitted |
| 5 | Verify reference number | Unique reference number is generated |
| 6 | Verify transaction status | Correct status is displayed |

---

## TC-003 – Mandatory Field Validation

**Test Type:** Negative Testing  
**Priority:** High

### Test Steps

| Step | Action | Expected Result |
|---|---|---|
| 1 | Navigate to transaction creation | Transaction screen is displayed |
| 2 | Leave mandatory field blank | Field remains empty |
| 3 | Click Submit | Submission is prevented |
| 4 | Verify validation message | Appropriate error message is displayed |

---

## TC-004 – Search Existing Transaction

**Test Type:** Functional / Regression  
**Priority:** Medium

### Test Steps

| Step | Action | Expected Result |
|---|---|---|
| 1 | Navigate to transaction search | Search screen is displayed |
| 2 | Enter transaction number | Number is accepted |
| 3 | Execute search | Matching transaction is displayed |
| 4 | Verify transaction details | Details match the submitted transaction |
| 5 | Verify status | Current transaction status is displayed |

---

## TC-005 – Invalid Transaction Search

**Test Type:** Negative Testing  
**Priority:** Medium

### Test Steps

| Step | Action | Expected Result |
|---|---|---|
| 1 | Navigate to transaction search | Search screen is displayed |
| 2 | Enter invalid reference number | Invalid number is accepted |
| 3 | Execute search | No matching transaction is displayed |
| 4 | Verify message | Appropriate no-results message is displayed |

---

## Test Case Coverage

| Test Case | Functional | Negative | E2E | Regression | Priority |
|---|---:|---:|---:|---:|---|
| TC-001 | ✓ |  |  | ✓ | High |
| TC-002 | ✓ |  | ✓ | ✓ | High |
| TC-003 |  | ✓ |  | ✓ | High |
| TC-004 | ✓ |  |  | ✓ | Medium |
| TC-005 |  | ✓ |  | ✓ | Medium |

---

## Tosca Automation Mapping

These test cases can be converted into Tosca automated TestCases using:

- Reusable Modules
- Test Step Blocks
- Parameterized test data
- Buffers for dynamic values
- Verification checkpoints
- Execution Lists
- Reusable components
- Regression execution
