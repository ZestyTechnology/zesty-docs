Calibrating the Dual Nimble
===========================

Because of the gear ratio inside the Nimble, There are a lot mor steps per millimeter than your usual number. 

.. note:: Start with 3000 steps/mm with a 1.8deg stepper and 1/16 microstepping

The Nimble has a nice flat surface you can use to set the ruler on, when measuring the filament, simply place it on top of the "ears" of the breech block.
Use a light coloured filament, place it in the breech, heat up the hot end and start the process.

* Measure 100 mm on the filament, by holding the filament against the ruler while the ruler stands on the breech block ears. 
* Mark the distance with a permanent marker.
* Extrude 50 mm using the firmware controls.
* Measure the remaining length to the mark made. 
* Calculate the new number of steps/mm using the following formula:

.. note:: New steps = current steps * actual mm extruded/50 (50 being the 50 mm of filament you wanted to extrude.)

* enter the new value in your firmware settings.
* Do the whole sequence again, to confirm that the steps per millimeter are now set correctly.
* if not, recalculate and re-confirm.

.. note:: Make sure you configure both the steppers the same 

Setting Dual Nozzles
--------------------

To set the nozzles for a Chimera to the same height, we suggest using the following procedure, suggested by Richard.

* Adjust one nozzle to roughly the middle of height range.
* Adjust the other nozzle higher.
* Drop the nozzle down to print height with a sheet of paper under it.
* Adjust the height until the nozzle grips the paper lightly.

The 1st nozzle is now set. Now for the second one.

* Drop the second nozzle until it is touching the paper.
* Rotate the paper and see around which nozzle it rotates.
	- If it is the first nozzle, lower the second nozzle a little more
	- If it is the second nozzle, raise it a bit.

The idea is to get the paper to rotate around each nozzle with the same force needed. As Richard said: "This is fiddly and time consuming but can be done! "

You have now set the extrusion rate of the Dual Nimble correctly and have the nozzles set right.
You can now start Using the Dual Nimble.

See the :doc:`Using the Nimble<./using>` page or click Next.
