# ESC Configuration
There are four on-board ESCs on the DroneCore.Power board, which can be configured through host PC(Linux / Windows) application called AMC_manager. AMC_manager are able to connect to ESC, configure parameters, identify motor, read error messages, update firmware and so on. For the purpose of switching between individual ESCs we provide configuration application, which is executed directly on jetson. Esc configuration app is a part of provided system image. 


## Connection and configuration flow
  - the use of complete DroneCore.Suite with nvidia jetson assembled is assumed.
  - connect usb cable from host PC (usb type A) to USB adapter Alink(usb micro B)
  - connect 3pin JST cable from USB adapter Alink to connector on DroneCore.Power board marked as CONFIG.
  - start AMC_manager application and open corresponding COM port (according to manual below)
  - connect usb cable from host PC to USB_DEV connector on the .Pilot board (or use WIFI and skip this step)
  - power on board (recommended to use battery or strong power supply as power source)
  - connect to nvidia jetson (ssh/serial terminal)
  - start esc_configuration app
  - follow the steps in esc_configuration app



## Configuration control script 
  - esc_configuration is simple console application which communicates with .Power board through I2C peripheral.
  - location of the script:  ???(location in system image) 
  - run script by `./esc_configuration`
<img src="uploads/cbd4191ab04b33b81c80ad062ba6d910/esc_config_app.png"  width="750"> 

  - pressing 'ENTER' will lead you through the whole configuration flow

 &nbsp;

**esc_configuration application flow:** 
```mermaid
graph TD
    A(Program state run) -->|start esc_configuration app| B(All OFF)
    B -->|'ENTER'| C(ESC0_active)
    B -->|'q'| A
    C -->|'ENTER'| D(All OFF)
    C -->|'q'| A
    D -->|'ENTER'| E(ESC1_active)
    D -->|'q'| A
    E -->|'ENTER'| F(All OFF)
    E -->|'q'| A
    F -->|'ENTER'| G(ESC2_active)
    F -->|'q'| A
    G -->|'ENTER'| H(All OFF)
    G -->|'q'| A
    H -->|'ENTER'| I(ESC3_active)
    H -->|'q'| A
    I -->|'ENTER' / 'q'| A 
```


## AMC_manager manual 
// stiahnutie appky 
//manual k appke (abldcmc projekt )

## Motor test 
// mission planner motor testing
// link na ardupilot wiki ak to maju zdokumentovane