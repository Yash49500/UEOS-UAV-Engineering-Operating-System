# Terminal Guidance UAV

| **Document ID** | UEOS-EX-003 |
|-----------------|-------------|
| **Version** | 0.1 |
| **Status** | Example |
| **Category** | Autonomous UAV Example |

---

# 1. Overview

This document demonstrates the implementation of a UAV capable of autonomous terminal guidance towards a selected target using onboard vision, target tracking, and real-time guidance algorithms.

The objective is to illustrate the complete perception-to-guidance pipeline used for autonomous terminal guidance research.

---

# 2. Mission Objective

The UAV shall:

1. Take off autonomously.
2. Navigate to the search area.
3. Detect potential targets.
4. Select the designated target.
5. Continuously estimate target position.
6. Compute guidance commands.
7. Perform terminal approach.
8. Reach the terminal point.
9. Complete the mission or execute recovery.

---

# 3. Mission Flow

```
Takeoff
   │
   ▼
Navigate to Search Area
   │
   ▼
Detect Target
   │
   ▼
Select Target
   │
   ▼
Track Target
   │
   ▼
Terminal Guidance
   │
   ▼
Target Reached?
   │
Yes────────────► Mission Complete
   │
No
   ▼
Continue Guidance
```

---

# 4. System Architecture

```
Camera
   │
   ▼
Object Detection
   │
   ▼
Target Tracking
   │
   ▼
Target Estimation
   │
   ▼
Guidance Algorithm
   │
   ▼
Flight Controller Interface
   │
   ▼
PX4 / ArduPilot
```

---

# 5. Hardware

| Component | Example |
|-----------|----------|
| Airframe | Quadcopter |
| Flight Controller | Pixhawk / CubePilot |
| Companion Computer | Raspberry Pi 5 / Jetson |
| Camera | CSI Camera / USB Camera |
| IMU | Integrated |
| GPS | u-blox |
| Telemetry | MAVLink |
| Battery | LiPo |

---

# 6. Software Stack

| Layer | Software |
|--------|----------|
| Operating System | Ubuntu |
| Robotics Middleware | ROS2 |
| Flight Stack | PX4 / ArduPilot |
| Communication | MAVLink |
| Detection | YOLO |
| Tracking | ByteTrack / StrongSORT |
| Guidance | Custom Guidance Algorithm |

---

# 7. Functional Modules

- Camera Interface
- Target Detection
- Target Tracking
- Target State Estimation
- Guidance Algorithm
- Flight Controller Interface
- Mission Manager
- Data Logger

---

# 8. Detection Pipeline

```
Camera
   │
   ▼
Image Acquisition
   │
   ▼
YOLO Detection
   │
   ▼
Target Selection
```

---

# 9. Tracking Pipeline

```
Detection
    │
    ▼
Tracker
    │
    ▼
Target State
```

---

# 10. Guidance Pipeline

```
Target State
      │
      ▼
Relative Position
      │
      ▼
Guidance Law
      │
      ▼
Desired Velocity
      │
      ▼
Flight Controller
```

---

# 11. Example Guidance Loop

```
Capture Image
      │
      ▼
Detect Target
      │
      ▼
Track Target
      │
      ▼
Estimate Relative Position
      │
      ▼
Compute Guidance Command
      │
      ▼
Send MAVLink Setpoint
      │
      ▼
Repeat
```

---

# 12. Guidance Algorithms

Possible guidance algorithms include:

- Pure Pursuit
- Proportional Navigation (PN)
- Augmented Proportional Navigation (APN)
- Line-of-Sight (LOS) Guidance
- Image-Based Visual Servoing (IBVS)
- Position-Based Visual Servoing (PBVS)
- PID Guidance
- Model Predictive Control (MPC)

---

# 13. Inputs

- Camera Images
- IMU
- GPS
- Vehicle Attitude
- Vehicle Position
- Vehicle Velocity
- Target Detection
- Target Tracking Output

---

# 14. Outputs

- Velocity Setpoints
- Position Setpoints
- Yaw Commands
- Flight Mode Commands
- Mission Status
- Flight Logs

---

# 15. Failure Handling

| Failure | Recovery |
|----------|----------|
| Target Lost | Search Pattern |
| Detection Failure | Hover |
| Tracking Failure | Re-detect Target |
| GPS Failure | Vision Navigation (if available) |
| Communication Loss | RTL |
| Low Battery | RTL |
| Camera Failure | Hover or Land |

---

# 16. Performance Goals

| Parameter | Target |
|-----------|--------|
| Detection FPS | ≥20 FPS |
| Tracking FPS | ≥30 FPS |
| Guidance Update Rate | ≥20 Hz |
| End-to-End Latency | <100 ms |
| Target Tracking Accuracy | >95% |
| Mission Success Rate | >90% |

---

# 17. Verification Strategy

- Unit Testing
- Software Simulation
- SITL
- Bench Testing
- Hardware-in-the-Loop
- Indoor Flight Testing
- Outdoor Flight Testing
- Terminal Guidance Validation

---

# 18. Related Documents

- Computer_Vision.md
- Flight_Control.md
- AI_System_Patterns.md
- MAVLink.md
- ROS2.md
- UAV_System_Architecture.md

---

# 19. Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 27-07-2026 | Initial Release |

---

**End of Document**