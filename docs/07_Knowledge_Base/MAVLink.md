# MAVLink

| **Document ID** | UEOS-KB-003 |
|-----------------|-------------|
| **Version** | 0.1 |
| **Status** | Active |
| **Owner** | Systems Integration Team |
| **Category** | Knowledge Base |

---

# 1. Purpose

This document provides an overview of the MAVLink communication protocol used in UAV systems developed under the UAV Engineering Operating System (UEOS).

---

# 2. What is MAVLink?

MAVLink (Micro Air Vehicle Link) is a lightweight, header-only communication protocol used for communication between:

- Flight Controllers
- Ground Control Stations (GCS)
- Companion Computers
- Payload Computers
- Cameras
- External Sensors

It is designed for low-bandwidth, reliable communication in autonomous systems.

---

# 3. Typical MAVLink Architecture

```
                  Ground Control Station
                           │
                     Telemetry Radio
                           │
                           ▼
                 Flight Controller (PX4)
                    │               │
             Companion PC       GPS / IMU
                    │
               AI Applications
                    │
            External Peripherals
```

---

# 4. Communication Interfaces

Common physical interfaces include:

- UART
- USB
- Ethernet
- UDP
- TCP
- Serial Radio
- Wi-Fi

---

# 5. MAVLink Message Structure

Every MAVLink packet contains:

- Start Byte
- Payload Length
- Sequence Number
- System ID
- Component ID
- Message ID
- Payload
- CRC

```
+-----------------------------------------------------------+
| Header | Payload | CRC |
+-----------------------------------------------------------+
```

---

# 6. System IDs

Each device on the MAVLink network has a unique System ID.

Example:

| Device | System ID |
|--------|-----------|
| Flight Controller | 1 |
| Ground Station | 255 |
| Companion Computer | 191 |
| Camera | 100 |

---

# 7. Component IDs

A System may contain multiple components.

Examples:

| Component | Component ID |
|-----------|--------------|
| Autopilot | 1 |
| Camera | 100 |
| Gimbal | 154 |
| Companion Computer | 191 |

---

# 8. Common MAVLink Messages

| Message | Purpose |
|----------|---------|
| HEARTBEAT | System status |
| ATTITUDE | Vehicle orientation |
| GLOBAL_POSITION_INT | GPS position |
| LOCAL_POSITION_NED | Local position |
| GPS_RAW_INT | Raw GPS data |
| BATTERY_STATUS | Battery information |
| SYS_STATUS | System health |
| COMMAND_LONG | Execute commands |
| COMMAND_ACK | Command acknowledgement |
| PARAM_REQUEST_LIST | Request parameters |
| PARAM_VALUE | Parameter values |
| MISSION_ITEM | Mission waypoint |
| MISSION_COUNT | Number of waypoints |

---

# 9. HEARTBEAT Message

The HEARTBEAT message indicates that a MAVLink component is active.

It contains information such as:

- Vehicle type
- Flight mode
- System status
- Armed state

---

# 10. Telemetry Data

Typical telemetry includes:

- GPS Position
- Local Position
- Attitude
- Velocity
- Battery Status
- Flight Mode
- Airspeed
- Altitude
- RC Inputs

---

# 11. Commands

Examples of MAVLink commands:

- Arm
- Disarm
- Takeoff
- Land
- Return to Launch (RTL)
- Set Flight Mode
- Upload Mission
- Start Mission
- Reboot Autopilot
- Calibrate Sensors

---

# 12. Parameters

Flight controllers expose configurable parameters.

Examples:

- PID gains
- RTL altitude
- Maximum speed
- Failsafe behaviour
- Battery thresholds
- GPS configuration

---

# 13. Mission Protocol

Mission upload consists of:

```
Ground Station
      │
MISSION_COUNT
      │
MISSION_REQUEST
      │
MISSION_ITEM
      │
MISSION_ACK
```

---

# 14. Companion Computer Integration

A companion computer can:

- Receive telemetry
- Send commands
- Upload missions
- Control flight modes
- Publish vision estimates
- Publish target positions
- Trigger payloads

Common software libraries:

- MAVSDK
- MAVROS
- pymavlink

---

# 15. Security Considerations

- Validate incoming messages.
- Ignore malformed packets.
- Restrict network access.
- Monitor communication loss.
- Protect command interfaces.
- Encrypt external communication channels where appropriate.

---

# 16. Performance Considerations

- Avoid unnecessary message rates.
- Prioritise critical telemetry.
- Monitor link bandwidth.
- Reduce packet loss.
- Use reliable serial connections where possible.

---

# 17. Best Practices

- Maintain unique System IDs.
- Verify Component IDs.
- Monitor HEARTBEAT messages continuously.
- Handle communication timeouts.
- Log important telemetry.
- Test all commands before flight.
- Verify protocol compatibility between software versions.

---

# 18. Related Documents

- PX4.md
- ROS2.md
- Flight_Control.md
- Software_Architecture.md
- Hardware_Architecture.md

---

# 19. Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.1 | 27-07-2026 | Initial Release |

---

**End of Document**