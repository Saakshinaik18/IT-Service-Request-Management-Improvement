# Business Requirements Document (BRD)
## IT Service Request and Help Desk Workflow Improvement

| Document Information | Details |
|---|---|
| Project Name | IT Service Request and Help Desk Workflow Improvement |
| Document Type | Business Requirements Document |
| Document Version | 1.0 |
| Status | Draft |
| Project Type | Independent Business Analysis Case Study |
| Business Domain | IT Service Management |
| Data Source | Anonymized Help Desk Tickets Dataset |
| Data Period | January 2016 – March 2023 |
| Prepared By | Independent Business Analyst |

---

## 1. Executive Summary

This project focuses on analysing the help desk ticket management process to identify opportunities for improving operational efficiency, ticket handling, workflow visibility and service delivery.

The analysis will use an anonymized help desk dataset containing historical ticket information, including issue types, priorities, statuses, creation and resolution dates, assignment details, workflow transitions and ticket comments.

The business requires better visibility into ticket lifecycle performance, workload distribution, recurring workflow delays and operational bottlenecks.

This Business Requirements Document defines the business needs, objectives, scope, stakeholder expectations and high-level requirements for the proposed improvement initiative.

## 2. Business Background

IT help desk teams manage incidents and service requests raised by users. These tickets pass through multiple workflow stages, involving different support team members before reaching a final resolution.

Effective ticket management requires:

- Accurate ticket categorization.
- Appropriate priority identification.
- Timely assignment to support personnel.
- Visibility into ticket status and progress.
- Monitoring of resolution timelines.
- Identification of recurring workflow delays.
- Reliable operational reporting.

Historical ticket information provides an opportunity to understand how requests move through the support process and where operational improvements may be required.

## 3. Business Problem

The organization requires better visibility into its help desk ticket lifecycle and operational performance.

Potential challenges to investigate include:

1. Delays in moving tickets through workflow stages.
2. Multiple assignment changes during ticket handling.
3. Repeated transitions between workflow statuses.
4. Differences in resolution duration across ticket priorities and types.
5. Accumulation of unresolved or pending tickets.
6. Limited visibility into support workload distribution.
7. Insufficient consolidated reporting for operational decision-making.

These challenges will be validated through historical ticket data analysis. They are not assumed to be confirmed findings.

## 4. Business Objectives

The project aims to:

1. Understand the existing help desk ticket management workflow.
2. Analyse ticket volumes across issue types and priorities.
3. Evaluate ticket resolution duration and workflow processing time.
4. Identify repeated status transitions and possible process bottlenecks.
5. Analyse assignment patterns and support team workload.
6. Identify opportunities to improve ticket tracking and operational visibility.
7. Define business requirements for improved management reporting.
8. Recommend measurable operational performance indicators.

## 5. Project Scope

### 5.1 In Scope

- Historical help desk ticket analysis.
- Ticket categorization and priority analysis.
- Ticket lifecycle and status analysis.
- Ticket creation and resolution duration analysis.
- Workflow transition analysis.
- Assignment and contributor analysis.
- Open, resolved and other status distribution.
- Identification of potential process bottlenecks.
- Business requirements documentation.
- Functional requirements documentation.
- As-Is and To-Be process analysis.
- KPI and reporting requirements.
- Business recommendations.

### 5.2 Out of Scope

- Implementation of a new ITSM platform.
- Modification of an existing ticket management system.
- Actual changes to ticket assignment rules.
- Production workflow automation.
- Live integration with ServiceNow, Jira or other platforms.
- Actual SLA compliance certification without agreed SLA targets and business calendars.
- Changes to organizational support policies.

## 6. Stakeholder Identification

The following stakeholders are proposed for this simulated business case.

| Stakeholder | Business Responsibility | Interest |
|---|---|---|
| Employees / Requesters | Raise tickets and receive support | High |
| Help Desk Support Analysts | Handle and resolve tickets | High |
| Help Desk Team Lead | Monitor workload and ticket progress | High |
| IT Service Desk Manager | Review operational performance | High |
| IT Operations Manager | Oversee service delivery | High |
| Business Analyst | Analyse requirements and process gaps | High |
| Reporting / Data Analyst | Support operational data analysis | Medium |

*Stakeholders are proposed personas for the case study, not actual interview participants.*

## 7. Business Requirements

The following high-level business requirements define what the organization needs.

| Requirement ID | Business Requirement | Priority |
|---|---|---|
| BR-001 | The business needs visibility into total ticket volumes by issue type and priority. | High |
| BR-002 | The business needs to monitor tickets across different workflow statuses. | High |
| BR-003 | The business needs visibility into average ticket resolution duration. | High |
| BR-004 | The business needs to identify tickets with prolonged processing times. | High |
| BR-005 | The business needs to understand assignment changes and contributor involvement. | Medium |
| BR-006 | The business needs to identify repeated workflow transitions and potential rework. | Medium |
| BR-007 | The business needs to analyse workload distribution across support personnel. | Medium |
| BR-008 | The business needs consolidated operational reports for management review. | High |
| BR-009 | The business needs historical trend analysis to identify changes in ticket demand. | Medium |
| BR-010 | The business needs consistent KPI definitions for operational performance monitoring. | High |

## 8. Business Rules and Definitions

The following preliminary business rules will guide the analysis.

| Rule ID | Business Rule |
|---|---|
| BRULE-01 | Each ticket must be identified using its unique issue ID. |
| BRULE-02 | Ticket analysis must distinguish incidents from service requests where the issue type is available. |
| BRULE-03 | Ticket priority must be analysed using the values available in the source dataset. |
| BRULE-04 | Resolution duration will be calculated using ticket creation and resolution timestamps, subject to data validation. |
| BRULE-05 | Tickets without a resolution timestamp must be treated separately from resolved tickets. |
| BRULE-06 | Workflow analysis must consider repeated status transitions. |
| BRULE-07 | Assignee-level analysis must account for tickets handled by multiple support personnel. |
| BRULE-08 | SLA compliance must not be calculated without approved SLA targets and applicable business-calendar rules. |

## 9. Reporting and KPI Requirements

The business requires visibility into the following performance indicators.

| KPI | Business Purpose |
|---|---|
| Total Ticket Volume | Understand overall support demand |
| Ticket Volume by Priority | Understand priority distribution |
| Ticket Volume by Issue Type | Identify common ticket categories |
| Average Resolution Duration | Measure ticket resolution efficiency |
| Open Ticket Count | Monitor unresolved workload |
| Workflow Processing Time | Identify time spent in workflow stages |
| Average Number of Workflow Steps | Understand workflow complexity |
| Reopened Ticket Count | Identify potential rework |
| Assignment / Contributor Count | Understand workload distribution |
| Monthly Ticket Trend | Monitor changes in support demand |

Actual KPI values, calculation definitions and reporting targets will be finalized after data profiling and business-rule validation.

## 10. Data Requirements

The case study will use the available help desk dataset components.

| Dataset | Business Use |
|---|---|
| issues.csv | Ticket details, type, priority, status and resolution |
| issues_snapshot.csv | Assignee-level ticket activity |
| issues_change_history.csv | Historical assignment and status changes |
| sample_utterances.csv | Ticket communication and interaction analysis |
| issues_snapshot_sample.xlsx | Sampled assignee performance assessment |
| holidays_by_country.csv | Holiday-calendar reference for applicable date analysis |

Key data fields include:

- Issue ID
- Issue Type
- Issue Priority
- Issue Created Date
- Issue Resolution Date
- Issue Status
- Issue Resolution
- Issue Assignee
- Contributor Count
- Workflow Processing Time
- Processing Steps
- Workflow Status Duration
- Status Change History

Data availability, completeness and suitability will be validated before finalizing the analysis.

## 11. Assumptions, Dependencies and Constraints

### Assumptions

- The supplied dataset represents historical help desk ticket activity.
- The dataset contains anonymized and masked fields.
- Available workflow and assignment history can support lifecycle analysis.
- The business requires better operational visibility.
- The proposed reporting requirements are suitable for a simulated IT service management scenario.

### Dependencies

- Availability of the relevant dataset files.
- Understanding of ticket status and resolution values.
- Validation of date and time fields.
- Agreement on KPI calculation rules.
- Availability of SLA definitions if SLA analysis is required.

### Constraints

- The data covers January 2016 to March 2023.
- Some fields have been masked for privacy.
- Actual stakeholder interviews are not included.
- Historical data may contain incomplete or inconsistent records.
- The project does not include production system implementation.

## 12. Expected Business Benefits

The proposed initiative is expected to support:

- Improved visibility into ticket lifecycle performance.
- Better understanding of support demand and priority distribution.
- Identification of potential workflow bottlenecks.
- Improved understanding of assignment and workload patterns.
- More consistent operational reporting.
- Better-informed service management decisions.

These benefits are proposed outcomes and will not be represented as achieved results.

## 13. Business Acceptance Criteria

The BRD will be considered ready for business review when:

1. Business objectives and scope are clearly documented.
2. Stakeholder groups and expectations are identified.
3. High-level business requirements are documented with unique IDs.
4. Business rules and KPI definitions are established or marked for validation.
5. Data requirements are documented.
6. Assumptions, constraints and dependencies are identified.
7. Business requirements are traceable to the proposed functional requirements.

## 14. Conclusion

This Business Requirements Document establishes the business needs for analysing and improving the help desk ticket management process.

The proposed initiative will focus on understanding ticket lifecycle performance, workflow efficiency, assignment patterns and operational reporting requirements.

The documented business requirements will provide the foundation for functional specifications, process mapping, user stories, acceptance criteria and subsequent validation activities.

---

**Document Owner:** Independent Business Analyst  
**Project:** IT Service Request and Help Desk Workflow Improvement  
**Document Version:** 1.0
