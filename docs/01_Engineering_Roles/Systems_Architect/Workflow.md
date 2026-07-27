# Systems Architect Workflow

| Field | Value |
|--------|-------|
| Document ID | UEOS-ARC-002 |
| Version | 0.1 |
| Status | Active |
| Owner | Systems Architect |
| Classification | Engineering Workflow |
| Last Updated | 2026-07-27 |

---

# 1. Purpose

This document defines the standard engineering workflow followed by the Systems Architect within the UAV Engineering Operating System (UEOS).

The objective is to transform approved engineering requirements into a coherent, modular, scalable, and verifiable system architecture that guides implementation and integration.

---

# 2. Workflow Overview

```
Receive Approved Requirements
        │
        ▼
Analyse System Requirements
        │
        ▼
Identify System Functions
        │
        ▼
Develop Functional Architecture
        │
        ▼
Develop Logical Architecture
        │
        ▼
Develop Physical Architecture
        │
        ▼
Define Interfaces
        │
        ▼
Allocate Functions
        │
        ▼
Develop Data Flow
        │
        ▼
Evaluate Architectural Alternatives
        │
        ▼
Conduct Architecture Review
        │
        ▼
Baseline Architecture
```

---

# 3. Phase 1 – Receive Project Inputs

## Objective

Understand the engineering problem before designing the architecture.

## Activities

- Review Mission Definition.
- Review System Requirements Specification (SRS).
- Review Requirement Traceability Matrix (RTM).
- Review research findings.
- Review project constraints.
- Clarify architectural assumptions.

## Deliverables

- Architecture Planning Notes

---

# 4. Phase 2 – Analyse System Requirements

## Objective

Understand what the architecture must satisfy.

## Activities

- Review functional requirements.
- Review performance requirements.
- Review safety requirements.
- Review interface requirements.
- Review environmental constraints.

## Deliverables

- Architecture Requirement Summary

---

# 5. Phase 3 – Identify System Functions

## Objective

Determine the major capabilities the UAV system must provide.

## Activities

- Identify system-level functions.
- Group related functions.
- Define subsystem responsibilities.
- Identify external interactions.

## Deliverables

- Functional Decomposition
- Function Catalogue

---

# 6. Phase 4 – Develop Functional Architecture

## Objective

Organise the system into functional subsystems.

Typical subsystems include:

- Mission Management
- Flight Control
- Navigation
- Perception
- AI & Decision Making
- Communication
- Power Management
- Payload Management

## Deliverables

- Functional Architecture Diagram

---

# 7. Phase 5 – Develop Logical Architecture

## Objective

Define how software and logical services interact.

## Activities

- Define software modules.
- Define processing pipelines.
- Define service responsibilities.
- Identify shared resources.

## Deliverables

- Logical Architecture Diagram

---

# 8. Phase 6 – Develop Physical Architecture

## Objective

Map logical components to physical hardware.

## Activities

- Select computing platforms.
- Allocate sensors.
- Allocate actuators.
- Allocate communication hardware.
- Define electrical relationships.

## Deliverables

- Physical Architecture Diagram

---

# 9. Phase 7 – Define Interfaces

## Objective

Specify how subsystems communicate.

## Interface Types

- UART
- CAN
- Ethernet
- SPI
- I2C
- USB
- GPIO
- MAVLink
- ROS 2 Topics
- DDS

Each interface shall define:

- Purpose
- Protocol
- Data format
- Timing requirements
- Error handling

## Deliverables

- Interface Control Document (ICD)

---

# 10. Phase 8 – Allocate Functions

## Objective

Assign system functions to engineering subsystems.

Example

| Function | Subsystem |
|----------|-----------|
| Object Detection | Computer Vision |
| Navigation | Flight Control |
| Mission Planning | AI |
| Telemetry | Communication |
| Power Distribution | Hardware |

## Deliverables

- Functional Allocation Matrix

---

# 11. Phase 9 – Develop Data Flow

## Objective

Describe how information moves through the UAV.

Example

```
Camera
   │
   ▼
Computer Vision
   │
   ▼
AI Decision Module
   │
   ▼
Mission Manager
   │
   ▼
Flight Controller
   │
   ▼
ESC
   │
   ▼
Motors
```

## Deliverables

- Data Flow Diagram

---

# 12. Phase 10 – Evaluate Architectural Alternatives

## Objective

Compare candidate architectures before selecting the baseline.

Evaluation criteria include:

- Performance
- Reliability
- Scalability
- Maintainability
- Modularity
- Complexity
- Cost
- Integration effort
- Safety

## Deliverables

- Architecture Trade Study
- Architecture Decision Record (ADR)

---

# 13. Phase 11 – Conduct Architecture Review

## Objective

Verify that the architecture satisfies project objectives.

## Review Checklist

- Requirements coverage
- Interface completeness
- Functional allocation
- Safety considerations
- Integration readiness
- Scalability
- Documentation quality

## Deliverables

- Architecture Review Report

---

# 14. Phase 12 – Baseline Architecture

## Objective

Freeze the approved architecture before detailed implementation.

## Activities

- Approve architecture.
- Assign version.
- Publish documentation.
- Notify engineering teams.

## Deliverables

- Architecture Baseline

---

# 15. Decision Gates

| Gate | Decision |
|------|----------|
| AG1 | Architecture Planning Approved |
| AG2 | Functional Architecture Approved |
| AG3 | Logical Architecture Approved |
| AG4 | Physical Architecture Approved |
| AG5 | Interfaces Approved |
| AG6 | Architecture Review Passed |
| AG7 | Architecture Baseline Released |

---

# 16. Success Criteria

The workflow is complete when:

- All requirements are addressed.
- Functional allocation is complete.
- Interfaces are fully documented.
- Data flow is defined.
- Architectural decisions are justified.
- Integration risks are acceptable.
- Architecture has been approved and baselined.

---

# 17. Best Practices

- Maintain separation of concerns.
- Design modular subsystems.
- Keep interfaces stable and simple.
- Minimise subsystem coupling.
- Record major architectural decisions.
- Validate architecture before implementation.

---

# 18. Related UEOS Documents

- Engineering Philosophy
- Engineering Lifecycle
- Systems Architect README
- Responsibilities
- Deliverables
- Prompt

---

# 19. Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 2026-07-27 | Initial Release |

---

# End of Document