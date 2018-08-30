Wiring it all up
================

Before we begin
---------------

There are various ways to wire it all up. It depends on your control board what the best way is. There are a lot of different boards and capabilities so we can only give you general intstructions. 

.. Note:: Remember, the pump and the fan for the radiator are 12V!

The Pump
--------
The pump must be on when the hot end is on. You can decide to switch the pump on and off automatically or simply wire it directly to the PSU, because the pump is so quiet. This means that the pump runs whenever the printer is on. 

Switching the pump on only when the hot end is switched on, can be done via the hot end fan control. 

Some control boards (like the Duet) can switch fan voltages, so if you can switch the fan control normally used for the heatsink fan of the E3D to 12V, do so. Then simply connect the water pump to that. 

If you cannot use 12V on your control board, you can use different ways to control it, for instance use a buck converter, or use the 5V to switch a 12V relay. 

The Radiator fan
----------------
The water itself has such a heat capacity that you might not need to run the fan for the radiator at all. It is only when you run the Kryo in a heated chamber that you might want to actively cool the water down. 

If you want to use automatic temperature control for the radiator fan, you have to connect a temperature sensor to the control board, so it can measure the water temp. Once you have done that, you can program the formware to switch the pump on as soon as the water temperature rises above 40 deg for instance.

One way to connect a water thermometer is to use a standard thermistor, that is taped to the outside of the radiator inlet hose with some electrician tape. Add some insulation around the outside to increase the accuracy. 

Alternatively, you can install a thermometer in the water system and connect it to a temperature indicator or to the control board. You will need to adjust the settings of the temp sensor in your firmware to get accurate readings. 
The temp sensor we sell uses a thermistor that can be used on normal control boards. 

Duet WiFi and Ethernet
----------------------

For the Duet WiFi and Ethernet boards, you can wire the pump into the FAN0 socket. If you don't have other 5V fans, you can switch the fan voltage to 12V on the board using the V Fan Jumper Select.
Control the pump with the following Gcode:

* M106 P0 T50 S1 H1

This will switch the pump plugged into FAN0 (P0) to 100% (S1) when the hot end (H1) reaches 50C (T50) 

If you cannot switch the overall fan voltage to 12V you can connect the + of the pump (red wire) to the VIN on the board and the - of the pump (black wire) to the GRD of FAN0.

For the Radiator fan you use a similar process, except you use FAN1 and for temperature sensing you use E1 connector. This is the second hot end thermistor control. In this case we use it for sensing the temperature of the water. 

The Gcode is as follows:

* M106 P1 T45 S0.5 H2

This will activate the fan plugged into FAN1 (P1) when the temperature reaches 45C (T45) at the thermistor plugged into E1 (H2) and it will run the fan at 50% (S0.5) of full speed. 

