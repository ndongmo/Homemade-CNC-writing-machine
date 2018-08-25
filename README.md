# Homemade CNC writing machine
DIY project which consists of the construction and the implementation of a CNC plotter using old DVD writers. The final plotting machine consists of three axes. The x-axis and y-axis work together to draw a 2D image on the paper. While the z-axis is used to lift and lower the pen onto the paper.

## Hardware Constraints:
1.   The paper size that we can draw on is limited by the coverage that our two step motors (taken from DVD) are able to cover which is 5cm. So the maximum area that we can cover is 5cmx5cm
2.   The speed of drawing is limited to the speed of the stepper motors (in steps per revolution)
3.   We need the system to be connected to an external computer/laptop because it can’t operate alone

## Software Constraints
1. Micro-controller has a limited memory so it is not possible to store complex drawings on it
2. We have assumed that each line of G-Code will be limited to 512 characters which is something that can be changed easily in the code as a constant.
3. We have to use an external program like inkscape to generate the G-code and we alo need GCTRL processing program from [Damellis](https://github.com/damellis/gctrl/blob/master/gctrl.pde) to send the G-Code to arduino.
