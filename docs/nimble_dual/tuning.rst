Tuning the Firmware
===================

The Nimble C/C is a different beast to standard extruders and therefore requires some quite specific firmware changes if you hope to get optimal performance. We recommend use of a 1.8 degree stepper, 0.9 degree stepers are great for your other axis, but with the Nimble it's just not required or advisable.

.. Note:: For 32 bit boards start at around 2700 steps/mm at 1/16 microstepping.

.. Note:: For 16 bit boards start at around 1200 steps/mm at 1/8 microstepping.

.. Note:: For 8 bit boards start at around 600 steps/mm at 1/4 microstepping.

Your settings will probably be slightly different, so after setting this do the normal extrusion calibration.

Configuring microstepping
-------------------------

Depending on your electronics microstepping will either be changed by altering jumpers, if your driver is configurable via software:

| **Marlin:** 
| If driver microstepping is settable via firmware.
| #define MICROSTEP_MODES {x,y,z,e0,e1}
| 
| **Repetier:**
| Usually configured via hardware jumpers.
| 
| **RepRap Firmware:**
| https://duet3d.com/wiki/G-code#M350:_Set_microstepping_mode
| 
| **Smoothieware:**
| http://smoothieware.org/extruder
| Version 1.0 board has microstepping fixed at 1/16
| Version 1.1 board fixed at 1/32. 
| Adjust steps accordingly.
| 


Current for the steppers
------------------------

The tuning of the stepper driver for efficient extrusion and retraction is a little different, than with a bowden system or other direct drive systems. Because the Nimble has so much torque available, you can/must run a much lower vref for your stepper than normal. This also helps getting the pulses across properly as you are not fighting decay in the pulses caused by too much current.
(Yes there is such a thing, have a look at the excellent work Ryan Carlyle has done: https://github.com/rcarlyle/StepperSim )

Start with the suggested vref and go down if needed. Don’t be tempted to simply increase vref if the stepper stalls. It feels contra-dictionary, but the science backs it up.

.. Note:: Suggested vref is 0.3V or 500 mA but it depends on your setup and actual voltage supplied.

Acceleration value
------------------

For the acceleration settings, let’s begin with a low setting and you can increase it later if you want to have a faster retraction. Again, the aim here is to move things as smoothly as possible.

.. Note:: Suggested acceleration setting is 120 mm/sec2

Jerk value
----------

Another aspect you need to reduce is the jerk value as it helps to move the gears and drive cable in a smooth way. The goal here is to get smooth motion, not harsh forced movements. After you adjust the jerk settings, we suggest you leave them as set and do not use them to tune the retraction. They have little if any measurable impact on print speed anyway.

.. Note:: Suggested jerk or instant speed change setting is 0.6 mm/sec or 40 mm/min

| **Marlin:**
| DEFAULT_EJERK = 0.6
| 
| **Repetier:**
| EXT0_MAX_START_FEEDRATE = 0.6
| 
| **RepRap Firmware:**
| M566 should have E value set to E40  (as it is set per minute)
| 
| **Smoothieware:**
| http://smoothieware.org/motion-control#junction-deviation
| Smoothie does not use jerk, you instead need to alter the Junction deviation setting, we suggest you start at 0.001 and work your way up in 0.001 increments.
| 

Retraction speed
----------------

For the normal extrusion and retraction settings in your slicer, please test the settings with the extruder multiplier set to 1 or 100% extrusion. Set the retraction speed to 30 mm/sec. This is the optimal retraction speed for PLA and should be the standard. You can increase retraction speed if you want to, but normally 30 mm/sec is perfect.

.. Note:: Suggested retraction speed is 30 mm/sec

Tuning it all
-------------

Now comes the fun part. You can start playing with the acceleration and vref settings to get better retraction, if you want to have faster retractions. Please leave the jerk settings as they are. Tuning the retraction is now a matter of give and take by playing with the settings. 

* Set the initial desired retraction speed and check to see if it stalls. If it does not, you can increase the acceleration value until your retraction starts to stall. 

* You can now do a few things. 
	- You can decrease the acceleration and leave it at that. 
	- Or you can decrease vref a bit further and try again. 
	- Or you can reduce the retraction speed. 

Up to you and what your situation and printer needs. By playing with these settings you can fine tune the whole retraction process.
Do try and keep the settings for both steppers the same. 

You are now ready to start using the Nimble C/C, so go to the :doc:`Using the Nimble C/C<./using>` page or click Next.

Troubleshooting
---------------
If these settings do not work for you, the first thing to try is to reduce the jerk setting. You can go as low as 0.1 mm/sec as the jerk setting has virtually no impact on your total print time. If you still find you cannot retract at the speed you need, reduce, let me repeat that, reduce the vref even further. You can go down as low as 0.1V. If it still does not work as you expect, contact us on chat and we will have a lively discussion about it.
