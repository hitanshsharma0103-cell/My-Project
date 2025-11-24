Project Development Report: Python Number Guessing Game

1. Executive Summary

The Python Number Guessing Game is a simple, command-line utility designed to provide an interactive, educational programming experience. The project successfully implements core Python concepts, including random number generation, iterative loops, and conditional logic, within a fun and engaging format. The primary goal was to create a functional, self-contained game that clearly demonstrates fundamental programming principles.

2. Project Objective

The main objectives of developing this game were:

To successfully utilize the random module in Python to select an unpredictable target number (between 1 and 100).

To implement a robust While loop structure that allows continuous user input until the correct answer is provided.

To use If/Elif/Else conditional statements to provide helpful feedback ("Bigger number please" or "Lesser number please") to the user.

To track and report the player's performance by counting the number of attempts taken to solve the puzzle.

3. Technical Implementation Details

The project is implemented in a single Python file, game.py.

3.1. Code Structure

The game's logic follows a straightforward sequence:

Initialization: The random.randint(1, 100) function is used to set the secret number (num). A counter variable (turns) is initialized to 0.

Game Loop: A while True loop initiates continuous execution.

Input and Conversion: The user is prompted to enter a guess, which is read as a string and immediately converted to an integer using int(input(...)).

Comparison and Feedback:

If guess == num, the game ends, and the success message is printed.

If guess < num, a hint ("Bigger number please") is given, and the turn counter is incremented.

If guess > num, a hint ("Lesser number please") is given, and the turn counter is incremented.

Conclusion: Once the loop breaks, the final turn count is displayed.

3.2. Key Code Snippet

The core logic revolves around the while loop:

turns = 0
while True:
    guess = int(input("Enter the guessed number = "))
    if (guess == num):
        # Successful Guess
        break
    elif (guess < num):
        # Hint for a larger number
        turns += 1
    elif (guess > num):
        # Hint for a smaller number
        turns += 1


4. Learning Outcomes

This project provided valuable experience in:

Modular Programming: Understanding and importing built-in Python modules (random).

Error Handling (Implicit): The game requires integer input, reinforcing the importance of type conversion (int()).

Algorithmic Thinking: The feedback mechanism encourages players to use efficient search strategies, typically a binary search approach (though the code does not enforce it).

User Experience (UX) at the Command Line: Providing clear, actionable messages to guide the user through the interaction.

5. Future Scope

Potential enhancements for future development could include:

Difficulty Settings: Allowing the user to select the range (e.g., 1-50, 1-1000).

Score Persistence: Implementing a high-score feature using file I/O to save the best turn counts.

Input Validation: Adding try-except blocks to handle non-integer input gracefully instead of crashing the program.