Assembling the Zesty Cryo
=======================


Before we begin
---------------

Because of the process used to make the plastic parts (SLS) there is a possibility of powder remaining inside some of the smaller openings. For instance, there might still be a little powder left in the holes for the mounting bolts. 
This is the moment to inspect the parts and to make sure they are all powder free. 

Step 1
------

.. figure:: images/3_step01.svg
    :alt: Groove mount insert
    :height: 286px
    :width: 400px

    Screw the Groove mount (part B) in the Cryo unit (part A)

    * Screw it tight and use a small spanner or pair of pliers to get it tight.

    .. Note:: The steps are the same if you are using the M12x1.5 insert (part C) or the Stub insert (part D)  

Step 2
------

.. figure:: images/3_step02.svg
    :alt: Insert heat break
    :height: 286px
    :width: 400px

    Insert the E3D V6 heat break into the bottom of the Cryo unit.


Step 3
------

.. figure:: images/3_step03.svg
    :alt: Prepare 6 mm hoses
    :height: 286px
    :width: 400px

    Slide the hose clamps (parts G) over the ends of the 6 mm hose.

    * Slide them at least 20 mm into the hoses


Step 4
------

.. figure:: images/3_step04.svg
    :alt: Connect input hose
    :height: 286px
    :width: 400px

    Connect the output of the pump to the bottom input nipple.

    * Position the hose clip between the two ridges.

Step 5
------

.. figure:: images/3_step05.svg
    :alt: Connect return hose
    :height: 286px
    :width: 400px

    Connect the return hose (that goes to the radiator) to the top output nipple.

    * Position the hose clip between the two ridges..

Step 6
------

.. figure:: images/3_step06.svg
    :alt: PTFE tubing
    :height: 286px
    :width: 400px

    Insert the PTFE tube until it is seated in the heatbreak.

    * Leave it longer than needed, so you can trim it to length after mounting.

    .. Note:: There is no retaining clips for the PTFE tube, so you will need to provide the clamping force by mounting it in an adapter that holds the PTFE tube or allow the Nimble to clamp down on the PTFE tube.

Step 7
------

Mount the Hydro unit as normal with the groove mount. 

.. Note:: To mount the unit use the side mounted holes. These holes are untapped for M3 but the screws will simply screw in. 

Step 8
------

.. figure:: images/3_step08.svg
    :alt: Assembled Heat block
    :height: 286px
    :width: 400px

    Screw in the heat block. 

    * Follow the standard E3D procedure for installing the heat block and nozzle.

Step 9
------

Guide the hoses to the Pump and Radiator in such a way that the printhead's full range of motion is not restricted by the hoses.

Step 10
-------

Insert the hose reducers to the 10 mm OD hoses coming from the Pump and Radiator and secure with hose clips.

Step 11
-------

Connect the 6 mm hoses from the Hydro unit to the reducers and secure with the hose clips.

Step 12
-------

Fill the pump water tank and switch it on.

* Check carefully for any leaks at every junction or connection.

Wiring up the pump for the Cryo
################

First run the extruder a minute or two, with no filament clamped. Just to bed the gears and drive cable in. Extrude and retract a few times. (You will have to switch off the temperature control as most controllers will not move the extruder stepper unless the hot end it up to temperature)
Use M302 P1 on RepRapFirmware to switch cold extrusion on (allow extrusion while cold) and M302 P0 to switch it off again.
For other firmware use M302 S0 to switch cold extrusion on and M302 S170 to set extrusion to a minimum temp of 170C.



Tuning the firmware
####################

Before using the Nimble you need to tune the firmware and calibrate the extrusion. You will need to tune the firmware first, as the Nimble is quite a different type of extruder. 

See the :doc:`Tuning the Firmware<./tuning>` page.

