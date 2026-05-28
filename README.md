Arduino Obstacle Avoiding Car – README
Overview

This project is an Arduino-based Obstacle Avoiding Car that uses:

Ultrasonic Sensor (HC-SR04)
Servo Motor
DC Motors with Motor Shield
Arduino UNO

The robot automatically detects obstacles and changes direction to avoid collisions.

Features
Automatic obstacle detection
Forward, backward, left, and right movement
Servo-based distance scanning
Adjustable motor speed
Smooth acceleration for battery protection
Required Components
Hardware
Arduino UNO
L293D Motor Shield
HC-SR04 Ultrasonic Sensor
Servo Motor
4 DC Motors
Robot Chassis
Battery Pack
Software Libraries

Install these Arduino libraries before uploading the code:

AFMotor Library
https://learn.adafruit.com/adafruit-motor-shield/library-install
NewPing Library
https://github.com/livetronic/Arduino-NewPing
Servo Library
https://github.com/arduino-libraries/Servo
Installing Libraries

In Arduino IDE:

Open Sketch
Select Include Library
Click Add .ZIP Library
Choose the downloaded ZIP files
Pin Configuration
Component	Arduino Pin
Ultrasonic TRIG	A0
Ultrasonic ECHO	A1
Servo Signal	10
Motor Connections
Motor	Shield Port
Front Left	M1
Front Right	M2
Rear Left	M3
Rear Right	M4
How It Works
The ultrasonic sensor continuously measures distance.
If an obstacle is detected within 15 cm:
Robot stops
Moves backward
Checks right and left directions using the servo
The robot turns toward the direction with more space.
Continues moving forward.
Important Constants
#define MAX_DISTANCE 200
#define MAX_SPEED 190
MAX_DISTANCE → Maximum sensing distance in cm
MAX_SPEED → Motor speed limit
Functions Used
Function	Purpose
moveForward()	Moves robot forward
moveBackward()	Moves robot backward
turnLeft()	Rotates robot left
turnRight()	Rotates robot right
moveStop()	Stops all motors
readPing()	Reads ultrasonic distance
lookLeft()	Scans left side
lookRight()	Scans right side
Upload Instructions
Connect Arduino to PC
Select correct Board and Port in Arduino IDE
Upload the code
Power the robot using batteries
Notes
Ensure battery voltage is sufficient for motors.
Servo default center position is 115.
Avoid setting motor speed too high for small batteries.
Possible Improvements
Add Bluetooth control
Add line-following capability
Add IR sensors
Use Li-ion battery pack
Add speed control using PWM
License

Free to use for educational and hobby projects.
