Range Sensor Overview
=====================

The Range Sensor has many different uses and applications. These applications may
include the use of the range sensor to detect the placcement on the field, or the
use of the Range Sensor to track the distance from an object. A distance can then
be applied to improve autonomous code or make programming the robot a more simple
task to perform.

An image of a Rev Range Sensor is shown here.
![alt text](https://raw.githubusercontent.com/ftccats/ftccats.github.io/master/Distance%20Sensor.jpg)

# Range Sensor Code Explanation
The Code Is Shown Here:

```java
/* Copyright (c) 2017 FIRST. All rights reserved.
 *
 * Redistribution and use in source and binary forms, with or without modification,
 * are permitted (subject to the limitations in the disclaimer below) provided that
 * the following conditions are met:
 *
 * Redistributions of source code must retain the above copyright notice, this list
 * of conditions and the following disclaimer.
 *
 * Redistributions in binary form must reproduce the above copyright notice, this
 * list of conditions and the following disclaimer in the documentation and/or
 * other materials provided with the distribution.
 *
 * Neither the name of FIRST nor the names of its contributors may be used to endorse or
 * promote products derived from this software without specific prior written permission.
 *
 * NO EXPRESS OR IMPLIED LICENSES TO ANY PARTY'S PATENT RIGHTS ARE GRANTED BY THIS
 * LICENSE. THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
 * "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO,
 * THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
 * ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE
 * FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
 * DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
 * SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
 * CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
 * OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
 * OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 */

package org.firstinspires.ftc.robotcontroller.external.samples;

import com.qualcomm.robotcore.eventloop.opmode.Disabled;
import com.qualcomm.robotcore.eventloop.opmode.LinearOpMode;
import com.qualcomm.robotcore.eventloop.opmode.TeleOp;
import com.qualcomm.robotcore.hardware.OpticalDistanceSensor;

/*
 * This is an example LinearOpMode that shows how to use
 * a Modern Robotics Optical Distance Sensor
 * It assumes that the ODS sensor is configured with a name of "sensor_ods".
 *
 * Use Android Studio to Copy this Class, and Paste it into your team's code folder with a new name.
 * Remove or comment out the @Disabled line to add this opmode to the Driver Station OpMode list
 */
@TeleOp(name = "Sensor: MR ODS", group = "Sensor")
@Disabled
public class SensorMROpticalDistance extends LinearOpMode {
  //instantiates new OpticalDistanceSensor
  OpticalDistanceSensor odsSensor;  // Hardware Device Object

  @Override
  public void runOpMode() {

    // get a reference to our Light Sensor object.
    //uses new method .get to store a certain parameter and take an OpticalDistanceSensor
    odsSensor = hardwareMap.get(OpticalDistanceSensor.class, "sensor_ods");

    // wait for the start button to be pressed.
    waitForStart();

    // while the op mode is active, loop and read the light levels.
    // Note we use opModeIsActive() as our loop condition because it is an interruptible method.
    while (opModeIsActive()) {

      // send the info back to driver station using telemetry function.
      telemetry.addData("Raw",    odsSensor.getRawLightDetected());
      telemetry.addData("Normal", odsSensor.getLightDetected());
      // gets update method from the class
      telemetry.update();
    }
  }
}

```

What the code does is utilize the fact that the OpMode is on, it will activate a forever loop
that will scan light levels and record the dictance traveled.

As displayed by comments, a new OpticalDistanceSensor is instantiated in order to create a 
new OpticalDistanceSensor that will inherit the properties of a LinearOpMode. This will allow
the program to inherit the proerties of LinearOpMode and will allow for DRY and very consistent
procedural decomposition without having to repeat code. It would also make code more organized. 
Adding on, the UML class diagram would be less cluttered and methds are easily identifiable.