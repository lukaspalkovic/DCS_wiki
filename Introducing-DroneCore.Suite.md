## Introducing DroneCore.Suite

**DroneCore.Suite** is a one stop autopilot and flight computer solution for developers of advanced drone systems demanding high computing power and high level of modularity. It creates the "core" of the drone containing most of necessary electronics to fly a quadcopter.

It consists of a control part called **DroneCore.Pilot** and power part called **DroneCore.Power**.

**DroneCore.Pilot** is based on Cube Orange - widely used flight controller by Hex.aero running on Ardupilot (or optionally PX4 flight stack) and Nvidia Jetson Xavier NX. Their rich interfaces allow connecting of most of sensor and other peripherals for drones available on the market.

**DroneCore.Power** contains 4 FOC ESCs with motor identification feature able to be configured for all common BLDC/PMSM drone motors on the market and telemetry interface providing real time data from the flight to the flight controller. Furthermore it provides battery voltage and current measurements including separate cell voltages.

DroneCore.Suite comes with both Cube and Xavier NX preconfigured  and communicating together and able to control a quadcopter out of the box. Developers no longer need to solve basic communication and compatibility issues coming from connecting two different IT worlds. It They can start to concentrate on their application needs from the beginning. Accompanying documentation provides a fast learning curve to start using various peripherals to control the drone and create the desired application.

Various software libraries (coming soon) further enrich the possibilities for the developer relieving him from complex configuration and programming tasks.