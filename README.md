# TIC TAC TOE
### Logic Used in the Tic-Tac-Toe Game Code
1. Define Constants
   - The code defines constants to represent the players and the board:
     - `COMPUTER = 1` 
     - `HUMAN = 2`
     - `SIDE = 3` (for a 3x3 board)
     - `COMPUTERMOVE = 'O'` 
     - `HUMANMOVE = 'X'`

2. Display the Board
   - The function `showBoard` prints the current state of the board. It uses formatted print statements to display the board in a 3x3 grid.

3. Show Instructions
   - The function `showInstructions` provides a guide to the player on how to choose a cell by showing which number corresponds to which cell.

4. Initialize the Board
   - The function `initialise` sets all cells in the board array to be empty (' ').

5. Announce the Winner
   - The function `declareWinner` takes a player (either COMPUTER or HUMAN) and prints a message indicating who won the game.

6. Check for Row Win
   - The function `rowCrossed` checks each row to see if all cells in a row are occupied by the same player's move and are not empty. If any row is completed, it returns true.

7. Check for Column Win
   - The function `columnCrossed` checks each column to see if all cells in a column are occupied by the same player's move and are not empty. If any column is completed, it returns true.

8. Check for Diagonal Win
   - The function `diagonalCrossed` checks both diagonals to see if all cells in a diagonal are occupied by the same player's move and are not empty. If any diagonal is completed, it returns true.

9. Check if the Game is Over
   - The function `gameOver` returns true if any row, column, or diagonal is completed by the same player's move.

10. Minimax Algorithm for Optimal Move Calculation
    - The function `minimax` uses the minimax algorithm to evaluate all possible moves and returns the best score for the computer. It:
      - Checks if the game is over and returns +1 for a human win, -1 for a computer win, or 0 for a draw.
      - Recursively evaluates each possible move, switching between the human and computer players, and calculates the best score based on whether the current move is for the computer or the human.

11. Calculate the Best Move for the Computer
    - The function `bestMove` iterates over all cells to find the best possible move for the computer by using the `minimax` function. It returns the index of the best move.

12. Play the Game
    - The function `playTicTacToe` handles the gameplay:
      - Initializes the board and shows instructions.
      - Enters a loop that continues until the game is over or the board is full:
        - If it's the computer's turn:
          - Uses `bestMove` to find the best move.
          - Updates the board with the computer's move.
          - Displays the board.
          - Switches to the human's turn.
        - If it's the human's turn:
          - Shows available positions.
          - Reads the human's move.
          - Validates and updates the board if the move is valid.
          - Displays the board.
          - Switches to the computer's turn.
      - After the loop, if the game is a draw, it prints "It's a draw". Otherwise, it announces the winner.

13. Main Function to Start the Game
    - The `main` function starts the game:
      - Prints the game title.
      - Asks the player if they want to go first.
      - Starts the game by calling `playTicTacToe` with the appropriate starting player.
      - Repeats the game until the player decides to quit.

