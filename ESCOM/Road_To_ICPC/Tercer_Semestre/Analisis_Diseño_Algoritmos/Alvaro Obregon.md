### Problem Description

Álvaro and José are competing in the presidential election of Tepito, which is represented as a grid with 2 rows and nnn columns. Each cell in the grid corresponds to a house, and each house supports either Álvaro or José.

- The grid is divided into **districts**, each consisting of **3 connected houses**.
- A set of cells is connected if you can move between them using only up, down, left, or right.
- Every house belongs to exactly one district.
- Each district casts a vote for the candidate supported by at least **2 out of its 3 houses**.

Álvaro, as the current president, knows in advance the candidate supported by each house and wants to divide the districts to maximize the number of votes he receives.

### Input

The input consists of multiple test cases:

1. The first line contains a single integer ttt (1≤t≤104), the number of test cases.
2. For each test case:
    - The first line contains an integer nnn (3≤n≤105,n is a multiple of 3)(3 \leq n \leq 10^5, n \text{ is a multiple of } 3)(3≤n≤105,n is a multiple of 3), the number of columns in the grid.
    - The next two lines each contain a string of length nnn, representing the grid. Each character is either 'A' (supports Álvaro) or 'J' (supports José).

The sum of nnn across all test cases will not exceed 10510^5105.

### Output

For each test case, output a single integer: the maximum number of districts Álvaro can ensure he wins by optimally dividing the houses.