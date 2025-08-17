# Quoridor Game – Embedded Implementation on LPC1768

This project is an embedded adaptation of the strategic board game *Quoridor*, developed for the LandTiger LPC1768 microcontroller board. The objective was to bring the mechanics of the original tabletop game into a fully autonomous system, running directly on hardware with no external software interface.

The implementation leverages the hardware capabilities of the LPC1768 board to create an interactive two-player experience, using real-time input handling, graphical output on an integrated display, and precise timing mechanisms to simulate gameplay dynamics in a constrained embedded environment.

---

## Project Overview

The game replicates the core logic of *Quoridor* on a 7×7 grid. Two players take turns moving pawns across the board, aiming to reach the opposite side while strategically placing barriers to delay their opponent. A key aspect of the game is balancing movement and obstruction without violating the rule that each player must always have at least one reachable path.

This embedded version runs entirely on the LPC1768 platform, responding to physical inputs and rendering the board state graphically in real time. Players interact through onboard buttons and a joystick, while the system enforces rules, tracks moves, and determines the winner autonomously.

---

## Key Features

- **Grid-Based Movement**: Players can move their pawn one tile per turn in horizontal or vertical directions, provided the move is not obstructed.
- **Barrier Mechanics**: Each player can place a limited number of barriers between tiles. Barriers cannot fully block an opponent's access to the goal.
- **Turn Management**: A timer is integrated into the system, limiting the duration of each turn. If time expires, the turn is automatically passed to the opponent.
- **Victory Detection**: The system continuously monitors each player's position and announces the winner as soon as the goal is reached.
- **Real-Time Interaction**: Input is processed immediately, and the interface updates the board state and player actions with minimal latency.

---

## Embedded Techniques

This project demonstrates the application of several embedded systems techniques, including:

- **Input Handling from Physical Devices**: Joystick and button inputs are captured and processed in real time to reflect user intentions and game commands.
- **Display Control**: The board and game state are rendered on the integrated GLCD display using low-level drawing routines optimized for responsiveness and clarity.
- **Interrupt-Driven Timing**: A countdown is managed through hardware timers and interrupt routines to enforce per-turn time limits and avoid polling delays.
- **Resource-Conscious Logic Design**: Game state and logic are managed using lightweight data representations, enabling full functionality within the memory constraints of the board.
- **Standalone Execution**: Once deployed, the game requires no PC connection or software debugging interface. All feedback is provided visually on the board.

---

## Application Context

This project was developed as a practical exercise in embedded system design, with a focus on combining user interaction, game logic, and hardware control into a cohesive and responsive application.

Beyond the game itself, the implementation demonstrates how interactive systems can be built on low-power microcontrollers with constrained computational resources, making it a useful prototype for developing interfaces, logic engines, or autonomous control systems in embedded environments.

