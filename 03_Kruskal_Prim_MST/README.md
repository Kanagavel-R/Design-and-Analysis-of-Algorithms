# Implementation of Kruskal's and Prim's Algorithms for Minimum Spanning Tree

## Aim

To implement Kruskal's and Prim's algorithms and find the Minimum Spanning Tree (MST) of a weighted undirected graph.

## Algorithms Used

### 1. Kruskal's Algorithm

Kruskal's algorithm constructs the Minimum Spanning Tree by selecting edges in increasing order of weight while avoiding cycles.

It uses the **Union-Find (Disjoint Set)** data structure with:

* Path Compression
* Union by Rank

**Time Complexity:** O(E log E)

**Space Complexity:** O(V)

### 2. Prim's Algorithm

Prim's algorithm starts from a selected vertex and repeatedly adds the minimum-weight edge that connects a vertex in the MST to a vertex outside the MST.

A **Min-Heap (Priority Queue)** is used to efficiently select the minimum-weight edge.

**Time Complexity:** O(E log V)

**Space Complexity:** O(V + E)

Where:

* `V` = Number of vertices
* `E` = Number of edges

## Graph Used

The program uses a weighted undirected graph with **7 vertices** and **11 edges**.

```text
Vertices: 0, 1, 2, 3, 4, 5, 6
```

## Input

The graph is represented using weighted edges:

```text
(0 - 1) : 7
(0 - 3) : 5
(1 - 2) : 8
(1 - 3) : 9
(1 - 4) : 7
(2 - 4) : 5
(3 - 4) : 15
(3 - 5) : 6
(4 - 5) : 8
(4 - 6) : 9
(5 - 6) : 11
```

## Sample Output

```text
=== Kruskal's MST ===
Edge (0 - 3) Weight: 5
Edge (2 - 4) Weight: 5
Edge (3 - 5) Weight: 6
Edge (0 - 1) Weight: 7
Edge (1 - 4) Weight: 7
Edge (4 - 6) Weight: 9
Total MST Cost: 39
```

Prim's algorithm will also produce an MST with the same total cost:

```text
=== Prim's MST ===
Total MST Cost: 39
```

The order of edges selected by Prim's algorithm may differ from Kruskal's, but the total MST cost is the same for this graph.

## Comparison

| Algorithm | Approach     | Time Complexity | Main Data Structure |
| --------- | ------------ | --------------- | ------------------- |
| Kruskal's | Edge-based   | O(E log E)      | Union-Find          |
| Prim's    | Vertex-based | O(E log V)      | Min-Heap            |

## Key Concepts

* Minimum Spanning Tree
* Greedy Algorithm
* Union-Find / Disjoint Set
* Path Compression
* Union by Rank
* Priority Queue / Min-Heap
* Weighted Undirected Graph

## Requirements

* Python 3.x
* No external libraries required

## How to Run

```bash
python mst_algorithms.py
```

## File

* `mst_algorithms.py` – Contains implementations of Kruskal's and Prim's algorithms for finding the Minimum Spanning Tree.
