# :rocket: Solving the Traveling Salesman Problem (TSP) with Branch-and-Cut

## Overview

This project focuses on solving the **Traveling Salesman Problem (TSP)** using the **Branch-and-Cut** method. The solution includes advanced cutting-plane techniques such as:

- **Connectivity Cuts**
- **2-Connected Cuts**
- **Blossom Inequalities** (using separation heuristics)

To benchmark the performance of the branch-and-cut implementation, I compare the solutions against a heuristic approach using [Google OR-tools](https://developers.google.com/optimization/routing/tsp).

---

## Objective

The goal of the project is to:
1. Solve TSP instances with an enhanced **Branch-and-Cut** algorithm.
2. Implement user-defined cuts and lazy cuts to strengthen the LP bounds.
3. Compare the solutions to Google OR-tools' heuristic solver.
4. Measure and report key performance metrics such as bounds, gaps, and runtime.

---

## Data 

The input data consists of TSP instances located in the **STSP** folder. The datasets are sourced from the **TSPLIB95** library, which provides problems in the form of:
- Lower triangular distance matrices
- Upper triangular distance matrices
- Full distance matrices

### TSPLIB Reference:
[TSPLIB95 Dataset Description](http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/)

---

## Methods and Approach

### Branch-and-Cut Algorithm
1. **Initial LP Relaxation**:
   - Solve the Linear Programming (LP) relaxation of the TSP.

2. **Cut Generation**:
   - **Connectivity Cuts**: Enforce subtour elimination constraints.
   - **2-Connected Cuts**: Strengthen solutions to ensure valid TSP tours.
   - **Blossom Inequalities**: Use separation heuristics to identify violated blossom inequalities.

3. **Lazy Cuts and User Cuts**:
   - Lazy cuts are added dynamically to eliminate infeasible solutions.
   - User cuts proactively strengthen the LP relaxation.

4. **Benchmarking**:
   - Solve the same TSP instances using Google OR-tools' heuristic solver for comparison.

---

## Features

- Implementation of **Branch-and-Cut** for solving TSP.
- Advanced **cutting-plane methods**: Connectivity cuts, 2-connected cuts, and blossom inequalities.
- Integration of **lazy cuts** and **user cuts** to dynamically improve LP relaxation.
- Benchmarking with **Google OR-tools** for heuristic-based TSP solutions.
- Comprehensive results reporting with performance metrics.

---

## Setup

### Prerequisites

- Python 3.8+
- Gurobi Optimizer (or any other LP solver)
- NetworkX (for graph-based cut identification)
- Google OR-tools

### Installation

1. Install dependencies:
   ```bash
   pip install gurobipy networkx ortools

