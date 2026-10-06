# Sample Test Data Management

## Overview

This document demonstrates a sample approach to managing test data for Tosca automation.

All data shown below is fictional and created only for portfolio demonstration.

---

## Sample Test Data

| Data ID | User Type | Transaction Type | Status | Expected Result |
|---|---|---|---|---|
| TD-001 | Standard User | Create | Active | Transaction created successfully |
| TD-002 | Standard User | Update | Active | Transaction updated successfully |
| TD-003 | Standard User | Search | Completed | Correct transaction displayed |
| TD-004 | Standard User | Create | Invalid | Validation message displayed |
| TD-005 | Standard User | Search | Invalid | No matching transaction displayed |

---

## Test Data Principles

For automation testing, test data should be:

- Reusable
- Maintainable
- Traceable
- Independent from test logic
- Easy to update
- Suitable for positive and negative scenarios

---

## Tosca Test Data Approach

A Tosca automation solution can use centralized and reusable test data to reduce duplication and improve maintainability.

Typical approach:

1. Identify data requirements from the test scenario
2. Define positive and negative test data
3. Parameterize values where appropriate
4. Separate test data from test logic
5. Reuse data across multiple TestCases
6. Maintain data for regression execution
7. Update data when application requirements change

---

## Example Data Parameterization

```text
Username       → TestUser01
TransactionType → Standard
Quantity       → 10
ReferenceType   → Portfolio
ExpectedStatus  → Completed
