# Builder-in-Residence — FIORA


# FIORA — Building an Indoor Delivery Robot, One Week at a Time

FIORA is our Builder-in-Residence project: an indoor delivery robot designed to carry documents and small items between selected locations in places such as colleges and offices. The idea is to reduce repeated trips for simple deliveries and make it easier for someone to request an item from another room.

We are developing FIORA step by step. We started with a simple physical base, then worked through the mechanical problems of fitting the motors and mecanum wheels. After several CAD and 3D-printing iterations, we got the rover moving with an Arduino-based motor-control setup. We then moved towards sensing and mapping by connecting a RPLIDAR A1M8 to a Raspberry Pi 5 and visualizing its scan data with ROS 2 and RViz2.

The project has not been straightforward. Parts did not fit as expected, printed dimensions differed from the CAD model, and two controller boards stopped working during electronics testing. Each problem forced us to check our assumptions and change the design or setup instead of simply following the original plan.

> **Current state:** The rover has been driven manually using Bluetooth, and we have connected the RPLIDAR A1M8 to ROS 2 and visualized scan data in RViz2. We have started mapping by manually moving the robot around an area. Fully autonomous navigation, reliable point-to-point delivery, and the Telegram delivery bot are still work in progress; they should not be treated as completed features yet.

## The idea behind FIORA

In a college or office, people often need to carry documents or small items from one room to another. FIORA is intended to help with those repeated indoor trips. A user should eventually be able to choose a destination, submit a delivery request, and have the robot travel to that location.

To work towards that goal, we need to solve several connected problems:

- **Mechanical design:** Build a stable base and fit the motors, mecanum wheels, mounts, and body together.
- **Motor control:** Drive all four motors reliably and make the robot respond to movement commands.
- **Perception and mapping:** Use LiDAR data to understand the surroundings and build a map of the operating area.
- **Navigation:** Use the map and the robot's dimensions to plan and follow a route safely.
- **User communication:** Provide a simple way to request a delivery and choose a destination.

We are treating these as separate milestones so that each part can be tested before we rely on the complete system.

## How the system is coming together

The design has changed as we learned more and tested different hardware. The following describes the current direction based on our documented progress, rather than a claim that every part is already integrated.

| Part | Current role / status |
|---|---|
| Chassis and mecanum wheels | A circular foam-sheet base was used for the early prototype. The wheel positions and motor mounts were adjusted through repeated fitting tests. |
| Custom couplers and motor mounts | Designed in CAD and 3D-printed because ready-made parts did not fit the wheel hub or were too expensive. The coupler and triangular motor-mount designs were refined through multiple iterations. |
| Motors and motor control | Four motors were tested using an Arduino Uno and an L293D Motor Driver Shield. An HC-05 Bluetooth module was added for manual wireless control. |
| Raspberry Pi 5 | Used as the onboard computer for LiDAR and ROS 2 work. |
| SLAMTEC RPLIDAR A1M8 | Provides 360-degree distance scans of the surrounding area. |
| ROS 2 and RViz2 | Used to receive and visualize LiDAR scan data and support the early mapping work. |
| Telegram bot | Planned as the user-facing method for selecting a delivery destination and requesting a delivery. The bot and autonomous delivery workflow are still to be implemented. |

### Why we changed some of our early choices

**Custom parts instead of ready-made adapters.** The available wheel-adapter models did not match our dimensions, and suitable ready-made parts were too expensive. Designing our own parts gave us more control over the fit, but it also taught us that CAD dimensions and printed dimensions do not always match exactly.

**A different motor-control setup.** Our first ESP32-S3 Pico setup with a TB6612FNG driver became extremely hot and was damaged. An ESP32 DevKit later stopped working too, although we could not confirm the cause. An L298 driver worked during testing but produced considerable heat and power loss. We then moved to an Arduino Uno with an L293D Motor Driver Shield and HC-05 Bluetooth control, which allowed us to get all four motors responding and drive the rover.

**Telegram instead of starting with WhatsApp.** We initially wanted to use WhatsApp because most people already have it. However, the official WhatsApp Business Platform API has setup, access, and verification requirements. Telegram's bot API looked more practical for our prototype, so we chose to explore that route.

## Main hardware and software

This list reflects the components and tools documented in the first seven weeks. It may change as we test the complete robot.

| Item | Use in FIORA |
|---|---|
| Mecanum wheels | Allow the chassis to be designed for movement in different directions. |
| GB37 geared motors | Drive the wheels. |
| Arduino Uno | Handles the current motor-control prototype. |
| L293D Motor Driver Shield | Drives the motors during the working manual-control tests. |
| HC-05 Bluetooth module | Receives commands for manual driving tests. |
| Raspberry Pi 5 | Runs the LiDAR and ROS 2 setup. |
| SLAMTEC RPLIDAR A1M8 | Measures distances around the robot. |
| ROS 2 | Robot software framework used for the LiDAR setup. |
| RViz2 | Visualizes the LiDAR scan data. |
| CAD and 3D printing | Used to design and test the coupler, motor mounts, and robot body. |
| Telegram Bot API | Planned for delivery requests and destination selection. |

## Development journal

These weekly notes explain what we tried, what did not work, the decisions we made, and what we planned to do next. The project is still developing, so the notes distinguish between completed tests and future goals.

- [Week 1 — Building the base and identifying the adapter problem](docs/week-01.md)
- [Week 2 — Designing and printing the coupler](docs/week-02.md)
- [Week 3 — Developing the motor mounts](docs/week-03.md)
- [Week 4 — Fixing the mechanical fit and starting electronics](docs/week-04.md)
- [Week 5 — Getting all four motors working](docs/week-05.md)
- [Week 6 — Connecting LiDAR and choosing a communication method](docs/week-06.md)
- [Week 7 — Visualizing scans and starting mapping](docs/week-07.md)

## What works so far?

Based on the work recorded through Week 7:

- The early chassis, custom coupler, and motor mounts have been designed and tested for fit.
- All four motors responded during tests using the Arduino Uno, L293D Motor Driver Shield, and HC-05 Bluetooth control.
- The rover was assembled and driven manually.
- The RPLIDAR A1M8 was connected to the Raspberry Pi 5 setup.
- LiDAR scan data was visualized with ROS 2 and RViz2.
- Initial mapping work was carried out by manually driving the robot around TinkerSpace.

These are useful milestones, but they do not yet mean FIORA can autonomously navigate to a delivery point.

## Current challenges and limitations

- **Robot footprint:** The LiDAR is mounted near the centre of the chassis. The scan origin alone does not represent the full size of the robot, so the robot's footprint needs to be represented correctly in the navigation setup.
- **Mapping and navigation:** We are still learning and testing the mapping workflow. Reliable localization, route planning, obstacle avoidance, and point-to-point autonomous driving remain future milestones unless separately demonstrated in later logs.
- **Power and reliability:** Earlier controller failures had unknown causes. The power and wiring setup needs to remain reliable as more components are integrated.
- **Body design:** The physical body must leave enough room for the motors, electronics, battery, and LiDAR without making the robot unnecessarily large or difficult to manufacture.
- **Delivery interface:** The Telegram bot and its connection to actual robot movement are planned work, not completed features in the first seven weeks.

## What we plan to do next

Our next steps are to improve the mapping setup, represent the robot's footprint properly, and work towards using a map for navigation. We also plan to build the Telegram bot around fixed delivery destinations, continue refining the body design, and check the power arrangement as the Raspberry Pi and other components are used together.

We will update this README as those milestones are tested. We want it to reflect what the robot can actually do, not just what we hope it will eventually do.

## Repository layout

```text
.
├── README.md              # Main project story and current status
├── mkdocs.yml             # MkDocs site configuration
├── docs/
│   ├── index.md           # Documentation home page
│   ├── week-01.md         # Weekly development logs
│   ├── week-02.md
│   ├── week-03.md
│   ├── week-04.md
│   ├── week-05.md
│   ├── week-06.md
│   └── week-07.md
├── code/                  # Firmware, scripts, and runnable software (add as available)
└── cad/                   # CAD designs and 3D-print files (add as available)
```

The `code/` and `cad/` folders are included in the intended structure; add the actual files as they are ready to share.

## Preview the documentation locally

If you have Python installed, install MkDocs Material and run the local preview from the repository root:

```bash
pip install mkdocs-material
mkdocs serve
```

MkDocs will print a local address in the terminal. Open that address in your browser to preview the documentation. The BIR repository's GitHub Pages settings and deployment workflow may need to be configured according to the template instructions.

---

*FIORA is being built one milestone at a time. The weekly logs are the record of that process, including the iterations and setbacks that shaped the design.*
