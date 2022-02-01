## Autonomous AI drone solution for developers

### Introduction

One-stop solution for drone developers combining the best features of Nvidia Jetson NX and The Cube autopilot with the AI ready autonomous software stack, rich connectivity and various payload support. Designing and developing of enterprise-grade autonomous drones has never been easier. It is time to focus on your drone based applications!

**DroneCore.Suite** consists of these main blocks

* **DroneCore.Pilot** - top board for control of the aircraft containing
* **DroneCore.Power** - bottom board with power electronic containing

DroneCore.Suite provides easy to use ROS based software stack supporting development of autonomous applications.

### First time setup

* **Assembly**

  If DroneCore.Power is used, connect external power supply to DroneCore.Power. Connect DroneCore.Pilot to DroneCore.Power using the 80pin board to board connector.

  If only DronCore.Pilot is used connect power supply directly to it. \
  **WARNING** - take special care about the power supply polarity. Reverse connection may lead to a permanent damage of both modules and the loss of warranty!
* **Power on** - Power on external power supply. If DroneCore.Power is used press power switch for several seconds. Power supply automatically switches and the whole board is powered. It is indicated by light underneath the Cube fligth controller.
* **Connection test** - 
* **Cube configuration -** in order to use DroneCore.Suite properly for flight, Cube flight controller must be correctly set and calibrated. This steps is to be performed when the DroneCore.Suite is already mounted within the drone frame in final position. 
* **Install script tutorial** - Jetson Xavier NX module is already preconfigured in a basic way supporting predefined peripheral drivers. If some other drivers are needed the module needs to be installed with corresponding drivers. In such case follow these steps.
* **Motor connection** - The step is required if DroneCore.Power module is used. ESCs onboard DroneCore.Power support BLDC motors. However, since they use field oriented control (FOC), the ESC must know the motor. Next section deals with the motor identification and proper ESC settings. Please follow the steps carefully to ensure the proper function of the whole propulsion system.
  * **Solder motor cables** - take special care to solder the motor cables corretly to the DroneCore.Power system. 
  * **ESC configuration and motor test -** follow the provided instructions
* **First connect your peripherals**

  The connector description can be found at.
  * DroneCore.Pilot connectors and pinouts
  * DroneCore.Power connectors and pinout