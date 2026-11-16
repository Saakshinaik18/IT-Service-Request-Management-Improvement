# Functional Requirements Document (FRD)
## IT Service Request and Help Desk Workflow Improvement

| Document Information | Details |
|---|---|
| Project Name | IT Service Request and Help Desk Workflow Improvement |
| Document Type | Functional Requirements Document |
| Version | 1.0 |
| Status | Draft |
| Project Type | Independent Business Analysis Case Study |
| Business Domain | IT Service Management |
| Proposed Solution | Help Desk Operations Monitoring and Reporting |
| Data Source | Anonymized Help Desk Tickets Dataset |
| Prepared By | Independent Business Analyst |

---

## 1. Introduction

### 1.1 Purpose

The purpose of this Functional Requirements Document is to define the functional behaviour, data inputs, processing requirements and expected outputs of the proposed Help Desk Operations Monitoring and Reporting solution.

This document translates the business requirements identified in the Business Requirements Document (BRD) into detailed functional requirements.

### 1.2 Project Overview

The proposed solution will enable IT service desk management to monitor historical help desk ticket information and evaluate operational performance.

The solution will use historical ticket records, workflow information, resolution details and assignment history to provide consolidated operational insights.

The proposed reporting solution will support ticket volume analysis, priority monitoring, status tracking, resolution duration analysis, workflow performance monitoring and assignment analysis.

### 1.3 Objectives

- Provide consolidated visibility into help desk ticket information.
- Enable ticket analysis by priority, type and status.
- Calculate and display ticket resolution duration.
- Identify tickets with prolonged processing times.
- Monitor workflow stage duration and transitions.
- Provide visibility into assignment and contributor patterns.
- Support operational decision-making through structured reporting.

---

## 2. Proposed Solution Overview

The proposed solution will consist of a reporting and analysis interface supported by historical help desk data.

### Main Functional Modules

| Module ID | Module Name | Description |
|---|---|---|
| MOD-01 | Ticket Overview | Display consolidated ticket statistics |
| MOD-02 | Priority Analysis | Analyse ticket distribution by priority |
| MOD-03 | Status Monitoring | Display tickets by current recorded status |
| MOD-04 | Resolution Analysis | Calculate ticket resolution duration |
| MOD-05 | Workflow Analysis | Analyse time spent across workflow stages |
| MOD-06 | Assignment Analysis | Review ticket assignments and contributor activity |
| MOD-07 | Trend Analysis | Analyse ticket trends over time |

---

## 3. System Users and Roles

The proposed solution will support the following user roles.

| Role ID | User Role | Expected Functionality |
|---|---|---|
| USER-01 | IT Service Desk Manager | Review consolidated operational reports |
| USER-02 | Help Desk Team Lead | Monitor ticket status, priorities and workload |
| USER-03 | IT Support Analyst | Review ticket and assignment-related information |
| USER-04 | IT Operations Manager | Review historical trends and operational performance |

The above roles are proposed user personas for the case study. Actual access permissions and security configurations are outside the implementation scope.

---

## 4. Functional Requirements

### 4.1 Ticket Overview Module

**FR-001: Total Ticket Count**

The solution shall display the total number of unique tickets available in the selected dataset or filter context.

**FR-002: Ticket Categorization**

The solution shall group tickets based on available issue types, including incidents and service requests where recorded.

**FR-003: Priority Distribution**

The solution shall display ticket distribution across available priority categories.

**FR-004: Ticket Summary**

The solution shall provide a consolidated view of total tickets, resolved tickets and unresolved or other status categories.

### 4.2 Priority Analysis Module

**FR-005: Priority-wise Filtering**

The solution shall allow users to filter ticket records by available priority values.

**FR-006: Priority Comparison**

The solution shall display ticket counts across different priority categories to support workload analysis.

**FR-007: Priority Trend Analysis**

The solution shall allow users to analyse ticket volume trends across priorities over selected time periods.

### 4.3 Status Monitoring Module

**FR-008: Status-wise Ticket Summary**

The solution shall display ticket counts grouped by the latest recorded issue status.

**FR-009: Status Filtering**

The solution shall allow users to filter records by available ticket statuses, such as Open, In Progress, Resolved and Done.

**FR-010: Unresolved Ticket Identification**

The solution shall identify tickets without a recorded resolution timestamp and present them separately for further review.

**FR-011: Ticket Detail View**

The solution shall allow users to view relevant ticket details, including issue ID, type, priority, status, creation date and resolution date where available.

### 4.4 Resolution Analysis Module

**FR-012: Resolution Duration Calculation**

The solution shall calculate ticket resolution duration using the difference between the issue creation timestamp and resolution timestamp for eligible records.

**FR-013: Average Resolution Duration**

The solution shall calculate average resolution duration for tickets with valid creation and resolution timestamps.

**FR-014: Long-duration Ticket Identification**

The solution shall allow users to identify tickets with resolution durations exceeding a configurable analysis threshold.

**FR-015: Resolution Trend Analysis**

The solution shall display resolution duration trends over selected reporting periods.

### 4.5 Workflow Analysis Module

**FR-016: Workflow Stage Analysis**

The solution shall display the time spent by tickets in available workflow stages using the corresponding workflow duration fields.

**FR-017: Workflow Transition Count**

The solution shall display the number of times tickets passed through individual workflow stages using available transition count fields.

**FR-018: Workflow Complexity Analysis**

The solution shall allow users to analyse the number of processing steps associated with each ticket.

**FR-019: Repeated Workflow Identification**

The solution shall identify tickets with repeated workflow transitions to support investigation of possible rework.

### 4.6 Assignment Analysis Module

**FR-020: Assignment History Analysis**

The solution shall display available assignment activity for tickets using the assignee-level snapshot information.

**FR-021: Contributor Analysis**

The solution shall display the number of contributors associated with each ticket.

**FR-022: Assignment Duration Analysis**

The solution shall analyse available assignee start and end timestamps to understand assignment activity duration.

**FR-023: Workload Distribution**

The solution shall provide a summary of ticket assignment distribution across available support personnel identifiers.

### 4.7 Trend and Reporting Module

**FR-024: Monthly Ticket Trend**

The solution shall display ticket volumes grouped by month based on ticket creation dates.

**FR-025: Historical Comparison**

The solution shall allow users to compare ticket trends across selected historical periods.

**FR-026: Filter-based Reporting**

The solution shall allow users to analyse reports using available filters, including date, priority, issue type and status.

**FR-027: Consolidated Reporting**

The solution shall provide a consolidated reporting view containing key operational indicators.

**FR-028: Data Refresh**

The solution shall support updating the analysis when a new valid dataset is provided and processed.

---

## 5. Input and Output Specifications

### 5.1 Input Requirements

The solution will use the following dataset fields.

| Input Field | Source Field | Purpose |
|---|---|---|
| Ticket ID | id | Unique ticket identification |
| Issue Number | issue_num | Project-level ticket reference |
| Issue Type | issue_type | Categorization |
| Priority | issue_priority | Priority analysis |
| Created Date | issue_created | Ticket creation analysis |
| Resolution Date | issue_resolution_date | Resolution duration |
| Resolution Type | issue_resolution | Resolution outcome analysis |
| Current Recorded Status | issue_status | Status monitoring |
| Contributor Count | issue_contr_count | Contributor analysis |
| Processing Time | wf_total_time | Total workflow processing time |
| Processing Steps | processing_steps | Workflow complexity |
| Workflow Duration | wf_{S} | Duration in individual workflow stages |
| Workflow Transition Count | wfe_{S} | Number of times a workflow stage was passed |
| Assignee | issue_assignee | Latest recorded assignee |
| Assignment Start | started | Assignee activity start |
| Assignment End | ended | Assignee activity end |

### 5.2 Expected Output Requirements

The solution shall provide:

1. Total ticket summary.
2. Priority-wise ticket distribution.
3. Issue type distribution.
4. Status-wise ticket summary.
5. Average resolution duration.
6. Long-duration ticket identification.
7. Workflow stage duration analysis.
8. Workflow transition analysis.
9. Assignment and contributor analysis.
10. Monthly ticket trend reports.

---

## 6. Business Rules and Data Validation

| Rule ID | Validation Rule |
|---|---|
| VAL-001 | Every ticket must have a valid unique issue ID. |
| VAL-002 | Ticket creation date must be available for resolution duration calculations. |
| VAL-003 | Resolution duration must only be calculated when valid creation and resolution timestamps exist. |
| VAL-004 | Tickets without resolution timestamps must be excluded from resolved-ticket average duration calculations. |
| VAL-005 | Negative resolution durations must be flagged for data-quality investigation. |
| VAL-006 | Missing priority values must be identified and handled separately. |
| VAL-007 | Duplicate ticket records must be investigated before calculating unique ticket counts. |
| VAL-008 | Assignment activity must be analysed using ticket ID and assignment sequence where available. |
| VAL-009 | Workflow duration values must be interpreted in seconds and converted where appropriate for reporting. |
| VAL-010 | Workflow transition counts must not be confused with total processing time. |
| VAL-011 | Masked user and project identifiers must not be used to infer real identities. |
| VAL-012 | SLA compliance must not be calculated unless approved SLA targets and applicable business-calendar rules are supplied. |

---

## 7. Exception Handling

| Exception ID | Scenario | Expected System Behaviour |
|---|---|---|
| EX-001 | Missing ticket creation date | Flag record for data-quality review |
| EX-002 | Missing resolution date | Classify separately as without recorded resolution timestamp |
| EX-003 | Invalid date values | Exclude from affected date calculations and flag |
| EX-004 | Missing priority | Group under Unknown / Not Available |
| EX-005 | Duplicate issue ID | Investigate duplicate records before aggregation |
| EX-006 | Missing assignment information | Exclude from assignee-specific analysis and report the limitation |
| EX-007 | Missing workflow information | Display unavailable values without assuming zero processing time |
| EX-008 | Invalid dataset structure | Display a data validation error and prevent unreliable reporting |

---

## 8. Non-Functional Requirements

The following non-functional requirements describe the expected quality of the proposed reporting solution.

| Requirement ID | Category | Requirement |
|---|---|---|
| NFR-001 | Performance | Reports should load within an acceptable time for the agreed dataset size. |
| NFR-002 | Usability | Reports should use clear labels, meaningful visualizations and consistent layouts. |
| NFR-003 | Accuracy | Calculated metrics should follow documented business rules. |
| NFR-004 | Data Integrity | The solution should preserve relationships between ticket and assignment records. |
| NFR-005 | Security | Masked identifiers should remain protected in published reports. |
| NFR-006 | Maintainability | KPI definitions and data transformations should be documented. |
| NFR-007 | Scalability | The proposed design should support future additions of historical ticket records. |
| NFR-008 | Availability | Reporting availability should be defined according to the eventual deployment environment. |

---

## 9. Requirements Traceability Matrix

The following matrix connects the functional requirements to their originating business requirements.

| BRD Requirement | Functional Requirement |
|---|---|
| BR-001 | FR-001, FR-002, FR-003 |
| BR-002 | FR-008, FR-009, FR-010, FR-011 |
| BR-003 | FR-012, FR-013, FR-015 |
| BR-004 | FR-014, FR-016 |
| BR-005 | FR-020, FR-021, FR-022 |
| BR-006 | FR-017, FR-018, FR-019 |
| BR-007 | FR-020, FR-021, FR-023 |
| BR-008 | FR-027 |
| BR-009 | FR-024, FR-025 |
| BR-010 | FR-026, FR-027 |

---

## 10. Acceptance Criteria

The proposed solution will be considered functionally acceptable when:

1. Ticket volume can be displayed using unique ticket identifiers.
2. Users can analyse tickets by type, priority and status.
3. Resolution duration is calculated using valid date and time fields.
4. Tickets without resolution timestamps are handled separately.
5. Workflow duration and transition counts are displayed correctly.
6. Assignment activity can be reviewed using available assignment records.
7. Historical ticket trends can be analysed by month.
8. Data-quality exceptions are identified and documented.
9. Reporting filters return the expected records.
10. Functional outputs can be validated against the source dataset and documented calculation rules.

---

## 11. Dependencies and Limitations

### Dependencies

- Availability of the anonymized help desk dataset.
- Availability of relevant ticket and workflow fields.
- Data profiling and validation.
- Agreed KPI calculation definitions.
- Business confirmation of any configurable reporting thresholds.

### Limitations

- The solution is a proposed reporting and analysis concept.
- No production application is being developed.
- Historical data covers January 2016 to March 2023.
- Masked identifiers limit identity-based analysis.
- SLA targets and business calendars are not provided.
- Functional behaviour will be demonstrated through portfolio analysis and reporting artifacts rather than a live production deployment.

---

## 12. Conclusion

This Functional Requirements Document defines the expected functionality of the proposed Help Desk Operations Monitoring and Reporting solution.

The requirements translate business needs into measurable system behaviours, data specifications, validation rules and acceptance criteria.

These functional requirements will serve as the foundation for subsequent process mapping, user stories, acceptance criteria, UAT test scenarios and the proposed reporting solution.

---

**Prepared By:** Independent Business Analyst  
**Project:** IT Service Request and Help Desk Workflow Improvement  
**Document:** Functional Requirements Document  
**Version:** 1.0
