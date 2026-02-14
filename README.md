# 🧠 DSA Patterns

A structured collection of common algorithmic patterns grouped by topic. Use this as a reference for complexity limits and problem-solving mental models.


---

## ⚡ System Constraint Rule of Thumb
> **The $10^8$ Rule:** Most modern systems/judges allow for roughly  100 million CPU operations per second. So, $10^8$ will take 1 second to execute, $10^9$ will take 10 seconds and keeps on increasing exponantially. 
> * If $N \leq 500 \rightarrow O(N^3)$ is usually fine ($500^3 \approx 1.25 \times 10^8$).
> * If $N \leq 10^4 \rightarrow O(N^2)$ is the limit.
> * If $N \leq 10^6 \rightarrow O(N \log N)$ or $O(N)$ is required.

---

## 📂 Patterns by Topic

### 🟣 Math
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Rectangle Area | Inclusion-Exclusion Principle for finding overlapping Area | [Leetcode](https://leetcode.com/problems/rectangle-area/description/) |
| Max Square Area | Sorting, Longest Consecutive Sequence Pattern | [Leetcode](https://leetcode.com/problems/maximize-area-of-square-hole-in-grid/description/) |
| Longest Mountain | Two pointer; prefer `while` loops for manual pointer control | [Leetcode](https://leetcode.com/problems/longest-mountain-in-array/) |

### 🟠 Sorting
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Selection Sort | Unstable; relative order of equal elements is not maintained | [Gfg](https://www.geeksforgeeks.org/dsa/selection-sort-algorithm-2/) |
| Bubble Sort | Stable; relative order is maintained via adjacent swaps | [Gfg](https://www.geeksforgeeks.org/dsa/bubble-sort-algorithm/) |
| Insertion Sort | Stable and in-place; efficient for small or nearly sorted data | [Gfg](https://www.geeksforgeeks.org/dsa/insertion-sort-algorithm/) |
| Counting Sort | Non-comparative; $O(N + K)$ time where $K$ is the range | [Leetcode](https://leetcode.com/problems/minimum-absolute-difference/) |

### ⚪ Bitwise Operations
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Min Bitwise Array | Pattern recognition; understand binary addition/carry logic | [Leetcode](https://leetcode.com/problems/construct-the-minimum-bitwise-array-i/description/) |

### 🔵 Hash Table
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Maximum Square Area | Calculate width combinations in $O(N^2)$, use HashSet for $O(1)$ lookup | [Leetcode](https://leetcode.com/problems/maximum-square-area-by-removing-fences-from-a-field/description/) |

### 🟣 Set / Multiset
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Divide Array | Use `std::multiset` (C++) or similar to track sliding window values | [Leetcode](https://leetcode.com/problems/divide-an-array-into-subarrays-with-minimum-cost-ii/) |

### 🟠 Binary Search
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Separate Squares | Binary Search on the Answer (searching over a continuous range) | [Leetcode](https://leetcode.com/problems/separate-squares-i/description/) |

### ⚪ Linked List
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Loop Detection | Floyd’s Cycle-Finding Algorithm (Fast & Slow pointers) | [Leetcode](https://leetcode.com/problems/linked-list-cycle/description/) |
| Cycle Entrance | Tortoise & Hare; mathematical offset to find the start of the loop | [Leetcode](https://leetcode.com/problems/linked-list-cycle-ii/description/) |

### 🟣 Stack
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Maximal Rectangle | Monotonic Stack; process 2D grid as a series of histograms | [Leetcode](https://leetcode.com/problems/maximal-rectangle/description/) |

### 🟠 DP
| Pattern | Description | Link |
| :--- | :--- | :---: |
| LCS | Longest Common Subsequence; DP state transitions (take/not-take) | [Leetcode](https://leetcode.com/problems/minimum-ascii-delete-sum-for-two-strings/) |
| Trapping Rainwater | Precompute Prefix/Suffix max, or use Two Pointers/Monotonic Stack | [Leetcode](https://leetcode.com/problems/trapping-rain-water/) |
| Champagne Tower | store excess liquid level wise. | [Leetcode](https://leetcode.com/problems/champagne-tower/description/?envType=daily-question&envId=2026-02-14) |

### 🔵 Tree
| Pattern | Description | Link |
| :--- | :--- | :---: |
| LCA | Lowest Common Ancestor; path tracing or recursive DFS | [Leetcode](https://leetcode.com/problems/smallest-subtree-with-all-the-deepest-nodes/description/) |
| Range Sum Query | Segment Tree ($4N$ nodes) for $O(\log N)$ updates and queries | [Leetcode](https://leetcode.com/problems/range-sum-query-immutable/) |

### 🟣 Graph
| Pattern | Description | Link |
| :--- | :--- | :---: |
| Rotten Oranges | Multi-source BFS; level-order traversal for shortest time | [Leetcode](https://leetcode.com/problems/rotting-oranges/description/) |
| 01 Matrix | BFS with multi-source start; uses direction arrays `{0, 1, 0, -1, 0}` | [Leetcode](https://leetcode.com/problems/01-matrix/description/) |
| Topological Sort | Kahn's Algorithm (BFS) or DFS+Stack; only for DAGs | [Gfg](https://www.geeksforgeeks.org/dsa/topological-sorting/) |
| Shortest Path (DAG) | Use Topological Sort + Relaxation for $O(V+E)$ efficiency | [Gfg](https://www.geeksforgeeks.org/dsa/shortest-path-for-directed-acyclic-graphs/) |
| Dijkstra | Greedy BFS using Priority Queue for weighted edges ($O(E \log V)$) | [Gfg](https://www.geeksforgeeks.org/dsa/dijkstras-algorithm-for-adjacency-list-representation/) |
