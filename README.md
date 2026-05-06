# chess-engine-

This repository contains a custom built, end to end chess ecosystem including a Graphical User Interface (GUI), a Move Validator, and an AI Engine, all written in Python. The project demonstrates the application of classic game theory algorithms and heuristic-based evaluation.

The architecture of this chess engine is built on three pillars: robust state management, optimized search, and heuristic evaluation. At its core, an **8x8 matrix** tracks piece positions represented by unique integers and enforces standard rules including **castling, en passant, and promotion**. A **recursive validation system** ensures integrity by simulating moves to prevent any action that would leave the player's king in an illegal check.

The engine’s "brain" utilizes the **Minimax algorithm** to explore future move trees, optimized by **Alpha-Beta pruning** to discard inferior branches and deepen the search. This efficiency is further boosted by **move ordering**, which prioritizes captures and promotions to speed up the pruning process. 

Judgment is provided by an **evaluation module** that scores positions based on **material weighting** (e.g., Queen = 9, Pawn = 1) and **positional analysis**, rewarding center control while penalizing structural weaknesses like doubled pawns. Finally, it prioritizes **king safety** by encouraging castling and defensive positioning.


**KEY TIPS TO IMPLEMENT:**

1. Installation & Setup
   Prerequisites(any one)
   1. Python 3.x
   2. Pygame

~ Type the command "brew python install"
~ After installation type the command "pip install pygame"

2. Clone the Repo:

Type these commands in your PC's terminal:

1. git clone https://github.com/yashvaibhav012/chess-engine.git

2. Install Pygame: pip install pygame

3. Setup Assets: Ensure your piece images are in the root folder.

4. Run the python file separately in a dedicated terminal: python game.py.
   

**FUTURE IMPROVEMENTS**

To take this engine to the next level, improvements should focus on search depth, evaluation accuracy, and performance:

* **Search Optimizations**: Implementing a **Quiescence Search** will prevent the "horizon effect" by continuing to search until a position is stable. **Transposition Tables** can store previously evaluated positions to avoid redundant calculations.
* **Refined Evaluation**: Adding an **Opening Book** or **Endgame Tablebases** would allow the engine to play perfectly in the first and last phases of the game. Advanced scoring for **pawn structures** (like passed or isolated pawns) would improve its strategic judgment.
* **Technical Performance**: Switching from matrix-based boards to **Bitboards** would accelerate move generation through bitwise operations. Adding **UCI Protocol** support would make the engine compatible with professional chess interfaces.
* **User Experience**: Enhancing the GUI with **drag-and-drop** controls, move history in **Algebraic Notation**, and audio effects would create a more polished, professional feel.

These updates would transform a foundational Minimax engine into a sophisticated, competitive chess program.

