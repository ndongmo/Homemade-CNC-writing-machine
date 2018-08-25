# Homemade CNC writing machine
DIY project which consists of the construction and the implementation of a CNC plotter using old DVD writers. The final plotting machine consists of three axes. The x-axis and y-axis work together to draw a 2D image on the paper. While the z-axis is used to lift and lower the pen onto the paper.

## Hardware Requirements
1. Servo motor
2. Two step motors (from old DVD/CD drives)
3. Motor shield L293D
2. Arduino Uno board
3. Jumper cables and connectors
4. USB 2.0 cable to connect Arduino to PC
5. Power supply. We use 6-12V power supply with 1000 mA peak current ([see Ardafruit tutorial on powering motor shield](https://learn.adafruit.com/adafruit-motor-shield-v2-for-arduino/powering-motors))
6.  Screws and nuts. 
7. Cables

## Software Requirements
1. Arduino IDE
2. Processing IDE
3. Inkscape (optional)
4. GCTRL processing program from [Damellis](https://github.com/damellis/gctrl/blob/master/gctrl.pde). It is used to send G-Code data to Arduino
