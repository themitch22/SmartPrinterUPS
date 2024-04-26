# SmartPrinterUPS
A smart programmable un-interruptable power supply for 3D printers and other DC powered devices. 

Design Requirements
===================

 - Automatically switch between a DC power supply and Batteries as a Un-Interruptable Power Supply. (Similar to the BTT 24V UPS: https://biqu.equipment/products/btt-ups-24v-v1-0-resume-printing-while-power-off-module)

 - Ability to handle an Ender 3 or equivalent 24V powered 3D printer - Max 240W DC output (24V/15A)

 - Batteries need to be commonly available: LiFEPO4 packs from Amazon, Powertool Batteries (Ryobi, Milwuakee, Bauer), SLA (Sealed Lead-Acid)

 - Main output disconnect relay that will disconnect the power when there's a fault or to conserve power remotely (like an IoT switch).

 - Ability to program voltage can current limits that will allow it to switch over to prevent damage to the batteries.

 - Data logging voltage and current while powered on to calculate a power discharge curve that can be used for battery time estimation and power consumption costs.

 - 3D printers with AC heated beds (Voron Trident/V2.4) can be used but the bed heat will drop causing thermal faults in Klipper and might cause irrecoverable prints.

 - Display and buttons to navigate info displays and set the cut-off setpoints and types of power sources.

 - Keep the board size less than 100x100mm and designed for use in FR (flame resistance) 3D printed cases.

Feature Creep
=============

 - Klipper/Moonraker integration so you can display the power consumption on a graph similar to temperature.

 - Ability to run certain Klipper macros when certain alarms are triggered (like power recovery and safe shutdown)

 - A built-in BMS, charger, and buck boost for lithium batteries so it can keep charged while plugged in to the main power supply, and output a regulated 24VDC.

 - Have a separate output for an AC inverter so you can power the bed heater on bigger printers with a separate battery or power source without discharging main printer battery.

 - Main disconnect relay can be used to stop thermal runaway events that can happen when mosfets fail, or the printer doesn't detect a current spike.

 - Possible CANBUS/Wifi/RS232 support so it can be used for other applications like automotive backup batteries, medical equipment, industrial applications.





