# Sample Defect Report

## Overview

This document demonstrates a sample defect reporting approach used in a software testing lifecycle.

The defect is fictional and created only for portfolio demonstration purposes.

---

## Defect Details

| Field | Details |
|---|---|
| Defect ID | BUG-001 |
| Summary | Transaction status is not updated after successful submission |
| Module | Business Transaction |
| Environment | QA |
| Severity | Major |
| Priority | High |
| Defect Type | Functional |
| Status | Retest |
| Reported By | QA |
| Assigned To | Development Team |

---

## Preconditions

- User has valid application access.
- Application is available in the QA environment.
- Required test data is available.
- User has permission to create a business transaction.

---

## Steps to Reproduce

1. Login to the application.
2. Navigate to the Business Transaction screen.
3. Create a new transaction.
4. Enter all mandatory information.
5. Submit the transaction.
6. Note the generated transaction/reference number.
7. Search for the submitted transaction.
8. Check the transaction status.

---

## Expected Result

The submitted transaction should be displayed with the correct updated status.

---

## Actual Result

The transaction is successfully submitted, but the status continues to display the previous status.

---

## Business Impact

Users may not be able to determine the actual processing status of the transaction, which could lead to incorrect business decisions or repeated submissions.

---

## Evidence

Typical evidence attached to a defect may include:

- Screenshot
- Execution log
- Test Case ID
- Test data reference
- Application error message
- Relevant timestamp

> No real application screenshots or confidential information are included in this portfolio.

---

## Defect Lifecycle

```text
New
 ↓
Assigned
 ↓
In Progress
 ↓
Fixed
 ↓
Ready for Retest
 ↓
Retest
 ↓
Closed

If the defect is not fixed successfully:

Retest
 ↓
Reopened
 ↓
Assigned
 ↓
Fixed

Retest Result
After the development fix is deployed:
1. Execute the original test case.
2. Verify the transaction status.
3. Confirm the expected result.
4. Execute related regression scenarios.
5. Update the defect status.

Expected Retest Outcome
Pass: Transaction status is updated correctly and the defect can be closed.

Fail: Status remains incorrect and the defect is reopened.

Jira Defect Reporting Approach
A well-documented defect should contain:
- Clear summary
- Environment
- Preconditions
- Reproducible steps
- Expected result
- Actual result
- Severity
- Priority
- Evidence
- Business impact
- Related Test Case ID
This helps development and QA teams investigate and resolve issues efficiently.

QA Best Practices
- Report defects with clear reproduction steps.
- Avoid duplicate defects by checking existing issues.
- Provide sufficient evidence.
- Clearly differentiate severity and priority.
- Link defects to relevant test cases where applicable.
- Retest fixes before closure.
- Perform regression testing for impacted functionality.
