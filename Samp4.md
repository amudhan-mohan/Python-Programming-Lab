Theoretical Concepts:
1. Importing Tkinter and Creating a Main Application Window:
Concept: Tkinter is the standard GUI toolkit for Python. It provides a set of tools for building desktop applications with graphical interfaces.

Syntax:
import tkinter as tk
root = tk.Tk()
In this Code:

'import tkinter as tk' imports the Tkinter module and aliases it as 'tk'.
'tk.Tk()' creates the main application window.

2. Creating a Grid Layout:
Concept: To display the Tic-Tac-Toe board, we can use a grid layout in Tkinter. Each cell in the grid can be a button where players can make their moves.

Syntax:
button1 = tk.Button(root, text='', command=lambda: make_move(0, 0))
button1.grid(row=0, column=0)
In this Code:

'tk.Button(root, text='', command=lambda: make_move(0, 0))' creates a button widget with empty text and binds it to a command (function) that makes a move at position (0, 0).
'button1.grid(row=0, column=0)' places the button in the grid layout at row 0, column 0.

3. Game Logic:
Concept: Implementing the game logic involves tracking the state of the board, validating moves, and checking for winning conditions or a draw.

Syntax:
def check_winner():
    # Check rows, columns, and diagonals for winning combinations

def make_move(row, col):
    # Update the board state and check for winner or draw

def reset_game():
    # Reset the board and game state

In this code:

'check_winner()' function checks for winning combinations in rows, columns, and diagonals.
'make_move(row, col)' function updates the board state with the player's move at a specified position and checks for a winner or draw.
'reset_game()' function resets the board and game state.

4. Displaying Game Results:
Concept: After each move, the program should check for a winning condition or a draw and display the result on the GUI.

Syntax:
result_label = tk.Label(root, text='')
result_label.grid(row=4, columnspan=3)

def display_result(result):
    result_label.config(text=result)
In this code:

'tk.Label(root, text='')' creates a label widget with empty text.
'result_label.grid(row=4, columnspan=3)' places the label in the grid layout at row 4, spanning across 3 columns.
'display_result(result)' function updates the label text to display the game result.

5. Main Loop:
Concept: The main loop of the Tkinter application continuously listens for events and updates the GUI accordingly.

Syntax:  
root.mainloop()
In this code:

'root.mainloop()' starts the Tkinter main loop, which listens for events (such as button clicks) and updates the GUI accordingly.

Aim:
To create a Python program using Tkinter for a two-player Tic-Tac-Toe game.

Algorithm:
1. Import the necessary modules: tkinter and messagebox.
2. Define a class TicTacToe to represent the game.
3. Initialize the game attributes such as the Tkinter root window, current player, game board, and buttons grid in the constructor (__init__ method).
4. Create a method create_board() to generate the game board with buttons.
5. Implement the make_move() method to handle player moves, update the board, and check for a winner or draw.
6. Define the check_winner() method to verify winning conditions by checking rows, columns, and diagonals.
7. Implement highlight_winner() method to visually highlight the winning combination on the GUI.
8. Implement check_draw() method to check for a draw condition.
9. Define end_game() method to display the result (winner or draw) using a messagebox and quit the game.
10. Add a play() method to start the main event loop using root.mainloop().
11. In the main block, create an instance of TicTacToe, and call its play() method to start the game loop.

Result:
Thus the Python program using Tkinter for a two-player Tic-Tac-Toe game has been executed successfully.



