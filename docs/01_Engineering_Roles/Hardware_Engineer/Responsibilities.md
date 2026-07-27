# Hardware Engineer Responsibilities

| Field | Value |
|--------|-------|
| Document ID | UEOS-HW-001 |
| Version | 0.1 |
| Status | Active |
| Owner | Hardware Engineer |
| Classification | Engineering Role |
| Last Updated | 2026-07-27 |

---

# Purpose

This document defines the responsibilities, ownership, authority, and decision-making responsibilities of the Hardware Engineer throughout the UAV engineering lifecycle.

The Hardware Engineer is responsible for designing, selecting, integrating, and validating all physical hardware that forms the UAV platform.

---

# Role Overview

The Hardware Engineer transforms the approved physical architecture into a practical, reliable, and manufacturable hardware system.

The role is responsible for ensuring that all hardware components operate together safely and efficiently while satisfying system requirements for performance, weight, power, reliability, maintainability, and environmental robustness.

---

# Primary Responsibilities

## Hardware Platform Design

Design the complete hardware platform that supports mission objectives.

Activities include:

- Select major hardware subsystems.
- Define hardware architecture.
- Ensure subsystem compatibility.
- Verify compliance with system requirements.

### Deliverables

- Hardware Design Document

---

## Component Selection

Evaluate and select appropriate hardware components.

Typical components include:

- Flight Controller
- Companion Computer
- ESCs
- Motors
- Propellers
- Batteries
- Power Distribution Board (PDB)
- GPS
- IMU
- Magnetometer
- Barometer
- Cameras
- LiDAR
- Radar
- Telemetry Modules
- RF Receivers
- Payload Devices

Selection criteria include:

- Performance
- Weight
- Power consumption
- Reliability
- Availability
- Environmental rating
- Cost
- Interface compatibility

### Deliverables

- Component Selection Report
- Bill of Materials (BOM)

---

## Electrical Architecture

Develop the electrical architecture of the UAV.

Activities include:

- Power distribution
- Signal routing
- Voltage rail definition
- Connector selection
- Grounding strategy
- Protection circuitry

### Deliverables

- Electrical Architecture Diagram

---

## Wiring and Interconnect Design

Design all wiring and hardware interconnections.

Activities include:

- Cable routing
- Connector allocation
- Wire gauge selection
- Harness design
- Signal separation
- Labelling conventions

### Deliverables

- Wiring Diagram
- Cable Harness Plan

---

## Power System Design

Design the complete power subsystem.

Activities include:

- Battery selection
- Voltage regulation
- Current estimation
- Power distribution
- Power redundancy (where applicable)
- Protection mechanisms

### Deliverables

- Power Budget
- Power Distribution Diagram

---

## Mechanical Integration

Ensure proper physical integration of all hardware.

Activities include:

- Sensor mounting
- Companion computer mounting
- Flight controller isolation
- Payload integration
- Centre of Gravity (CG) management
- Structural mounting verification

### Deliverables

- Mechanical Integration Plan

---

## Thermal Management

Evaluate thermal behaviour of the hardware platform.

Activities include:

- Identify heat sources.
- Assess airflow.
- Evaluate cooling requirements.
- Verify operating temperatures.
- Recommend passive or active cooling.

### Deliverables

- Thermal Assessment Report

---

## EMI / EMC Considerations

Reduce electrical interference between subsystems.

Activities include:

- Separate power and signal wiring.
- Minimise electromagnetic interference.
- Protect sensitive sensors.
- Verify grounding strategy.
- Reduce noise on communication buses.

### Deliverables

- EMI/EMC Assessment

---

## Hardware Interfaces

Ensure compatibility between interconnected hardware.

Typical interfaces include:

- UART
- SPI
- I²C
- CAN
- USB
- Ethernet
- GPIO
- PWM
- ADC

### Deliverables

- Hardware Interface Specification

---

## Hardware Validation

Verify the assembled hardware platform before software integration.

Activities include:

- Power-on inspection.
- Voltage verification.
- Current verification.
- Sensor connectivity testing.
- Communication testing.
- Connector verification.
- Functional hardware testing.

### Deliverables

- Hardware Validation Report

---

## Manufacturing and Assembly Support

Support production and assembly activities.

Activities include:

- Review manufacturability.
- Produce assembly documentation.
- Define inspection procedures.
- Support prototype assembly.
- Support hardware revisions.

### Deliverables

- Assembly Guide
- Assembly Checklist

---

# Decision Authority

The Hardware Engineer has authority to:

- Select hardware components.
- Approve wiring architecture.
- Define connector standards.
- Recommend mechanical layouts.
- Recommend power system changes.
- Approve hardware revisions.

Major architectural changes require approval from the Systems Architect and Chief Systems Engineer.

---

# Responsibilities by Lifecycle Phase

| Phase | Responsibility |
|--------|----------------|
| Mission Definition | Support |
| Requirements Engineering | Support |
| Research & Benchmarking | Support |
| System Architecture | Support |
| Detailed Design | Lead |
| Implementation | Lead |
| Integration | Support |
| Verification | Support |
| Validation | Support |
| Deployment | Support |

---

# Interaction with Engineering Teams

| Engineering Role | Interaction |
|------------------|-------------|
| Systems Architect | Implements physical architecture |
| Research Engineer | Reviews evaluated components |
| Embedded Systems Engineer | Defines hardware interfaces |
| Flight Control Engineer | Integrates avionics hardware |
| Computer Vision Engineer | Integrates cameras and companion computers |
| Communication Engineer | Integrates RF and telemetry hardware |
| Safety Engineer | Reviews hardware safety and failure modes |
| Test Engineer | Supports hardware verification |
| Technical Writer | Documents hardware design and assembly |

---

# Responsibility Boundaries

The Hardware Engineer is responsible for:

- Hardware selection
- Electrical architecture
- Wiring design
- Power systems
- Mechanical integration
- Thermal management
- EMI/EMC considerations
- Hardware validation
- Manufacturing support

The Hardware Engineer is **not** responsible for:

- Firmware development
- Flight control algorithms
- AI models
- Computer vision software
- Mission planning software

---

# Key Performance Indicators (KPIs)

Performance is measured using:

- Hardware Requirement Coverage
- Power Budget Accuracy
- Component Compatibility
- Assembly Success Rate
- Hardware Failure Rate
- Hardware Validation Pass Rate
- Weight Budget Compliance
- Thermal Performance
- Documentation Completeness

---

# Common Mistakes

Avoid:

- Selecting incompatible components.
- Exceeding power or weight budgets.
- Ignoring connector compatibility.
- Poor cable routing.
- Inadequate thermal management.
- Placing sensors where vibration or EMI degrades performance.
- Designing without considering manufacturability or maintenance.

---

# Best Practices

- Prefer standard interfaces.
- Keep wiring organised and documented.
- Minimise unnecessary weight.
- Design for modular replacement.
- Validate components individually before full integration.
- Consider maintenance and field servicing during design.
- Review power and thermal margins early.

---

# Related UEOS Documents

- Engineering Philosophy
- Engineering Lifecycle
- Systems Architect
- Interface Control Document (ICD)
- Hardware Engineer README
- Workflow
- Deliverables

---

# Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 2026-07-27 | Initial Release |