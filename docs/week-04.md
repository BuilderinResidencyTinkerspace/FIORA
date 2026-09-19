# Week 4

**Goal this week:** redesign the coupler so the motor and wheel assembly fits properly inside the base and get into electronis

## What we did

So, we started redesigning the coupler. We first looked at the coupler design we were already using and checked where there was any extra or unused space. Honestly, there was quite a lot of space that was not being used.

After the metal shaft entered the coupler, there was around 4 mm of space left towards the wheel adapter. Out of that, around 3 mm was free space, while only about 1 mm was being used by the motor-to-wheel adapter.

So, we decided to make better use of that space. We redesigned the coupler by extending the hexagonal section further towards the wheel adapter. This allowed the hexagonal part of the coupler to go deeper into the hexagonal hole of the wheel adapter.

After printing and testing the new design, we found that the coupler was going fully into the wheel adapter as we wanted. So, that part was completed.
After that, we placed the whole setup on the base and checked whether the wheel was sitting correctly inside the wheel cutout. And yes, it is.


<img width="500" alt="Week 4 - FIORA" src="https://github.com/user-attachments/assets/acc77d93-2788-4bbb-8154-a6bae021b669" />

Finally, we assembled everything together, and at last, everything was fitting properly. 


<img width="500" alt="FIORA - Motor Mounting" src="https://github.com/user-attachments/assets/57a46d48-fd8e-49dd-abf6-c919f10f8e59" />

<img width="500" alt="FIORA - Motor Mounting" src="https://github.com/user-attachments/assets/32452ae2-c6ab-4189-8e9c-91c21187cef0" />

<img width="400" alt="FIORA - Motor Mounting" src="https://github.com/user-attachments/assets/10aaf61c-4842-4359-8aa6-52150283235e" />

so now we are going to our next stage and thats electronics. 

We then started working on the electronics side of the project. And, just like everyone else, our first task was to get the motors running.
For this, our first core microcontroller was the **ESP32-S3 Pico**, and we used the **TB6612FNG motor driver**. We first uploaded the code to the microcontroller and then connected the motor driver to test it.
After a few initial tries, it started working. We then used the setup to test the motors and make sure they were rotating properly.
But suddenly, the setup stopped working. At the same time, we started getting laptop notifications saying that there might be some problem with the ESP32. We immediately checked the ESP32 by touching it, and it was extremely hot. So, we quickly disconnected the data cable and checked the setup.

When we checked the cable as well, we noticed that it had also become hot. We rechecked the ESP32, and unfortunately, it was already burned. We still don't know the exact reason why it happened.

Since we didn't want to waste more time, we decided to try another ESP32 model. We switched to an **ESP32 DevKit**, and initially, it worked without any problems. We were able to run our tests with it, but suddenly, that board also stopped working. We suspected that there might be some issue with the power supply, but we couldn't confirm the exact cause.

So, we decided to move to an **Arduino Uno** instead. Since we were changing the controller, we also had to change the motor driver. We first tried using an **L298 motor driver**. It worked, but we noticed that it produced a lot of heat during operation. Because of this, there was also a noticeable power loss, which made it less suitable for our setup.

We started looking for another motor driver that would work better for our rover. That's when we found the **Arduino L293D Motor Driver Shield**. It was completely new to us, so we had to spend some time understanding how it worked and figuring out the connections.

Once we figured it out, we started testing it. We also needed a way to control the rover wirelessly, so we added an **HC-05 Bluetooth module**. We uploaded the required code to the Arduino and connected the HC-05 to the controller.

For the first test, we used a Bluetooth car controller app and controlled a single motor through Bluetooth. The motor responded correctly, so we then connected all the motors to the motor driver shield and tested them again. All the motors were working properly.

After confirming that the electronics were working, we assembled the motors, motor driver, Arduino, Bluetooth module, and battery onto the base. Finally, we tested the complete setup by driving the rover.

And this time, everything worked properly. The rover moved as expected, which was a big step forward for us.


## Problems and blockers

-

## Decisions

-

## Next week

-

## Links

- Code:
- Photos / CAD:
