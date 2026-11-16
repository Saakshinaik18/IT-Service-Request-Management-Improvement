# User Stories and Acceptance Criteria
## Project: IT Service Request and Help Desk Workflow Improvement

### 1. Introduction

This document translates the business and functional requirements into user stories with testable acceptance criteria.

The user stories are designed for a proposed Help Desk Operations Monitoring and Reporting solution using historical help desk ticket data.

### 2. User Personas

| Persona | Description |
|---|---|
| IT Service Desk Manager | Reviews overall ticket performance and operational trends. |
| Help Desk Team Lead | Monitors ticket assignments, workflow stages and workload distribution. |
| IT Support Analyst | Reviews ticket information, status and assignment details. |
| IT Operations Manager | Uses consolidated reports to understand operational performance. |

These are proposed project personas, not actual stakeholders interviewed.

### 3. User Stories

#### US-001: View Overall Ticket Volume

**Related Requirement:** FR-001, FR-002

As an IT Service Desk Manager,  
I want to view the total number of tickets,  
so that I can understand the overall help desk workload.

**Acceptance Criteria:**
- The system displays the total number of unique tickets.
- Tickets are counted using the available unique ticket identifier.
- Duplicate records are handled according to the defined data validation rules.
- The ticket count is updated when the reporting dataset is refreshed.

#### US-002: Analyse Ticket Priority

**Related Requirement:** FR-003, FR-005, FR-006

As a Help Desk Team Lead,  
I want to view tickets by priority,  
so that I can understand the distribution of high- and low-priority requests.

**Acceptance Criteria:**
- Tickets are grouped by their recorded priority.
- The report displays ticket counts for each available priority category.
- Users can filter the report by priority.
- Missing priority values are identified separately rather than assigned an assumed priority.

#### US-003: Monitor Ticket Status

**Related Requirement:** FR-008, FR-009, FR-010

As an IT Support Analyst,  
I want to view tickets by their latest recorded status,  
so that I can understand their current recorded workflow position.

**Acceptance Criteria:**
- Tickets are grouped by their latest available status.
- Users can filter tickets by status.
- Tickets without a resolution timestamp can be identified.
- The report distinguishes recorded status from inferred resolution state.

#### US-004: Analyse Ticket Resolution Duration

**Related Requirement:** FR-012, FR-013, FR-015

As an IT Service Desk Manager,  
I want to view ticket resolution duration,  
so that I can understand historical resolution patterns.

**Acceptance Criteria:**
- Resolution duration is calculated using valid creation and resolution timestamps.
- Records with missing or invalid timestamps are excluded from the average calculation.
- Average resolution duration is displayed for eligible records.
- The report supports historical resolution trend analysis.

#### US-005: Identify Long-Processing Tickets

**Related Requirement:** FR-014, FR-016

As a Help Desk Team Lead,  
I want to identify tickets with longer processing durations,  
so that I can investigate possible workflow delays.

**Acceptance Criteria:**
- Users can apply a configurable analysis threshold.
- Tickets exceeding the selected threshold are highlighted.
- Workflow stage durations are displayed using available workflow duration fields.
- The threshold is an analytical setting and is not represented as an SLA target.

#### US-006: Monitor Assignment Activity

**Related Requirement:** FR-020, FR-021, FR-022

As a Help Desk Team Lead,  
I want to review ticket assignment activity,  
so that I can understand assignment patterns and contributor involvement.

**Acceptance Criteria:**
- Available assignment information is displayed.
- Contributor count is displayed where available.
- Assignment duration is calculated using valid start and end timestamps.
- Missing assignment information is identified rather than fabricated.

#### US-007: Identify Workflow Transitions

**Related Requirement:** FR-017, FR-018, FR-019

As an IT Service Desk Manager,  
I want to analyse workflow transitions and processing steps,  
so that I can identify possible rework and workflow complexity.

**Acceptance Criteria:**
- Available workflow transition counts are displayed.
- Processing step information is analysed where available.
- Repeated transitions can be highlighted for investigation.
- Repeated transitions are treated as potential rework indicators, not confirmed process failures.

#### US-008: View Historical Ticket Trends

**Related Requirement:** FR-024, FR-025

As an IT Operations Manager,  
I want to view monthly ticket volume and historical trends,  
so that I can understand changes in help desk demand.

**Acceptance Criteria:**
- Ticket volume is grouped by the recorded creation date.
- Monthly trends are displayed chronologically.
- Users can compare available historical periods.
- Records with invalid creation dates are excluded from date-based analysis.

#### US-009: Use Consolidated Operational Reports

**Related Requirement:** FR-026, FR-027

As an IT Service Desk Manager,  
I want to view consolidated operational reports,  
so that I can review ticket volume, priority, status, assignment and resolution information in one place.

**Acceptance Criteria:**
- The reporting view includes the agreed operational KPIs.
- Users can filter by available date, priority, issue type and status fields.
- KPI definitions are consistent across reporting views.
- The report displays information derived from the supplied dataset.

### 4. Requirement Traceability Summary

| User Story | Related Functional Requirements |
|---|---|
| US-001 | FR-001, FR-002 |
| US-002 | FR-003, FR-005, FR-006 |
| US-003 | FR-008, FR-009, FR-010 |
| US-004 | FR-012, FR-013, FR-015 |
| US-005 | FR-014, FR-016 |
| US-006 | FR-020, FR-021, FR-022 |
| US-007 | FR-017, FR-018, FR-019 |
| US-008 | FR-024, FR-025 |
| US-009 | FR-026, FR-027 |

### 5. Assumptions and Limitations

- User stories describe proposed solution functionality.
- Acceptance criteria are proposed validation conditions.
- The project is a portfolio case study, not a live production implementation.
- Historical dataset fields determine which reporting capabilities can be demonstrated.
- SLA compliance cannot be evaluated without approved SLA targets and business calendar rules.
- Actual stakeholder approval and development sign-off have not been obtained.

### 6. Conclusion

These user stories translate the project's business and functional requirements into testable statements.

They provide a foundation for the next stage: User Acceptance Testing (UAT) planning.
