# Week 0 — Ideate

**Goal this week:**  
Land on a project idea and validate whether our planned hardware and software stack can realistically support an autonomous indoor delivery robot.

---

## What we did

* Brainstormed multiple robotics project directions for the 9-week build.
* Finalized the concept:
  **FIORA** — an autonomous indoor material delivery robot that:
  * Transports documents, materials, and small packages between designated locations
  * Navigates indoor environments autonomously
  * Detects and avoids obstacles
  * Provides a touchscreen interface for delivery requests and robot status
* Identified potential applications:
  * Offices
  * Warehouses
  * Hospitals
  * Hospitality
  * Other indoor facilities
* Planned the core hardware:
  * Raspberry Pi
  * Arduino UNO R4
  * 4 × encoder geared motors
    * GB37 12V 60 RPM 
  * 4 × mecanum wheels
  * 2 x L298N motor drivers
  * SLAMTEC RPLIDAR A1M8
  * IMU MPU-6050
  * DWIN 7-inch touchscreen
* Evaluated the feasibility of:
  * ROS 2 Jazzy
  * SLAM Toolbox
  * Nav2
  * LiDAR-based mapping
  * Encoder-based odometry
  * IMU-based motion feedback
  * * Explored Telegram as the communication interface for FIORA:
  * Users can send delivery requests through a Telegram bot
  * FIORA can receive commands remotely
  * Robot status and delivery completion can be sent back to the user
* Planned Telegram-based features:
  * Delivery request
  * Destination selection
  * Delivery status updates
  * Battery/status notifications
  * Delivery completion notification

---

## Problems and blockers

* Autonomous navigation requires reliable integration between:
  * LiDAR
  * Wheel encoders
  * IMU
  * ROS 2
  * Motor controller
* Mecanum wheels introduce additional complexity in:
  * Odometry
  * Wheel synchronization
  * Motion control
* The foam-sheet prototype chassis needs reinforcement around motor mounting points.
* The battery must safely supply both motors and electronics.
* The DWIN touchscreen requires separate UI design and DGUS configuration.
* LiDAR-based mapping and navigation still need to be validated on the actual robot.
* TELEGRAM DELIVERY        
 * Internet connection is required for Telegram communication.
 * Telegram API/token security must be maintained.
 * Network delays may affect command and status updates.
 * Raspberry Pi must stay connected and online.

---

## Decisions

* Finalized the project name: **FIORA**
* Finalized the core objective:
  * **Autonomous indoor material delivery**
* Selected the core navigation stack:
  * **ROS 2 + LiDAR + SLAM Toolbox + Nav2**
* Selected **TB6612FNG** motor drivers for the prototype.
* Selected **YDLIDAR X2** for indoor mapping and navigation.
* Selected a **DWIN 7-inch touchscreen** for the user interface.
* Decided to keep advanced features modular so they can be added after the core system works.
* Possible future features:
  * 4G connectivity using SIM7600
  * Charging dock
  * Delivery queue
  * QR-based delivery confirmation
  * Smart cargo locking
  * Voice notifications

---

## Next week

* Start building the physical prototype:
  * Fabricate the chassis
  * Install motors and mecanum wheels
  * Mount motor drivers
* Test:
  * Individual motor operation
  * Encoder feedback
  * Mecanum wheel movement
  * ESP32 motor control
* Begin communication between the ESP32 and main computer.
* Set up the ROS 2 environment for LiDAR and navigation testing.

---

## Links

* **Code:**
* **Photos / CAD:**
## Weekly logs

Start with [Week 1](week-01.md) and fill one in each week.
