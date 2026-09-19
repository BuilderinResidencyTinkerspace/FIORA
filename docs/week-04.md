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

so now we are going to our next stage and that electronics. 

nammal electronicil work cheyyan thudangi. and first ellavarudeyum pole thanne nammudeyum task motor karakuka ennayirunnu. so nammal mammude 1st core micro controller is esp32 s3 pico vestion aan.
and TB6612FNG motordriver aayrunnu. njngal first mculekk code applode cheythu ennit motor driver connct cheythunoki at first kurach try it was working njngal ath vech motors okke karaki aayrunnu.

but suddently it was not working appozhanel und lapinn notification verunne esp32 have some problem enn oke paranjitt. so njngal esp32 touch cheyth nokumbol ind its too hot appol thanne njngal data cable okke disconnect cheythu. nokkumbol anell cable okke heat aayittund aayrunnu. wew recheked the esp again and it was burned. the real reason enthan enn njngalk ippolum ariyilla. so njngal time waste cheyyanda enn vicharichitt vere esp32 models use cheyyan vicharichu. and we tried esp32 devkit 
ath first okke preshnam illand thanne work cheythinayrunnum but suddently ath work cheyyand aay. and we think its power issue anne aan vicharikune. so. njagal arduino unoyilek mari. athukond thanne njngalk motor driver koode mattendi vanu. nagane njgal L298 use cheythu. but L298 has also limit. lots of heat produce avunnuath kond thane vallathe power lose indayirunnu. so njngal ath solve cheyan vendi vera oru driver search cheyth kond irinnu. tahts how njngal arduino L293D motor driver shield enna oru module kandethiyath. an itwas new to use us. but atlast we figured it out and started our work. we also needed to install a bluetooth module we had to drive the rover when it works. so also added a BT HC-05 module for bluetooth connection, and we uploaded the code to arduino and connected to the bluetooth and tested by moving a motor using BT car contrioller app and its was working, so we connected all motors to the sheild and tested again, it was all working properly. we assembled every motor and controlers and bettery to the base and drove our rover and it moves just fine.  

## Problems and blockers

-

## Decisions

-

## Next week

-

## Links

- Code:
- Photos / CAD:
