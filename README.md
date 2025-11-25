# Mancala AI Agent

This project implements an AI player for the classic board game **Mancala**, using search algorithms to choose strong moves. The AI was developed, tested, and analyzed in **Jupyter Notebook**, making it easy to visualize gameplay, run experiments, and compare performance across algorithms.

---

## 🎯 Overview

## 🎯 Overview

This project builds an intelligent Mancala-playing agent using the **AIMA (Artificial Intelligence: A Modern Approach) game framework**, which provides the foundational abstractions for adversarial search. The files **`games.py`** and **`utils.py`** used in this project come directly from the official AIMA Python repository and serve as the base for game state handling, search logic, and utility functions.

On top of the AIMA framework, this project implements custom Mancala game mechanics, a utility function, and AI agents using **Minimax** and **Alpha-Beta pruning** with configurable search depth. All simulations and performance experiments were run in **Jupyter Notebook**, making it easy to visualize results, compare algorithms, and analyze win rates across different depths and strategies.

The goal of the project is to design an intelligent Mancala agent that can consistently outperform a random player.  
To achieve this, the project integrates:

- A full Mancala game implementation  
- Minimax search  
- Alpha-Beta pruning  
- Evaluation functions  
- Runtime and win-rate comparisons  
- Experimentation tools inside Jupyter Notebook  

This project was created as part of exploring game AI, adversarial search, and decision-making strategies.

---

## 🕹 Features

- Complete playable Mancala game engine
- AI agent using:
  - Minimax  
  - Alpha-Beta Pruning  
- Adjustable search depth (plies)
- Utility/evaluation function based on score difference
- Random player for benchmarking
- Includes:
  - Win-rate experiments  
  - Runtime comparisons  
  - Analysis of plies vs performance  
- All experiments and results run directly inside **Jupyter Notebook**


## Key Findings (from experiments)

### Minimax AI vs Random (Depth 5)
- **AI win rate:** ~97%  
- **Random win rate:** ~3%  
- **Average turns per game:** 25–30  
- **Typical moves:**  
  - AI: ~15 moves  
  - Random: ~16 moves  
- **Conclusion:** AI is *significantly* better than random, because it searches ahead and chooses optimal actions using an evaluation function.

### Alpha-Beta AI vs Random (Depth 5)
- **Average time per game:** ~0.0722 seconds  
- **Time for 100 games:** ~10 seconds  
- **Win rates:**  
  - AI: ~97%  
  - Random: ~3%  
- **Turns per game:** identical to minimax (25–30 turns)  
- **Observation:** Behavior is nearly identical to Minimax because Alpha-Beta is the same algorithm with skipped branches, not different logic.  
*(PDF source: Page 1–2 of Course Project Questions.pdf)* :contentReference[oaicite:0]{index=0}

### Alpha-Beta AI vs Random (Depth 10)
- **Average time per game:** ~0.1604 seconds  
- **Time for 100 games:** ~8 seconds  
- **Win rates:**  
  - AI: ~98%  
  - Random: ~2%  
- **Shows:** Increasing plies gives a *very tiny* win-rate improvement.

### Performance Comparison: Minimax vs Alpha-Beta
- **Minimax (5 plies):** ~34 seconds per 100 games  
- **Alpha-Beta (5 plies):** ~10 seconds per 100 games  
- **Speedup:** ~24 seconds faster (Alpha-Beta ~3.4× faster)  
- **Projected Minimax (10 plies):** ~73 hours

### 📈 Win Rate vs Depth (2, 5, 10 plies)
A plotted curve (Page 2) shows a **very small upward trend** as plies increase — but the improvement is minimal because:

- The evaluation function is simple.
- Alpha-Beta already performs extremely well against random.
- Random opponents don’t exploit deeper strategies.

### ❓ Does deeper search improve wins?
**Yes — but only slightly.**  
The improvement is small because the evaluation function from AIMA is not very complex, and the random opponent is weak.  
(Page 3) :contentReference[oaicite:1]{index=1}

---

## 🕹 Features

- Complete Mancala gameplay engine  
- Minimax and Alpha-Beta pruning AI  
- Adjustable search depth  
- Utility function based on score difference  
- Random opponent for benchmarking  
- Runtime measurements in Jupyter Notebook  
- Win-rate graphs and statistical analysis  

---

## 📓 Jupyter Notebook

This project uses a Jupyter Notebook (`.ipynb`) to:

- Run full game simulations  
- Visualize performance  
- Adjust search depth interactively  
- Record game logs, runtimes, and outcomes  
- Test the AI against random opponents

To open the notebook:

```bash
jupyter notebook
