## Autonomous AI drone solution for developers

### Introduction

One-stop solution for drone developers combining the best features of Nvidia Jetson NX and The Cube autopilot with the AI ready autonomous software stack, rich connectivity and various payload support. Designing and developing of enterprise-grade autonomous drones has never been easier. It is time to focus on your drone based applications!

**DroneCore.Suite** consists of these main blocks

* **DroneCore.Pilot** - top board for control of the aircraft containing
* **DroneCore.Power** - bottom board with power electronic containing

DroneCore.Suite provides easy to use ROS based software stack supporting development of autonomous applications.

### First time setup

* **First connect your peripherals** 

  The connector description can be found at
  * DroneCore.Pilot connectors and pinouts 
  * DroneCore.Power connectors and pinout
* **Motor connection** - ESCs onboard DroneCore.Power support BLDC motors. However, since they use field oriented control (FOC), the ESC must know the motor. Next section deals with the motor identification and proper ESC settings.
  * ESC configuration and motor test

Motor connection 