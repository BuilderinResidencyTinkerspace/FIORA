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

<img width="500" alt="FIORA - Base" src="https://github.com/user-attachments/assets/7b4ed960-7f42-4f68-ab21-4e7f24e14db1" />

so now we are going to our next stage and thats electronics. 

We then started working on the electronics side of the project. And, just like everyone else, our first task was to get the motors running.
For this, our first core microcontroller was the **ESP32-S3 Pico**, and we used the **TB6612FNG motor driver**.
We set up the circuit on a breadboard and tested it to make sure everything was connected and working properly.

<img width="400" alt="TB6612FNG Driver and ESP32-S3 Pico" src="https://github.com/user-attachments/assets/02acdefe-900c-4829-93f6-7f7c0b3e5005" />

We first uploaded the code to the microcontroller and then connected the motor driver to test it.
After a few initial tries, it started working. We then used the setup to test the motors and make sure they were rotating properly.

<img width="400" alt="Working Process" src="https://github.com/user-attachments/assets/fc5beb70-cd73-40cf-8e6b-4b21e86b3411" />


But suddenly, the setup stopped working. At the same time, we started getting laptop notifications saying that there might be some problem with the ESP32. We immediately checked the ESP32 by touching it, and it was extremely hot. So, we quickly disconnected the data cable and checked the setup.

When we checked the cable as well, we noticed that it had also become hot. We rechecked the ESP32, and unfortunately, it was already burned. We still don't know the exact reason why it happened.



## Problems and blockers
* The coupler had a lot of unused space, so we had to redesign it to make better use of the available space.
* The ESP32-S3 Pico became extremely hot during testing and was eventually damaged.
* We could not identify the exact reason why the ESP32-S3 Pico burned.
* The data cable also became hot during the incident.

## Decisions
* We redesigned the coupler by making better use of the available space and extending the hexagonal section further into the wheel adapter.
* We decided to start the electronics testing using the ESP32-S3 Pico and TB6612FNG motor driver.
* After the ESP32-S3 Pico failed, we will need to test with another controller before continuing the electronics integration.

## Next week
* Test another controller and motor driver setup.
* Get the motors running again.
* Continue with the electronics integration of FIORA.



## Links

- Code:
- Photos / CAD:
