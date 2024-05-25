# FloraGrow [![stability-release-candidate](https://img.shields.io/badge/stability-pre--release-48c9b0.svg)](https://github.com/mkenney/software-guides/blob/master/STABILITY-BADGES.md#release-candidate)

## Overview
This project revolves around the topic of smart irrigation in smart homes. First release is a power supplied soil moisture sensor (Sense PS). It connects via MQTT to an IoT software such as Home Assistant, ioBroker, Node-RED or similar. Later, there will likely be a variant that is powered by a battery and a valve controller with flow meters to complete the irrigation system.

<img width="350" alt="image" src="https://github.com/Elektroarzt/floragrow/assets/61664171/24fca857-ed9b-4213-821d-297480db23ae">
<img width="350" alt="image" src="https://github.com/Elektroarzt/floragrow/assets/61664171/734b0c6d-95bb-40ba-81a5-4be0aeca1550">
<img width="350" alt="image" src="https://github.com/Elektroarzt/floragrow/assets/61664171/d4eaf9d8-0a77-40e2-b17f-2aae4da73ebf">


The Sense PS has the following features:
- Measurement of soil moisture and device temperature
- WiFi connection to an MQTT broker
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

### PCB
The PCB has two layers with planes for 3.3V on top and GND on the bottom side. It is populated from both sides to achieve a compact form factor. The power cord leads are directly soldered to SMD pads on the PCB.

<img width="350" alt="FloraGrow Sense PS PCB top" src="https://github.com/Elektroarzt/floragrow/assets/61664171/905aee47-8427-4945-a408-d85a72fc7ef2">
<img width="352" alt="FloraGrow Sense PS PCB bottom" src="https://github.com/Elektroarzt/floragrow/assets/61664171/79f98e80-1627-4cef-a77b-8b71a5135669">

### Firmware
The ESP32 of the Sense PS can be programmed with the firmware of the manufacturer of the sensor [available here](https://github.com/BeFlE/SoMoSe). The firmware facilitates the following MQTT topics:

**Published topics**

 Topic                          | Values                  | Notes
 :----------------------------- |:------------------------|:--------------------------------------------------
 somose_name/1/Humidity         | number (0...255)        | raw value of the sensor
 somose_name/1/Humidity-Average | number (0...255)        | smoothed, average value of the sensor
 somose_name/1/Name             | string                  | name of the sensor
 somose_name/1/Temperature      | number                  | temperature of the sensor in degree celsius

For details on the MQTT topics see website of the seonsor manufacturer. Be sure to have the ESP32 programmed before potting ;)
After programming, the device is capable for OTA updates via its web interface.

### ESPhome
For direct integration into Home Assistant, ESPhome configuration files also can be downloaded from the sensor [manufacturer site](https://github.com/BeFlE/SoMoSe).

### Mechanics
All components are soldered to the PCB and mounted into the housing. The whole circuit is potted with 2 components resin to ensure outdoor capability.
If someone is interested in a complete device including all parts (PCBA, ESP32, housing, etc.) you can contact me under elektroarzt@digital-filestore.de.

https://github.com/Elektroarzt/floragrow/assets/61664171/9023889c-925e-4a48-a43b-feb629170dae

## Credits
The Sense Board utilizes the excellent SoMoSe (Soil Moisture Sensor) developed by BeFIE you can find under
https://github.com/BeFlE/SoMoSe and is sold on Amazon Germany
