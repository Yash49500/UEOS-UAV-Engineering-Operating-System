# Requirements Engineer Deliverables

| Field | Value |
|--------|-------|
| Document ID | UEOS-REQ-003 |
| Version | 0.1 |
| Status | Active |
| Owner | Requirements Engineer |
| Classification | Engineering Deliverables |
| Last Updated | 2026-07-27 |

---

# 1. Purpose

This document defines the engineering artefacts that shall be produced by the Requirements Engineer during the lifecycle of a UAV engineering project.

These deliverables ensure that every engineering activity is driven by approved, measurable, traceable, and verifiable requirements.

---

# 2. Deliverable Overview

| ID | Deliverable | Lifecycle Phase | Status |
|----|-------------|-----------------|--------|
| REQ-01 | Stakeholder Requirements | Requirements | Mandatory |
| REQ-02 | System Requirements Specification (SRS) | Requirements | Mandatory |
| REQ-03 | Functional Requirements | Requirements | Mandatory |
| REQ-04 | Non-Functional Requirements | Requirements | Mandatory |
| REQ-05 | Requirement Traceability Matrix (RTM) | Requirements | Mandatory |
| REQ-06 | Requirement Allocation Matrix | Architecture | Mandatory |
| REQ-07 | Requirement Review Report | Requirements | Mandatory |
| REQ-08 | Requirement Verification Matrix | Verification | Mandatory |
| REQ-09 | Requirement Change Log | Throughout | Mandatory |
| REQ-10 | Requirement Baseline | Project Milestones | Mandatory |

---

# 3. Deliverable Descriptions

---

## REQ-01 — Stakeholder Requirements

### Purpose

Capture all stakeholder expectations before engineering begins.

### Contents

- Stakeholder Identification
- Operational Needs
- Business Objectives
- User Expectations
- Constraints

### Output

Stakeholder Requirements Document

---

## REQ-02 — System Requirements Specification (SRS)

### Purpose

Translate stakeholder needs into engineering requirements.

### Contents

- Functional Requirements
- Performance Requirements
- Safety Requirements
- Interface Requirements
- Environmental Requirements
- Regulatory Requirements

### Output

Approved SRS

---

## REQ-03 — Functional Requirements

### Purpose

Describe what the UAV system shall do.

### Examples

- Autonomous Take-off
- Balloon Detection
- Object Tracking
- Autonomous Navigation
- Mission Completion

### Output

Functional Requirement List

---

## REQ-04 — Non-Functional Requirements

### Purpose

Define quality attributes of the system.

### Examples

- Maximum Weight
- Flight Time
- Detection Accuracy
- Maximum Speed
- Reliability
- Maintainability

### Output

Non-Functional Requirement List

---

## REQ-05 — Requirement Traceability Matrix (RTM)

### Purpose

Ensure complete traceability across the engineering lifecycle.

### Traceability

Mission

↓

Stakeholder Need

↓

Requirement

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

### Output

Requirement Traceability Matrix

---

## REQ-06 — Requirement Allocation Matrix

### Purpose

Assign requirements to engineering disciplines.

### Example

| Requirement | Owner |
|------------|-------|
| Navigation | Flight Control Engineer |
| Object Detection | Computer Vision Engineer |
| AI Decision Making | AI Engineer |
| Communication | Communication Engineer |
| Electronics | Hardware Engineer |

### Output

Requirement Allocation Matrix

---

## REQ-07 — Requirement Review Report

### Purpose

Document requirement quality reviews.

### Includes

- Review Findings
- Open Issues
- Recommended Changes
- Approval Status

### Output

Requirement Review Report

---

## REQ-08 — Requirement Verification Matrix

### Purpose

Map every requirement to its verification method.

### Verification Methods

- Inspection
- Analysis
- Simulation
- Bench Testing
- Flight Testing

### Output

Requirement Verification Matrix

---

## REQ-09 — Requirement Change Log

### Purpose

Track all approved requirement modifications.

Each entry shall include:

- Requirement ID
- Change Description
- Reason
- Impact Assessment
- Approval
- Date

### Output

Requirement Change Log

---

## REQ-10 — Requirement Baseline

### Purpose

Freeze approved requirements before implementation.

### Includes

- Approved Requirements
- Version Number
- Approval Date
- Change History

### Output

Requirement Baseline Document

---

# 4. Deliverable Timeline

```
Mission Definition
        │
        ▼
Stakeholder Requirements
        │
        ▼
System Requirements
        │
        ▼
Requirement Review
        │
        ▼
Requirement Allocation
        │
        ▼
Requirement Traceability
        │
        ▼
Verification Matrix
        │
        ▼
Requirement Baseline
        │
        ▼
Requirement Change Management
```

---

# 5. Quality Criteria

Every deliverable shall be:

- Complete
- Measurable
- Unambiguous
- Traceable
- Verifiable
- Version Controlled
- Reviewed
- Approved

---

# 6. Related UEOS Documents

- Engineering Philosophy
- Engineering Lifecycle
- Requirements Engineer README
- Responsibilities
- Workflow
- Prompt

---

# 7. Revision History

| Version | Date | Description |
|----------|------------|----------------|
| 0.1 | 2026-07-27 | Initial Release |

---

# End of Document   