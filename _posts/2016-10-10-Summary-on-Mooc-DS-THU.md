---
layout: post
title: Summary on MOOC-DS-THU
tags: [algorithm]
---
Recently I took a MOOC -- Data Structure, by Professor Junhui Deng at THU. I am not a CS student, though I learned some basic courses like Algorithm and Computer Architecture. I treasure this chance of practicing programming as well as getting familiar with different data structures. Totally there are 12 assignments ([problem description](https://github.com/muchuanyun/Cpp_DS_exercise/blob/master/PA_text.md)), which can be classified to several groups according to the data structure being used. Here I would like to summarize my thinking regarding to each problem.

## Array

#### Range_Inquiry
The idea is straitforward: first we sort all the integral points, then use binary search to find the two indices for given query interval $$ [a,b]$$. What needs to be noticed is that the answer depends on the binary search result.

* What if we find $$ a $$ is in the sorted array?

So I use a `flag` to indicate the search result. Be careful with the array indexing (make sure it is legal).

#### Lighthouse
After the initial analysis, it is not hard to find that the problem can be transformed to find the number of inversions in an array. Imitating `mergesort`, the main idea here is recursion. Notice that the answer could overflow.

## List

#### Zuma
Once a new bead needs to be inserted, first we need find the insert position. Then check the beads before and after it, count the number of beads with the same color. If the count is less than 3, the insertion is valid, so we create a new bead and add it to the list. Otherwise, there is no need to add new bead, and we can just eliminate the adjacent two beads. Notice that after the elimination, there is possibility that there are three or more adjacent beads with same color in the new list. 

## Stack

#### Train
Focus on the top element of the stack.

## Tree

#### BinTree Rebuild
The core idea is recursion.

#### Temperature
An implementation of 2-d tree. Considering the efficiency, the leaf node can contain more than 1 point.


## Graph

#### TSP
The problem asks for the longest route in a DAG. First construct the graph as an _adjacent list_, and keep a value representing the maximum route lengthtill now for each node. Then apply the idea of topological sort. Use a stack to record the nodes with in-degree 0. If a node is visited, the in-degree of its neighbors minus 1.

#### Broadcast
Use BFS to color nodes. Note that the graph is undirected.

#### Toy
It is not hard to know a state transition graph is needed here. Every node has 3 children. Considering the efficiency, the graph should be built before the inquiry. For this case, there are $$ 8! $$ possible permutations. The hash function is a little tricky, check [Lehmer code](https://en.wikipedia.org/wiki/Lehmer_code) and [Numbering permutations](https://en.wikipedia.org/wiki/Permutation#Numbering_permutations). For each inquiry, use BFS to find the required (i.e. initial) state.

## Binary Heap

#### Schedule
An implementation of heap.

