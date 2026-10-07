# SLE-3: Architectural Design (Full C4 Model)

**Course:** 02AML204 – Introduction to Artificial Intelligence
**Programme:** SY B.Tech. CSE (AI & ML), Sem-VI
**Name:** Sharvil S. Chavan
**PRN:** 25UAM085
**Division:** B
**GitHub:** https://github.com/SharvilChavan-10

---

## Overview

This SLE documents the architecture of my **Maze Solver System (BFS / DFS)** using all four levels of the C4 model. It is the same system built in SLE-1 and profiled in SLE-2.

| SLE | Focus |
| --- | --- |
| SLE-1 | Code (agent / search) + AI Contribution Log |
| SLE-2 | Performance profiling and comparison report |
| **SLE-3** | **Full architecture design (C4)** |

## The System

The system generates grid mazes (walls, one start, one goal) and solves them with two uninformed search algorithms: Breadth-First Search (BFS) and Depth-First Search (DFS). For every run it records execution time, nodes expanded and path length, on mazes of size 20×20, 40×40 and 70×70.

## C4 Summary

| Level | What it shows |
| --- | --- |
| 1. Context | Student / Operator ↔ Maze Solver System; external: Python runtime, Matplotlib |
| 2. Container | 6 containers: Maze Generator, Experiment Driver, Search Engine, Neighbour Generator, Result Reporter, Output Module |
| 3. Component | Inside the Search Engine: Frontier, Goal Test, Node Expander, Visited Set + Parent Map, Path Reconstructor |
| 4. Code | `make_maze()`, `neighbors()`, `bfs()`, `dfs()`, `reconstruct()`, `run_trials()` |

## Repository Contents

```
.
├── SLE3_25UAM085_SharvilChavan.docx   # Main report (C4 diagrams + explanations)
├── README.md                          # This file
├── AI_CONTRIBUTION_LOG.md             # Honest record of AI use
└── maze_search.py                     # Implementation from SLE-2 (referenced by Level 4)
```

> Adjust the list above to match what is actually in your repository.

## How to Run the Code (from SLE-2)

Requirements: Python 3 and Matplotlib.

```bash
pip install matplotlib
python maze_search.py
```

## Key Design Decisions

- Generator, neighbours, search and reporting are separate containers, so BFS and DFS run on the same maze with the same move rule.
- BFS and DFS differ only in the Frontier (FIFO queue vs LIFO stack).
- A visited set with a parent map rebuilds the path at the end instead of storing a full path in every frontier entry.
- Timing is kept outside the search logic so measuring does not change the algorithm.
- No Heuristic container, because BFS and DFS are uninformed. A* could be added later as a new component.

## AI Use

AI (Claude) was used for this SLE. See [AI_CONTRIBUTION_LOG.md](AI_CONTRIBUTION_LOG.md) for details.
