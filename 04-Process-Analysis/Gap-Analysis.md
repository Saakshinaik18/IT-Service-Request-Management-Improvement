# Gap Analysis – IT Service Request and Help Desk Workflow Improvement

## 1. Introduction

This document analyses the differences between the current (As-Is) and proposed (To-Be) IT service request management processes.

The objective is to identify potential process gaps and recommend improvements to ticket tracking, assignment visibility, workflow monitoring and operational reporting.

This analysis is based on an anonymized historical help desk ticket dataset covering January 2016 to March 2023.

## 2. Gap Analysis Objectives

- Understand the current ticket management workflow.
- Identify potential gaps in process visibility and monitoring.
- Define improvements for the proposed future-state workflow.
- Align proposed improvements with the business and functional requirements.
- Support better operational reporting and decision-making.

## 3. As-Is vs To-Be Comparison

| Process Area | As-Is Process | Identified Gap / Opportunity | Proposed To-Be Process |
|---|---|---|---|
| Request creation | IT service requests are created and recorded. | Consistent request categorization should be supported. | Categorize and record requests systematically. |
| Priority management | Priority information is available in historical ticket records. | Priority-based monitoring can improve operational visibility. | Assess and record request priority. |
| Ticket assignment | Tickets are assigned to support personnel. | Assignment activity and workload distribution need better visibility. | Track assignment information and ownership. |
| Ticket investigation | Support personnel review and investigate tickets. | Ticket status updates should be consistently monitored. | Maintain clear ticket status updates. |
| Workflow monitoring | Tickets move through different workflow stages. | Time spent in workflow stages may require closer monitoring. | Monitor workflow stages and processing duration. |
| Resolution tracking | Resolution information is recorded for eligible tickets. | Resolution duration and unresolved records need visibility. | Monitor resolution time and outstanding tickets. |
| Exception handling | Further investigation may be required when an issue remains unresolved. | A clear escalation and follow-up approach is recommended. | Continue investigation or escalate unresolved requests. |
| Management reporting | Historical ticket records are available. | Consolidated operational reporting can improve decision-making. | Provide reporting on volume, priority, status, assignment and resolution trends. |

## 4. Identified Process Improvement Opportunities

### 4.1 Request Categorization and Priority Visibility

**Opportunity:** Improve visibility into ticket categories and priority levels.

**Proposed improvement:** Maintain consistent categorization and priority information to support operational monitoring.

### 4.2 Assignment and Workload Monitoring

**Opportunity:** Improve visibility into ticket ownership and assignment activity.

**Proposed improvement:** Track assignment information and review workload distribution across support personnel.

### 4.3 Workflow Monitoring

**Opportunity:** Identify workflow stages where tickets spend longer processing time.

**Proposed improvement:** Monitor workflow stage duration and repeated transitions to identify potential bottlenecks and rework.

### 4.4 Resolution Monitoring

**Opportunity:** Improve visibility into ticket resolution duration and tickets without recorded resolution timestamps.

**Proposed improvement:** Monitor resolution trends and flag records requiring further review.

### 4.5 Operational Reporting

**Opportunity:** Provide a consolidated view of historical help desk performance.

**Proposed improvement:** Develop reporting views for ticket volume, priority, status, assignment activity, workflow duration and resolution trends.

## 5. Proposed Business Benefits

The proposed improvements are expected to support:

- Better visibility into help desk operations.
- Improved ticket assignment monitoring.
- More effective identification of workflow bottlenecks.
- Better understanding of ticket resolution patterns.
- More consistent operational reporting.
- Improved data-driven decision-making.

These are expected benefits and have not been measured through a live implementation.

## 6. Requirements Traceability

| Business Requirement | Related Functional Requirements | Improvement Area |
|---|---|---|
| BR-001 | FR-001, FR-002, FR-003 | Ticket volume and priority visibility |
| BR-002 | FR-008, FR-009, FR-010, FR-011 | Ticket status monitoring |
| BR-003 | FR-012, FR-013, FR-015 | Resolution analysis |
| BR-004 | FR-014, FR-016 | Long-duration ticket and workflow monitoring |
| BR-005 | FR-020, FR-021, FR-022 | Assignment tracking |
| BR-006 | FR-017, FR-018, FR-019 | Workflow transition analysis |
| BR-007 | FR-020, FR-021, FR-023 | Workload distribution |
| BR-008 | FR-027 | Consolidated operational reporting |
| BR-009 | FR-024, FR-025 | Historical trend analysis |
| BR-010 | FR-026, FR-027 | Consistent reporting and filtering |

## 7. Assumptions and Limitations

- The analysis uses anonymized historical help desk ticket records.
- The As-Is workflow is a high-level interpretation of the available dataset, not a verified organizational SOP.
- The To-Be workflow represents proposed improvements, not an implemented production process.
- Actual stakeholder interviews and organizational process validation have not been conducted.
- SLA compliance and breach analysis are excluded because approved SLA targets and business calendar rules are not available.
- Improvement benefits have not been quantified or validated through implementation.

## 8. Conclusion

The gap analysis identifies opportunities to improve visibility into IT service request categorization, assignment activity, workflow processing, resolution patterns and operational reporting.

The proposed To-Be workflow addresses these opportunities through structured monitoring, clearer process steps and consolidated reporting.

This analysis provides a foundation for the next project activities, including user story development and User Acceptance Testing (UAT) planning.
