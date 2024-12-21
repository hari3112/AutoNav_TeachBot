# AutoNav_TeachNot
This project contributed to the TeachingAssistantBot by designing and implementing its autonomous navigation system. This involved setting up the mobile base and integrating it with algorithms that enable the bot to autonomously navigate to specified goals. The project focus was on ensuring the robot could move efficiently and accurately within its environment, laying the foundation for future enhancements such as NLP and speech recognition integration.
This robot is a 2 wheel differential drive mobile robot which has been developed by following linorobot setup using Arduino-Mega 2560 in ROS-Noetic.
Refer the linorobot from the link https://linorobot.org/


# Hardware Used
Arduino Mega 2560

Raspberry pi 4 Model B

MPU 6050

RPlidar A1M8

L298D motor driver

N20 12V motor with Encoder.




Edit the motor configuration in the firmware

# Motor configuration

//define your robot' specs here

#define MAX_RPM 330               // motor's maximum RPM

#define COUNTS_PER_REV 1550       // wheel encoder's no of ticks per rev

#define WHEEL_DIAMETER 0.10       // wheel's diameter in meters

#define PWM_BITS 8                // PWM Resolution of the microcontroller

#define LR_WHEELS_DISTANCE 0.235  // distance between left and right wheels

#define FR_WHEELS_DISTANCE 0.30   // distance between front and rear wheels

#define MAX_STEERING_ANGLE 0.415  // max steering angle. This only applies to Ackermann steering

# Uploading the codes

cd ~/linorobot_ws/src/linorobot/teensy/firmware

platformio run --target upload


# Launch base driver

roslaunch linorobot bringup.launch

# Launch mapping packages

roslaunch linorobot slam.launch

Save the map in the maps folder inside linorobot folder

# Launch navigation packages

roslaunch linorobot navigate.launch




