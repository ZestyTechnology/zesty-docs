Calibrating the Nimble Sidewinder V2
===========================

Because of the gear ratio inside the Sidewinder V2, There are a lot more steps per millimeter than your usual number. 

.. note:: Start with 1800 steps/mm with a 1.8deg stepper and 1/16 microstepping

The Sidewinder has a nice flat surface you can use to set the ruler on, when measuring the filament, simply place it on top of the "ears" of the breech block.
Use a light coloured filament, place it in the breech, heat up the hot end and start the process.

* Measure 100 mm on the filament, by holding the filament against the ruler while the ruler stands on the breech block ears. 
* Mark the distance with a permanent marker.
* Extrude 50 mm using the firmware controls.
* Measure the remaining length to the mark made. 
* Calculate the new number of steps/mm using the following formula:

.. note:: New steps = current steps * 50/actual mm extruded (50 being the 50 mm of filament you wanted to extrude.)

* enter the new value in your firmware settings.
* Do the whole sequence again, to confirm that the steps per millimeter are now set correctly.
* if not, recalculate and re-confirm. 

You have now set the extrusion rate of the Sidewinder correctly and have the nozzles set right.
You can now start Using the Sidewinder.

See the :doc:`Using the Sidewinder<./using>` page or click Next.
