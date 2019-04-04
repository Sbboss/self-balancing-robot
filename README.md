# self-balancing-robot
It is a bot having 2 wheels. Also provided code that balances it and also balances payload depends upon the structure and material you used to build it. I suggest you make a Prototype Model first so you are able to get that how this little dude works(The bot). My Model is approx. 10 inches in height & 3 inches in breadth & 5 inches in length.

The Bot consists of the following things:-

1. Arduino UNO:- It is basically a micro-controller which takes 5V as input and is used to control many things like LEDs, Time Buzzer and many more things based on the set of codes uploaded to it. To upload code in Arduino you must have to use Arduino IDE, to write codes for Arduino generally in C/C++ (Arduino).
Note: On our project, we used it to control 2 things : 
2. The MPU6050+accelerometer:- It is a 3-axis gyroscope and accelerometer too. https://www.robomart.com/gy-521-mpu-6050-module-3-axis-analog-gyro-sensors-3-axis-accelerometer-module
3. H-Bridge L298D: Used to control the wheel of the bot. It takes at least 9V to move the wheels and at max 12V. **We give the power supply to the L298D by an external source like an adapter of 9V**.https://www.robomart.com/l298-stepper-motor-driver-board-for-arduino-avr-smart-car-robot?search=l298d&dsearch=l298d

We already set the reading of MPU6050 gyroscope in the code, the reading is present in the code. These readings are captured by using another code that used to get the reading of gyroscope on your screen of all 3-axis (Code is provided). the values change as altitude changes so you can get your own values by this code provided.
# Princple:-
  It works on the principle of counter balance means it balances by counter its weight.
# Working:-
  The 2 wheels setted on the robot always moves opposite direction to the direction in which the robot is leaning. Suppose if the body is leaning the right then the wheels moves to left and counter the weight to balance it.When the readings setted on MPU6050 changes then it gives a false signal to Arduino which means the body to leaning a particular position either right or left. To get the correct leaning posture the values of MPU6050 helps the Arduino to compare whether the body is leaning right or left. After getting the correct leaning direction. Arduino give order to L298D to move the wheels in which direction.

The question arises that How to set the speed of wheel to stop when they balance it perfectly?

The answer is very interesting it based on 3 values called PID values. These values are setted according to your Model height, weight, length and many more factor. Also this is the toughest part to do as these values are not easily fit to your robot. We(My team) also took around 1 week to make the whole project and 4 days to find the correct the PID values.It stands for: **P-Proportional, I-Integral ,D-Derivative**.

The PID particularly for L298D which tells that what is the speed and direction of wheels.

**I provided code as .cpp
  and .ino for Arduino IDE too.**
  
  
 
 Thankyou Keep Supporting me if this helped you than please leave a comment and also if you have any problem also leave a comment i definitely help you :)  
