# AI_Project - Weapon Infrared Detection AI
Class: CS3793  
Term: Spring 2022  
Project Proposal: Weapon Infrared Detection AI  
AI Research Team:  
Joe Miller, David Kent, Joshua Ellis, Jose Sarmiento Ruiz, Jacob Shawver

## Table of Contents:
* [Background](#background)
* [Purpose/Hypothesis](#purpose/hypothesis)
* [Technologies](#technologies)
* [Existing Methods](#existingMethods)

## Background:
The prominence of weapon violence in the form of small crime and domestic terrorism is a huge concern for many families. Unfortunately, prevention for these attacks is often very costly, time-inefficient, and can heighten our fears of the attacks rather than reduce it. One of the main preventative strategies is installing metal detectors before building entrances or patting down individuals to detect weapons that one may conceal beneath clothing. Though effective, this is costly, increases wait times to enter buildings, and potentially heightens anxiety of those entering.

Fortunately, there may be a way to make these security procedures much more efficient using artificial intelligence. Object detection is a widely-studied field in the realm of AI, and the ability to train an AI to detect handguns and knives is at this point almost trivial given widely available public datasets. As such, our group hopes to utilize this to train an AI to be able to detect weapons concealed by the user by using the infrared/thermal spectrum, detecting cold spots on the body caused by the hidden weapon. If feasible, this could greatly improve the efficiency of preventative measures, while also pre-empting potential privacy concerns caused by installing an always-active camera for a building entrance.


## Purpose/Hypothesis:
We believe that the existing methods are outdated and should be replaced. We want to show that the usage of FLIR AI object detection would increase the percentage and reliability of detection….   

## Technologies:


## Existing Methods:
Active Sensors:
Using a bandwidth of 400 Mhz it does a 2D scan of the target, that is at a maximum of 3 - 4 meters away.[2] Active Imaging uses the radiation reflections from the scanned scene to create an image.[5] This procedure takes a couple of minutes. While faster than passive sensors, being locked at 400 Mhz, the image produced by the scan is way worse and makes it hard to distinguish a concealed weapon from the body. The higher the frequency the better the resolution of the image. One of the reasons it has trouble displaying a clear image is that weapons have many faceted surface parts, which can reflect the radiation differently and thus requires good positioning or luck for the sensors to catch all of them. Another negative of this method  is it being easily stopped by heavy materials like cotton, since the low frequencies don’t have enough power to penetrate them and be reflected back.[2] Thanks to it having a bad reliability in catching the reflections bouncing off of metallic objects and the other mentioned issues, makes it, compared to other detection methods, one of the worst with its detection probability being the lowest.[1]

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/ActiveSensors.png)

(Fig. 11, [2], left picture unarmed person, right picture armed person)

### Phased Array Antenna:
This uses a Stepped frequency continuous wave radar inside a phase array, to find the item that is hidden and what kind of item it is. The way this works is that the synthesized pulse hits the object, creates ringing, which each different tone has to be known before the scan, and returns as something known as the Late Time Response(LTR). The returned radiation contains  information, which can be used to identify any objects hidden. The issue that exists with this method is that the Complex Natural Resonant (CNR) frequencies that are inside of the LTR are not just from the hidden object, but also from the surroundings being hit by the radiation, since the CNR frequencies independent of the shapes, and thus it can end up messing with the end result. Another part that corrupts the results is the length of time needed for each section of the body to return to the transmitter and receiver.[6]

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/PhasedArrayAntenna.png)  
(Figure 1,Phased Array Imaging, [6])

### Walk-Through Metal Object Detector
The most basic of all detection systems. It produces a magnetic field with any metallic object. This interaction between the detector and the metallic or electrically conductive object generates an electric current, which the machine then detects. The problem with this is that in today’s age, with the invention of 3D printers that can create weapons out of material that are not electrically conductive, this machine can be outsmarted. There also exists the problem with locality, since these machines cannot be placed in areas where they can get wet.[3]

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/WalkThroughObjectMetalDetector.png)  

### Image Processing With IR:
Uses sensors to pick up infrared radiation emitted from the targets
body to be sent to an image processing algorithm. The underlying theory is that the infrared radiation emitted by the human body is absorbed by the clothing and then re-emitted by it. As a result, infrared radiation can be used to show the image of a concealed weapon only when the clothing is tight, thin and stationary [4]. In contrast to this, using IR detection will not work on loose fitting clothing, the infrared radiation gets blurry and spread over the clothing. This decreases the likelihood that it can be processed to a degree that the weapon will be detected.

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/ImageProcessingWithIR.png)  
This shows how a target's body heat can be masked through clothing

### Passive Sensor At 94Hz:
This method uses Passive mm-wave (MMW) imaging to detect concealed weapons under any kind of clothing [2]. This method is very effective with natural illumination during its original tests, but is very time consuming and generally low quality in terms of resolution.With the advent of LNAs with an improved noise ﬁgure, effort was put into an optimisation of the scanning process. The scanning time was reduced to 2.5minutes using only a single channel receiver [2]. Although the resolution of a passive sensor is far superior to that of an active sensor, It is still lackluster in regards to what is observable to the human eye.

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/PassiveSensorAt94HZ.png)

(fig. 4., [2])
Shows the nature of the terrible resolution of passive sensing


Why AI detection using FLIR Imaging is better:
