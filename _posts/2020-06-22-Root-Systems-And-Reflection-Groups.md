---
title: 'Root Systems and Reflection Groups'
date: 2020-06-22
permalink: /posts/RootSystemsAndReflectionGroups/
tags:
  - Lie Algebras
  - Group Theory
---

I first came across the notion of root systems from [Humphreys](https://books.google.com/books/about/Introduction_to_Lie_Algebras_and_Represe.html?id=gCUlAQAAIAAJ). Leading up to that section, Humphreys presents the root space decomposition of a finite-dimensional semisimple Lie algebra, and at the end he notes some interesting properties that these roots have. These proeprties seem rather forced observatio a priori, but upon learning about the general theory of root systems, it becomes rather amazing that root systems do indeed arise in the theory of semisimple Lie algebras.

This connection between something as algebraic like Lie algebras with something as geometric and, to an extent, combinatorial like root systems has deep consequences. Namely, from classifying (reduced crystallographic) root systems, one can classify all possible simple Lie algebras; see [here](https://almosttrivial.github.io/posts/SimpleClassification/) for details.

However, root systems arise beyond just this classical study, appearing in more general constructions like affinization, superification, and quantization of Lie algebras. They also have deep connections to a family of groups known as Coxeter groups, and this is the perspective I plan on expanding upon here and in future blog posts. In particular, I will predominantly be following another book of [Humphreys](https://books.google.com/books/about/Reflection_Groups_and_Coxeter_Groups.html?id=ODfjmOeNLMUC).

The theory of root systems takes place in a real Euclidean space \\(V\\) equipped with a positive-definite symmetric bilinear form \\((\lambda,\mu)\\). In such a space, one can associate to any vector \\(\alpha\in V\\) the linear operator of **reflection** along \\(\alpha\\) i.e. the linear map

\begin{equation*}
   s\_{\alpha}(\lambda) := \lambda - \frac{2(\lambda,\alpha)}{(\alpha,\alpha)}\alpha
\end{equation*}

Note that this operator fixes pointwise every vector orthogonal to \\(\alpha\\) and send \\(\alpha\mapsto-\alpha\\). Moreover, this map is an orthogonal involution i.e.

\begin{equation*}
   (s\_{\alpha}(\lambda),s\_{\alpha}(\mu)) = (\lambda,\mu),\quad\quad s\_{\alpha}^{2} = \text{id}
\end{equation*}
