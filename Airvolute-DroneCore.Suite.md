### Autonomous AI drone solution for developers

One-stop solution for drone developers combining the best features of Nvidia Jetson NX and The Cube autopilot with the AI ready autonomous software stack, rich connectivity and various payload support. Designing and developing of enterprise-grade autonomous drones has never been easier. It is time to focus on your drone based applications!

DroneCore.Suite consists of two main blocks

* DroneCore.Pilot - top board for control of the aircraft containing
  * Jetson Xavier NX
  * Cube flight controller
  * Internal 5V power supply
  * Power selector
  * Peripheral connectors
  * USB hub
* DroneCore.Power - bottom board with power electronic containing
  * 

<div>

**Mechanical parameters**

* Weight 247g - including Cube orange, Xavier NX, Xavier heatsink with fan
* Dimensions 115 x 80 x 45mm
* Mount with 4 screws/spacers M3 109 x 74mm
* WiFi module
* WiFi antennas 2pcs

**Electrical parameters**

* Power supply range: 12V – 35V (6S LiHV)
* Integrated DC/DC converter for control circuits
* Redundant power supply with power good monitoring for control unit
* Current protected peripheral connectors
* 4 x FOC UAVCAN ESC 40A, featuring motor identification and motor diagnostics
* Power sensor, SMBUS

**<span dir="">Ardupilot (Cube) Connections</span>**

* <span dir="">PPM input</span>
* <span dir="">PWM output (7 + 7 lines)</span>
* <span dir="">2x CAN</span>
* <span dir="">4x UART</span>
* <span dir="">2x I2C</span>
* <span dir="">Buzzer</span>
* <span dir="">Power sensor input</span>
* <span dir="">ADC input</span>
* Buzzer

**Jetson connections:**

* PCI Express (M2, Key E connector)
* 4 USB 3.0 (ZIF connectors, reductions available)
* Gigabit Ethernet (ZIF connector, reductions available)
* 6 CSI (22 pin)
* 4 GPIO
* UAV CAN, UART, I2C, SPI
* IMU BMI088 and barometer BMP388 on board
* USB 2.0 for debugging
* Micro SD card
* Video output connector (micro HDMI)
* Fan

<div>

**DroneCore.Power** <span dir="">(bottom power board)</span>

* <span dir="">4 x FOC UAVCAN ESCs – 40A peak / </span>20A permanent
* <span dir="">power sensor</span>, SMBUS<span dir="">,</span>
* <span dir="">LED Driver for 4x WS2812B strips</span>

</div>![aepilot1_block_diagram.svg](uploads/1ec747cd8155ff306736bedccf6e980f/aepilot1_block_diagram.svg)

</div>