# Comparative Analysis of Naive, Rabin-Karp, and KMP Algorithms for String Matching

## Aim

To implement and compare the Naive String Matching, Rabin-Karp, and Knuth-Morris-Pratt (KMP) algorithms based on the number of character comparisons performed.

## Algorithms Used

### 1. Naive String Matching

The Naive algorithm checks the pattern against the text at every possible position.

* **Worst Case:** O(n × m)
* **Space Complexity:** O(1), excluding the output list

### 2. Rabin-Karp

Rabin-Karp uses a rolling hash to efficiently identify possible pattern matches and verifies characters when hash values match.

* **Average/Expected Time:** O(n + m)
* **Worst Case:** O(n × m)
* **Space Complexity:** O(1), excluding the output list

### 3. Knuth-Morris-Pratt (KMP)

KMP uses the Longest Prefix Suffix (LPS) array to avoid unnecessary comparisons when a mismatch occurs.

* **Time Complexity:** O(n + m)
* **Space Complexity:** O(m)

## Input

```text
Text: AABAACAADAABAABA
Pattern: AABA
```

## Sample Output

```text
Naive -> Matches at: [0, 9, 12], Comparisons: ...
KMP -> Matches at: [0, 9, 12], Comparisons: ...
RK -> Matches at: [0, 9, 12], Comparisons: ...
```

The exact comparison count may vary if the implementation is modified.

## Performance Analysis

The program generates a random text of length 10,000 using the characters `A`, `B`, `C`, and `D`.

It tests the following patterns:

```text
AB
ABCD
ABCDAB
ABCDABCD
```

The number of character comparisons performed by each algorithm is displayed for comparison.

## Comparison

| Algorithm  | Average/Expected | Worst Case | Main Technique    |
| ---------- | ---------------- | ---------- | ----------------- |
| Naive      | O(n × m)         | O(n × m)   | Direct comparison |
| Rabin-Karp | O(n + m)         | O(n × m)   | Hashing           |
| KMP        | O(n + m)         | O(n + m)   | LPS array         |

Where:

* `n` = length of text
* `m` = length of pattern

## Requirements

* Python 3.x
* No external libraries required

## How to Run

```bash
python string_matching.py
```

## File

* `string_matching.py` – Contains implementations of Naive, Rabin-Karp, and KMP string matching algorithms along with comparative analysis.
