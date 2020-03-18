# About The Project
For my sophomore grade level project (wearable device challenge) I created a device using a smoke and heart sensor to detect hazardous air quality outdoors or to simply help someone stop smoking. 

# Repository Contents
- The file main.ino is the program, written in C++, which handles the logic with the arduino board, both sensors, and the 4 LED lights I used. 
- The file smokeDangerPoster.pdf is the poster I created to go along with this project. The poster includes the data I collected through the C++ program and graphs to go with it. I collected individual data for each sensor to help with stable values I could later use to code my LED lights. The poster also includes several pictures of the development process of the device and descriptions of all the different attributes. The final prototype can be seen at the bottom of the poster. 

# What The Device Does
Our device uses two sensors, a heart pulse monitor, as well as an air quality / smoke sensor to collect data about the surrounding area the device user is in as well as the users heart rate. If the air quality sensor measures at a concentration of 1150+ parts per million (ppm), the first red LED will flash, signaling a harmful air quality. As for the heart rate monitor, if the user registers a heart rate of anywhere to 120 and above beats per minute (BPM), the second red LED will flash, signaling an abnormally high heart rate. 

![](devicePic.png)

`Note: Keep in mind that certain values (ppm & BPM) are within retrospect of the data that the sensors collected, they are subject to change depending on the quality and lifespan of the sensor`
