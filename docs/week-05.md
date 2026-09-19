
# Week 5

**Goal this week:**
Our main goal this week was to continue working on the electronics, find a reliable motor controller and driver setup, and get all four motors running properly.
and starting to designing 3D model body for fiora.

## What we did

Since we didn't want to waste more time, we decided to try another ESP32 model. We switched to an **ESP32 DevKit**, and initially, it worked without any problems. We were able to run our tests with it, but suddenly, that board also stopped working. We suspected that there might be some issue with the power supply, but we couldn't confirm the exact cause.
we 

So, we decided to move to an **Arduino Uno** instead. Since we were changing the controller, we also had to change the motor driver. We first tried using an **L298 motor driver**. It worked, but we noticed that it produced a lot of heat during operation. Because of this, there was also a noticeable power loss, which made it less suitable for our setup.

<img width="400" alt="FIORA - Base with Arduino and L298 Motor Driver" src="https://github.com/user-attachments/assets/d11fbb09-0f7d-426d-93fe-c42c090a1d4e" />

We started looking for another motor driver that would work better for our rover. That's when we found the **Arduino L293D Motor Driver Shield**. It was completely new to us, so we had to spend some time understanding how it worked and figuring out the connections.
Once we figured it out, we started testing it. We also needed a way to control the rover wirelessly, so we added an HC-05 Bluetooth module. We uploaded the required code to the Arduino and connected the HC-05 to the controller.

For the first test, we used a Bluetooth car controller app and controlled a single motor through Bluetooth. The motor responded correctly, so we then connected all the motors to the motor driver shield and tested them again. All the motors were working properly.

After confirming that the electronics were working, we assembled the motors, motor driver, Arduino, Bluetooth module, and battery onto the base. Finally, we tested the complete setup by driving the rover.

<img width="400" alt="FIORA - Base with Arduino and L298 Motor Driver" src="https://github.com/user-attachments/assets/7f19810d-9c86-4eab-a3aa-5d188a17202b" />

And this time, everything worked properly. The rover moved as expected, which was a big step forward for us.

Now, we were planning to start making the 3D model for FIORA. Alen was working on designing the 3D-printed model, while Shamil was working on building the prototype body from his side. We had already drawn a model, and our plan was to make the final body similar to that design.

**How the Drawing Guided the Design**

The drawing gave us a basic reference for how we wanted FIORA to look and how the different parts should be arranged. We used it as a starting point while designing the 3D model, especially for the overall shape, size, and placement of the main components. Instead of designing everything from scratch, we could use the drawing as a guide and gradually modify the 3D model to match the planned design.

<img width="500" alt="FIORA - 3D Model Design" src="https://github.com/user-attachments/assets/de93ace8-9348-43e4-a502-1d498d1ba1f2" />
<img width="500" alt="FIORA - Design" src="https://github.com/user-attachments/assets/6c164d37-a1aa-423c-b2ac-62742e631dc6" />

At the same time, Shan came and told us that we needed to use LiDAR for the project. It was a **SLAMTEC RPLIDAR A1M8**, a 360-degree laser range finder. We didn't really have much of a choice, so we agreed to use it.

This was our first time working with LiDAR, so we knew we had to spend some time learning about it and figuring out how we could use it with FIORA.

<img width="500" alt="FIORA - LiDAR" src="https://github.com/user-attachments/assets/68d1a346-6e68-4ecf-be18-ea1dec6a0ccf" />



-

## Problems and blockers

* Continue testing and improving the motor control system.
* Start working with the RPLIDAR A1M8.
* Learn how to connect and read LiDAR data.
* Start integrating the LiDAR with the Raspberry Pi and FIORA.
*Continue developing the 3D model and prototype body.

## Decisions

* We decided to move from the ESP32 to an Arduino Uno for the motor control.

* We decided not to continue with the L298 motor driver because of the heat and power loss.

* We selected the Arduino L293D Motor Driver Shield for controlling the four motors.

* We added an HC-05 Bluetooth module for wireless control during testing.

* We decided to include the SLAMTEC RPLIDAR A1M8 in FIORA and start learning how to use it.

* We decided to use our existing body design as the reference for developing the 3D-printed body.

## Next week

* Start working with the RPLIDAR A1M8.

* Learn how to connect and read LiDAR data.

* Start integrating the LiDAR with the Raspberry Pi and FIORA.

* Continue developing the 3D model
## Links

- Code:
- Photos / CAD:
