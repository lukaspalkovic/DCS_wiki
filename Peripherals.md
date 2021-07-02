**Peripherals block diagram** 

![aepilot1_block_scheme.svg](uploads/5891a87aa9bcc1f4ddd29ee52ee2a210/aepilot1_block_scheme.svg)

##**Nvidia Jetson peripherals** 
   - **GPIOs**

   `Setup rules:` 
```
   $ sudo groupadd -f -r gpio
   $ sudo usermod -a -G gpio your_user_name
```
Install custom udev rules by copying the 99-gpio.rules file into the rules.d directory:
```
$ sudo cp /opt/nvidia/jetson-gpio/etc/99-gpio.rules /etc/udev/rules.d/
```
You may either need to reboot or reload the udev rules :
```
sudo udevadm control --reload-rules && sudo udevadm trigger
```

   `EXAMPLE: Set gpio64 logic level to LOW and then to HIGH`
```
cat /sys/kernel/debug/gpio

root@ubuntu:/home/user_name# echo 64 > /sys/class/gpio/export
root@ubuntu:/home/user_name# echo out > /sys/class/gpio/gpio64/direction
root@ubuntu:/home/user_name# echo 0 > /sys/class/gpio/gpio64/value
root@ubuntu:/home/user_name# echo 1 > /sys/class/gpio/gpio64/value
```
&nbsp;

   `User controllable GPIOs with their kernel mapping numbers (NANO): `

| HW number | Kernel mapping number | usage|
| :--- | :---: | :--- |
| Gpio4 | 65 | 5V_AP_SWITCH |
| Gpio6 | 64 | USB MUX SELECT |
| Gpio11 | 200 | CAM_MCLK3 |
| Gpio12 | 194 | Free gpio | 
| Gpio13 | 38 | Free gpio |

   `User controllable GPIOs with their kernel mapping numbers (NX) !TODO! : `

| HW number | Kernel mapping number | usage|
| :--- | :---: | :--- |
| Gpio4 | ? | 5V_AP_SWITCH |
| Gpio6 | ? | USB MUX SELECT |
| Gpio11 | ? | CAM_MCLK3 |
| Gpio12 | ? | Free gpio | 
| Gpio13 | ? | Free gpio |

**The Cube peripherals**

**Interconnection Jetson <--> Cube** 