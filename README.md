# Aire

![](./resources/3d.png)

## Description
'Aire' is a PCB designed to control a fan with three relays and automatize it with [Home Assistant](https://www.home-assistant.io/).

Firmware used in this device is [fw-aire](https://github.com/GuilleGonzzalez/fw-aire), a custom made firmware implemented using [Arduino Home Assistant](https://github.com/dawidchyrzynski/arduino-home-assistant/tree/main) Arduino library ([docs](https://dawidchyrzynski.github.io/arduino-home-assistant/)).

## Power supply
The board is powered with a 230VAC power supply.

## Microprocessor
Espressif [ESP8266](https://www.espressif.com/en/products/modules) module.

## Environmental sensing
The board has enviromental sensors to measure temperature, humidity and atmospheric pressure:

### Temperature and humidity sensor
* Sensirion [SHT40](https://sensirion.com/products/catalog/SHT40).

### Pressure sensor
* Bosch [BMP581](https://www.bosch-sensortec.com/products/environmental-sensors/pressure-sensors/bmp581/).
  
## LEDs and buttons
The device has three LEDs for showing the status to the user.
* A power LED (LED1): shows the status of the fan.
* A general device LED (LED2): shows the status of the general air machine.
* A LED reserved for the future.

The device has a button for flash the firmware in the microcontroller, and is also used for the user.

The board has an external connector available for the three LEDs and the button.

## Pin assignment

| PIN     | Func    |
| ------- | ------- |
| GPIO14  | FAN1    |
| GPIO12  | FAN2    |
| GPIO13  | FAN3    |
| I2C_EXP | LED1    |
| I2C_EXP | LED2    |
| I2C_EXP | LED3    |
| GPIO16  | BMP_INT |
| GPIO2   | BUZZ    |
| GPIO0   | BTN     |

Due there were no available GPIOS, the board has the [PCA9536D](https://www.nxp.com/docs/en/data-sheet/PCA9536.pdf) IO Expander, in which the three LEDs are connected 

| IO EXP PIN | Func      |
| ---------- | --------- |
| IO0        | LED1      |
| IO1        | LED2      |
| IO2        | LED3      |
| IO3        | TestPoint |

## Enclosure (WIP)
* Custom made in [Fusion 360](https://www.autodesk.es/products/fusion-360/overview).

# Changelog
All notable changes to this project will be documented in this section.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

## [2.0.0] - 2023-09-04
### Added
- First stable release in this repository

[Unreleased]: https://github.com/GuilleGonzzalez/hw-aire
[2.0.0]: https://github.com/GuilleGonzzalez/hw-aire/releases/tag/v2.0.0
