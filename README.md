# Snake Game – COMPENG 2SH4 Course Project

This repository contains the final group project for COMPENG 2SH4 – Principles of Programming (Fall 2024, McMaster University). The project implements the classic Snake Game in C++ using object-oriented design (OOD) principles and the MacUILib library for console-based graphics and input. The project was completed as a two-person group assignment.

🎮 Game Overview:
The Snake Game follows the classic mode design:
- A snake head starts on the game board with length 1.
- A random food item spawns on the board.
- Using WASD controls, the player moves the snake.
- When the snake eats food:
  - The snake grows by +1 segment.
  - The score increases by 1.
  - A new food item spawns at a random empty location.
- If the snake collides with its own body → Game Over.
- The snake wraps around board boundaries (no hard walls).

🛠️ Features Implemented:
Core Game Mechanics:
- Input Handling – Non-blocking keyboard input using MacUILib_hasChar() and MacUILib_getChar().
- Board Rendering – ASCII grid with borders (#), snake body (*), and food (@).
- Snake Movement – Based on a finite-state machine (FSM), with support for wraparound at edges.
- Food Generation – Randomly generated at unoccupied cells.
- Scoring System – Tracks length-based score via snake body size.
- End-Game Condition – Triggered when the snake collides with itself.

Object-Oriented Design:
- objPos Class – Encapsulates an x-y coordinate and symbol.
- objPosArrayList Class – Custom array-based list for storing sequences of positions.
  - Used to represent the snake body as a dynamic list of segments.
- Player Class – Handles snake movement, growth, and collision detection.
- GameMechs Class – Manages input, game state (score, exit/lose flags), and board size.
- Food Handling – Integrated into the game mechanics (single food object).

Development Practices:
- Implemented Rule of Six / Minimum Four in classes to ensure safe memory handling.
- Followed incremental testing – validated objPos and objPosArrayList independently before integration.
- Verified memory management using platform-specific profilers (Valgrind / Dr. Memory).

👥 Team Notes
- This was a group project (2 members) completed for COMPENG 2SH4.
- All mandatory features were implemented and validated against the project rubric.

📜 Acknowledgements
Course: COMPENG 2SH4 – Principles of Programming (Fall 2024)
Instructor & TAs for providing skeleton code, MacUILib, and project guidance.
