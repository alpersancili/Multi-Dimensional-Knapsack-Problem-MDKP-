# Multi-Dimensional-Knapsack-Problem-MDKP-
This repository presents a Python implementation of the Multi-dimensional Knapsack Problem using dynamic programming. The code is designed to solve the problem efficiently for scenarios where items have weights in multiple dimensions, and the goal is to maximize the total value of the selected items without exceeding the capacities in any dimension

PROBLEM OVERVIEW

The Multi-dimensional Knapsack Problem is an extension of the classic knapsack problem. It arises in real-world optimization problems where:
Each item has weights in multiple dimensions (e.g., weight, volume, energy).
The knapsack has a capacity limit for each dimension.
The objective is to select a subset of items that maximizes the total value while staying within the capacity limits of all dimensions.

CODE EXPLANATION

1. Function: multi_dimensional_knapsack
The function multi_dimensional_knapsack solves the problem using a dynamic programming approach.

Input Parameters
values: A list of integers representing the values of the items.
weights: A list of lists, where each inner list represents the weights of an item across different dimensions.
capacities: A list of integers representing the capacities of the knapsack for each dimension.

Output
Returns the maximum value achievable without exceeding the capacity in any dimension.

Steps
Initialization:
Determine the number of items (n) and the number of dimensions (k).
Initialize a multi-dimensional dictionary (dp) to store the maximum value for every combination of capacities.

Dynamic Programming Table Update:
For each item, iterate over all possible capacity combinations in reverse to avoid overwriting.
Check if the item can be included in the current capacity combination (c).
If valid, calculate the new capacity tuple and update the DP table if including the item gives a better value.

Return Result:
The answer is stored in dp[tuple(capacities)], which represents the maximum value achievable with full capacity in all dimensions.

OUTPUT EXPLANATION

The algorithm computes the maximum value achievable while adhering to the given capacity constraints. Here's a breakdown of how the result 50 is obtained:

Item Details:
Item 1: Value = 10, Weights = [3, 2]
Item 2: Value = 20, Weights = [4, 3]
Item 3: Value = 30, Weights = [5, 6]

Optimal Solution:
The optimal solution involves selecting Item 2 (value = 20) and Item 3 (value = 30).
Total value = 20 + 30 = 50.

Capacity Verification:
Item 2 uses capacities [4, 3], leaving [6, 7].
Item 3 uses capacities [5, 6], leaving [1, 1].
Both items fit within the given capacities [10, 10].

Thus, the maximum value achievable is 50.
