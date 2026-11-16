# Requirements Traceability Matrix (RTM)

## 1. Purpose

The Requirements Traceability Matrix (RTM) establishes a relationship between business requirements, functional requirements, user stories and UAT test cases.

It helps ensure that documented business needs are addressed by the proposed solution and covered by planned validation scenarios.

**Project:** IT Service Request and Help Desk Workflow Improvement

**Document Status:** Proposed – Portfolio Case Study

## 2. Requirements Traceability Matrix

| Business Requirement | Functional Requirement | User Story | UAT Test Case | Coverage |
|---|---|---|---|---|
| BR-001: Ticket volume visibility | FR-001, FR-002, FR-003 | US-001, US-002 | UAT-001, UAT-002, UAT-003 | Mapped |
| BR-002: Ticket status monitoring | FR-008, FR-009, FR-010, FR-011 | US-003 | UAT-004, UAT-005 | Mapped |
| BR-003: Resolution duration visibility | FR-012, FR-013, FR-015 | US-004 | UAT-006 | Mapped |
| BR-004: Identify prolonged processing | FR-014, FR-016 | US-005 | UAT-007 | Mapped |
| BR-005: Assignment and contributor visibility | FR-020, FR-021, FR-022 | US-006 | UAT-008 | Mapped |
| BR-006: Workflow transition visibility | FR-017, FR-018, FR-019 | US-007 | UAT-009 | Mapped |
| BR-007: Workload distribution | FR-020, FR-021, FR-023 | US-006 | UAT-008 | Mapped |
| BR-008: Consolidated operational reporting | FR-027 | US-009 | UAT-012 | Mapped |
| BR-009: Historical trend analysis | FR-024, FR-025 | US-008 | UAT-010 | Mapped |
| BR-010: Consistent KPI definitions and filters | FR-026, FR-027 | US-009 | UAT-011, UAT-012 | Mapped |

## 3. Traceability Coverage

The following checks are proposed for maintaining traceability:

- Every business requirement should link to one or more functional requirements.
- Every functional requirement should be linked to an appropriate user story or documented as a technical or non-user-facing requirement.
- User stories should have acceptance criteria.
- Test cases should validate the relevant functional requirements.
- Changes to requirements should be reviewed for their impact on related documents and test cases.

## 4. Change Impact Assessment

When a requirement changes, the Business Analyst should review:

1. The affected business requirement.
2. Related functional requirements.
3. Impacted user stories and acceptance criteria.
4. Required updates to UAT test cases.
5. Any impact on scope, dependencies or project documentation.

## 5. Assumptions and Limitations

- Traceability mappings are based on the proposed BRD, FRD, user stories and UAT test plan.
- Coverage indicates documented mapping, not successful implementation or testing.
- UAT cases have not been executed.
- No stakeholder approval or production deployment is claimed.
- SLA-related requirements remain excluded because approved SLA targets and business calendar rules are unavailable.

## 6. Document References

- Business Requirements Document: `BRD.md`
- Functional Requirements Document: `FRD.md`
- User Stories: `../05-User-Stories/User-Stories.md`
- UAT Test Cases: `../06-UAT/UAT-Test-Cases.md`
- Stakeholder Analysis: `../02-Stakeholder-Analysis/Stakeholder-Analysis.md`
- Gap Analysis: `../04-Process-Analysis/Gap-Analysis.md`
