# Constraint Satisfaction Problems

> This repository was an assignment for the course ***CSDS3203  Introduction to Artificial Intelligence***

This repository explores how **Constraint Satisfaction Problems (CSPs)** can be used to solve two engaging problems: a cryptarithmetic puzzle and a fireworks scheduling challenge in Oman. The implementation uses a CSP framework adapted from the `aima-python` library.

> Solved by: [*JaberAlJ*](https://github.com/JaberAlJ)

---

## 📌 Objectives

- Understand and apply CSPs to real-world scenarios.
- Utilize a CSP framework to define:
  - Variables
  - Domains
  - Constraints
  - Neighbors
- Solve problems using:
  - Backtracking search
  - Inference methods (e.g., forward checking, MRV, LCV)
- Discover multiple valid solutions through domain manipulation.

## ⚙️ Project Structure
```
├── CSP/
│   ├── aima/
│   │   ├── __pycache__/
│   │   ├── __init__.py
│   │   ├── csp.py
│   │   ├── search.py
│   │   └── utils.py
│   └── res/
│       ├── colors/
│       └── oman.png
└── applying-constraints-satisfaction-problems.ipynb
```

## ➕ Problem 1: Solving a Cryptarithmetic Puzzle

📐 **Equation**: `RIGHT + LEFT = CENTER`  
🔢 **Goal**: Assign unique digits (0-9) to each letter so the equation holds.

### 🛠️ Implementation Steps
- Define letters and carry-over variables (`C1` to `C5`)
- Apply `all_diff_constraint` and arithmetic logic per column
- Solve using an **AC-based CSP solver**

## 🎆 Problem 2: Scheduling Fireworks in Oman

📅 **Context**: Fireworks across Oman's governorates for National Day (Nov 18–22, 2023)
⚠️ **Constraints**:
- Neighboring governorates must not celebrate on the same day
- Muscat (8): Nov 18
- Dhofar (10): Nov 22

🗺️ **Approach**
- Modeled as a map coloring problem
- Assigned dates as colors
- Defined neighbors based on geography

🧪 **Solving Method**
- Used plain backtracking search and enhanced versions:
- Forward checking
- Minimum Remaining Value (MRV)
- Least Constraining Value (LCV)

## 🙏 Acknowledgements
This project was inspired by the textbook Artificial Intelligence: A Modern Approach (4th Edition) by Russell and Norvig. Code snippets and ideas are adapted with educational intent.

## 📚 References
- Russell, S., & Norvig, P. (2021). Artificial Intelligence: A Modern Approach (4th Ed.).
- `aima-python`