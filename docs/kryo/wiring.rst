Wiring it all up
================

Before we begin
---------------

There are various ways to wire it all up. It depends on your control board what the best way is. There are a lot of different boards and capabilities so we can only give you general intstructions. 
.. Note:: Remember, the pump and the fan for the radiator are 12V!

The Pump
--------
The pump must be on whenever the hot end is switched on. You can decide to switch the pump on and off automatically or simply wire it directly to the PSU, because the pump is so quiet. This means that the pump runs whenever the printer is on. 

Switching the pump on only when the hot end is switched on, can be done via the hot end fan control.  
Some control boards (like the Duet) can switch fan voltages, so if you can switch the fan control normally used for the heatsink fan of the E3D to 12V, do so. Then simply connect the water pump to that.  

The Radiator fan
----------------
If you want to use automatic temperature control for the radiator fan, you have to connect a temperature sensor to the control board, so it can measure the water temp. Once you have done that, you can program the formware to switch the pump on as soon as the water temperature rises above 40 deg for instance. 
One way to connect a water thermometer is to use a standard thermistor, that is taped to the radiator inlet hose with some electrician tape. Add some insulation around the outside to increase the accuracy. 
Alternatively, you can install a thermometer in the water system and connect it to a temperature indicator or to the control board. You will need to adjust the settings of the temp sensor in your firmware to get accurate readings. 
The temp sensor we sell uses a thermistor that can be used on normal control boards. 
