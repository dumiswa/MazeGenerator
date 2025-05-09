# 🧩 Algorithmic Dungeons – Assignments 01, 02 & 03

This repository contains three university assignments from the *Algorithms* course. Each assignment builds upon the previous to develop a progressively more complex system: starting with binary space partitioning for dungeon generation, then converting the dungeon into a graph for structural representation, and finally implementing multiple pathfinding algorithms.

---

## 📘 Assignment 01 – Binary Space Partitioning

This assignment uses **Binary Space Partitioning (BSP)** to procedurally generate dungeon rooms within a defined 2D space.

### ✅ Implemented Features

- **Recursive splitting** of the base rectangle into sub-rectangles, alternating horizontal and vertical cuts.
- Generated **room dimensions randomly** within each leaf node, constrained by a minimum size.
- Ensured all doors were placed **between adjacent partitions**, avoiding corners or disconnected areas.
- **Removed rooms** with minimum and maximum area to meet quality requirements.
- Color-coded rooms based on **door count**, aiding visual analysis.

### 🛠 Technical Notes

- Each leaf of the BSP tree can contain a single room.
- Room positions and sizes are stored and used to compute overlaps and adjacency for door placement.
- The dungeon structure is stored as a flat list of rooms and connections.

---

## 📗 Assignment 02 – Graph Construction and Tile View

The dungeon is converted into a **graph** where each room and door is treated as a node, enabling abstract reasoning about structure and navigation.

### ✅ Implemented Features

- Constructed a **graph representation** of the dungeon:
  - Nodes: Rooms and doors
  - Edges: Valid connections between rooms and their corresponding doors
- Graph is internally stored as an adjacency list.

### 🛠 Technical Notes

- Clicking a node triggers a path to be computed via a selected algorithm.
- Node selection is filtered against the graph to ensure only valid targets are processed.
- Added a tile-based visual rendering layer to replace the primitive wireframe.

---

## 📕 Assignment 03 – Pathfinding (Sufficient Level)

Implemented two fundamental shortest-path search algorithms to compute the shortest path between nodes based on node count.

### ✅ Implemented Features

- **Recursive depth-first search** (DFS variant) to find the shortest path by node count.
- **Breadth-first search (BFS)** implemented iteratively using a queue to guarantee shortest path (minimum number of nodes).
- Upon clicking a valid target node, the selected algorithm computes the path from current node to target.
- Path is executed step-by-step once computed.

### 🛠 Technical Notes

- Graph is assumed unweighted; all edges are considered equal cost.
- Recursive algorithm tracks visited nodes and builds the path via backtracking.
- BFS uses a FIFO queue and `came_from` map to reconstruct the shortest route No weighting, heuristics, or Dijkstra/A* functionality is present in this version.

---

## 📸 Demo 

![0507(1) (2)](https://github.com/user-attachments/assets/4b63831c-2ff0-4b71-a32e-ace5a329678d)

---




