# Graduate Algorithms

The following is a study guide for OMSCS GA Algorithms course CS-8803-GA.

## Big O notation and computational complexity

Algorithm questions

- Is it correct?
- How much time does it take, as a function of n?
- Can we do better?

f(n) and g(n) as running times of 2 different algorithms on inputs of size n.

Let f(n) and g(n) be functions from positive integers to positive reals. We say f=O(g) (which means that "f grows no faster than g") if there is a constant c>0 such that f(n)<c*g(n)
$$
\Omega(g) \\
\Theta(g)
$$


#### Common Sense rules for big O

1. Multiplicative constants can be omitted; `14n^2 --> n^2`
2. `n^a` dominates `n^ b` if `a>b`; `n^2` dominates `n`
3. any exponential dominates any polynomial: `3^n` dominates `n^5` (it even dominates `2^n`)
4. Likewise, any polynomial dominates any log; `n` dominates `(logn)^3` also means, e.g. `n^2` dominates `nlogn`



### Data Structures

#### Heap

#### Stack

#### Priority Queue

#### Adjacency List



### Terminology

#### Lemma

#### Property

#### Proof

#### Induction

#### Contradiction





## Dynamic Programming

Dynamic programming has no recursion in algorithm. Memoization will not be used in this course.

Widely used, challenging at first, then easy. Practice, practice, practice!



The steps to solving a Dynamic Programming problem are:

- Define the entries of your table in words. E.g. `T(i)` or `T(i,j)` is ....
  - prefix
  - add constraint - include last element
- State a recurrence for the entries of your table in terms of smaller subproblems
- Write pseudo code for your algorithm to solve this problem
- Analyze the running time of your algorithm

#### Classic Problems

There are a handful of classic Dynamic Programming problems that most problems can be reduced to:

* **Fibonacci (FIB)**

- **Longest Increasing Subsequence (LIS)**
  - subsequence = subset of elements in order (can skip)
  - substring = set of consecutive elements
- **Longest Common Subsequence(LCS)**
  - 
- **Knapsack**
  - With repetition
  - Without repetition
- **Chain Matrix Multiplication**
- **Shortest Path**
  - **Bellman Ford**



## RSA

The RSA protocol is ubiquitous in computing.

### Modular Arithmetic

#### Inverse

#### Euclid's Greatest Common Denominator Algorithm

#### Fermat's Little Theorem



### RSA Protocol



### Primality Testing

## Divide and Conquer

Divide and conquer is a powerful approach to improving computational complexity of an algorithm

- Multiplication
- Complex Numbers
- Fast Fourier Transform (FFT)
  - Roots of Unity
- Median

## Bloom Filters (not tested)

Probabilistic membership checker.



## Graph Algorithms



### Graphs

- directed vs undirected
- representations 
  - adjacency matrix
  - adjacency list
- Connectivity
  - undirected = Connected Components (CC)
  - directed = Strongly Connected Components (SCC)
- Edges in DFS tree:
  - Undirected
    - Tree Edges
    - Non-tree Edges
  - Directed (shows pre/post ordering for (u,v) edge types)
    - Tree Edges
      - `post(u) > post(v)`
    - Forward Edges - node to non-child descendant
      - `post(u) > post(v)`
    - Back Edges - lead to an ancestor in DFS tree
      - `post(u) < post(v)`
    - Cross Edges - lead to neither descendant nor ancestor, lead to a completely unexplored vertex
      - `post(u) > post(v)`

* Directed Acyclic Graph (DAG)
  * **Property** : In a DAG every edge leads to a vertex with a lower post number
  * **Property** : Every DAG has at least one source (highest post) and one sink (lowest post)
  * **Property**: Every DG is a DAG of it's SCCs.

`n = |V|` 

`m = |E|`

- Walks vs. Paths: a walk allows repeats.
- If a graph has a negative weight cycle it is not a well defined shortest path problem

### Explore

- **Property** 1: If explore subroutine is started at a node `u` then it will terminate precisely when all nodes reachable from `u` have been visited
- **Property 2**: Node that receives the highest `POST` number in a DFS must lie in a source Strongly Connected Component.
- **Property 3**: If `C` and `C'` are SCCs and there is an edge from a node in `C` to a node in `C'` then the highest post number in `C` is *bigger* than the highest post number in `C'`







### Depth First Search (DFS)

$$
O(n+m)
$$



### Breadth First Search (BFS)

$$
O(n+m)
$$



### Dijkstra

$$
O((n+m)logn)
$$





### 

### Bellman Ford

$$
O(n^2m)
$$



### Floyd-Warshall

$$
O(n^3)
$$



### Strongly Connected Components (SCC)

Found in two runs of DFS. `O(n+m)`



### Minimum Spanning Tree (MST)

An MST is:

- Connected
- Undirected
- Acyclic
- Of minimum total weight

A minimum spanning tree is found using Kruskal's or Prim's algorithm

#### Kruskal (Greedy)

`O(mlog(n))`



#### Prim

`O((m+n)log(n))`

### Max Flow



#### Ford Fulkerson



#### Edmond's Carp

`O(nm^2)`



#### Residual Graph





### Max Flow = Min Cut



### Image Segmentation



### Flow w/ Demands



### Graph Problems

- 2SAT
- Bipartite Matching
- Map Coloring
- Topological Sorting
- 



## NP Completeness

### Search Problems

Form: Given instance `I`

- Find a solution `S` for `I` if one exists
- Output `NO` if `I` has no solution

Requirement: to be a search problem:

If given an instance `I` and a solution `S` then we can verify that `S` is a solution to `I` in polynomial time (polynomial in `|I|`)

### N and NP

- N - 

### Reductions



### 3-SAT

Conjunctive Normal Form (CNF)



### Graph Problems



## Linear Programming (LP)



### Duality



### Max SAT



### Knapsack



### Halting

Undecideability



