Motor Control
=============

Motor control is one of the most important concepts of FRC programming, because it is what allows the robot to move.

Controller Types
----------------
There are two types of motor controllers, CAN (Controller Area Network) and PWM (Pulse Width Modulation.)
Typically, CAN controllers are preferred because CAN, like USB, is a serial connection, which allows for more features than the single analog value provided by PWM. For example, CAN controllers support internal PID loops, velocity commands, and more.

Library Requirements
--------------------
Almost all CAN motor controllers have their own libraries that are separate from core WPILib. These libraries must be installed to utilize the advanced features of the CAN controllers.

