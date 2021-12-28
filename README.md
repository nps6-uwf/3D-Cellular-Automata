# 3D-Cellular-Automata
A 3D cellular automata simulation synchronized with electronic music.  All of the code is contained within the main.html.

<p align="center">
<img src="https://github.com/nps6-uwf/3D-Cellular-Automata/blob/main/assets/screenshot.png?raw=true"></img>
</p>

The live website can be viewed here: <a href="https://nps6-uwf.github.io/3D-Cellular-Automata/main.html">3D Cellular Automata Simulation</a>.  

The grid size should be kept less than or equal to 20<i>x</i>20<i>x</i>20, you can set this by ajusting the grid size parameter in the menu.  No performance optimizations are used so this simulation is only suitable for smaller grids.  You can also adjust the fraction of cubes <i>alive</i>, this value should be a float between 0 and 1, note that a value of 0 will kill all of the cubes.  You can also adjust the cube size, you may also need to adjust the cube spacing, if you make the cubes too big and they start to overlap strange behavior can occur.  You can change the background color to a solid rgb color, make sure the format remains consistent to what is preset in the text input.  If you let the simulation run you will notice the background is a pulsing radial gradient, setting the background color will only change the center of the radial gradient.  If you want to get rid of the radial gradient you can modify the code.  The rotational velocity dictates how fast the cube rotates in the x & y directions, by default this is set to be a function of the song's frequency, so if you want full control, use the pause button in the settings menu.

The update rules of the automata are governed by two sets, rule 1 and rule 2.  I have called rule 1 the <b>survival</b> criterion, any cube with <i>n</i> neighbors where <i>n</i> is also a member of rule 1 will survive to a future generation, all other live cubes will die.  Rule 2 is the <b>Rebirth</b> criterion, any dead cube with <i>m</i> neighbors where <i>m</i> is also a member of rule 2 will be reborn.  There are two neighborhood functions that I have defined, you have full control to select which neighborhood to run your simulation.  The standard neighborhood only considers cubes the border one of the cubes 6 faces to be a neighbor.  The extended neighborhood, considers all 26 cubes surrounding a single cube a neighbor.  The simulation speed, is how fast the updates are applied to the 3D grid of cubes.  The spatial oscillation checkbox refers to the dynamic change in inter-cube spacing, you can make this feature more pronounced by setting the javaScript variables <i>upperOscLimit</i> & <i>lowerOscLimit</i>.






