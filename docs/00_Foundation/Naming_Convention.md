# Naming Convention

| Field | Value |
|--------|-------|
| Document ID | UEOS-FND-004 |
| Version | 0.1 |
| Status | Active |
| Owner | Chief Systems Engineer |
| Reviewer | Project Maintainers |
| Approval Authority | UEOS Core Team |
| Classification | Foundation |
| Last Updated | 2026-07-27 |

---

# 1. Purpose

This document defines the official naming conventions used throughout the UAV Engineering Operating System (UEOS).

A consistent naming convention improves readability, traceability, maintainability, and collaboration across engineering teams.

These standards apply to all repository assets, including documentation, source code, scripts, datasets, hardware, software, and project artefacts.

---

# 2. Scope

This convention applies to:

- Documents
- Folders
- Scripts
- Source Code
- Images
- Diagrams
- Hardware Components
- Software Modules
- AI Models
- Datasets
- Configuration Files
- Git Branches
- Releases
- Engineering Artefacts

---

# 3. General Rules

Names shall be:

- Descriptive
- Concise
- Consistent
- Searchable
- Unique where required

Avoid:

- Spaces
- Abbreviations without definition
- Personal names
- Generic names (Test, Temp, Final, New)

---

# 4. Folder Naming

Folders shall use:

```
Pascal_Case
```

Examples:

```
00_Foundation
01_Engineering_Roles
02_Engineering_Process
03_System_Architecture
Hardware_Selection
Mission_Definition
```

Do not use:

```
foundation
Foundation Files
misc
temp
new folder
```

---

# 5. Markdown Documents

Markdown documents shall use:

```
Pascal_Case.md
```

Examples:

```
Engineering_Philosophy.md
Mission_Definition.md
System_Architecture.md
Verification_and_Validation.md
```

---

# 6. Source Code

Programming language conventions should follow community standards.

Examples:

Python

```
object_detector.py
flight_controller.py
mission_manager.py
```

C++

```
FlightController.cpp
MissionPlanner.cpp
VisionPipeline.cpp
```

Headers

```
FlightController.hpp
MissionPlanner.hpp
```

---

# 7. Variables

Python

```
snake_case
```

Example

```python
target_position
camera_frame
flight_mode
```

C++

```
camelCase
```

Example

```cpp
targetPosition
cameraFrame
flightMode
```

Constants

```
UPPER_CASE
```

Example

```cpp
MAX_ALTITUDE
CAMERA_FPS
SAFE_DISTANCE
```

---

# 8. Classes

Classes shall use:

```
PascalCase
```

Example

```cpp
FlightController
ObjectDetector
MissionPlanner
```

---

# 9. Functions

Python

```python
calculate_velocity()
detect_balloon()
estimate_pose()
```

C++

```cpp
calculateVelocity()
detectBalloon()
estimatePose()
```

---

# 10. Hardware Components

Use descriptive component names.

Examples

```
Pixhawk_6X
Raspberry_Pi_5
Jetson_Orin_Nano
OAK_D_Lite
GPS_M10
```

Avoid

```
controller
camera
board
module
```

---

# 11. AI Models

Model names should contain:

```
<Model>_<Dataset>_<Version>
```

Examples

```
YOLOv11_VisDrone_v1
YOLOv11_Balloon_v2
RTDETR_COCO_v1
```

---

# 12. Datasets

Datasets should follow:

```
<Application>_<Location>_<Version>
```

Examples

```
BalloonDetection_Dataset_v1
DroneTracking_Dataset_v2
LandingPad_Dataset_v1
```

---

# 13. Images

Image names should describe the content.

Examples

```
System_Block_Diagram.png
Power_Distribution.png
Camera_Mount.png
```

Avoid

```
image1.png
new.png
photo.png
```

---

# 14. Diagrams

Use descriptive names.

Examples

```
Mission_Flowchart.drawio
Software_Architecture.drawio
Flight_Control_Block_Diagram.drawio
```

---

# 15. Configuration Files

Examples

```
px4_config.yaml
camera_config.yaml
mission_config.json
```

---

# 16. Git Branches

Feature

```
feature/object-detection
feature/system-architecture
feature/document-template
```

Bug Fix

```
bugfix/camera-calibration
bugfix/readme-links
```

Documentation

```
docs/user-manual
docs/checklists
```

Release

```
release/v0.1
release/v1.0
```

---

# 17. Commit Messages

Use imperative verbs.

Examples

```
Add Engineering Philosophy

Update Flight Test Checklist

Refactor Repository Structure

Improve Architecture Documentation

Fix Broken Links
```

Avoid

```
Update

Done

Changes

Fix

Work
```

---

# 18. Release Tags

Use semantic versioning.

Examples

```
v0.1.0

v0.2.0

v1.0.0

v2.1.3
```

---

# 19. Engineering Artefacts

Mission Documents

```
Mission_Definition.md
```

Requirements

```
System_Requirements.md
```

Architecture

```
System_Architecture.md
```

Test Plans

```
Flight_Test_Plan.md
```

Risk Assessment

```
Risk_Assessment.md
```

Verification

```
Verification_Report.md
```

---

# 20. Reserved Prefixes

| Prefix | Purpose |
|----------|---------------------------|
| UEOS | Framework Documents |
| SYS | System Artefacts |
| HW | Hardware |
| SW | Software |
| AI | Artificial Intelligence |
| SIM | Simulation |
| TEST | Testing |
| DOC | Documentation |

---

# 21. Best Practices

- Keep names short but meaningful.
- Use consistent terminology.
- Avoid duplicate names.
- Avoid personal naming styles.
- Prefer clarity over brevity.
- Follow language-specific conventions.

---

# 22. References

- Repository Standards
- Document Template
- Engineering Philosophy

---

# 23. Revision History

| Version | Date | Author | Description |
|----------|------------|--------|----------------|
| 0.1 | 2026-07-27 | UEOS | Initial Version |

---

# End of Document