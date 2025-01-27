# Rock, Paper, Scissors Game

## Description

This is a simple implementation of the classic game **Rock, Paper, Scissors**, where:

- Player A always plays **Rock**.
- Player B plays randomly, either **Rock**, **Paper**, or **Scissors**.

The game is played for a total of **100 rounds**. After each round, the result is evaluated as one of the following:
- **WIN**: Player A wins the round.
- **LOSE**: Player B wins the round.
- **DRAW**: Both players play the same move, resulting in a draw.

The program keeps track of the number of wins for each player and the number of draws. At the end of the 100 rounds, the results are displayed.

### Game Rules
- **Rock** beats **Scissors**.
- **Scissors** beats **Paper**.
- **Paper** beats **Rock**.
- If both players make the same move, it's a **Draw**.

## Features

1. **Game Logic**:
    - The game logic is encapsulated in the `Game` class, which determines the outcome of each round.

2. **Random Player B**:
    - Player B's moves are selected randomly using a random number generator.

3. **Rock Player A**:
    - Player A always chooses **Rock**.

4. **Round Evaluation**:
    - The result of each round (win, loss, or draw) is determined by comparing Player A’s move (always **Rock**) with Player B's randomly chosen move.

5. **Final Results**:
    - After all 100 rounds, the program outputs the number of wins for each player and the total number of draws.

6. **Reproducibility**:
    - A fixed random generator is used during tests to ensure consistent results across runs. This is important for testing scenarios like large rounds or edge cases.

## Code Overview

### Classes and Enums

1. **Move Enum**:
    - The `Move` enum defines the possible moves for the players: **ROCK**, **PAPER**, and **SCISSORS**.
    - The `getRandomMove()` method is used to randomly select a move for Player B.

2. **Result Enum**:
    - The `Result` enum represents the possible outcomes of a round: **WIN**, **LOSE**, and **DRAW**.

3. **Game Class**:
    - The `Game` class contains the main logic for evaluating the round results.
    - The `play()` method compares the moves of Player A and Player B to determine the result of the round.

4. **Main Class**:
    - The `Main` class runs the game for 100 rounds and tracks the number of wins and draws for both players.
    - After all rounds are played, the final results are printed.

### Randomness Control for Testing

In the `Move` enum, the randomness can be controlled by setting a fixed `Random` object using the `setRandom()` method. This allows for reproducible tests, which is useful when testing edge cases or large numbers of rounds.

```java
public static void setRandom(Random newRandom) {
    random = newRandom;
}
```
How to Run

Clone the repository:


git clone <repository-url>

Build the project:

mvn clean install

Run the main class:

mvn exec:java -Dexec.mainClass="org.example.Main"

Run tests:

mvn test

Conclusion
This is a simple implementation of Rock, Paper, Scissors with a fixed player (Player A always plays Rock) and a random player (Player B chooses randomly). It includes basic game logic, test coverage, and handles edge cases like 0 rounds and large numbers of rounds. The code is designed to be simple, yet easily extendable and testable.







