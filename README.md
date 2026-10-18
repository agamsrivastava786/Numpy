Tic-Tac-Toe Game Using NumPy and Streamlit

Project Overview: -

This project is an interactive, browser-based Tic-Tac-Toe game developed using **Python, NumPy, and Streamlit**. It demonstrates how Python programming and numerical computation can be combined with a lightweight web interface to create a functional game application.

The game features a 3×3 board where two players take turns placing X and O symbols. The application automatically checks the board after every move, identifies the winner, detects a draw, and allows players to restart the game.

Project Objective: -

The primary objective of this project is to develop a simple, interactive game while applying fundamental Python programming concepts and numerical computing techniques.

The project aims to: -

- Implement Tic-Tac-Toe game rules using Python.
- Use NumPy arrays to represent and process the game board.
- Apply conditional statements, loops, functions, list comprehension and logical operations to determine game outcomes.
- Build an interactive user interface using Streamlit.
- Manage game state across user interactions using Streamlit session state.
- Demonstrate how a Python application can be converted into a browser-based interactive experience.

Technologies Used: -

| Python | Core programming language and game logic |
| NumPy | Board representation and numerical calculations |
| Streamlit | Interactive web-based user interface |
| Git and GitHub | Version control and project hosting |

Methodology and Implementation

1. Game Board Initialization: -

The game board is represented using a 3×3 NumPy array initialized with zeros.

- `0` represents an empty cell.
- `1` represents player X.
- `-1` represents player O.

This numerical representation simplifies the process of checking winning conditions through array calculations.

2. Session State Management: -

Streamlit's session state is used to maintain the game information across application reruns.

The application maintains three main state variables:

- `board`: Stores the current state of the 3×3 game board.
- `current`: Identifies the player whose turn it is.
- `result`: Stores the game outcome, including a win or draw.

This approach allows the game to preserve previous moves when a player clicks a button.

3. Winning Condition Detection Using NumPy: -

A custom `check_winner()` function evaluates the board after each move.

The function uses:

Row-wise summation:** Checks whether any row sums to `3` or `-3`.
Column-wise summation:** Checks whether any column sums to `3` or `-3`.
Diagonal calculation:** Uses `np.trace()` and `np.fliplr()` to evaluate both diagonals.
Draw detection:** Checks whether all board positions have been occupied without a winner.

Because X is represented by `1` and O by `-1`, a completed winning line produces a sum of `3` for X or `-3` for O.

