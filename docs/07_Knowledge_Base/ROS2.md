# ROS2

| **Document ID** | UEOS-KB-006 |
|-----------------|-------------|
| **Version** | 0.1 |
| **Status** | Active |
| **Owner** | Robotics Software Team |
| **Category** | Knowledge Base |

---

# 1. Purpose

This document provides an overview of ROS2 (Robot Operating System 2), its architecture, communication model, and its role in UAV systems developed under the UAV Engineering Operating System (UEOS).

---

# 2. What is ROS2?

ROS2 (Robot Operating System 2) is an open-source robotics middleware that provides standardized libraries, communication mechanisms, and development tools for building distributed robotic systems.

ROS2 is commonly used as the software framework running on a UAV companion computer.

Typical applications include:

- Computer Vision
- AI Inference
- Object Detection
- Object Tracking
- Navigation
- SLAM
- Path Planning
- Multi-Robot Systems
- Sensor Fusion

---

# 3. ROS2 Architecture

```
                ROS2 System

        +-----------------------+
        |      ROS2 Nodes       |
        +-----------------------+

      Camera      MAVROS      AI Node
         │            │            │
         └──────DDS Communication──┘
                    │
          Navigation / Control
                    │
             Flight Controller
```

---

# 4. Core Concepts

ROS2 consists of several fundamental components.

- Nodes
- Topics
- Publishers
- Subscribers
- Services
- Clients
- Actions
- Parameters
- Packages
- Workspaces

---

# 5. Nodes

A Node is an independent software process responsible for performing a specific task.

Examples:

- Camera Node
- Detection Node
- Tracking Node
- Navigation Node
- MAVROS Node
- Logger Node

---

# 6. Topics

Topics provide asynchronous communication between nodes.

Example:

```
Camera Node
      │
      ▼
 /camera/image_raw
      │
      ▼
Detection Node
```

Common UAV topics:

- /camera/image_raw
- /camera/camera_info
- /imu
- /gps
- /odom
- /tf
- /cmd_vel
- /vision_pose

---

# 7. Publishers and Subscribers

Publishers send data.

Subscribers receive data.

Example:

```
Camera Node
Publisher
     │
     ▼
Image Topic
     │
     ▼
Subscriber
Detection Node
```

---

# 8. Services

Services provide synchronous request-response communication.

Example:

```
Calibration Request
        │
        ▼
Camera Service
        │
        ▼
Calibration Response
```

Typical uses:

- Sensor calibration
- Parameter updates
- Diagnostics

---

# 9. Actions

Actions are used for long-running tasks.

Typical UAV actions include:

- Navigate to waypoint
- Follow target
- Scan area
- Return home
- Autonomous landing

---

# 10. Parameters

ROS2 parameters configure node behaviour at runtime.

Examples:

- Camera resolution
- Detection confidence
- Frame rate
- PID gains
- Logging level
- AI model path

---

# 11. Packages

A ROS2 package contains software components such as:

- Nodes
- Launch files
- Configuration files
- Libraries
- Messages
- Services
- Actions

---

# 12. Workspace Structure

Typical workspace:

```
ros2_ws/

├── src/
├── build/
├── install/
├── log/
└── README.md
```

---

# 13. Launch System

Launch files start multiple nodes together.

Typical launch sequence:

```
Launch File

├── Camera Node
├── MAVROS
├── Detection Node
├── Tracking Node
└── Logger
```

---

# 14. Communication Middleware

ROS2 uses DDS (Data Distribution Service).

Benefits:

- Low latency
- Reliable communication
- Distributed architecture
- QoS support
- Scalable networking

---

# 15. Quality of Service (QoS)

Important QoS policies include:

- Reliability
- Durability
- History
- Depth
- Deadline
- Liveliness

QoS should be selected according to application requirements.

---

# 16. UAV Applications

ROS2 is commonly used for:

- Computer Vision
- Autonomous Navigation
- AI Inference
- Object Tracking
- Precision Landing
- Visual Servoing
- Swarm Robotics
- Mission Coordination
- Sensor Fusion

---

# 17. ROS2 and Flight Controllers

Typical integration:

```
ROS2
   │
MAVROS / MAVSDK
   │
MAVLink
   │
PX4 / ArduPilot
   │
Flight Controller
```

---

# 18. Development Workflow

```
Create Package
        │
        ▼
Implement Nodes
        │
        ▼
Build Workspace
        │
        ▼
Launch System
        │
        ▼
Simulation
        │
        ▼
Bench Test
        │
        ▼
Flight Test
```

---

# 19. Best Practices

- Design nodes with a single responsibility.
- Minimize inter-node dependencies.
- Use parameters instead of hardcoded values.
- Record important topics for debugging.
- Use launch files for repeatable deployments.
- Select appropriate QoS settings.
- Test nodes independently before full system integration.

---

# 20. Related Documents

- PX4.md
- ArduPilot.md
- MAVLink.md
- Computer_Vision.md
- Software_Architecture.md

---

# 21. Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 27-07-2026 | Initial Release |

---

**End of Document**