oasis
=====

This driving suite is a for a mecanum wheel chassis. It incorporates four individually-driven mecanum wheels and a gyro sensor. Without these, the suite cannot function to its full potential.

The suite incorporates three main tasks:
- the gyro task
- the drive task
- the superdrive task

=====

Gyro Task

The gyro task calculates a heading and is very accurate... more accurate than Xander's current example program (as of August 2, 2014). It's more accurate for two reasons:
1. It takes a large sampling (100 samples) of gyro readings to calculate an average base reading. This eliminates the problem where the header (yaw) readings climb.
2. It uses the internal clocks instead of delays, which allows you to use other tasks simultaneously.

PROBLEM: If you have just booted up the NXT, the gyro reading will climb if you run this program first. I don't know why. If you need to run the program first, make a tiny program and run it before you use this one.

=====

Drive Task

This is a simple task for driving with the mecanum wheels. Nothing fancy.

=====

SuperDrive Task

This is a task that incorporates both the above driving mode and a second mode that allows the robot to spin freely while moving. I will call this the free-spinning mode in the program's documentation. The free-spinning mode gets a heading, and lets the driver move the robot relative to that heading regardless of the actual heading of the robot. 

To switch to this mode, hold button six. (I may make this toggle-able later) To change the base heading, press 5.
