# ESC Configuration
There are four on-board ESCs on the DroneCore.Power board, which can be configured through host PC(Linux / Windows) application called AMC_manager. AMC_manager are able to connect to ESC, configure parameters, identify motor, read error messages, update firmware and so on. For the purpose of switching between individual ESCs we provide configuration script, which is executed directly on jetson. Esc configuration script is a part of provided system image. 


## Connection and configuration flow
  - the use of complete DroneCore.Suite with nvidia jetson assembled is assumed.
  - connect usb cable from host PC (usb type A) to USB adapter Alink(usb micro B)
  - connect 3pin JST cable from USB adapter Alink to connector on DroneCore.Power board marked as CONFIG.
  - start AMC_manager application and open corresponding COM port (according to manual below)
  - connect usb cable from host PC to USB_DEV connector on the .Pilot board (or use WIFI and skip this step)
  - power on board (recommended to use battery or strong power supply as power source)
  - connect to nvidia jetson (ssh/serial terminal)
  - start esc_configuration skript by executing `sudo ./esc_configuration` (Location: ??)
  - follow the steps in esc_configuration script



## Configuration control script 
// manual k skriptu , priebeh konfiguracie (diagram - aepilot1 projekt wiki) 

## AMC_manager manual 
// stiahnutie appky 
//manual k appke (abldcmc projekt )

## Motor test 
// mission planner motor testing
// link na ardupilot wiki ak to maju zdokumentovane