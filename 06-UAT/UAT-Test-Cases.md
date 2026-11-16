# User Acceptance Testing (UAT) – Test Cases

## 1. Purpose

This document defines proposed User Acceptance Testing (UAT) scenarios for the IT Service Request and Help Desk Workflow Monitoring and Reporting solution.

The objective is to verify that the proposed reporting features meet the functional requirements documented in the FRD.

**Testing status:** Test cases are designed for portfolio demonstration. They have not been executed against a live production system.

## 2. UAT Scope

The proposed testing covers:

- Ticket volume and category reporting
- Priority distribution and filtering
- Ticket status monitoring
- Resolution duration analysis
- Long-processing ticket identification
- Assignment activity analysis
- Workflow transition analysis
- Historical ticket trends
- Consolidated operational reporting

## 3. UAT Test Cases

| Test Case ID | Requirement ID | Test Scenario | Expected Result |
|---|---|---|---|
| UAT-001 | FR-001 | Verify total ticket count | System displays the correct count of unique tickets. |
| UAT-002 | FR-002 | Verify ticket count by issue type | Tickets are grouped under the corresponding issue types. |
| UAT-003 | FR-003, FR-005 | Filter tickets by priority | Reports display records matching the selected priority. |
| UAT-004 | FR-008, FR-009 | Filter tickets by status | Reports display tickets matching the selected status. |
| UAT-005 | FR-010 | Identify tickets without a resolution timestamp | Tickets with missing resolution timestamps are identified separately. |
| UAT-006 | FR-012, FR-013 | Verify resolution duration calculation | Duration is calculated using valid creation and resolution timestamps. |
| UAT-007 | FR-014 | Identify long-processing tickets | Tickets exceeding the configured analysis threshold are flagged. |
| UAT-008 | FR-020, FR-021 | Review assignment activity | Assignment records and contributor counts are displayed accurately. |
| UAT-009 | FR-017, FR-019 | Review workflow transitions | Workflow transition counts are displayed and repeated transitions can be identified. |
| UAT-010 | FR-024, FR-025 | Review monthly ticket trends | Ticket volumes are grouped by month using the created date. |
| UAT-011 | FR-026 | Apply report filters | Selected filters produce the corresponding report results. |
| UAT-012 | FR-027 | Verify consolidated reporting | The reporting view presents the defined operational metrics together. |

## 4. Detailed Test Case Example

### UAT-006: Verify Resolution Duration Calculation

**Requirement:** FR-012, FR-013

**Preconditions:**
- Ticket creation timestamp is available.
- Ticket resolution timestamp is available.
- Both timestamps contain valid date and time values.

**Test Steps:**
1. Select a ticket with valid creation and resolution timestamps.
2. Retrieve the creation timestamp.
3. Retrieve the resolution timestamp.
4. Calculate the difference between the two timestamps.
5. Compare the calculated duration with the reported resolution duration.

**Expected Result:**

The reported resolution duration matches the difference between the valid creation and resolution timestamps.

Tickets with missing or invalid timestamps should be excluded from the valid duration calculation or flagged for review.

## 5. Defect and Issue Tracking Template

| Defect ID | Test Case ID | Issue Description | Severity | Status |
|---|---|---|---|---|
| DEF-001 | UAT-006 | To be recorded if an incorrect duration is identified | To be assigned | Not Tested |

*This is a sample defect-tracking template, not a record of an actual defect.*

## 6. UAT Sign-off

| Role | Responsibility | Sign-off Status |
|---|---|---|
| Business User | Review whether reporting meets business needs | Pending |
| Business Analyst | Validate requirements and expected results | Pending |
| Development Team | Address reported defects | Pending |

## 7. Assumptions and Limitations

- Test cases are proposed based on the documented FRD.
- Testing has not been performed against a live application.
- Historical dataset records may be used to prepare sample test data.
- SLA compliance is excluded because approved SLA targets and business calendar rules are not available.
- Actual test results, defects and sign-off will be recorded only after execution.
