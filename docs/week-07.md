# Week 7

## Goal this week

Our main goal this week was to continue working on the **RPLIDAR A1M8** and understand how to use its scan data for mapping and navigation in FIORA. We also planned to **complete the 3D model of FIORA and start printing the body parts**. Along with this, we wanted to improve the overall design and move forward with both the LiDAR setup and the physical build of the robot.

## What we did.

We first wanted to check whether we could create a map using the LiDAR. So, we connected the **RPLIDAR A1M8 to ROS 2** and used **RViz2** to visualize the scan data. We then manually mapped the surroundings to understand how the LiDAR scans the environment and how the data could be used for mapping in FIORA.

<img width="500" alt="LiDAR Mapping" src="https://github.com/user-attachments/assets/47839a0f-7f5c-4459-ba7a-7ccb6dce4bd3" />

The red lines shown in RViz2 represent the obstacles detected by the LiDAR's laser. After connecting the LiDAR to the prototype body, we manually drove the robot using **Bluetooth** to test how the LiDAR scanned the surroundings.

We started our mapping and design work at **TinkerSpace**, so we planned to map the entire space. However, we came across a problem during the initial mapping process. The LiDAR was mounted at the centre of the robot's body. This meant that if any part of the robot's body hit an obstacle, the LiDAR might not detect it because the obstacle could be outside the LiDAR's scanning position.

We discussed this problem with **Devadath**, and he suggested a solution. He explained that RViz2 has an option to account for the robot's body dimensions. We could specify the diameter of the robot's body so that the mapping and navigation system could consider the robot's size instead of relying only on the LiDAR's position.

Following his suggestion, we added the dimensions of our prototype body in RViz2 and configured it accordingly. After making these adjustments, we continued with the mapping process.


<img width="400" alt="LiDAR and Prototype Body" src="https://github.com/user-attachments/assets/276a3658-a8ec-4971-aed4-e2069c5d5d72" />

<img width="500" alt="LiDAR Mapping" src="https://github.com/user-attachments/assets/cdb55a54-be26-4436-91d0-c6ff7e05a672" />

https://github.com/user-attachments/assets/bc92c07e-f1ff-470a-ac00-ad31e8d23390

After making these adjustments, we reached that stage of the process and were ready to continue mapping the TinkerSpace area. We had completed the initial setup and solved the issue of accounting for the robot's body size in RViz2. From there, we continued working on mapping the surroundings using the LiDAR and manually driving the prototype.


## Problems and blockers
* The LiDAR was mounted at the centre of the robot's body, so it could not detect every obstacle that might come into contact with the outer parts of the robot.
* We needed to configure the robot's body dimensions in RViz2 to account for the actual size of the prototype.
* We were still learning how to use LiDAR scan data for mapping and navigation.

## Decisions
* We decided to use ROS 2 and RViz2 to visualize the LiDAR scan data and work on mapping.
* We manually drove the prototype using Bluetooth while testing the LiDAR and mapping process.
* We added the prototype body's dimensions in RViz2 to account for the robot's size.
* We decided to continue mapping the TinkerSpace area using the LiDAR.

## Next week
* Improve the mapping setup and test the accuracy of the generated map.
* Use **SLAM (Simultaneous Localization and Mapping)** to create a map of the surroundings.
* Add fixed delivery points to the Telegram bot so users can select a destination.
* Work towards enabling **automatic delivery**, where FIORA can navigate to the selected point and deliver the item.

## Links

- Code:
- Photos / CAD:
