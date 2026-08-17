# Implementation of Single Source Shortest Path Algorithm (Dijkstra's)

## Aim

To implement Dijkstra's algorithm to find the shortest paths from a single source vertex to all other vertices in a weighted graph.

## Algorithm

Dijkstra's algorithm is a greedy algorithm that repeatedly selects the unvisited vertex with the minimum tentative distance and relaxes its adjacent edges.

A **Min-Heap (Priority Queue)** is used to efficiently select the vertex with the minimum distance.

## Steps

1. Initialize the distance of the source vertex as `0` and all other distances as infinity.
2. Insert the source vertex into the priority queue.
3. Extract the vertex with the minimum distance.
4. Relax all its adjacent edges.
5. Update the distance and predecessor if a shorter path is found.
6. Repeat until the priority queue becomes empty.
7. Reconstruct the shortest path using the predecessor array.

## Graph Used

The program uses the following directed weighted graph:

```text
0 → 1 (4)
0 → 2 (1)
1 → 3 (1)
2 → 1 (2)
2 → 3 (5)
3 → 4 (3)
4 → 5 (2)
```

Source vertex:

```text
0
```

## Sample Output

```text
Shortest paths from vertex 0:

  Vertex   Distance                           Path
-------------------------------------------------------
       0          0                              0
       1          3                       0 -> 2 -> 1
       2          1                            0 -> 2
       3          4                    0 -> 2 -> 1 -> 3
       4          7                 0 -> 2 -> 1 -> 3 -> 4
       5          9              0 -> 2 -> 1 -> 3 -> 4 -> 5
```

## Time Complexity

Using a Min-Heap:

**O((V + E) log V)**

Where:

* `V` = Number of vertices
* `E` = Number of edges

## Space Complexity

**O(V + E)** for the graph, distance array, predecessor array, visited set, and priority queue.

## Important Note

Dijkstra's algorithm works correctly when all edge weights are **non-negative**. It should not be used when the graph contains negative edge weights.

## Key Concepts

* Single Source Shortest Path
* Greedy Algorithm
* Graph Representation
* Edge Relaxation
* Min-Heap / Priority Queue
* Shortest Path Reconstruction

## Requirements

* Python 3.x
* No external libraries required

## How to Run

```bash
python dijkstra.py
```

## File

* `dijkstra.py` – Python implementation of Dijkstra's Single Source Shortest Path algorithm with shortest path reconstruction.
