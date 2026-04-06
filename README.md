# 🧭 A* Search Algorithm in Grid Environment

## 📌 Project Overview

This project demonstrates the implementation of the **A* (A-star) search algorithm** in a constrained grid environment. The goal is to compute the optimal path from a starting point to a goal node while avoiding obstacles using heuristic-based search strategies.

The implementation focuses on comparing heuristic functions and analyzing their impact on pathfinding efficiency and optimality.

---

## 🎯 Objectives

* Implement the A* search algorithm from scratch
* Model a 2D grid environment with obstacles
* Apply and compare different heuristic functions
* Ensure optimal pathfinding with admissible heuristics
* Analyze performance behavior

---

## 🧱 Environment Setup

The environment is represented as a **6×6 grid**, where:

* `0` → Free cell (walkable)
* `1` → Obstacle (blocked)

The agent can move in **four directions only**:

* Up
* Down
* Left
* Right

Each move has a uniform cost of **1**.

The goal position is fixed at:

```
(5, 5)
```

---

## 🧠 Heuristic Functions

Heuristics guide the A* algorithm by estimating the remaining cost to reach the goal.

### 1. Manhattan Distance

* Formula:

  ```
  h(n) = |x_n - x_goal| + |y_n - y_goal|
  ```
* Suitable for grid movement without diagonals
* Guarantees optimality (admissible & consistent)

### 2. Chebyshev Distance

* Formula:

  ```
  h(n) = max(|dx|, |dy|)
  ```
* Provides a tighter estimate in some cases
* Also admissible and consistent

---

## ⚙️ Algorithm Details

The A* algorithm uses:

* **g(n)** → Cost from start to current node
* **h(n)** → Estimated cost to goal
* **f(n) = g(n) + h(n)** → Evaluation function

### Key Steps:

1. Initialize open and closed sets
2. Select node with lowest `f(n)`
3. Expand neighbors
4. Update costs and paths
5. Repeat until goal is reached

---

## 🔍 Neighbor Expansion

Neighbors are generated based on valid moves:

* Must stay within grid boundaries
* Must not be an obstacle

---

## 📊 Features

* Grid-based visualization logic
* Multiple heuristic support
* Optimal path reconstruction
* Clean and modular implementation

---


---

## 📈 Expected Output

* Optimal path from start to goal
* Path cost
* Comparison between heuristic behaviors

---

## 🧪 Technologies Used

* Python
* NumPy
* Heap Queue (priority queue)
* Pandas (optional for analysis)

---

## 💡 Key Insights

* A* guarantees optimal solutions when using admissible heuristics
* Heuristic choice affects performance but not correctness
* Grid constraints significantly influence path complexity

---

## 📌 Conclusion

This project provides a clear and practical implementation of heuristic search using A*. It highlights how intelligent search strategies outperform uninformed approaches in pathfinding problems.

---


This project is open-source and available under the MIT License.
