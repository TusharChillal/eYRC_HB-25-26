# HoloBattalion (HB) | Multi-Robot Autonomous Warehouse System
### e-Yantra Robotics Competition 2025-26 | Team ID: 3081

This repository serves as a professional portfolio for Team 3081's implementation of the **HoloBattalion** theme. The project focuses on the coordinated control of a holonomic robot fleet designed for automated sorting and storage in a simulated cold-storage environment.

---

## Project Demonstrations
* **Software Simulation:** [Watch on YouTube](https://youtu.be/Cn1KS8OC27Y)
* **Physical Hardware Run 1:** [Watch on YouTube](https://youtu.be/FS7TUFY_0mY)
* **Physical Hardware Run 2:** [Watch on YouTube](https://youtu.be/B4PnHWnY4M4)

---

## System Overview
The mission involves three autonomous holonomic robots—**Glacio, Crystal, and Frostbite**—operating under a centralized control system. The robots must identify, pick, and stack color-coded crates into designated zones before a 250-second "spoilage" timer expires.

### Key Technical Challenges:
* **Holonomic Motion Control:** Implementing 3-wheel omni-drive kinematics for $360^\circ$ maneuverability.
* **Multi-Agent Coordination:** Managing path planning for three bots simultaneously to avoid collisions.
* **Precision Stacking:** Utilizing feedback for structured interlocking crate placement.



---

## Hardware Engineering
As the **Team Lead**, I spearheaded the hardware integration and PCB development to ensure the bots met the strict competition constraints (max 8cm radius).

### Component Breakdown:
| Category | Specification |
| :--- | :--- |
| **Controller** | ESP32 WROOM (WiFi/Bluetooth enabled) |
| **Locomotion** | 3x MG995 Continuous Rotation Servos with 38mm Omni-wheels |
| **Manipulator** | MG90s Servo-driven articulated arm |
| **Power** | 11.1V 3S LiPo with XL4015 Buck Regulation |
| **Sensing** | IR Sensors for localized feedback |

### Custom PCB Design
We designed a custom PCB to centralize power distribution and signal routing, reducing wire clutter and improving system reliability.
> **Note:** See the `images/` folder for high-resolution photos of the custom PCB and the final physical robot assembly.

---

## Software Architecture
The system utilizes a hybrid control architecture. While the source code is protected under competition rules, the high-level logic includes:

* **Middleware:** ROS 2 Humble on Ubuntu 22.04.
* **Perception:** Real-time localization via an overhead camera using **OpenCV** and **ArUco** marker tracking.
* **Communication:** Micro-ROS / Serial communication between the ROS 2 master and ESP32 clients.
* **Strategy:** An optimized task-allocation algorithm that dynamically calculates the most efficient robot-to-crate pairings.



---

## Skills & Expertise
* **Robotics:** ROS 2 (Nodes, Actions, Services), Kinematics, Path Planning.
* **Embedded Systems:** C++/Arduino, ESP32, PCB Layout, Power Management.
* **Computer Vision:** ArUco Marker Detection, Coordinate Transformation.

---

## Team 3081
* **Tushar** - Team Lead | Navigation & Embedded Systems
* [Team Member 2 Name]
* [Team Member 3 Name]
* [Team Member 4 Name]

---
*Disclaimer: Source code and detailed logic are withheld in compliance with e-Yantra competition guidelines to maintain academic integrity.*
