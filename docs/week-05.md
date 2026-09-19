
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



-

## Problems and blockers

-

## Decisions

-

## Next week

-

## Links

- Code:
- Photos / CAD:
