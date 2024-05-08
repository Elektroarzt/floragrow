## Overview

This project revolves around the topic of smart irrigation in the smart home. First, I will release a soil moisture sensor. This sensor is powered by a power supply and connects via MQTT to an IoT software such as Home Assistant, ioBroker, Node-RED, or similar. Later, there will likely be a variant that is powered by a battery.

### Schematic
![FloraGrow Sense PS V2 0 schematic](https://github.com/Elektroarzt/floragrow/assets/61664171/1fc1ced2-c58f-468e-8b4b-dea82ee26cf0)

### Mechanics
As a little teaser, here is a video of the prototype in action:

https://github.com/Elektroarzt/floragrow/assets/61664171/9023889c-925e-4a48-a43b-feb629170dae

The data upload will follow shortly. The following functions will be implemented:
- ESP32-C3 Super Mini DevBoard
- Wide range power supply input 5...40V DC
- Usage of standard components
- 3D printed housing
- epoxy resin encapsulated electronics to meet outdoor requirements
