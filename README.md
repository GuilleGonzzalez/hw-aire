# Aire

![](./resources/3d.png)

## Description

'Aire' is a PCB designed to control a fan with three relays and automatize it with [Home Assistant](https://www.home-assistant.io/).

Firmware used in this device is [fw-aire](https://github.com/GuilleGonzzalez/fw-aire), a custom made firmware implemented using [Arduino Home Assistant](https://github.com/dawidchyrzynski/arduino-home-assistant/tree/main) Arduino library ([docs](https://dawidchyrzynski.github.io/arduino-home-assistant/)).

## Power supply

The board is powered with a 230VAC power supply.

## Microprocessor

Espressif [ESP32-S2-SOLO](https://www.espressif.com/en/products/modules) module (NRND).

## Environmental sensing

The board has enviromental sensors to measure temperature, humidity and atmospheric pressure:

### Temperature and humidity sensor

* Sensirion [SHT40](https://sensirion.com/products/catalog/SHT40).

### Pressure sensor

* Bosch [BMP581](https://www.bosch-sensortec.com/products/environmental-sensors/pressure-sensors/bmp581/).

## LEDs and buttons

//TODO: review

The device has three LEDs for showing the status to the user.
* A power LED (LED1): shows the status of the fan.
* A general device LED (LED2): shows the status of the general air machine.
* A LED reserved for the future.

The device has a button for flash the firmware in the microcontroller, and is also used for the user.

The board has an external connector available for the three LEDs and the button.

## Pin assignment

| PIN     | Func    |
| ------- | ------- |
| TODO    | TODO    |


## Enclosure (WIP)
* Custom made in [Fusion 360](https://www.autodesk.es/products/fusion-360/overview).

# Changelog
All notable changes to this project will be documented in this section.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

## [3.0.0] - 2024-04-24
### Fix
- Change microcontroller for more GPIOs
- Remove IO expander
- SMD LEDs
- Change connectors to JST
- Add external connector
- Envirometal sensors with cutouts for avoid hot
## [2.0.0] - 2023-09-04
### Added
- First stable release in this repository

[Unreleased]: https://github.com/GuilleGonzzalez/hw-aire
[2.0.0]: https://github.com/GuilleGonzzalez/hw-aire/releases/tag/v2.0.0
