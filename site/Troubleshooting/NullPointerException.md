---
layout: default
title: NullPointerException
nav_order: 2
parent: Troubleshooting
---

## NullPointerException
Example: 
```
NullPointerException - Attempt to invoke virtual method java.lang.Object com.qualcomm.robotcore.hardware.HardwareMap.get (java.lang.Class, java.lang.String) on a null object reference
```

## Fixes:

This happens when the robot can’t find a certain motor or sensor. Check that you’re running the right program and Hardware Map first, and if all the motors and sensors you need are added to the hardware map. 

Check that you named everything correctly. The names in the Hardware Map are case-sensitive.

Another common fix is that one of the motor/sensor wires got unplugged. Check that all the wires around the robot are plugged in.

This could also be a problem with the programming itself. Check for an issue where you made a motor, but set it to `null`, then never initialized it. 

For example:
```
DcMotor leftMotor = null;
leftMotor.setPower(1);
```
would crash.

This is a problem that can happen in all Java programs, not just with FTC.