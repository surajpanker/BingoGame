 BingoGame
 
Goal of this program: A bingo game must be simulated by creating a bingo card from a file with integers in it and playing the game of bingo. 


A correct sample input file for this program would be a list of 25 numbers that would be valid for a bingo card. 
	-Example: 1, 5, 7, 11, 14, 17, 19, 24, 27, 28, 33, 36, 37, 39, 44, 46, 49, 51, 57, 59, 62, 65, 66, 69, 71.


Algorithm Analysis and Methods:

-fillCard(String filename): I first need a method that takes a correctly formatted input file and places the integers in the list into a two-dimensional integer array. This array is then returned. 

-printCard(int[][] cardArray2D): I also need a method that, when called, displays the two-dimensional array that is given to it as a parameter in a correct format that represents a bingo card.

-playGame(): I also need a method that begins the game by calling other methods that simulate the game. 

-numberGenerator: This method is called with playGame() to generate a random number, check to see if it has already been called, and setting the bitset for that number to true once it finds one 
 that has not been called. It then checks to see if the number called is on the card, and sets the value of that position in the card to "0" if it is found. To check and see if a number was 
 already called, I used an instance of a bitSet and declared it as a global variable. If a number was called, the bitSet at that value was set to true. Every time a number was called, its
 bitSet value was checked, and if it were false, that implied that that number had not already been used.

-checkforWin(): This method is called by playGame() to check and see if the random number that was chosen caused a bingo. Loops for horizontal, vertical, and diagonal bingos are then used to check
 and see what type of bingo was obtained. If the sums any of the rows, columns, or diagonals were 0, then that implied that a bingo was obtained.

-checkHorizontalSum(): A method used to check the sums of the rows so that hard-coding sums was not necessary.

-checkVerticalSum(): A method used to check the sums of the columns so that hard-coding sums was not necessary.

-printCard(String[][] cardArray): I then realized I need to create a String version of the two dimensional integer type array of the bingo numbers so that the ones that were called could be converted
 to "X"'s instead of "0"'s. I made a second printCard method that takes a String type two dimensional array and displays it. Once a bingo was called, a loop used to check each value in the bingo card, 
 and changed all of the "0"'s that had occurred to "X"'s. 




Types and Size of Data Structures:

-Two 2D arrays were used (one of int type and one of String type) that were each [5][5]. (A bingo card has 5 rows and 5 columns)

-A bitSet was used of size (75). (75 different numbers could be called)

-An int array was used of size (75) for the numbers that were called. (75 different numbers could be called).

