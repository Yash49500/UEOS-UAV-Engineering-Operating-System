# Safety Engineer Responsibilities

| Field | Value |
|--------|-------|
| Document ID | UEOS-SAFE-001 |
| Version | 0.1 |
| Status | Active |
| Owner | Safety Engineer |
| Classification | Engineering Role |
| Last Updated | 2026-07-27 |

---

# Purpose

This document defines the responsibilities, authority, ownership, and engineering boundaries of the Safety Engineer throughout the UAV engineering lifecycle.

The Safety Engineer is responsible for identifying hazards, assessing risks, deriving safety requirements, validating mitigation strategies, and ensuring that the UAV system operates within acceptable safety limits.

---

# Role Overview

The Safety Engineer provides independent oversight of system safety across all engineering disciplines.

The role is responsible for ensuring that hazards are identified early, risks are systematically reduced, safety requirements are traceable, and every subsystem complies with the approved safety strategy.

The Safety Engineer owns the system safety process but does not own subsystem implementation.

---

# Primary Responsibilities

## System Safety Planning

Develop the overall safety strategy for the project.

### Activities

- Define safety objectives.
- Develop the System Safety Plan.
- Establish safety processes.
- Define safety review milestones.
- Allocate safety responsibilities.

### Deliverables

- System Safety Plan

---

## Hazard Identification

Identify hazards associated with the UAV system.

### Activities

- Functional Hazard Assessment (FHA)
- Preliminary Hazard Analysis (PHA)
- Operational Hazard Analysis (OHA)
- Hazard brainstorming workshops
- Hazard classification
- Maintain Hazard Log

### Deliverables

- Hazard Analysis Report
- Hazard Log

---

## Risk Assessment

Evaluate identified hazards using a structured risk assessment process.

### Activities

- Severity assessment
- Likelihood assessment
- Risk matrix evaluation
- Residual risk assessment
- Risk acceptance recommendations

### Deliverables

- Risk Assessment Report

---

## Safety Requirements Engineering

Derive measurable safety requirements from identified hazards.

### Activities

- Allocate safety requirements.
- Define safety constraints.
- Establish safety acceptance criteria.
- Maintain traceability.
- Review requirement completeness.

### Deliverables

- Safety Requirements Specification

---

## Safety Architecture

Review the system architecture from a safety perspective.

### Activities

- Assess redundancy.
- Evaluate fault containment.
- Review fault isolation.
- Review graceful degradation.
- Assess watchdog mechanisms.
- Review emergency control paths.

### Deliverables

- Safety Architecture Review

---

## Failure Analysis

Analyse failure mechanisms throughout the system.

### Activities

- Failure Modes and Effects Analysis (FMEA)
- Fault Tree Analysis (FTA)
- Failure propagation analysis
- Common cause analysis
- Single point failure analysis

### Deliverables

- FMEA Report
- Fault Tree Analysis

---

## Safety Reviews

Conduct independent engineering safety reviews.

### Activities

- Review subsystem designs.
- Review software safety.
- Review hardware safety.
- Review communication safety.
- Review operational procedures.
- Review verification evidence.

### Deliverables

- Safety Review Report

---

## Fault Detection & Recovery

Ensure failures are detected and handled safely.

### Activities

- Define fault detection strategies.
- Review recovery mechanisms.
- Validate failsafe behaviour.
- Review emergency procedures.
- Assess recovery timing.

### Deliverables

- Fault Recovery Assessment

---

## Safety Verification

Verify that all safety requirements have been implemented correctly.

### Activities

- Requirement verification
- Fault injection testing
- Redundancy verification
- Watchdog verification
- Emergency procedure verification

### Deliverables

- Safety Verification Report

---

## Safety Validation

Validate the complete UAV under representative operating conditions.

### Activities

- Ground safety testing
- Flight safety testing
- Emergency procedure validation
- Human override validation
- Operational safety assessment

### Deliverables

- Safety Validation Report

---

## Safety Case Management

Maintain the complete body of evidence supporting system safety.

### Activities

- Collect safety evidence.
- Maintain traceability.
- Record residual risks.
- Document assumptions.
- Maintain approval history.

### Deliverables

- Safety Case

---

# Decision Authority

The Safety Engineer has authority to:

- Require hazard analysis.
- Reject unsafe subsystem designs.
- Require additional verification.
- Request design modifications to reduce risk.
- Suspend safety approval until corrective actions are completed.
- Approve closure of verified hazards.

The Safety Engineer does **not** have authority to redesign subsystem implementations. Design changes remain the responsibility of the owning engineering team.

---

# Responsibilities by Lifecycle Phase

| Phase | Responsibility |
|--------|----------------|
| Mission Definition | Support |
| Requirements Engineering | Lead |
| Research & Benchmarking | Support |
| System Architecture | Lead |
| Detailed Design | Lead |
| Implementation | Support |
| Integration | Lead |
| Verification | Lead |
| Validation | Lead |
| Deployment | Lead |
| Maintenance | Lead |

---

# Interaction with Engineering Teams

| Engineering Role | Interaction |
|------------------|-------------|
| Chief Systems Engineer | Safety governance and approval |
| Requirements Engineer | Derive and allocate safety requirements |
| Systems Architect | Review architectural safety |
| Hardware Engineer | Review hardware failure modes |
| Embedded Systems Engineer | Review firmware safety mechanisms |
| Flight Control Engineer | Review control system safety and failsafes |
| Computer Vision Engineer | Review perception-related hazards |
| AI Engineer | Review autonomy and decision-making hazards |
| Communication Engineer | Review communication failure modes |
| Simulation Engineer | Validate hazards in simulation |
| Test Engineer | Plan and review safety verification tests |
| Technical Writer | Maintain safety documentation |

---

# Responsibility Boundaries

The Safety Engineer is responsible for:

- Safety planning
- Hazard identification
- Risk assessment
- Safety requirements
- Safety architecture reviews
- Failure analysis
- Safety verification
- Safety validation
- Safety case management

The Safety Engineer is **not** responsible for:

- Flight control implementation
- AI algorithm development
- Computer vision implementation
- Hardware design
- Embedded application software
- Communication implementation
- Mission execution

---

# Key Performance Indicators (KPIs)

Performance is measured using:

- Hazards identified before implementation
- Safety requirement traceability
- Residual risk level
- Verification coverage
- Validation success rate
- Hazard closure rate
- Safety review completion
- FMEA completion
- FTA completion
- Safety Case completeness

---

# Common Mistakes

Avoid:

- Performing hazard analysis after implementation.
- Accepting undocumented residual risks.
- Assuming software failures are impossible.
- Ignoring human operational errors.
- Closing hazards without objective evidence.
- Treating safety as a one-time activity.

---

# Best Practices

- Identify hazards as early as possible.
- Maintain a living Hazard Log.
- Use quantitative evidence whenever practical.
- Design for fault tolerance.
- Validate degraded operating modes.
- Maintain independent safety reviews.
- Ensure full traceability from hazard to verification.

---

# Related UEOS Documents

- Engineering Philosophy
- Engineering Lifecycle
- Safety Engineer README
- Workflow
- Deliverables
- Chief Systems Engineer
- Systems Architect
- Flight Control Engineer
- AI Engineer
- Communication Engineer
- Test Engineer

---

# Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 2026-07-27 | Initial Release |