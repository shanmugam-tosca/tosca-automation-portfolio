# Tosca Automation Approach

## Overview

This document describes a sample approach for designing and maintaining automated tests using **Tricentis Tosca**.

The approach focuses on reusable components, maintainability, test data management and reliable regression execution.

> All examples are fictional and created for portfolio demonstration purposes.

---

## 1. Requirement Analysis

The automation process starts with understanding the business requirement and identifying:

- Business workflows
- Functional requirements
- Positive scenarios
- Negative scenarios
- Integration points
- Regression scope
- Data requirements

Test scenarios are then mapped to the relevant requirements.

---

## 2. Application Scanning and Module Creation

The required application screens and controls are identified and modeled as reusable Tosca Modules.

Typical activities include:

- Scan application screens
- Identify controls
- Create Modules
- Rename controls with meaningful names
- Remove unnecessary technical objects
- Maintain reusable Modules

### Example

```text
Login Module
├── Username
├── Password
└── Login Button

Transaction Module
├── Transaction Type
├── Reference Number
├── Quantity
├── Submit Button
└── Status

3. Test Case Design
Reusable Modules are combined to create business-oriented Tosca TestCases.
Example:
TC_Create_Transaction

Login Module
      ↓
Transaction Navigation Module
      ↓
Create Transaction Module
      ↓
Enter Test Data
      ↓
Submit Transaction
      ↓
Verify Status

The TestCase should represent a complete business scenario rather than individual technical actions.

4. Test Step Blocks
Reusable Test Step Blocks can be created for common activities.
Examples:
- Login
- Application Navigation
- Create Transaction
- Search Transaction
- Logout
This reduces duplication and makes automation easier to maintain.

5. Test Data Management
Test data is separated from test logic wherever possible.
Examples of reusable test data include:
- User credentials
- Transaction types
- Reference values
- Business dates
- Quantities
- Expected statuses
The same automation logic can therefore be executed with multiple data combinations.

6. Verification and Validation
Automated tests should contain appropriate verification points.
Examples:
- Verify page navigation
- Verify field values
- Verify transaction number
- Verify status
- Verify success/error messages
- Verify downstream results
Assertions should focus on meaningful business outcomes.

7. Execution Lists
Tosca ExecutionLists can be organized based on testing requirements.
Example:
ExecutionList
│
├── Smoke Suite
│   ├── Login
│   ├── Navigation
│   └── Basic Transaction
│
├── Functional Suite
│   ├── Create Transaction
│   ├── Update Transaction
│   └── Search Transaction
│
└── Regression Suite
    ├── End-to-End Scenarios
    ├── Positive Scenarios
    └── Negative Scenarios

8. Test Execution
During execution, results are reviewed to identify:
- Passed tests
- Failed tests
- Technical failures
- Application defects
- Environment issues
- Test data issues
Failed executions are analyzed before raising defects.

9. Defect Management
Application defects are reported with sufficient information for investigation.
Typical defect information:
- Summary
- Environment
- Test Case ID
- Steps to reproduce
- Expected result
- Actual result
- Severity
- Priority
- Evidence
- Business impact
Defects can be tracked using tools such as Jira.

10. Regression Testing
After application changes or defect fixes, relevant regression suites are executed.
Regression automation helps validate that existing functionality continues to work after changes.
Typical regression cycle:
Requirement Change
       ↓
Impact Analysis
       ↓
Update Automation
       ↓
Execute Regression Suite
       ↓
Analyze Results
       ↓
Defect Reporting
       ↓
Retest
       ↓
Regression Closure

11. Automation Maintenance
Automation assets should be reviewed regularly.
Maintenance activities include:
- Updating changed application controls
- Removing obsolete Modules
- Updating test data
- Updating TestCases
- Reviewing failed executions
- Improving reusable components
- Maintaining ExecutionLists

12. Quality Practices
A maintainable Tosca automation solution should follow these principles:
- Reusability
- Maintainability
- Readability
- Modularity
- Data separation
- Meaningful naming conventions
- Minimal duplication
- Business-focused validation
Automation Lifecycle
Requirement Analysis
        ↓
Test Scenario Identification
        ↓
Module Creation
        ↓
TestCase Design
        ↓
Test Data Preparation
        ↓
Test Step Block Reuse
        ↓
ExecutionList Creation
        ↓
Test Execution
        ↓
Result Analysis
        ↓
Defect Management
        ↓
Regression Testing
        ↓
Maintenance

Summary
A structured Tosca automation approach helps create scalable and maintainable automated testing solutions.
The key focus areas are:
- Reusable Modules
- Business-oriented TestCases
- Test Step Blocks
- Test Data Management
- ExecutionLists
- Meaningful validations
- Regression automation
- Continuous maintenance
