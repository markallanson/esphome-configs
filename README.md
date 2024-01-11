# esphome-configs
My ESPHome Configurations

## General Configuration Approach
I split out as much configuration as I can into separate configuration files to keep the node specific
configuration files as light as possible. These shared configuration files are included in the node 
specific files. I also use packages a bit as well. 

## Shared Configurations
* `default-sensors.yaml` contains a set of default sensors I want present on all devices. 
* `shared-nodemcu-32.yaml` contains default NodeMCU ESP32 configuration shared across all such devices.
* `shared-wifi.yaml` contains default WiFi configuration for all devices.
* `shared.yaml` contains other miscellaneous shared configuration to apply to all devices.

## The Nodes

### boiler-temperature-monitor (Work in progress)
This device is simply a collection of Dallas temperature sensors for reading temperate information related
to my heating and hot water system, it records temperatures for:

* Radiator flow and return.
* Hot water cylinder (unvented) flow and return.
* Cold water inlet temperature
* Under floor heating loop overall flow and return temperature (not individual loop temperatures, I may do a 
  separate node for recording those).

I may also do an overall boiler flow and return temperature (because, why not, while I am here).
