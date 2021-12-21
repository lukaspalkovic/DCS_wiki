# ESC Configuration
There are four on-board ESCs on the DroneCore.Power board, which can be configured through host PC(Linux / Windows) application called AMC_manager. AMC_manager are able to connect to ESC, configure parameters, identify motor, read error messages, update firmware and so on. For the purpose of switching between individual ESCs we provide configuration script, which is executed directly on jetson. Esc configuration script is a part of provided system image. 

## Connection and setup
  - the use of complete DroneCore.Suite with nvidia jetson assembled is assumed.
  - connect usb cable from host PC (usb type A) to usb/serial converter(usb micro B)
  - connect 3pin JST cable from usb/serial converter to connector on DroneCore.Power board marked as CONFIG.
  - open AMC_manager application and open corresponding COM port (according to manual below)
  - start

## Configuration control script and configuration flow
// manual k skriptu , priebeh konfiguracie (diagram - aepilot1 projekt wiki) 

## AMC_manager manual 
// stiahnutie appky 
//manual k appke (abldcmc projekt )

## Motor test 
// mission planner motor testing
// link na ardupilot wiki ak to maju zdokumentovane