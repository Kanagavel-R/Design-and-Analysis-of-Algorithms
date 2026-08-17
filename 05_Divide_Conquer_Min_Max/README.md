# To Find Min-Max Value by Applying Divide and Conquer Technique

## Aim

To find the minimum and maximum values in an array using the Divide and Conquer technique and compare its number of comparisons with the Naive approach.

## Technique Used

### Divide and Conquer

The array is recursively divided into smaller subarrays until each subarray contains one or two elements.

The minimum and maximum values of the divided portions are then combined to obtain the overall minimum and maximum.

### Steps

1. Divide the array into two halves.
2. Recursively find the minimum and maximum of each half.
3. Compare the two minimum values to find the overall minimum.
4. Compare the two maximum values to find the overall maximum.
5. Return the final minimum and maximum values.

## Input

```text
Array: [3, 1, 7, 4, 9, 2, 8, 5, 6, 0]
```

## Sample Output

```text
Array: [3, 1, 7, 4, 9, 2, 8, 5, 6, 0]
Minimum Value : 0
Maximum Value : 9
D&C Comparisons   : 13
Naive Comparisons : 18
```

The program also performs a comparison analysis for array sizes:

```text
10
100
1000
10000
```

## Comparison Analysis

The Naive approach performs approximately:

**2(n - 1) comparisons**

The optimized Divide and Conquer approach performs approximately:

**3n/2 - 2 comparisons** for an even-sized array.

Therefore, the Divide and Conquer approach reduces the number of comparisons compared with the Naive approach.

## Time Complexity

**O(n)**

Although the array is recursively divided, every element is processed a constant number of times.

## Space Complexity

**O(log n)** due to the recursion stack for a balanced divide-and-conquer implementation.

## Recurrence Relation

The recurrence can be represented as:

```text
T(n) = 2T(n/2) + O(1)
```

Using the Master Theorem:

```text
T(n) = O(n)
```

## Key Concepts

* Divide and Conquer
* Recursion
* Minimum and Maximum
* Comparison Counting
* Recurrence Relation
* Master Theorem

## Requirements

* Python 3.x
* No external libraries required

## How to Run

```bash
python min_max.py
```

## File

* `min_max.py` – Python implementation of the Min-Max problem using Divide and Conquer, with comparison analysis against the Naive approach.
