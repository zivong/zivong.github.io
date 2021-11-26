---
layout: post
title: Notes on Walter Rudin's Principles of Mathematical Analysis
category: Notes
tags: [mathematics, analysis]
math: true
---
[Walter Rudin](https://www.ams.org/notices/201303/rnoti-p295.pdf)'s [*Principles of Mathematical Analysis*](https://web.math.ucsb.edu/~agboola/teaching/2021/winter/122A/rudin.pdf) was first published in 1953. The version I read is the 3rd edition published in 1976.

- toc
{: toc }

## Preface

> This book is intended to serve as a text for the course in analysis that is usually taken by [advanced undergraduates](https://www.bgsu.edu/graduate/graduate-programs/advanced-undergraduate-status-policies-and-procedures.html) or by first-year students who study mathematics.

> Experience has convinced me that it is pedagogically unsound (though logically correct) to start off with the construction of the real numbers from the rational ones. At the beginning, most students simply fail to appreciate the need for doing this. Accordingly, the real number system is introduced as an ordered field with the least-upper-bound property, and a few interesting applications of this property are quickly made. However, Dedekind's construction is not omitted. It is now in an Appendix to Chapter 1, where it may be studied and enjoyed whenever the time seems ripe.

This teaching strategy is currently my favorite.

## 1. The Real and Complex Number Systems

### Introduction

The rational number system is inadequate for describing continuous quantity. A classical example is that the diagonal length \\(l\\) of a square with unit sides can not be a rational number; because by the Pythagorean theorem, \\(l^2=2\\), but it's easy to prove that this equation has no rational solution.

A more closely examination: Let \\(A\\) be the set of all positive rationals \\(p\\) such that \\(p^2 < 2\\) and \\(B\\) consist of all positive rationals \\(p\\) such that \\(p^2 > 2\\), then *\\(A\\) contains no largest number and \\(B\\) contains no smallest*.

To prove this, we associate each rational \\(p\\) with a number \\(q\\):

$$
\begin{equation}
    q = p - \frac{p^2 - 2}{p+2} = \frac{2p+2}{p+2}
\end{equation}
$$

Then

$$
\begin{equation}
    q^2 - 2 = \frac{2(p^2-2)}{(p+2)^2}
\end{equation}
$$

If \\(p \in A\\), then \\(p^2 < 2\\). (1) shows that \\(q > p\\), and (2) shows that \\(q^2 < 2\\), thus \\(q \in A\\).

If \\(p \in B\\), then \\(p^2 > 2\\). (1) shows that \\(q < p\\), and (2) shows that \\(q^2 > 2\\), thus \\(q \in B\\).

This example illustrates that there are some "gaps" in the rational number system; it's not a "continuous" number system.

### Ordered Sets

An *order* on set \\(S\\) is a relation, denoted by \\(<\\), with the following properties:

1. If \\(x,y \in S\\) then one and only one of the following statements

   $$
   x < y, x = y, y < x
   $$

   is true.

2. If \\(x,y,z \in S\\) and \\(x < y, y < z\\), then \\(x < z\\).

An *ordered set* is a set on which an order is defined.

If \\(E\\) is a subset of an ordered set \\(S\\), and there exists a \\(\beta \in S\\) such that \\(x \leq \beta\\) for every \\(x \in E\\), then we call \\(E\\) is *bounded above*, and \\(\beta\\) is an *upper bound* of \\(E\\). In the similar way, we can define the concepts of *bounded below* and *lower bound*.

The *least upper bound* of \\(E\\) is also called the *supremum* of \\(E\\), and denoted by \\(\sup E\\); the *greatest lower bound* of \\(E\\) is also called the *infimum* of \\(E\\), and denoted by \\(\inf E\\).

An ordered set \\(S\\) is said to have the *least-upper-bound property*, if for every non-empty subset \\(E\\) and \\(E\\) is bounded above, there exists a \\(\sup E\\) in \\(S\\).

The example discussed in [Introduction](#introduction) shows that the rational set \\(\mathbf{Q}\\) has no the least-upper-bound property. So can we say that the least-upper-bound property is an expression of continuity? No, because the integer set \\(\mathbf{Z}\\) has the least-upper-bound property, but we don't think it's continuous in our intuition. Maybe the least-upper-bound property plus the denseness can express the concept of continuity?

There is a close relation between greatest lower bounds and least upper bounds: *Every ordered set with the least-upper-bound property has also the greatest-lower-bound property*.

Proof: Suppose \\(S\\) is an ordered set with the least-upper-bound property, and \\(B \subset S\\) and \\(B\\) is bounded below. Let \\(L\\) be the set of all lower bounds of \\(B\\). \\(\sup L\\) exists in \\(S\\) since \\(S\\) has the least-upper-bound property. For every \\(x \in B\\), we have \\(\sup L \leq x\\) since \\(x\\) is an upper bound of \\(L\\). So that \\(\sup L\\) is a lower bound of \\(B\\). For every \\(x \in L\\), we have \\(x \leq \sup L\\), so that \\(\sup L\\) is the greatest lower bound of \\(B\\), i.e. \\(\sup L = \inf B\\). \\(\blacksquare\\)

### Fields

{% include mathjax-equation-numbering.html %}
