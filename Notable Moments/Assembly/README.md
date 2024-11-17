## Assmbley and Machine Structures

While pursuing my Bachelor's Degree, I also indulged in some Assembly projects in order to:

- Efficiently translate C/C++ code into assembly language.
- Perform simple optimizations by hand.
- Trace and debug at the assembly level.
- Understand and extend simple CPU implementations.
- Understand basic interrupt/exception handling.
- Make simple performance estimates for assembly code.

The provided project here is based upon the C++ code that is given on: https://onlinegdb.com/IXVUtL6lU

This project atims to translate the C++ code into Assembly in order to implement a game where a human user tries to escape four robots. The robots will attempt to get closer to the human. When a robot has the same x-y coordinates as the human, the game is over. Two arrays x[4] and y[4] keep track of the x and y coordinates of the four robots. The positions of the human and the four robots are initialized in the program. On each step, when the user enters a move, the positions of the human and the robots are updated. This continues until the human dies.

In the main loop, the user is prompted to enter a move. Once this happens, the program calls the function **moveRobots()** in order to update the position of the robots as they try to catch the human. arg0 is the base address of the array that contains the x coordinates of the four robots. arg1 is the base address of the array that contains the y coordinates of the robots. arg2 is the x coordinate of the human, and arg3 is the y coordinate of the human.

**moveRobots()** updates the positions of the four robots, and returns 1 if the human is alive, and a 0 if the human is head. Each coordinate of a robot is updated by calling the function **getNew()**, which returns the new coordinate baed on the current coordinate of the robot and the current coordinate of the human. The function **getNew()** uses simple rules to move a robot closer to the human. If the difference in the coordinates is >= 10, the robot's coordinate will move 10 units closer to the human. If the difference in the coordinates is < 10, the robot's coordinate will move one unit closer to the human.

The pdf file contains my translation and implementation of this task.
