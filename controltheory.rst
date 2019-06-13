Control Theory
==============
Control theory is the underlying means of moving anything in a controlled and efficient manner. This page will show various means of controlling a mechanism, some better than others.

Terminology
-----------
*error*: the difference between the current value and setpoint

*setpoint*: the value the controller targets

*steady-state*: error sustained over a long period

Bang-Bang
---------
Bang-Bang is one of the simplest control algorithms out there, but is rarely used in FRC. Essentially, the algorithm states that if the value is below the target, go up at a constant rate, and if the value is above the target, go down at a constant rate. In theory, this seems okay, but once you take inertia into account, you can get a lot of instability and oscillation. Variants exist that try to remedy its weak points, but you're probably better off using a more advanced algorithm.

PID
---
PID (Proportional Integral Derivative) control is pretty much your go-to algorithm. It was developed over 100 years ago to steer naval ships, but its versatility means it can be applied to almost any scenario.

PID is configured with three "gain" values. **kP** is the scale that error affects the final output. kP does most of the heavy lifting, and can be used alone, if desired.
**kI** is the scale that the integral of error (sum over time) affects the final output. It can be used to combat steady-state error, when the controller stops at a point other than the setpoint. It is typically not reccommended due to its instability, and should be replaced with a good feed-forward.
**kD** is the scale that the derivative of error (change over time) affects the final output. It is used to dampen the controller's output if it is moving too quickly, and is used to combat overshoot.

Each gain of PID must be tuned to reach a good controller. There are empirical ways of doing it, but experimentation is almost always necessary to reach the best controller possible.

.. image:: https://media1.tenor.com/images/d8c07c69d7d6fa992876f6207d7875db/tenor.gif?itemid=5063488