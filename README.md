# About The Project 
For my sophomore grade level project (wearable device challenge) I created a device using a smoke and heart sensor to detect hazardous air quality outdoors or to simply help someone stop smoking. The device is made with Arduino and coded with C++.

## What The Device Does
Our device uses two sensors, a heart pulse monitor, as well as an air quality / smoke sensor to collect data about the surrounding area the device user is in as well as the users heart rate. If the air quality sensor measures at a concentration of 1150+ parts per million (ppm), the first red LED will flash, signaling a harmful air quality. As for the heart rate monitor, if the user registers a heart rate of anywhere to 120 and above beats per minute (BPM), the second red LED will flash, signaling an abnormally high heart rate. 

## Device

![](devicePic.png)

## Repository Contents
* The file [main.ino](https://github.com/aahmad4/Arduino-Smoke-Danger-Device/blob/master/main.ino) is the program, written in C++, which handles the logic with the arduino board, both sensors, and the 4 LED lights I used. 
* The file [smokeDangerPoster.pdf](https://github.com/aahmad4/Arduino-Smoke-Danger-Device/blob/master/smokeDangerPoster.pdf) is the poster I created to go along with this project. The poster includes the data I collected through the C++ program and graphs to go with it. I collected individual data for each sensor to help with stable values I could later use to code my LED lights. The poster also includes several pictures of the development process of the device and descriptions of all the different attributes. The final prototype can be seen at the bottom of the poster. 

## Clone
```bash
git clone https://github.com/aahmad4/Arduino-Smoke-Danger-Device
```

## Implementation

Keep in mind that the certain values PPM (Parts Per Million) and BPM (Beats Per Minute) are within retrospect of the data that the sensors collected, they are subject to change depending on the quality and lifespan of the sensor.

Knowing this, depending on the quality of your Heart Rate Sensor, I would change the BPM value here to match the data.
```c++
 if (BPM > 120)
   {
    digitalWrite(10, LOW);
    digitalWrite(8, HIGH); 
   }
   else
   {
    digitalWrite(8, LOW);
    digitalWrite(10, HIGH); 
   }
```
Likewise, I would change the PPM value here, once again depending on the quality of your Gas Sensor.
```c++
void loop()
{
   gasValue = analogRead(gasPin);
  Serial.println(gasValue);
   if (gasValue < 500)
   {
    digitalWrite(4, HIGH); 
    digitalWrite(2, LOW); 
   }
   else 
   {
    digitalWrite(2, HIGH);
    digitalWrite(4, LOW);
   }
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

