# **Electronics**
### Power Distribution Modules
There are two different types of power distribution modules, or the main thing that distributes the software.
There is the REV one (REV Expansion Hub), and the modern robotics one (Core Power Distribution Module).
The REV one have the wiring ports of motors, sensors, servos, etc. all one the same board, also it has 4 motor ports.
The modern robtics one distributes it to many different other modules.
The other modules includes motor controller, servo controller, device interface, and the legacy module.
The motor controller have 2 motor ports, the servo controller and device interface have a lot.

REV Expansion Hub:
![REV](https://raw.githubusercontent.com/ftccats/ftccats.github.io/master/REVHub.png)

Core Power Distribution Module:
![PowerDistribution](https://raw.githubusercontent.com/ftccats/ftccats.github.io/master/CorePowerDistribution.png)

Learn about basic Core Power Distribution Module Wiring:
[Wiring Modern Robotics Power Distribution Module](https://www.youtube.com/watch?v=lbeAefQTZXQ)

### General Wiring Tips
* If something is not working, make sure when you configure the robot, you set the correct ports to the correct things.
* Make sure the wires are plugged in correctly and not loose, correctly means the color to itself. As in red to red, black to black, etc. Also, white sometimes goes to yellow.
* Label your wires, label both ends the same thing, preferably what you named it in the program.

If REV Expansion Hub does not have enough ports for your robot, you can connect both of them together!

How to connect them:
[Connecting REV Hubs](https://www.youtube.com/watch?v=7rbLDden-Rs)

### SRS programmer
The SRS programmer is a device that can limit the movement of a Smart Robot Servo.

Some of its features are:
* 3 programming modes
1. Continuous rotation
2. Angular limits
3. Reset to factory defaults
* Test modes
1. Automatic sweep:  Press the test button once
2. Manual position/direction: Press the test button twice
3. Return to default: Press the test button three times
There is a switch at the top, it is either c with stands for continuous, s stands for servo, or the range right now.
![SRSProgrammer](https://raw.githubusercontent.com/ftccats/ftccats.github.io/master/SRSProgrammer.jpeg)

To change the range follow these steps:
1. Connect the servo to the programmer
2. Turn the programmer on and put it on servo mode, s on the top switch
3. Manually rotate the servo to the wanted most left position, then press and release the left button, the left LED will illuminate if the poisition is valid
4. Repeat step 3 for the desired right position
5. After both LED lights of right and left have both illuminated once, press and release the program button. If the program LED blinks and then stays on, it indicates you successfully changed the servo range.

For more information on the SRS Programmer, click [here](http://www.revrobotics.com/content/docs/REV-31-1108-UM.pdf)
