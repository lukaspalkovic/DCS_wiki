**Peripherals block diagram** 

![aepilot1_block_scheme.svg](uploads/5891a87aa9bcc1f4ddd29ee52ee2a210/aepilot1_block_scheme.svg)

**Nvidia Jetson peripherals** 
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

   `EXAMPLE: Set value on gpio64 to gnd`
```
cat /sys/kernel/debug/gpio

root@ubuntu:/home/aepilot1# echo 64 > /sys/class/gpio/export
root@ubuntu:/home/aepilot1# echo out > /sys/class/gpio/gpio64/direction
root@ubuntu:/home/aepilot1# echo 0 > /sys/class/gpio/gpio64/value
root@ubuntu:/home/aepilot1# echo 1 > /sys/class/gpio/gpio64/value
```
&nbsp;



**The Cube peripherals**

**Interconnection Jetson <--> Cube** 