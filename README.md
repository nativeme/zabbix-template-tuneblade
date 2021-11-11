# zabbix-template-tuneblade
Zabbix templete for monitoring TuneBlade Airplay devices via REST API.
## Description
TuneBlade is audio streaming software for AirPlay recivers by **BreakFree Audio**.  
TuneBlade homepage: http://www.tuneblade.com/  
BreakFree Audio homepage: http://www.breakfreeaudio.com/  

This template utilises TuneBlade's built-in REST-API with Zabbix LLD Macros to automaticaly generate TuneBlade devices items in Zabbix, with all properties availible through API.  

Combo yaml file It comes with 2 templates:
1. Template App TuneBlade
2. Template App TuneBlade Discovered device

## Templates

### Template App TuneBlade
Points to maschine where you have installed your TuneBlade instance.  
It will GET list of your devices connected to TuneBlade instance and run Zabbix LLD macro over it.
### Template App TuneBlade Discovered device
It defines device schema for TuneBlade's AirPlay device.  
Every discovered device will be created based on this properties and triggers.

## Triggers
### tuneblade_device_not_streaming
Throws problem when TuneBlade Airplay device not streaming.