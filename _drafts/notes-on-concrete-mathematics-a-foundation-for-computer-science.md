---
layout: post
title: 'Notes on Concrete Mathematics: A Foundation for Computer Science'
category: Notes
tags: [computer, mathematics]
math: true
---
[*Concrete Mathematics: A Foundation for Computer Science*](https://www.csie.ntu.edu.tw/~r97002/temp/Concrete%20Mathematics%202e.pdf) by [Ronald Graham](http://www.math.ucsd.edu/~fan/ron/), [Donald Knuth](https://www-cs-faculty.stanford.edu/~knuth/), and Oren Patashnik was first published in 1989. The version I read is the 2nd edition published in 1994.

- toc
{: toc }

## 1. Recurrent Problems

> THIS CHAPTER EXPLORES three sample problems that give a feel for what's to come. They have two traits in common: They've all been investigated repeatedly by mathematicians; and their solutions all use the idea of *recurrence*, in which the solution to each problem depends on the solutions to smaller instances of the same problem.

### 1.1 The Tower of Hanoi

The Tower of Hanoi was invented by the French mathematician [Edouard Lucas](https://en.wikipedia.org/wiki/%C3%89douard_Lucas) in 1883. We are given a tower of \\(n\\) disks, initially stacked in decreasing size on one of three pegs. The objective is to transfer the entire tower to one of the other pegs, moving only one disk at a time and never moving a larger one onto a smaller.

One way to solve this type of problem is to apply **"recursive thinking."** Let \\(T_n\\) be the minimum number of moves that will transfer \\(n\\) disks from one peg to another under Lucas' rules. For moving \\(n\\) disks from peg A to peg C, we have to move \\(n-1\\) disks from peg A to peg B, and then move the last disk from peg A to peg C, and finally move the \\(n-1\\) disks from peg B to peg C. So we have

$$
T_n = 2T_{n-1} + 1
$$

Then

$$
T_n + 1 = 2 (T_{n-1} + 1)
$$

So that

$$
T_n + 1 = 2^n(T_0 + 1)
$$

Obviously, \\(T_0 = 0\\), so we have

$$
T_n = 2^n - 1
$$

### 1.2 Lines in the Plane
