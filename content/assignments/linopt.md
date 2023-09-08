---
title: "Linear Optimization Assignment"
date: 2023-09-08T04:37:40\vec{z}
draft: false
toc: true
---

**Note:** Submit in R/Python.

## Assignment 1

### Input

1. Excel file with \\(m+2\\) rows and \\(n+1\\) columns in the form
\begin{equation}
\myvec{\vec{c}^{\top} & 0 \\\\ \vec{\vec{z}}^{\top} & 0 \\\\ \vec{A} & \vec{b}}
\end{equation}

### Algorithm

1. Verify that \\(\vec{z}\\) is feasible.

2. while (\\(\vec{z}\\) is not a vertex):
    * divide \\(A\\) into tight rows \\(A\_1\\) and untight rows \\(A\_2\\).
    * Let \\(S\\) be the null space of \\(A\_1\\), and choose any \\(u \in S\\).
    * \\(\vec{z} \leftarrow \vec{z} + \alpha u\\).

3. while (\\(\vec{z}\\) is not an optimum vertex):
    * Let \\(A\_1\\) be tight rows and \\(A\_2\\) be untight rows.
    * Let \\(R\_i,\ 1 \le i \le n\\) be the rows of \\(A\_1\\).
    * Let \\(C\_i,\ 1 \le i \le n\\) be the rows of \\(A\_1^{-1}\\).
    * Let cost \\(c = \sum\_{i=1}^n\alpha\_iR\_i\\).
    * Suppose \\(\alpha\_j\\) is negative for some \\(j\\).
    * \\(\vec{z} \leftarrow \vec{z} - \beta C\_j\\) where \\(\beta > 0\\).

### Output

1. The sequences of vertices along with cost at vertex per line.
2. Vertices only, do NOT print initial vertex and cost.

# Assignment 2

## Input

Same as assignment 1

## Statement

Here, we assume that the polytope is unbounded and \\(A\\) is non-degenerate and rank of \\(A\\) is \\(n\\).

## Algorithm

1. Verify that \\(\vec{z}\\) is feasible.

2. while (\\(\vec{z}\\) is not a vertex):
    * divide \\(A\\) into tight rows \\(A\_1\\) and untight rows \\(A\_2\\).
    * Let \\(S\\) be the null space of \\(A\_1\\), and choose any \\(u \in S\\).
    * **Note:** Since the polytope is unbounded, we cannot move in the direction of \\(u\\) and guarantee that we reach a vertex. Instead, we move opposite to \\(u\\) i.e. \\(\vec{z} \leftarrow \vec{z} - \alpha u\\). This is because \\(A\\) has rank \\(n\\).

3. while (\\(\vec{z}\\) is not an optimum vertex):
    * Let \\(A\_1\\) be tight rows and \\(A\_2\\) be untight rows.
    * Let \\(R\_i,\ 1 \le i \le n\\) be the rows of \\(A\_1\\).
    * Let \\(C\_i,\ 1 \le i \le n\\) be the rows of \\(A\_1^{-1}\\).
    * Let cost \\(c = \sum\_{i=1}^n\alpha\_iR\_i\\).
    * Suppose \\(\alpha\_j\\) is negative for some \\(j\\).
    * \\(\vec{z} \leftarrow \vec{z} - \beta C\_j\\) where \\(\beta > 0\\).
    * **Note:** If objective function keeps increasing, then cost is unbounded, output error appropriately. 
