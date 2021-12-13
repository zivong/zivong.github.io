---
layout: post
title: Notes on Rudin's Principles of Mathematical Analysis
category: Notes
tags: [mathematics, analysis]
math: true
---
[Walter Rudin](https://en.wikipedia.org/wiki/Walter_Rudin)'s [*Principles of Mathematical Analysis*](https://web.math.ucsb.edu/~agboola/teaching/2021/winter/122A/rudin.pdf) was originally published in 1953. The version I read is the 3rd edition published in 1976.

In addition to this book, Rudin had also written other two higher-level books on analysis: [*Real and Complex Analysis*](https://59clc.files.wordpress.com/2011/01/real-and-complex-analysis.pdf) and [*Functional Analysis*](https://59clc.files.wordpress.com/2012/08/functional-analysis-_-rudin-2th.pdf). These three books are familiarly known to students as "Baby Rudin", "Papa Rudin", and "Grandpa Rudin".

- toc
{: toc }

## Preface

> Experience has convinced me that it is pedagogically unsound (though logically correct) to start off with the construction of the real numbers from the rational ones. At the beginning, most students simply fail to appreciate the need for doing this. Accordingly, the real number system is introduced as an ordered field with the least-upper-bound property, and a few interesting applications of this property are quickly made. However, Dedekind's construction is not omitted. It is now in an Appendix to Chapter 1, where it may be studied and enjoyed whenever the time seems ripe.

## Chapter 1. The Real and Complex Number Systems

### Introduction

The rational number system is inadequate for describing continuous quantity. For example, according to the Pythagorean theorem, the diagonal length \\(l\\) of a square with unit sides satisfies \\(l^2=2\\), but it's easy to prove that \\(l\\) couldn't be any rational number. We denote \\(l\\) by \\(\sqrt{2}\\), and call \\(\sqrt{2}\\) is an "irrational number". We can use a sequence of rational numbers to tend to \\(\sqrt{2}\\).

> But unless the irrational number \\(\sqrt{2}\\) has been clearly defined, the question must arise: Just what is it that this sequence "tends to"?

Let \\(A\\) be the set of all positive rationals \\(p\\) such that \\(p^2 < 2\\) and let \\(B\\) consist of all positive rationals \\(p\\) such that \\(p^2 > 2\\). Now we associate each rational \\(p\\) with a number \\(q\\):

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

- If \\(p\in A\\), then \\(p^2 < 2\\). (1) shows that \\(q > p\\), and (2) shows that \\(q^2 < 2\\), thus \\(q \in A\\).
- If \\(p\in B\\), then \\(p^2 > 2\\). (1) shows that \\(q < p\\), and (2) shows that \\(q^2 > 2\\), thus \\(q \in B\\).

That means *\\(A\\) contains no largest number and \\(B\\) contains no smallest*.

An irrational number cuts the rational set into left and right halves, the left set has no largest number and the right set has no smallest; in reverse, we can use the combination of the left and right sets to represent this irrational number. This is the idea of [Dedekind's cut](https://en.wikipedia.org/wiki/Dedekind_cut).

{% include mathjax-equation-numbering.html %}

### Ordered Sets

An *order* on a set \\(S\\) is a relation, denoted by \\(<\\), with the following properties:

1. If \\(x,y \in S\\), then one and only one of the following statements

   $$
   x < y, x = y, y < x
   $$

   is true.

2. If \\(x,y,z \in S\\) and \\(x < y, y < z\\), then \\(x < z\\).

An *ordered set* is a set on which an order is defined.

Suppose \\(S\\) is an ordered set, and \\(E \subset S\\). If there exists a \\(\beta \in S\\) such that \\(x \leq \beta\\) for every \\(x \in E\\), we say that \\(E\\) is *bounded above*, and call \\(\beta\\) an *upper bound* of \\(E\\). We can also define the concepts of *bounded below* and *lower bound* in a similar way.

The *least upper bound* of \\(E\\) is also called the *supremum* of \\(E\\), and denoted by \\(\sup E\\); the *greatest lower bound* of \\(E\\) is also called the *infimum* of \\(E\\), and denoted by \\(\inf E\\).

An ordered set \\(S\\) is said to have the *least-upper-bound* property, if the following is true: If \\(E\subset S\\), and \\(E\\) is bounded above, then \\(\sup E\\) exists in \\(S\\).

The rational set \\(\mathbf{Q}\\) has no the least-upper-bound property. The least-upper-bound property could be thought of as another expression of continuity.

Theorem: Every ordered set with the least-upper-bound property also has the greatest-lower-bound property.

Proof: Suppose \\(S\\) is an ordered set with the least-upper-bound property and \\(E \subset S\\) is bounded below. Let \\(B\\) be the set of all lower bounds of \\(S\\), then for every \\(x \in B\\) and \\(y \in S\\), we have \\(x \leq y\\). Thus \\(B\\) is bounded above, \\(\sup B\\) exists in \\(S\\). For every \\(y \in S\\), \\(\sup B \leq y\\) holds since \\(y\\) is an upper bound of \\(B\\). Thus \\(\sup B\\) is a lower bound of \\(S\\). On the other side, for every \\(x \in B\\), \\(x \leq \sup B\\) holds since its definition. Thus \\(\sup B = \inf S\\). \\(\blacksquare\\)

### Fields
