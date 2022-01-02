---
layout: post
title: Reading Walter Rudin's "Principles of Mathematical Analysis"
category: Notes
tags: [mathematics, analysis]
math: true
---
Here are some notes I took while I was reading [Walter Rudin](https://en.wikipedia.org/wiki/Walter_Rudin)'s [*Principles of Mathematical Analysis*, 3rd Edition](https://web.math.ucsb.edu/~agboola/teaching/2021/winter/122A/rudin.pdf) (1976).

- toc
{: toc }

## Chapter 1. The Real and Complex Number Systems

### Introduction

Rational numbers are inadequate for handling continuous quantities such as the length of a line segment. For example, according to the Pythagorean theorem, the diagonal length \\(l\\) of a square with unit sides satisfies \\(l^2=2\\), but it's easy to prove that this equation has no rational solution.

For this example, Rudin gave a deeper look: Let \\(A\\) be the set of all positive rationals \\(p\\) such that \\(p^2 < 2\\) and let \\(B\\) consist of all positive rationals \\(p\\) such that \\(p^2 > 2\\), then *\\(A\\) contains no largest number and \\(B\\) contains no smallest.*

Proof: We associate with each rational \\(p > 0\\) the number

$$
\begin{equation}
q = p - \frac{p^2-2}{p+2} = \frac{2p+2}{p+2}
\end{equation}
$$

Then

$$
\begin{equation}
q^2 - 2 = \frac{2(p^2-2)}{(p+2)^2}
\end{equation}
$$

If \\(p \in A\\), then \\(p^2 < 2\\). So \\(q > p\\) since (1), and \\(q \in A\\) since (2). If \\(p \in B\\), then \\(p^2 > 2\\). So \\(q < p\\) since (1), and \\(q \in B\\) since (2). \\(\blacksquare\\)

{% include mathjax-equation-numbering.html %}

### Ordered Sets

An ordered set \\(S\\) is said to have the *least-upper-bound property* if the following is true: If \\(E \subset S\\), \\(E\\) is not empty and bounded above, then \\(\sup E\\) exists in \\(S\\).

From the example discussed in the last section, we know that the rational set \\(\mathbf{Q}\\) has no the least-upper-bound property. So the least-upper-bound property can be thought as another expression of continuity.

Theorem: *Every ordered set with the least-upper-bound property has also the greatest-lower-bound property.*

It's not hard to prove this theorem through rigorous but cumbersome logical argument, but we can instantly *understand* this theorem if we think about that the order on the set is "mirror symmetrical".

### Fields
