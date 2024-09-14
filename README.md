# Knapsack Problem

## Introduction

In computer science, time complexity is the computational complexity that descriebs the amount of computer time it takes to run an algorithm. It is estimated to by counting the number of elementary operations, assuming each takes a fixed amount of time.

Time complexity is typically expressed as a function of input size, with a focus on its asymptotic behaviour as input size increases, since the exact function is usually difficult to compute. Common examples are:
- Constant - the complexity is bounded by a value that does not depend on the size of the input (ex. accessing any single element in an array).
- Logarithmic - the ratio of the number of operations to the size of the input decreases and tend to zero as n increase (ex. operations in binary threes or binary search)
- Linear - runtime increases at most linearly with the size of the input
- Log-Linear - linear time complexity, multiplied by log n, a logarithmic time complexity
- Quadratic - runtime scales quadratically with the input (ex. bubble sort)
- Cubic - runtime scales cubically with the input
- Exponential - runtime doubles with each addition of the input n

A real-world application of time time complexity is the Knapsack problem. Given a set of items, each with a weight and a value, determine which items to include in the collection so that the total weight is less than or equal to a given limit and the total value is as large as possible. 

## Problem formulation

Most common class is the 0-1 Knapsack problem, which restricts the number of copies of each kind of item to zero or one.
Given a set of n items numbered from 1 to n, each with weight of w_1, and a value v_i, along with a maximum weight capacity W.

$$
\begin{align*}
\text{max} & \sum_{i=1}^{n} v_i \cdot x_i \\
\text{sub} & \sum_{i=1}^{n} w_i \cdot x_i \leq W \\ & x_i \in \{0, 1\}
\end{align*}
$$

The decision problem form is NP-complete, thus there is no known algorithm that is both correct and fast (in polynomial time) in all cases.

## Application in portfolio management

Given a portfolio of repos, each one with a daily interest expense and a cost to repay fully, what is the most expensive set of repos that I can afford to repay given my cash position?
As the number of repos increases... the number of possible combinations doubles each time.

## Different approaches

### Brute force

Check all possible combinations, sort by daily interest expense and select the most expensive repo package we can afford to repay,

