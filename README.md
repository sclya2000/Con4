# Con4
I implemented a traditional version of Connect Four, with the added features that the players 
can undo their moves as well as save and return to the game. The game is made up of multiple classes. GameObj contains
the basic information of a possible object in the game. Chip represents a chip in the game. Each slot on the game board is
represented by a chip. The Chip contains its location on the board as well as its color which determines its identity. White Chips
are "empty" slots on the board, Red chips are for the Red player, and Blue Chips are for the Blue player. GameVisual
holds the code for drawing and displaying the board and the chips. It also contains the methods for checking if a player's 
move gives them four chips in a row. The GameBoard class holds the primary game logic for how different objects interact with 
one another. Game is the class that specifies the frame and widgets of the GUI.

2D Arrays:
I used a 2D array of Chip objects that I created that stores the information of each Chip. The structure of the game is the
2D array which represents the Connect Four board. Each Chip contains a different Color that identifies it as 
either "empty" slot (White Chip), Red player, or Blue player. When the game starts, all of the Chips in the board are white to 
represent an empty board. 

Collections: 
I stored each move that occurs during a game in a collection in order in a LinkedList since I will 
only need to add/remove from the head of the list. The LinkedList is of type String which contains the 
coordinate of each slot, so that when a player wants to undo their last move, the slot that they had previously 
dropped a chip in will be set back to White which represents an empty slot. When a user needs to undo, it will 
remove the last move from the list and revert that Chip back to an "empty" state. 

File I/O: 
I stored the state of the game so that the users can pause or exit the game if the user chooses to. 
The information of the current turn as well as the state of the game is stored in a text file, and when 
the user wants to resume the game, the information from the text file is read, translated, and displayed. 
The file contains the information that represents the user whose turn it is as well
as the board with all of the chips in the position it was saved in. 

Testable Component:
The main state of my game is the board (2D array). I have methods that take in coordinates as a parameter, 
and checks if adding a chip at that location allows a player to win or not. I also tested if the color of Chips were updating
correctly. 
