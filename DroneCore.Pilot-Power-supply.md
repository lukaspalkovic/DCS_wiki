**Power supply diagram**

![aepilot1_power_supply_diagram.svg](uploads/fd7d7291101b34e284d886675b0bf097/aepilot1_power_supply_diagram.svg)

[PDF FORMAT](uploads/3475e310a2746c29dc62faa2b54d5e2e/aepilot1_power_supply_diagram.pdf)

&nbsp;

**DroneCore.Pilot power consumption**

Default system configuration consists of DroneCore.Pilot board connected with the Cube Orange and NVIDIA® Jetson Xavier™ NX Module. Power consumption of the whole system depends on usage of Jetson Xavier™ NX computing power and peripheral devices connected to board. 
This paragraph assumes that NVIDIA® Jetson Xavier™ NX is in 20W power mode and no other peripheral is connected to board, except one imx477 CSI camera. Video stream processing is the situation where the 20W power mode starts to play a role. We describe some default situations for reference.
 
  - **Situation 1:**

    - NVIDIA® Jetson Xavier™ NX: booted, with no user code running

    - Cube Orange: 

&nbsp;


**5V DC/DC specification**
  - output voltage 