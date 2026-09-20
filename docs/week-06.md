# Week 6

**Goal this week:** 

Our main goal this week was to start working with the RPLIDAR A1M8, understand how it works, and get the LiDAR data running on the Raspberry Pi. We also planned to continue working on the 3D body design and improve the rover's overall setup.

## What we did

so this week w strated with LIDAR-

We needed to understand how LiDAR would fit into FIORA. Since FIORA is planned to be an autonomous indoor delivery robot, the LiDAR can help the robot detect its surroundings and understand the environment around it. The **RPLIDAR A1M8** can scan the area around the robot and provide distance measurements, which can later be used for mapping and navigation.
we started with a basic setup to understand how the RPLIDAR A1M8 works. We connected the LiDAR to the Raspberry Pi 5 and first focused on getting the raw scan data from the sensor.

Our first goal was not to start autonomous navigation immediately. We wanted to make sure the LiDAR itself was working correctly and that the Raspberry Pi could communicate with it. Once we were able to receive the scan data, we could move on to understanding how the data could be used for mapping and navigation in FIORA.

While we were working on the LiDAR, Shan told us that there was someone in the TinkerSpace community who had worked with LiDAR before. He said he could connect us with that person so they could help us set up the LiDAR and mapping.

That was how we met **Devadath**. He is an AI engineer who also works on hardware-related projects and has good knowledge of IoT and related technologies. With Devadath's help, we started working on setting up the LiDAR.

At the same time, we started thinking about how we could actually use the LiDAR to make FIORA deliver something from one point to another. We wanted to have a system where a user could select a destination and the robot would deliver the item to that location.

Our first idea was to use **WhatsApp**. We thought we could create a bot using the WhatsApp API and set a few fixed points on the LiDAR map. The user could then select one of those points, and FIORA could make the delivery to that location.

**why we initially chose whatsapp**

The main reason we first thought of using **WhatsApp** was because almost everyone already has it on their phone. We didn't want people to download another app or go to a separate website just to use FIORA. They could simply use WhatsApp, which they already know and use regularly, and send the delivery request from there. We felt this would make the system much easier and more convenient for everyone.

So, we explained our idea to **Devadath** and discussed our plan to use WhatsApp for communicating with FIORA. He explained that the **WhatsApp API is not an open API that anyone can simply use for a personal project**. It has to be accessed through Meta's official system, with the required setup, permissions, and verification. Because of these restrictions, we could not simply create a WhatsApp bot and start using it for our project.

Since this made WhatsApp difficult to implement for our project, we started looking for another option. The next option we considered was **Telegram**, since Telegram provides an API that makes it easier to create and use our own bot. So, we decided to explore Telegram as the communication method for FIORA.

So, we thought of using **Telegram** instead. The plan was to use the Telegram API to create a bot through which users could select a delivery destination and send the delivery request to FIORA.

We discussed this idea with Shan and he agreed with the approach. well most of the basic 3D design and base of FIORA were also almost completed, so we could start focusing more on the software, LiDAR, and delivery communication side of the project.

## Problems and blockers

-

## Decisions

-

## Next week

-

## Links

- Code:
- Photos / CAD:
