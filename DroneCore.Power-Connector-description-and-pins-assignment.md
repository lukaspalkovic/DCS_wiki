## Board to board top connector
![b2b_connecto_powerb](uploads/1d3214b69ac5ceef298804148f1d1814/b2b_connecto_powerb.png)

## Top side connectors 

//ADD photo of new revision with connectors pin1 direction mark (changes in config connector 2pin->3pin)

**CONFIG**
| pin | function |
| ------ | ------ |
| 1 | GND |
| 2 | NC |
| 3 | COM |


**EXT. BUTTON**
| pin | function |
| ------ | ------ |
| 1 | 3V3 |
| 2 | BUTTON |
| 3 | GND |

**EXT. CAN**
| pin | function |
| ------ | ------ |
| 1 | GND |
| 2 | CAN N |
| 3 | CAN_P |
| 4 | 5V |

**LED FRONT L, LED FRONT R, LED BACK L, LED BACK R, LED ADD**
- sum of current of all led channels on 5V line is limited to 2.5A

| pin | function |
| ------ | ------ |
| 1 | 5V |
| 2 | PWM |
| 3 | GND |

## Bottom side connectors

//ADD photo of new revision (changed logo and regulator unassembled)

**BAT CELLS**
| pin | function |
| ------ | ------ |
| 1 | CELL6 |
| 2 | CELL5 |
| 3 | CELL4 |
| 4 | CELL3 |
| 5 | CELL2 |
| 6 | CELL1 |

**BMS I2C**
| pin | function |
| ------ | ------ |
| 1 | GND |
| 2 | I2C_SDA |
| 3 | I2C_SCL |
| 4 | 3V3 |