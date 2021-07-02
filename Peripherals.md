## Peripherals block diagram

![aepilot1_block_scheme.svg](uploads/5891a87aa9bcc1f4ddd29ee52ee2a210/aepilot1_block_scheme.svg)
[PDF FORMAT](uploads/9856a56d99b819fba1efde74f8734ce4/aepilot1_block_schematic.pdf)

## Nvidia Jetson peripherals
- **PINMUX**
  - Jetson Nano pinmux spreadsheet, customized for aepilot1 : !TODO! upload spreadsheets
  - Jetson Xavier NX pinmux spreadsheet, customized for aepilot1 : 

&nbsp;

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

   `User controllable GPIOs with their kernel mapping numbers (NANO):`

| HW number | Kernel mapping number | usage|
| :--- | :---: | :--- |
| Gpio4 | 65 | 5V_AP_SWITCH |
| Gpio6 | 64 | USB MUX SELECT |
| Gpio11 | 200 | CAM_MCLK3 |
| Gpio12 | 194 | Free gpio | 
| Gpio13 | 38 | Free gpio |
| GPIO_EXP1 | ? | Free gpio |
| GPIO_EXP2 | ? | Free gpio |

   `User controllable GPIOs with their kernel mapping numbers (Xavier NX):`

| HW number | Kernel mapping number | usage|
| :--- | :---: | :--- |
| Gpio4 | !TODO! | 5V_AP_SWITCH |
| Gpio6 | ? | USB MUX SELECT |
| Gpio11 | ? | CAM_MCLK3 |
| Gpio12 | ? | Free gpio | 
| Gpio13 | ? | Free gpio |
| GPIO_EXP1 | ? | Free gpio |
| GPIO_EXP2 | ? | Free gpio |

- **Serial ports**
   - jetson nano (rev. 3+):
      - ttyTHS1 = uart to autopilot
      - ttyTHS2  = uart to 'GPS_Jetson' connector
      - ttyS0  = uart to GPIO pin header

    - xavier nx (rev. 3+):
      - ttyTHS0 = uart to autopilot
      - ttyTHS1 = uart to 'GPS_Jetson' connector
      - ttyTCU0 = debug uart (GPIO pin header)
&nbsp;

   `Example program:` //link to git 

&nbsp;

- **SPI ports**
  - jetson nano
    - spidev0.0 = SPI0 (Jetson) connector 
    - spidev0.1 = SPI0 (Jetson) connector
    - spidev1.0 = accelerometer
    - spidev1.1 = gyroscope
    - spidev1.2 = barometer
  - xavier nx
    - spidev0.0 = SPI0 (Jetson) connector
    - spidev0.1 = SPI0 (Jetson) connector
    - spidev2.0 = accelerometer
    - spidev2.1 = gyroscope
    - spidev2.2 = barometer

&nbsp;

    `Example program:` //link to git 

&nbsp;

- **I2C**
  - common
    - i2c-30 = CSIA connector
    - i2c-32 = CSIB connector
    - i2c-31 = CSIC connector
    - i2c-33 = CSID connector
    - i2c-35 = CSIE connector
    - i2c-34 = CSIF connector

  - jetson nano
    - i2c-? = B2B connector (power board)
    - i2c-? = GPS(Jetson) connector
    - i2c-? = M2 key E connector

  - jetson xavier nx
    - i2c-? = B2B connector (power board)
    - i2c-? = GPS(Jetson) connector
    - i2c-? = M2 key E connector
  
&nbsp;
  
    `Example program:`


## The Cube peripherals

## Interconnection Jetson <--> Cube 