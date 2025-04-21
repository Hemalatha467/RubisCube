# 🧠 Rubik’s Cube Solver using Reinforcement Learning

This project explores the use of **Q-learning**, a form of reinforcement learning (RL), to teach an agent how to solve a **3x3x3 Rubik’s Cube** from scratch — without any built-in solving logic or human heuristics.

---

## 🎯 Objective

To develop an AI agent that:
- Learns to solve a Rubik’s Cube using **feature-based Q-learning**
- Trains via interactions with a custom cube simulation environment
- Operates without pre-defined algorithms or human solving strategies
- Solves the cube in fewer moves and less time as learning improves

---

## 🧩 Key Features

### 🧱 Custom Cube Environment (`Puzzle.py`)
- Simulates the Rubik's Cube with support for all valid rotations
- Tracks cube state and offers utility functions like `isGoalState()`, `move()`, etc.
- Supports reward feature extraction (e.g., number of solved sides, correct placements)

### 🤖 Q-Learning Agent (`Agent.py`)
- Learns optimal actions based on state-action Q-values
- Uses an **epsilon-greedy** strategy for exploration vs. exploitation
- Bootstraps learning with **pattern-based Q-value initialization**
- Tracks state visitation and adjusts learning dynamically

### ✅ Unit Testing (`tests.py`)
- Verifies the correctness of cube rotations and state transitions
- Tests goal-state detection and cube equality methods
- Ensures stable, bug-free environment behavior for training

---

## 🚀 How It Works

1. A cube state is initialized — either solved, scrambled, or n-move away.
2. The agent chooses a move (face rotation) based on its Q-table.
3. A reward is given based on how close the result is to a solved state.
4. Q-values are updated using the Bellman equation.
5. The agent repeats this across many episodes to refine its solving strategy.

---

## 🧪 Features Used for Reward Shaping

- Number of fully solved sides
- Number of pieces correctly placed on each face
- (Planned) Cross and X pattern recognition

---

## 🛠️ Project Structure
├── Puzzle.py # Rubik’s Cube environment 
├── Agent.py # Q-learning agent
├── tests.py # Unit tests for cube logic

## 🧠 Authors
- Hemalatha Ganipisetti  
- Addi Poojeetha Reddy

