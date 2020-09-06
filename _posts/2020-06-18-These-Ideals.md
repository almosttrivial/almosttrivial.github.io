---
title: 'The Deal With These Ideals'
date: 2020-06-18
permalink: /posts/TheseIdeals/
tags:
  - Lie Algebras
---

The study of complex semisimple Lie algebras is a very well understand and marvelous thing. From the study of the structure of a semisimple Lie algbera, to their classification, and to their representation theory via highest weights; I recommend [Humphreys](https://www.springer.com/gp/book/9780387900537) for the interested reader. To those with familiarity whether through a formal class or self-studying, there are certain structures along the way that should have made an impression on you. In particular, certain ideals of a Lie algebra are very prolific and determine much of the structure of the overall Lie algebra. These include

1. The maximal solvable radical, commonly denoted \\(\text{Rad}(\mathfrak{g})\\).
2. The Killing form radical, commonly denoted \\(\mathfrak{g}^{\perp}\\).
3. The nilradical, or maximal nilpotent ideal, commonly denoted \\(\text{Nil}(\mathfrak{g})\\).
4. The nilpotent radical defined as the intersection of all kernels of irreducible finite-dimensional representations of \\(\mathfrak{g}\\), commonly denoted \\(\mathfrak{s}\\).

Admittedly I was not aware of the fourth ideal during my initial reading of Humphreys. However, I came across it on a [mathoverflow](https://mathoverflow.net/questions/149391/on-radicals-of-a-lie-algebra) post, and its relation with the other ideals were nice.

This post is meant to explore certain relations satisfied between these ideals and their proofs, ultimately leading to the interesting chain of ideals

\begin{equation}
   \mathfrak{s}\subseteq \text{Nil}(\mathfrak{g})\subseteq \mathfrak{g}^{\perp}\subseteq \text{Rad}(\mathfrak{g})
\end{equation}

Throughout this post, I am assuming my Lie algebra \\(\mathfrak{g}\\) is finite-dimensional and over a characteristic zero field \\(\mathbb{K}\\), which may have to be algebraically closed at times.

**Proposition** The maximal solvable ideal is the orthogonal complement to the derived subalgebra with respect to the Killing form i.e. \\(\text{Rad}(\mathfrak{g})) = \[\mathfrak{g},\mathfrak{g}\]^{\perp}\\).

**Proof**




**Proposition** \\(\[\mathfrak{g},\text{Rad}(\mathfrak{g})\] = \[\mathfrak{g},\mathfrak{g}\]\cap\text{Rad}(\mathfrak{g})\\).

**Proof**




**Proposition** \\(\[\mathfrak{g},\text{Rad}(\mathfrak{g})\] = \mathfrak{s}\\).

**Proof**




**Proposition** \\(\mathfrak{s}\subseteq \text{Nil}(\mathfrak{g})\\).

**Proof**
It clearly suffices to prove that \\(\mathfrak{s}\\) is nilpotent, which by Engel's theorem is equivalent to proving each element is ad-nilpotent.



**Proposition** \\(\text{Nil}(\mathfrak{g})\subseteq \mathfrak{g}^{\perp}\\).

**Proof**
To proceed we need only prove that every element of the nilradical is orthogonal to all of \\(\mathfrak{g}\\).



**Proposition** \\(\mathfrak{g}^{\perp}\subseteq \text{Rad}(\mathfrak{g})\\).

**Proof**
It suffices to prove that the Killing form radical is a solvable ideal.


Note that when the Lie algebra is semisimple all of the ideals coincide: they are in fact all zero! However, there are cases for which some ideals are zero while others are nonzero. For instance, 
