# Requirements Engineer Workflow

| Field | Value |
|--------|-------|
| Document ID | UEOS-REQ-002 |
| Version | 0.1 |
| Status | Active |
| Owner | Requirements Engineer |
| Classification | Engineering Workflow |
| Last Updated | 2026-07-27 |

---

# 1. Purpose

This document defines the standard engineering workflow followed by the Requirements Engineer within the UAV Engineering Operating System (UEOS).

The workflow transforms stakeholder needs and mission objectives into structured, measurable, verifiable, and traceable engineering requirements that guide the complete system development lifecycle.

---

# 2. Workflow Overview

```
Receive Mission Definition
        │
        ▼
Study Stakeholder Needs
        │
        ▼
Analyse Operational Concept (ConOps)
        │
        ▼
Identify System Functions
        │
        ▼
Develop System Requirements
        │
        ▼
Classify Requirements
        │
        ▼
Review Requirement Quality
        │
        ▼
Allocate Requirements
        │
        ▼
Create Traceability Matrix
        │
        ▼
Support Architecture Team
        │
        ▼
Support Verification Team
        │
        ▼
Manage Requirement Changes
```

---

# 3. Phase 1 – Receive Project Inputs

## Objective

Understand the project before writing any requirements.

## Activities

- Review Mission Definition.
- Review Stakeholder Analysis.
- Review Operational Concept (ConOps).
- Review project constraints.
- Clarify ambiguities.

## Deliverables

- Requirement Planning Notes
- Requirement Development Plan

---

# 4. Phase 2 – Analyse Stakeholder Needs

## Objective

Identify what stakeholders expect from the system.

## Activities

- Identify stakeholders.
- Gather expectations.
- Identify operational needs.
- Resolve conflicting expectations.
- Prioritise stakeholder requirements.

## Deliverables

- Stakeholder Requirement List

---

# 5. Phase 3 – Analyse Operational Concept

## Objective

Understand how the UAV will operate.

## Activities

- Review mission sequence.
- Study operational environment.
- Identify system interactions.
- Identify failure scenarios.

## Deliverables

- Operational Requirement List

---

# 6. Phase 4 – Identify System Functions

## Objective

Determine what the system must do.

## Activities

- Break down the mission into functions.
- Identify subsystem responsibilities.
- Define system boundaries.
- Identify external interfaces.

## Deliverables

- Functional Decomposition
- Functional Requirement List

---

# 7. Phase 5 – Develop System Requirements

## Objective

Convert mission needs into engineering requirements.

## Activities

- Write functional requirements.
- Write performance requirements.
- Write safety requirements.
- Write interface requirements.
- Write environmental requirements.
- Assign requirement identifiers.

## Deliverables

- System Requirements Specification (SRS)

---

# 8. Phase 6 – Requirement Quality Review

## Objective

Ensure every requirement meets engineering standards.

Every requirement shall be:

- Correct
- Clear
- Complete
- Consistent
- Feasible
- Measurable
- Verifiable
- Traceable
- Unique

## Deliverables

- Requirement Review Report

---

# 9. Phase 7 – Requirement Allocation

## Objective

Allocate requirements to engineering disciplines.

Examples

| Requirement Type | Engineering Role |
|------------------|------------------|
| Flight Control | Flight Control Engineer |
| Vision | Computer Vision Engineer |
| AI | AI Engineer |
| Electronics | Hardware Engineer |
| Firmware | Embedded Systems Engineer |
| Testing | Test Engineer |

## Deliverables

- Requirement Allocation Matrix

---

# 10. Phase 8 – Requirement Traceability

## Objective

Maintain traceability throughout the project lifecycle.

```
Mission

↓

Stakeholder Need

↓

System Requirement

↓

Architecture

↓

Subsystem

↓

Implementation

↓

Test Case

↓

Verification

↓

Validation
```

## Deliverables

- Requirement Traceability Matrix (RTM)

---

# 11. Phase 9 – Support System Architecture

## Objective

Ensure the architecture satisfies every requirement.

## Activities

- Review architecture documents.
- Check requirement allocation.
- Identify missing requirements.
- Review interfaces.

## Deliverables

- Requirement Compliance Report

---

# 12. Phase 10 – Support Verification

## Objective

Ensure every requirement has a verification method.

Verification methods include:

- Inspection
- Analysis
- Simulation
- Bench Testing
- Integration Testing
- Flight Testing

## Deliverables

- Requirement Verification Matrix

---

# 13. Phase 11 – Requirement Change Management

## Objective

Manage requirement modifications throughout the project lifecycle.

## Activities

- Receive change requests.
- Analyse impact.
- Update documentation.
- Notify engineering teams.
- Update traceability.

## Deliverables

- Requirement Change Log

---

# 14. Decision Gates

| Gate | Decision |
|------|----------|
| RG1 | Requirement Planning Approved |
| RG2 | Stakeholder Requirements Approved |
| RG3 | System Requirements Approved |
| RG4 | Requirement Review Completed |
| RG5 | Requirement Allocation Approved |
| RG6 | Traceability Verified |
| RG7 | Verification Strategy Approved |

---

# 15. Success Criteria

The workflow is complete when:

- Stakeholder needs are documented.
- All requirements are measurable.
- Requirements are uniquely identified.
- Every requirement has an owner.
- Every requirement has a verification method.
- Traceability is complete.
- SRS has been approved.

---

# 16. Best Practices

- Write one requirement per statement.
- Use measurable values wherever possible.
- Avoid implementation-specific wording unless necessary.
- Review requirements with stakeholders.
- Maintain complete traceability.
- Version control every revision.

---

# 17. Related UEOS Documents

- Engineering Philosophy
- Engineering Lifecycle
- Chief Systems Engineer Workflow
- Verification and Validation
- System Requirements Specification

---

# 18. Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 2026-07-27 | Initial Release |

---

# End of Document