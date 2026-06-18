# Sudoku Solver using CSP & Simulated Annealing

An Artificial Intelligence project that solves **9×9** and **16×16 Sudoku** puzzles using two different AI approaches:

- Constraint Satisfaction Problem (CSP) with Backtracking Search
- Simulated Annealing (SA)

The project compares both techniques in terms of execution time, completeness, constraint violations, and search efficiency.

---

## Features

### Constraint Satisfaction Problem (CSP)

- Backtracking Search
- Minimum Remaining Values (MRV)
- Most Constraining Variable (MCV)
- Least Constraining Value (LCV)
- Forward Checking
- Pure Backtracking implementation (without heuristics) for comparison

### Simulated Annealing (SA)

- Cost-based optimization
- Neighbor generation using random modifications
- Probabilistic acceptance of worse states
- Configurable:
  - Initial temperature
  - Cooling rate
  - Maximum iterations

---

## Supported Sudoku Sizes

- ✅ 9 × 9 Sudoku
- ✅ 16 × 16 Sudoku

---

## Constraint Satisfaction Formulation

Each Sudoku cell represents a variable.

Domains:

- 1–9 for 9×9 puzzles
- Appropriate symbol set for 16×16 puzzles

Constraints:

- Every row contains unique values.
- Every column contains unique values.
- Every sub-grid contains unique values.

---

## CSP Heuristics

The CSP solver combines multiple heuristics to reduce the search space:

- Minimum Remaining Values (MRV)
- Most Constraining Variable (MCV)
- Least Constraining Value (LCV)
- Forward Checking

These heuristics significantly reduce unnecessary backtracking and improve solving speed.

---

## Simulated Annealing

The Sudoku board is treated as an optimization problem.

The cost function penalizes:

- Duplicate values in rows
- Duplicate values in columns
- Duplicate values in sub-grids
- Empty cells

The algorithm repeatedly generates neighboring states and decides whether to accept them based on the current temperature.

---

## Experimental Evaluation

The project compares both algorithms using:

- Execution Time
- Solution Completeness
- Number of Constraint Violations
- Number of Backtracks (CSP)
- Number of Iterations (SA)

Experiments were conducted on:

- Easy
- Medium
- Hard

for both:

- 9×9 Sudoku
- 16×16 Sudoku

---

## Results Summary

### CSP with Heuristics

✔ Fastest overall performance

✔ Produces complete solutions

✔ Very low backtracking

✔ Excellent for standard Sudoku puzzles

---

### CSP without Heuristics

- Extremely slow
- Large number of backtracks
- Often reaches the imposed backtracking limit
- Demonstrates the importance of heuristic search

---

### Simulated Annealing

✔ Good scalability

✔ Produces near-optimal solutions

✔ Escapes local minima

✔ Performance depends on parameter tuning

✖ Does not guarantee an optimal solution

---

## Project Structure

```
.
├── sudoku.py
├── csp_solver.py
├── simulated_annealing.py
├── heuristics.py
├── utils.py
├── puzzles/
├── results/
├── graphs/
└── README.md
```

> The exact file structure may vary depending on your implementation.

---

## Technologies

- Python 3
- Object-Oriented Programming
- Constraint Satisfaction Problems (CSP)
- Simulated Annealing
- Search Algorithms
- Artificial Intelligence

---

## Future Improvements

- Genetic Algorithms
- Hybrid CSP + Simulated Annealing solver
- Parallel search
- Better parameter tuning for SA
- Interactive GUI for Sudoku solving

---

## Authors

- **Hanan Alawawda**
- **Amjad Adi**

Birzeit University  
Department of Electrical & Computer Engineering

Course: **ENCS3340 – Artificial Intelligence**

---

## License

This project was developed for educational purposes as part of the ENCS3340 Artificial Intelligence course.
