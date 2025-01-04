# WB_Heidelb_Amperf_EC
Wallbox Connect and Control for Amperfied / Heidelberg EnergyControl

These Integration shows the Data of the EnergyControl Wallbox of the Conpany Amperfied formerly known as Heidelberg.

The Communication is over Modbus RTU and need a wired connection to the Wallbox.
At the Wallbox itself there have to be some dip switches set to allow communication.

The Modbus protocol is documented under https://www.amperfied.de/wp-content/uploads/2023/03/20220809_AMP-Erweiterte-ModBus-Registerbeschreibung.pdf

In the configuration.yaml you have to add a modbus section
(I only have these modbus usage therefore i named it modbus.yaml)

modbus: !include modbus.yaml

in the same folder in which the configuratin.yaml is placed you should copy the modbus.yaml file

If Hardware connection is established and Homeassistant is restarted the entities are added.

A Photovoltaic optimized vehicle charging could be established with these communication.

The current could be defined from 0, and 6.0 till 16.0 Amp in 0.1 Amp Steps
depending on the vehicle there could be additional restrictions / Amp Steps included.

