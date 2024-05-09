# FloraGrow ![Static Badge](https://img.shields.io/badge/stability-beta-orange)

## Overview
This project revolves around the topic of smart irrigation in smart homes. First, I will release a soil moisture sensor. This sensor is powered by a power supply and connects via MQTT to an IoT software such as Home Assistant, ioBroker, Node-RED or similar. Later, there will likely be a variant that is powered by a battery and a valve controller with flow meters to complete the irrigation system.

<img width="400" alt="image" src="https://github.com/Elektroarzt/floragrow/assets/61664171/703e603e-a8ef-4864-9fb5-a0efed62c016">

### Schematic
<img width="1200" alt="image" src="https://github.com/Elektroarzt/floragrow/assets/61664171/1fc1ced2-c58f-468e-8b4b-dea82ee26cf0">

### Mechanics
As a little teaser, here is an exploded assembly video of the functional model:

https://github.com/Elektroarzt/floragrow/assets/61664171/9023889c-925e-4a48-a43b-feb629170dae

The data upload will follow shortly. The following design parameters will be implemented:
- ESP32-C3 Super Mini DevBoard
- compatible to XIAO ESP32-C3 with external antenna for extended WiFi range
- Wide range power supply input 5...40V DC
- 3D printed housing
- strain relief
- epoxy resin encapsulated electronics to meet outdoor requirements
- Usage of standard components

## Credits
The Sense Board utilizes the excellent SoMoSe (Soil Moisture Sensor) developed by BeFIE you can find under
https://github.com/BeFlE/SoMoSe and is sold on Amazon Germany
