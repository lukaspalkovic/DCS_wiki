# Connection to Nvidia Jetson

There are three ways how to connect to Nvidia Jetson from host computer: micro-usb cable connection through SSH, micro-usb cable connection through serial terminal (putty), wireless connection through SSH.

## Micro-usb connection through SSH
  - connect usb cable from host computer to micro-usb port on DroneCore.Pilot marked as USB_DEV. 
  - power on board and wait till jetson boots
  - open terminal on Linux host computer 
  - type `ssh DCS_user@192.168.55.1`  (DCS_user is default username)
<img src="uploads/eb7acc496b64095a67dc39314b6d13c5/ssh_login11.png"  width="750">  

  - enter password (default password = dronecore)
<img src="uploads/955bef4efbb5c315fc2b5219becb61c4/ssh_login22.png"  width="750">  

  - you are in

&nbsp;

## WIFI connection through SSH
  - WIFI card with antennas must be assembled on the board. (M2 WIFI cards verified: Intel AC-9260NGW, Intel AC-8265NGW)
  - power on board and wait till jetson boots
  - jetson automatically creates WIFI hotspot with SSID: DSC_wifi, PASSWORD: dronecore
  - find this WIFI network and connect to it from Linux host PC
<img src="uploads/52cc71e9190475f28771bdd5e0324d9b/wifi1.png"  width="750">  

  - open terminal on host PC and type `ssh DCS_user@10.42.0.1` (DCS_user is default username)  
  - enter password (default password = dronecore)
<img src="uploads/8a592c0297ebc1c782a4185d820ba9dd/wifi_login1.png"  width="750">  

- you are in


&nbsp;

## Micro-usb connection through serial console
  - connect usb cable from host computer to micro-usb port on DroneCore.Pilot marked as USB_DEV. 
  - power on board and wait till jetson boots
  - open serial terminal program (putty, teraterm, gtkterm etc.) on Linux or Windows host PC
  - open corresponding port (jetson is commonly identified as ttyACM0 on Ubuntu host PC)
<img src="uploads/edc0350a560e80ebbc4ef88b28b4ffe9/putty.png"  width="750">
  
  - enter user name of user (DCS_user is default username)
  - enter password (default password = dronecore)
<img src="uploads/3f25c164a0b12c55afae16040ec46048/putty2.png"  width="750"> 

  - you are in


&nbsp;


## Some useful hints:

- **Changing ubuntu hostname:**
  - execute following commands in terminal

  - `hostnamectl set-hostname desired_hostname`    
  - `sudo reboot`

- **Changing ubuntu user-name:**
  - execute following commands in terminal

  - `sudo usermod -l desired_username current_username`  
  - `sudo usermod -d /home/desired_username -m desired_username`  
  - `sudo groupmod -n desired_username current_username`

- **Changing ubuntu user-password:**
  - execute following commands in terminal  

  - For user password: `passwd`

  - For root password: `sudo passwd`

- **Changing WIFI SID/PASSWORD:**
  - execute following commands in terminal
//add how to change automatic wifi hotspot sid/pass
