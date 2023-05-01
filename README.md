Download Link: https://assignmentchef.com/product/solved-cs211-project7-dungeon-crawler
<br>



In this project you will be creating a dungeon crawler game. In this program you will have a player character that will move from room to room in the dungeon collecting chests and accumulating gold. The objective is to have the character accumulate the maximum amount of gold and exit the dungeon. Once you exit a room you cannot return to said room.

Controls

You will have a character that moves using the ‘w’,’a’,’s’, and ’d’ keys. You will go through the dungeon collecting chests until you reach an exit or hit the ‘q’ button to quit the game.

<h2>Class Break Down</h2>




For this assignment you will be writing a C++ Program that will contain the following classes:

<ol>

 <li>Tile Class

  <ol>

   <li>Chest Class</li>

   <li>Door Class</li>

   <li>Wall Class</li>

  </ol></li>

 <li>Room Class</li>

 <li>Player Class</li>

</ol>




For the purposes of this assignment the classes and interfaces are defined below, along with the basic interactions.

<ol>

 <li>The <strong>Tile Class </strong>is a class that contains abstract methods, the purpose of this class is to create a common access class that the player can interact with, without knowing whether they are dealing with a Wall, a Tile, a Chest or a Door. The tile itself will be the parent.</li>

</ol>




<ol>

 <li>The generic tile is the floor that the player stands on. This role is not interactive aside from the player’s ability to stand on it.</li>

 <li>The wall tile is a barrier, when the player reaches the edge of the M*N matrix (rows 0 and M, columns 0 and N) the player will be placed back on the tile from the previous move.</li>

 <li>The chest tile is a tile that when found will contain a number. This number will be added to the score.</li>

 <li>There will be a defined number of doors.</li>

 <li><strong>Inheritance</strong> will be required to be used for these tiles, as the M*N matrix will only be defined as a Tiles matrix</li>

 <li>It will also have a data member for if the player is on that tile</li>

</ol>













<ol start="2">

 <li>The <strong>Room</strong> will contain a N*M matrix of Tiles (This is a dynamic matrix similar to Project 3)</li>

</ol>




<ol>

 <li>The N*M matrix will have its size determined by the input file and have a border added to it (1 space wide, see earlier maze project) b. This class will contain N*M Matrix of Tiles</li>

</ol>




<ol>

 <li>The matrix will contain a number of doors that will be placed according to the input</li>

</ol>

file

<ol>

 <li>The Matrix will contain some number of chests as defined in the input file</li>

</ol>




<ol start="3">

 <li>The <strong>User interface</strong> will process the commands given by the User and will interact with the rooms, determining what actions will be taken and keeping track of the player’s current location in the Dungeon (filename) and in the room (x,y coordinates).</li>

</ol>




<ol>

 <li>The command F: used to find a path to a door using DFS</li>

 <li>The WASD keys: used to send the player to a new tile adjacent to current tile.</li>

 <li>The H key: used to remind the player of the commands and what characters represent which tile types.</li>

 <li>The G key: used to print the score</li>

</ol>




<ol start="4">

 <li>The <strong>Player</strong> Class will contain the following items</li>

</ol>




<ol>

 <li>A value in which to store the amount of gold collected</li>

 <li>The number of tiles visited</li>

 <li>Current x,y location</li>

</ol>




<h2>Program Commands</h2>




You have to read the user’s input keys and execute proper actions. Project 6 should help you set up the process of reading user input from standard input.




<table width="623">

 <tbody>

  <tr>

   <td width="86"><strong>Q</strong></td>

   <td width="536">Exit the program</td>

  </tr>

  <tr>

   <td width="86"><strong>W</strong></td>

   <td width="536">Your Player will move to the neighboring tile above. If the current position is (x , y) after reading “W” key input, you should move the player to neighboring tile at position (x, y-1).</td>

  </tr>

  <tr>

   <td width="86"><strong>A</strong></td>

   <td width="536">Your Player will move to the neighboring left tile. If the current position is (x , y) after reading “A” key input, you should move the player to neighboring tile at position (x-1, y).</td>

  </tr>

  <tr>

   <td width="86"><strong>S</strong></td>

   <td width="536">Your Player will move to the neighboring tile below. If the current position is (x , y) after reading “S” key input, you should move the player to neighboring tile at position (x, y+1).</td>

  </tr>

  <tr>

   <td width="86"><strong>D</strong></td>

   <td width="536">Your Player will move to the neighboring right tile. If the current position is (x , y) after reading “D” key input, you should move the player to neighboring tile at position (x+1, y).</td>

  </tr>

  <tr>

   <td width="86"><strong>H</strong></td>

   <td width="536">Print a list of all available commands</td>

  </tr>

  <tr>

   <td width="86"><strong>G</strong></td>

   <td width="536">Print Player’s score</td>

  </tr>

  <tr>

   <td width="86"><strong>F</strong></td>

   <td width="536">Find a path to a door using DFS and print the path</td>

  </tr>

  <tr>

   <td width="86"><strong>B </strong><strong>(Optional)</strong></td>

   <td width="536">Find the Shortest path to the nearest door using BFS and print the path</td>

  </tr>

 </tbody>

</table>




<h2>Program Input (your maze project will be helpful)</h2>




Your input file will be formatted in the following format:

X Y (size X by Y)

S X Y (Start location of person)

O X Y (List of obstacles)

<ul>

 <li>X Y Point_Value (chests)</li>

 <li>X Y “filename.txt”(Doors see project 6)</li>

 <li>X Y (Dungeon Exit, will only be in 1 file)</li>

</ul>




You will be required to write a .txt which contains your own custom room design. It will be called “Room5.txt” This room will also contain your dungeon’s exit.




<strong>Display/Output </strong>




A sample room <strong>CAN </strong>look like this (we are not binding you to these ascii characters, but please make sure it’s obvious what everything is:

********************

*P                       *

*****************   *

<ul>

 <li>*</li>

 <li>****************</li>

 <li>* *</li>

 <li>C *    * D     *</li>

</ul>

********************




At the end of the game you will print out the number of gold coins collected.




<h2>Multiple Source Code Files</h2>




Your program is to be written using at least two source code files. One of the source file files is to contain the main function of the program named in a file using your net-id and Program name, like:

net-idProj7.cpp

You must have at least one file for each of the classes listed above and 1 for the file that will contain your main.

You will also be required to create your own text file for a room. This should be called “Room5.txt”




The above implies that you will need to write any appropriate .h file(s) and a makefile.




<h2>Coding Style</h2>




Don’t forget to use good coding style when writing your program.  Good coding style makes your program easier to be read by other people as the compiler ignores these parts/differences in your code.

<strong>Elements of good code style include (but may not be limited to):</strong>

<ul>

 <li>Meaningful variable names</li>

 <li>Use of functions/methods</li>

 <li>Proper indentation</li>

 <li>Use of blank lines between code sections</li>

 <li>In-line comments</li>

 <li>Function/method header comments</li>

 <li>File header comments</li>

</ul>

The Code Review Checklist also hints at other elements of good coding style.


