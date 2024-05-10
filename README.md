# FloraGrow ![Static Badge](https://img.shields.io/badge/stability-beta-orange)

## Overview
This project revolves around the topic of smart irrigation in smart homes. First release is a power supplied soil moisture sensor (Sense PS). It connects via MQTT to an IoT software such as Home Assistant, ioBroker, Node-RED or similar. Later, there will likely be a variant that is powered by a battery and a valve controller with flow meters to complete the irrigation system.

<img width="400" alt="image" src="https://github.com/Elektroarzt/floragrow/assets/61664171/703e603e-a8ef-4864-9fb5-a0efed62c016">

The Sense PS has the following features:
- ESP32-C3 Super Mini DevBoard
- wide range power supply input 5...40V DC
- 3D printed housing
- strain relief
- epoxy resin encapsulated electronics to meet outdoor requirements
- usage of standard components

### Schematic
The schematic is quiet simple, only a few devices are put together.
 
<img width="1200" alt="image" src="https://github.com/Elektroarzt/floragrow/assets/61664171/1fc1ced2-c58f-468e-8b4b-dea82ee26cf0">

### Partslist
You can buy the components at the following sources:
 Component                     | Name                             |Source
 :-                            |:-                                |:-
 ESP32 Development Board       | ESP32 C3 Super Mini              | Ali Express
 Soil Moisture Sensor          | SoMoSe                           | Amazon Germany
 Buck converter                | DD4012SA (3.3V Version)          | Ali Express
 Soil Moisture Sensor          | SoMoSe                           | Amazon Germany
 Electrolytic Capacitor        | 220uF /10V radial                | Reichelt, Amazon, etc.
 Power cable                   | H05RN-F 2x1                      | Amazon, some hardware stores
 Screws                        | M3 x 6mm                         | hardware store
 Housing components            | see housing 3D models folder     | self printed

### Mechanics
All components are assembled on the PCB and mounted into the housing. The whole circuit is potted with 2 components resin to ensure outdoor capability.

https://github.com/Elektroarzt/floragrow/assets/61664171/9023889c-925e-4a48-a43b-feb629170dae

## Credits
The Sense Board utilizes the excellent SoMoSe (Soil Moisture Sensor) developed by BeFIE you can find under
https://github.com/BeFlE/SoMoSe and is sold on Amazon Germany
