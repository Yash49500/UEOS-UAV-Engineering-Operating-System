# PX4 Autopilot

| **Document ID** | UEOS-KB-004 |
|-----------------|-------------|
| **Version** | 0.1 |
| **Status** | Active |
| **Owner** | Flight Software Team |
| **Category** | Knowledge Base |

---

# 1. Purpose

This document provides an overview of the PX4 Autopilot flight stack used in UAV systems developed under the UAV Engineering Operating System (UEOS).

---

# 2. What is PX4?

PX4 is an open-source autopilot software platform designed for autonomous aerial, ground, marine, and robotic vehicles.

It provides:

- Flight stabilization
- Navigation
- Mission execution
- Sensor fusion
- Failsafe management
- Vehicle control
- Hardware abstraction

PX4 supports both manual and fully autonomous flight.

---

# 3. PX4 System Architecture

```
Mission Planner
        │
        ▼
Mission Manager
        │
        ▼
Navigator
        │
        ▼
Position Controller
        │
        ▼
Attitude Controller
        │
        ▼
Mixer
        │
        ▼
ESCs
        │
        ▼
Motors
```

---

# 4. Major PX4 Modules

| Module | Purpose |
|----------|---------|
| Commander | Vehicle state management |
| Navigator | Mission execution |
| EKF2 | State estimation |
| Position Controller | Position control |
| Attitude Controller | Attitude stabilization |
| Rate Controller | Angular rate control |
| Mixer | Motor output generation |
| Logger | Flight data logging |
| MAVLink | Communication |
| Parameters | System configuration |

---

# 5. Supported Vehicle Types

PX4 supports multiple vehicle platforms.

- Multirotor
- Fixed Wing
- VTOL
- Rover
- Boat

---

# 6. Flight Modes

Common PX4 flight modes include:

- Manual
- Stabilized
- Altitude
- Position
- Hold
- Mission
- Offboard
- Return
- Land
- Takeoff

---

# 7. Sensor Inputs

PX4 integrates data from multiple onboard sensors.

Typical sensors include:

- IMU
- Accelerometer
- Gyroscope
- Magnetometer
- GPS
- Barometer
- Optical Flow
- Airspeed Sensor
- Rangefinder
- Vision Systems

---

# 8. State Estimation

PX4 estimates the vehicle state using sensor fusion.

State estimates include:

- Position
- Velocity
- Orientation
- Altitude
- Angular Rates

Common estimator:

- EKF2

---

# 9. Offboard Control

Offboard mode allows an external computer to command the UAV.

Typical companion computers include:

- Raspberry Pi
- NVIDIA Jetson
- Intel NUC

Applications:

- AI Navigation
- Object Tracking
- Precision Landing
- Visual Servoing
- Swarm Coordination

---

# 10. Mission Management

Mission capabilities include:

- Waypoint navigation
- Survey missions
- Autonomous takeoff
- Autonomous landing
- Return-to-Launch
- Geofence monitoring

---

# 11. Parameter System

PX4 uses configurable parameters for system behaviour.

Examples:

- PID gains
- Flight limits
- Maximum velocity
- RTL altitude
- Battery failsafe thresholds
- Sensor calibration

---

# 12. Logging

PX4 records flight data for analysis.

Typical logged data:

- IMU
- GPS
- Attitude
- Position
- Battery
- RC Inputs
- Actuator Outputs
- Sensor Health
- CPU Load

Common log formats:

- ULog
- CSV (converted)

---

# 13. Safety Features

PX4 includes several built-in safety mechanisms.

- Arming checks
- Battery failsafe
- RC failsafe
- GPS failsafe
- Geofence
- Kill switch
- Emergency landing
- Return-to-Launch

---

# 14. Development Workflow

```
Develop Feature
        │
        ▼
Simulation (SITL)
        │
        ▼
Bench Testing
        │
        ▼
Hardware-in-the-Loop (HITL)
        │
        ▼
Flight Testing
        │
        ▼
Deployment
```

---

# 15. Simulation

PX4 supports Software-in-the-Loop (SITL) simulation.

Common simulators include:

- Gazebo
- JMAVSim
- AirSim

Simulation is recommended before hardware testing.

---

# 16. Companion Computer Integration

Common integration methods:

- MAVLink
- MAVSDK
- MAVROS
- ROS2
- UART
- Ethernet
- UDP

Typical companion computer responsibilities:

- AI inference
- Vision processing
- Mission planning
- Object detection
- Target tracking
- Sensor processing

---

# 17. Best Practices

- Perform sensor calibration before flight.
- Keep firmware versions documented.
- Test parameter changes in simulation first.
- Enable comprehensive flight logging.
- Validate failsafe behaviour.
- Maintain configuration backups.
- Review logs after every flight.

---

# 18. Related Documents

- Flight_Control.md
- MAVLink.md
- ROS2.md
- Software_Architecture.md
- Hardware_Architecture.md

---

# 19. Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 27-07-2026 | Initial Release |

---

**End of Document**