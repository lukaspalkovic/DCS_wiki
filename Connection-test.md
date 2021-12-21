There are three ways how to connect to Nvidia Jetson from host computer: micro-usb cable connection through SSH, micro-usb cable connection through serial terminal (putty), wireless connection through SSH.





.

.

.

### Some useful hints:

**Changing ubuntu hostname:**
  - execute following commands in terminal

`hostnamectl set-hostname desired_hostname`    
`sudo reboot`

**Changing ubuntu user-name:**
 - execute following commands in terminal

`sudo usermod -l desired_username current_username`  
`sudo usermod -d /home/desired_username -m desired_username`  
`sudo groupmod -n desired_username current_username`

**Changing ubuntu user-password:**
 - execute following commands in terminal  

For user password:  
`passwd`

For root password:  
`sudo passwd`

**Changing WIFI SID:**
 - execute following commands in terminal
...
