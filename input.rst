Input
=====
When accessing inputs from a controller, there are two available types of data. Analog axes, like thumbsticks and triggers, provide a decimal value between -1 and 1 which represents the position of the axis. Digital values, like buttons or bumpers, simply provide a true/false value based on if the button is pressed.

Deadzones
-------------
Because sensors aren't perfect, noise can be introduced into analog inputs. A "deadband" or "deadzone" may help to reduce the effects of noise or subtle movements. Essentially, a zone around zero is created where the value of the input will always be zero, so a value of 0.001 will still register as nothing. Outside of that zone, the input is mapped to be zero at the edges of the deadzone, then continued to (1,1) and (-1,-1).

Expo
----
To improve fine control, analog inputs are typically raised to a power, called expo (short for, you guessed it, exponent.) This gives more "resolution" when doing fine maneuvers while still allowing full speed to be reached.