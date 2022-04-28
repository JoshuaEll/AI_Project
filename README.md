# AI_Project - Weapon Detection 
Class: CS3793  
Term: Spring 2022  
Project Proposal: Weapon Infrared Detection AI  
Team 10: Joe Miller, Joshua Ellis, David Kent, Jacob Shawver, Jose Sarmiento Ruiz  

AI Research
Joe Miller, David Kent, Joshua Ellis, Jose Sarmiento Ruiz, Jacob Shawver

Background:
We chose the topic of object detection for weapons, because it is an important part to keep the people safe. There are a lot of methods in use today…..

Purpose/Hypothesis:
We believe that the existing methods are outdated and should be replaced. We want to show that the usage of FLIR AI object detection would increase the percentage and reliability of detection….    
Existing Methods:
Active Sensors:
Using a bandwidth of 400 Mhz it does a 2D scan of the target, that is at a maximum of 3 - 4 meters away.[2] Active Imaging uses the radiation reflections from the scanned scene to create an image.[5] This procedure takes a couple of minutes. While faster than passive sensors, being locked at 400 Mhz, the image produced by the scan is way worse and makes it hard to distinguish a concealed weapon from the body. The higher the frequency the better the resolution of the image. One of the reasons it has trouble displaying a clear image is that weapons have many faceted surface parts, which can reflect the radiation differently and thus requires good positioning or luck for the sensors to catch all of them. Another negative of this method  is it being easily stopped by heavy materials like cotton, since the low frequencies don’t have enough power to penetrate them and be reflected back.[2] Thanks to it having a bad reliability in catching the reflections bouncing off of metallic objects and the other mentioned issues, makes it, compared to other detection methods, one of the worst with its detection probability being the lowest.[1]

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/ActiveSensors.png)

(Fig. 11, [2], left picture unarmed person, right picture armed person)

Phased Array Antenna:
This uses a Stepped frequency continuous wave radar inside a phase array, to find the item that is hidden and what kind of item it is. The way this works is that the synthesized pulse hits the object, creates ringing, which each different tone has to be known before the scan, and returns as something known as the Late Time Response(LTR). The returned radiation contains  information, which can be used to identify any objects hidden. The issue that exists with this method is that the Complex Natural Resonant (CNR) frequencies that are inside of the LTR are not just from the hidden object, but also from the surroundings being hit by the radiation, since the CNR frequencies independent of the shapes, and thus it can end up messing with the end result. Another part that corrupts the results is the length of time needed for each section of the body to return to the transmitter and receiver.[6]

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/PhasedArrayAntenna.png)


(Figure 1,Phased Array Imaging, [6])

Acoustic-Based Hard Object Detector:
This is a handheld device that creates soundwaves and uses these to detect potential weapons. Depending on the material the volume of the sound reflected changes. Hard objects, especially metal, make loud sounds, while things like plastic make low sounds. The problem with this method is, that it gets triggered by all kinds of objects, not only weapons and items made out of leather will create a loud sound making it possible to hide weapons inside of or under it.[3] Another issue is that this kind of method is normally not automated and requires a Human to be present, which can endanger them.


Image Processing With IR:
Uses sensors to pick up infrared radiation emitted from the targets
body to be sent to an image processing algorithm. The underlying theory is that the infrared radiation emitted by the human body is absorbed by the clothing and then re-emitted by it. As a result, infrared radiation can be used to show the image of a concealed weapon only when the clothing is tight, thin and stationary [4]. In contrast to this, using IR detection will not work on loose fitting clothing, the infrared radiation gets blurry and spread over the clothing. This decreases the likelihood that it can be processed to a degree that the weapon will be detected.

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/ImageProcessingWithIR.png)

(this is a dogshit source im gonna change this btw)
This shows how a target's body heat can be masked through clothing

Passive Sensor At 94Hz:
This method uses Passive mm-wave (MMW) imaging to detect concealed weapons under any kind of clothing [2]. This method is very effective with natural illumination during its original tests, but is very time consuming and generally low quality in terms of resolution.With the advent of LNAs with an improved noise ﬁgure, effort was put into an optimisation of the scanning process. The scanning time was reduced to 2.5minutes using only a single channel receiver [2]. Although the resolution of a passive sensor is far superior to that of an active sensor, It is still lackluster in regards to what is observable to the human eye.

![alt text](https://github.com/tr201/AI_Project/blob/main/GitHubImages/PassiveSensorAt94HZ.png)

(fig. 4., [2])
Shows the nature of the terrible resolution of passive sensing


Why AI detection using FLIR Imaging is better:
