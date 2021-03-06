# SRF_Library
This is Arduino library for Ultrasonic Distance Sensor
---
### Ultrasonic Distance Sensor
The ultrasonic sensor measures the distance of the nearest object, sending the result to the serial port. It can work from 2 cm to 3 m. It measures the time spent by the signal to reach the object and return to the sensor.
##### SRF05 
The latest model SRF05 Detection range of 3 cm from the original SRF04 to 3 m, increased to 1 cm to 4 meters. SRF04 is compatible with the original. Also has smaller side lobes. 

Ultrasonic module can be used to identify obstructions, 1 cm to 4 meters. Can be easily connected to the micro-controller, such as BASICX. 

The ultrasound module will be applied to the robot module. With this module, available in the sonar obstacle within the exact distance. Your robot will be able to bat-like sonar to detect by the surroundings, only a small piece of code, you can obstacles to accurate distance control your motor running, so that your robot can easily of avoiding obstacles. 

![capture](https://s20.picofile.com/file/8442371418/1.jpg)
---
### How to connect Srf05 to Arduino Uno board

![capture](https://s18.picofile.com/file/8440096050/2.png)
---
### Sample code 

```c:
### include the SRF_LIB library
#include "SRF_LIB"

### create SRF object with trig and echo pins
#define trig 13
#define echo 12
SRF srf(trig, echo);

void setup() {
  ### create variables to store distance
  int distance_cm = 0;
  int distance_mm = 0;
}

void loop() {
  ### measure the distance in cm and mm
  distance_cm = srf.dist_cm();
  distance_mm = srf.dist_mm();
  ### print distance on serial monitor with 9600 baud rate
  Print_dist_cm(9600);
  Print_dist_mm(9600);
  delay(50);
}
```
---
### License Information
This product is open source!

So, Feel free to download, use or make any changes you like to this file
Also, you can contact me with email, instagram and telegram to talk about it.
+ Email: Saeedtajikhk@gmail.com
+ Instagram: saeedthk
+ Telegram: SaeedThk

Your friend Saeed Tajik Hesarkuchak.

