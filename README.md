Download Link: https://assignmentchef.com/product/solved-c-program-to-play-a-simplified-version-of-the-amazeing-labyrinth
<br>
The purpose of this programming project is to write a C++ program to play a simplified version of The aMAZEing Labyrinth. This is a competitive tile shifting game, in which two players take turns sliding tiles into perpendicular lanes on the board. In our case one of the players is the computer plays random moves. The tiles have vertical lines, horizontal lines, or crosses on them. The goal is for one player to create a continuous path in one of the lanes using the lines in the tiles from their side of the board to the opposite side. The first player to do so wins.

REQUIREMENTS:

<ul>

 <li>You must organize your program into three files: o euidHW4func.h This file will contain the include directives for the necessary libraries, any enumerated data types, any type definitions, any structure definitions, and the list of function prototypes (i.e. function declarations) o euidHW4main.cpp This file will contain the local include directive for the header file as well as the main function for the program o euidHW4func.cpp This file will contain the local include directive for the header file as well as all function definitions (except the main) used in the program o Be sure to replace euid with your EUID</li>

 <li>As with all homework programs in this course, your program’s output will initially display the department and course number, your name, your EUID, and your email address.</li>

 <li>Define an enumerated type to store the different tile types that can be on the board: o + CROSS o – HORIZONTAL o | VERTICAL o X LOCKED o EMPTY</li>

 <li>Define an enumerated type that represents two colors, RED and BLUE. This will keep track of each player’s game pieces.</li>

 <li>Define a structure (i.e. struct) to represent a tile that contains the tile’s enumerated type, its enumerated color, and an integer value representing which lane it is in.</li>

 <li>Inside the main(), you will need to declare a two-dimensional, dynamic array representing the 7-by-7 board the tiles will be placed in</li>

 <li>To initialize the board, you will need to define a function that takes in the two-dimensional board and its size. Remember that the size should not be a global constant, so you will need to use pointers for the array. o The function will need to prompt the user for the name of the file containing the initial state of the board. This file will be a text file in comma separated value (CSV) format with each line representing one row on the board. If an incorrect file name is entered, the program should reprompt the user for a correct file name until one is received. o Using the information in the file, the board should be populated with tiles matching those described in the file. Keep in mind that an X is a LOCKED tile and cannot be moved during the game, and a ‘ ‘ is an EMPTY slot that does not currently contain a tile. o Examples of these input files can be found on the CSE machines at /home/jeh0289/public/csce1030/fa18/project4 You can cd directly into this directory and cp the files into your home directory for easy access.</li>

 <li>You will then need to print out the game instructions using a function you have defined. See the SAMPLE OUTPUT for an example of the instructions.</li>

 <li>Next you should begin the game</li>

</ul>

o At the beginning of each turn you should print out the state of the board using a function you have defined that takes in the two-dimensional board and its size. The player’s tiles should be colored red, the computer’s tiles should be colored blue, and the LOCKED tiles should be the default color. See printColor.cpp for an example on how to color your text.

o You will then need to prompt the user for which of the lanes 1-7 they would like to push a tile into and what type of tile they would like to push (-,|, or+). If the user inputs a lane that does not exist or a symbol that is not a possible tile type, politely inform them of the mistake and reprompt. You should also give them the option of surrendering by entering -1, a sentinel value, when asked for the lane number.

If a user surrenders then output a polite message and end the game. o Using the user’s specifications, you should create a new tile and then attempt to slide the tile into the board using a function you have defined. This function should take in the board, its size, and the new tile. To slide a tile for the player, you should slide it vertically from the bottom of the board in the appropriate lane. If a tile already exists in that spot, it and all other movable tiles above it that are touching should be moved up. A tile that slides out of the board’s boundaries is removed from the board. Note that a tile cannot be slid into a LOCKED tile.

If a player attempts to slide a tile into a lane that would result in a LOCKED tile being moved, you should ignored the move, politely report the mistake the player, and forfeit their current turn. o Using a function you define, you should create a tile for which the computer should choose a random lane and tile type.

This tile should be slid in horizontally from the left side of the board using your previously defined tile sliding function. If the computer attempts to slide a tile into a lane that would result in a LOCKED tile being moved, you should ignored the move, politely report the computer’s mistake to the player, and forfeit the computer’s current turn. o The game should continue until either the player or computer has created a continuous path in one of the lanes using the lines in the tiles from their side of the board to the opposite side.

You should check for this using a function that takes in the board and its size, and return a Boolean. The final state of the board should be displayed along with congratulatory message if the user won, or a consoling message about their defeat.

<ul>

 <li>Once the game is complete, you will need to return the memory allocated for the board back to the freestore.</li>

 <li>Your code should be well documented in terms of comments. For example, good comments in general consist of a header (with your name, course section, date, and brief description), comments for each variable, commented blocks of code, and function header comments.</li>

 <li>You may create your own input files defining the board, but they must be created on the CSE machines. Failure to do so may result in a program that works on your personal computer, but not on the files we will use to test it on the CSE machines.</li>

 <li>Your program will be graded based largely on whether it works correctly on the CSE machines (e.g., cse01, cse02, …, cse06), so you should make sure that your program compiles and runs on a CSE machine.</li>

 <li>You should contact your instructor if there is any question about what is being asked for.</li>

 <li>This is an individual programming assignment that must be the sole work of the individual student. Any instance of academic dishonesty will result in a grade of “F” for the course, along with a report filed into the Academic Integrity Database. You may assume that all input will be of the appropriate data type, although the range (e.g., an integer) may be out of bounds of the region. Please pay attention to the SAMPLE OUTPUT for specific details about the flow and input/output of the program. You shall use techniques and concepts discussed in class – you are not to use global variables, goto statements, or other items specifically not recommended in this class.</li>

</ul>