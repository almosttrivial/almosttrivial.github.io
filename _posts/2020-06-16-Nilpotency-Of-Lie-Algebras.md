---
title: 'Nilpotency Of Lie Algebras'
date: 2020-06-16
permalink: /posts/NilpotencyOfLieAlgebras/
tags:
  - Lie Algebras
---

I wrote in an earlier blog post that the adjoint representation of a Lie algebra was a very informative representation. This blog post will explore one of the quintessential notions of a Lie algebra which is formulated in terms of the Lie bracket ([deja vu](https://almosttrivial.github.io/posts/SolvabilityofLieAlgebras/)): nilpotency.

First, consider the following sequence of subspaces of a Lie algebra \\(\mathfrak{g}\\):

\\(    \mathfrak{g}^{1} := \mathfrak{g},\quad \mathfrak{g}^{k} := \left[\mathfrak{g},\mathfrak{g}^{k}\right]\\)

Then the following two observations are readily proved

* \\(\mathfrak{g}^{k+1}\subseteq\mathfrak{g}^{k}\\) for each \\(k\\).
    
* \\(\mathfrak{g}^{k}\\) is an ideal for each \\(k\\).

The reader is encouraged to verify these statements themselves.

The series \\(\\{\mathfrak{g}^{k}\\}\_{k\in\mathbb{N}}\\) is called the \\(\textbf{lower central series}\\) of \\(\mathfrak{g}\\). Now, one may ask whether the lower central series is infinite or if it eventually stabilizes in some sense for large enough \\(k\\). This leads to the notion of nilpotency:

\\(\textbf{Definition}\\) A Lie algebra is \\(\textbf{nilpotent}\\) if there exists \\(k\\) such that \\(\mathfrak{g}^{k} = \\{0\\}\\).

Now, before the aforementioned deja vu gets overwhelming, the attentive reader might notice that this series is reminisicent of the derived series, and hence nilpotency seems similar to solvability. And their suspicions are valid! Indeed, the following inclusion is trivial to show by induction

\\(\mathfrak{g}^{(k-1)}\subseteq\mathfrak{g}^{k}\\)

Hence, every nilpotent Lie algebra is indeed solvable. However, the inclusion need not hold! Indeed, consider the two dimensional Lie algbera with basis vectors \\(x \\) and \\(y\\) with the bracket defined by \\([x,x] = [y,y] = 0 = [x,y] - y\\). Then one readily sees that

\\(\mathfrak{g}^{(2)} = [\mathfrak{g}^{(1)},\mathfrak{g}^{(1)}] = [[\mathfrak{g},\mathfrak{g}],[\mathfrak{g},\mathfrak{g}]] = [\mathbb{C}y,\mathbb{C}y] = \{0\}\\)

while \\(\mathfrak{g}^{k} = \mathbb{C}y\\) for all \\(k\geq 2\\). Hence, there are some properties particular for nilpotent Lie algberas that do not necessarily hold for solvable Lie algebras, but of course any result about solvable Lie algebras also holds for nilpotent Lie algebras. In particular, we have the following three properties on nilpotency, the proofs to which are nicely presented in Humphreys (put a section/reference):

* If \\(\mathfrak{g}\\) is solvable, then so are all subalgebras and homomorphic images of \\(\mathfrak{g}\\).
    
* If \\(I\\) is a solvable ideal of \\(\mathfrak{g}\\) such that \\(\mathfrak{g}/I\\) is solvable, then \\(\mathfrak{g}\\) is also solvable.
    
* If \\(I\\) and \\(J\\) are solvable ideals, then so is \\(I + J\\).




The last property is a particularly important one since it implies that for any Lie algebra, there is a maximal solvable ideal, where here maximal means it is not properly contained in a solvable ideal. The existence of this unique ideal is trivial: just add all solvable ideals! This is called the \\(\textbf{radical}\\) of \\(\mathfrak{g}\\) and is denoted by \\(\text{Rad}(\mathfrak{g})\\). In the event that there are no nontrivial solvable ideals, \\(\text{Rad}(\mathfrak{g}) = \\{0\\}\\) and the Lie algebra is called \\(\textbf{semisimple}\\).

The maximality of the radical paired with the second solvability property above readily implies that \\(\mathfrak{g}/\text{Rad}(\mathfrak{g})\\) is semisimple. Given how easy it is to obtain a semisimple Lie algebra, it might not be a big surprise that a bulk of the theory on Lie algebras is with regards to semisimple Lie algebras. I discuss a few of the main properties here, here, and here. However, as I said, semisimplicity is so common, and its properties are so powerful, that most future blog posts about Lie algebras will be with regards to semisimple Lie algebras.

For now, I would like to present a very nice theorem that is not in Humphreys and that some Lie algebra classes seem to not go over, if at all mention. This is the Levi decomposition of a Lie algebra:

\\(\textbf{Theorem}\\)  If \\(\mathfrak{g}\\) is a finite dimensional Lie algebra over a characteristic zero field, then there exists a semisimple subalgebra \\(\mathfrak{s}\subset\mathfrak{g}\\), complementary to the radical \\(\text{Rad}(\mathfrak{g})\\) such that

\\(   \mathfrak{g} = \mathfrak{s}\ltimes\text{Rad}(\mathfrak{g})\\)

This is called the \\(\textbf{Levi decomposition}\\) of \\(\mathfrak{g}\\), and \\(\mathfrak{s}\\) is called a \\(\textbf{Levi factor}\\). For those unfamiliar with Lie theory or perhaps this notation, the direct sum of Lie algebras can always be made into a Lie algebra, but decomposing a particular Lie algebra into a direct sum of such is not necessarily possible. Namely, in order to decompose a Lie algebra, the factors must actually be ideals of the initial Lie algebra, not just subalgebras. This is similar to in ring theory and group theory where one can decompose rings and groups into ideals and normal subgroups, respectively. I think I might write about this in a future blog post since the reason for this is nicely presented categorically.

For now, you might be wondering, well if this isn't a direct sum of ideals, what kind of decomposition is this? Well, the above decomposition is a semi-direct sum. For a discussion on semi-direct products and a proof on the Levi decomposition, see here. As for the rest of this blog post, I am about done. Taking the Levi decomposition for granted, it follows that to understand any finite dimensional Lie algebra, one can proceed to understand all solvable and semisimple Lie algebras. The latter will constitute a bulk of future blog posts, while the former is actually a very hard problem! Solvable Lie algebras behave poorly and get very complicated as you go up in dimensions. To my knowledge, the classification of solvable Lie algebras is only up to dimension 7 (REFERENCE). There are definitely some families and particular dimensions that one can make specific arguments for, but nothing as unifying as what is done for semisimple Lie algebras. Weird, right?
