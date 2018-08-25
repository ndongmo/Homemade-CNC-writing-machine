# Homemade CNC writing machine
DIY project which consists of the construction and the implementation of a CNC plotter using old DVD writers. The final plotting machine consists of three axes. The x-axis and y-axis work together to draw a 2D image or text on the paper. While the z-axis is used to lift and lower the pen onto the paper.

## Hardware Requirements
1. Servo motor
2. Two step motors (from old DVD/CD drives)
3. Motor shield L293D
2. Arduino Uno board
3. Jumper cables and connectors
4. USB 2.0 cable to connect Arduino to PC
5. Power supply. We use 6-12V power supply with 1000 mA peak current ([see Ardafruit tutorial on powering motor shield](https://learn.adafruit.com/adafruit-motor-shield-v2-for-arduino/powering-motors))
6.  Screws and nuts
7. Cables
8. Pen holder. We use a chewing gum box, but you can use anything else which is able to lift and lower the pen

## Software Requirements
1. Arduino IDE
2. Processing IDE
3. Inkscape (optional)
4. GCTRL processing program from [Damellis](https://github.com/damellis/gctrl/blob/master/gctrl.pde). It is used to send G-Code data to Arduino

## Hardware tasks
* Dismantle the two DVD-DRIVES and obtain the step motors from them.
* Prepare the platform for mounting the step motors and the servo. It should consists of two planes, one horizontal and one vertical and they are perpendicular to each other. 
* Install the pen holder that is used to attach the pen to the vertical plan. 
* Install the surface on which we can mount the paper.
* Wiring the steps motors and servo to the motor shield and then connecting the motor shield to the arduino board.

<img src="https://github.com/ndongmo/Homemade-CNC-writing-machine/blob/master/designer_bb.png" width="450" height="300" />

## Software task
The software task is some codes written in the Arduino IDE to control the operation of the microcontroller. Our code is based on [Adidax code source](https://github.com/adidax/mini_cnc_plotter_firmware)

## How to use 
1. Connect Arduino and PC via the USB cable
2. Plug in the power supply to the Arduino DC jack
3. Install the paper on the platform
4. You will need a G-Code file describing the pattern to draw. You can create it yourself or you can use **inkscape** with gcodetools extension from [cnc-club](https://github.com/cnc-club/gcodetools) to generate the G-Code file
5. Open the G-Code file and change pen up and pen down lines
   * 'G00 Z........' by 'M300 S30'
   * 'G01 Z........ F100.0(Penetrate)' by 'M300 S50'
6. Start GCTRL processing program, press 'g' for file selection option and select your G-Code file. **NB \:** we configure GCTRL with the portname = "COM7", you may need to change it in case your arduino is using another port

## Final product
<img src="https://github.com/ndongmo/Homemade-CNC-writing-machine/blob/master/img_1.jpg" width="450" height="600" align="left" />
<img src="https://github.com/ndongmo/Homemade-CNC-writing-machine/blob/master/img_2.jpg" width="450" height="600" align="left" />
<img src="https://github.com/ndongmo/Homemade-CNC-writing-machine/blob/master/img_3.jpg" width="450" height="600" align="right" />
<img src="https://github.com/ndongmo/Homemade-CNC-writing-machine/blob/master/img_4.jpg" width="450" height="600" align="right" />
