# Implementation and Performance Analysis of Interpolation Search

## Aim

To implement the Interpolation Search algorithm and compare its performance with Binary Search.

## Algorithm

1. Initialize `low` and `high`.
2. Calculate the estimated position using the interpolation formula.
3. Compare the target with the element at the estimated position.
4. If the target is found, return its index.
5. If the target is smaller, search the left subarray.
6. If the target is larger, search the right subarray.
7. Repeat until the element is found or the search space becomes empty.

## Requirements

* Python 3.x

## How to Run

```bash
python interpolation_search.py
```

## Sample Output

```text
Array: [2, 5, 10, 15, 23, 35, 48, 60, 75, 90, 105, 120]
Searching for: 35
Found at index: 5, Comparisons: 1
```

The program also displays a performance comparison between Interpolation Search and Binary Search for different input sizes.

## Time Complexity

* Best Case: **O(1)**
* Average Case: **O(log log n)**
* Worst Case: **O(n)**

## Space Complexity

* **O(1)**

## Files

* `interpolation_search.py` – Python implementation and performance analysis.
README.md
