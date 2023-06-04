# ESPHOME-Growatt
Read Growatt Solar inverter data with ESPHome 

## Goal 
Add Solar data to my Home Assistant dashboard without the use of a cloud solution offered by the manufacturer of the inverter.

## Hardware
That was actually very simple.
The Growatt inverters use an USB dongle to send the data to the internet, I replaced the USB dongle with my own. My own USB dongle is an UART combined with an ESP-01 board.

![image](https://github.com/WaarlandIT/ESPHOME-Growatt/assets/53364386/7a3920a0-4d42-4e5f-84fb-64957582b2e8)

Because they fit nicely together it was an easy choice. 

## Software
ESPHome is the easiest way to create a Home Assistant compatible agent. 
Check the ESPHome.io website for how to program the ESP-01, the needed yaml file is in this repository. Make sure you add the wifi details and an API key to the yaml, personally I use a secrets.yaml for my wifi and api details so that the integration scripts are clean.

## Usage
After programming the ESP-01 add the dongle in the USB port of the inverter find the allocated IP in your wifi router. 

![image](https://github.com/WaarlandIT/ESPHOME-Growatt/assets/53364386/d68157f7-7551-4dca-862f-c040747037a3)


Use the Home Assistant ESPHome integration to add the dongle.
When you check the Sensors you will see something like this:

![image](https://github.com/WaarlandIT/ESPHOME-Growatt/assets/53364386/b9e3e7b2-da70-434a-8248-19f1a68ffcde)


I found the yaml somewhere on a forum and altered it for my usecase, not sure who the original author is. 
