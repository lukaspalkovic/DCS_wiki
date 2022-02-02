# Connection to flight controller

Follow these instructions to connect to flight controller from [Mission Planner](https://ardupilot.org/planner/docs/mission-planner-installation.html) or [QGroundControl](https://docs.qgroundcontrol.com/master/en/getting_started/download_and_install.html)  from host PC. There are three preffered ways how to connect to flight controller: 
  - UDP ( WIFI connection)
  - UDP ( through micro-USB cable plugged in USB_DEV connector on the DroneCore.Pilot board )  
  - USB ( directly connected from host PC to flight controller ) 
 
### UDP(through USB) connection
  - connect usb cable from host PC to micro-USB connector on DroneCore.Pilot board marked as USB_DEV
  - power-on DroneCore.Pilot board
  - connect to jetson through ssh [LINK NA CONNECTION TEST SEKCIU](blabla)
  - open /etc/profile configuration file ```sudo nano /etc/profile```
  - find and set MAVROS_GCS_URL as ```export MAVROS_GCS_URL="udp-b://192.168.55.1@"```
  - execute command to run mavros: ```roscd mavros && roslaunch mavros apm.launch```
  - run QGroundControl or Mission planner on host PC and it should automatically connect
  - NOTE: if there is some issues with connecting from Windows host, there is likely problem with firewall or antivirus software

### UDP(through WIFI) connection
  - assumed DroneCore.Pilot assembled with WIFI card and connected to same network as host PC
  - assumed known IP address of jetson in network ( to find IP address execute ```ifconfig``` on jetson and check IP of wlan0 connection )
  - connect to jetson through ssh [LINK NA CONNECTION TEST SEKCIU](blabla)
  - open /etc/profile configuration file ```sudo nano /etc/profile```
  - exchange IP address of MAVROS_GCS_URL to the wlan0 one 
  - execute command to run mavros: ```roscd mavros && roslaunch mavros apm.launch```
  - run QGroundControl or Mission planner on host PC and it should automatically connect
  - NOTE: if jetson is set up as WIFI access-point, IP address is standardly _10.42.0.1_
  - NOTE: if there is some issues with connecting from Windows host, there is likely problem with firewall or antivirus software

### USB connection
  - connect USB cable from host PC directly to flight controller
  - open QGroundControl or Mission planner and connect to corresponding COM port




# Flight controller configuration

In order to perform the first flights, the flight controller must be configured for the vehicle. Typically one should follow the instructions for his type of vehicle and used firmware. In case of default DroneCore.Suite, the flight controller is Cube orange with Arducopter 4.1. configured for use on Quadcopter Discovery UAV by Airvolute and this manual is optimized for the aforementioned configuration.

Basically, user ought to follow the instructions flight controller firmware manual. However, there are some specific settings needed to run DroneCore.Suite correctly.

If you use a different vehicle type or autpilot, please check also the section Specifics.

### Default settings

The Cube Orange supplies with DroneCore.Suite is already loaded with firmware and settings. If in any case the default configuration has to be restored it is recommended to follow the firmware update manual and load the settings from this **settings file**(TODO) according to Load presaved part of the [**Mission Planner CONFiguration and Tuning**](https://ardupilot.org/planner/docs/mission-planner-configuration-and-tuning.html).

### Ardupilot configuration (based on Ardupilot documentation)

* Use GCS software to connect to ardupilot via [USB, UART or UDP connection](https://ardupilot.org/copter/docs/common-connect-mission-planner-autopilot.html)
* [Get familiar with your peripherals and input and output systems](https://ardupilot.org/copter/docs/common-basic-operation.html)
* Ensure your are using the correct ESC configuration for your motor if FOC ESCs are used (TODO link)
* Set up your vehicle [frame type](https://ardupilot.org/copter/docs/frame-type-configuration.html)
* Assign the [motors to the outputs](https://ardupilot.org/copter/docs/frame-type-configuration.html).
* If using CAN ESCs configure the CAN communication accordingly (TODO Jaro comment)
* Test your motor settings.
* If you are using also radio control, [configure and calibrate it](https://ardupilot.org/copter/docs/common-radio-control-calibration.html).
* [Calibrate accelerometer.](https://ardupilot.org/copter/docs/common-accelerometer-calibration.html)
* [Calibrate the compass.](https://ardupilot.org/copter/docs/common-compass-calibration-in-mission-planner.html#common-compass-calibration-in-mission-planner)
* If using GPS, [mount and configure the GPS module](https://ardupilot.org/copter/docs/common-installing-3dr-ublox-gps-compass-module.html).
* [Set transmitter modes. ](https://ardupilot.org/copter/docs/common-rc-transmitter-flight-mode-configuration.html)These will serve for manual control of the drone. The flight mode can be changed externally via MAVLINK, which is also a case in autonomous control from flight computer Xavier NX (TODO check wording consistency).
* Based on ESC you are using consider [calibrating also your ESCs](https://ardupilot.org/copter/docs/esc-calibration.html). This is not needed in case of DroneCore.Power which has a separate section (TODO)
* Activate failsafe mechanism according to your needs. We recommend at least these options: battery, radio (if using R/C control), EKF, vibration, crash
* Follow the [first flight instructions](https://ardupilot.org/copter/docs/common-tuning.html) to make your first flight, tune PID settings and related 

### Specifics

#### COM settings 

* Serial 2 protocol is reserved for Flight computer(TODO naming convention) and must be set to _Mavlink 2_
* Board to board interconnection between The Cube (TODO naming) on DroneCore.Pilot and DroneCore.Power is using CAN1 interface
* 

(TODO height measurement)