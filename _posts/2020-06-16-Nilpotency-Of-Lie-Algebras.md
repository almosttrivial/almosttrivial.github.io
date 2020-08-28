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

\\(\mathfrak{g}^{(2)} = [\mathfrak{g}^{(1)},\mathfrak{g}^{(1)}] = [[\mathfrak{g},\mathfrak{g}],[\mathfrak{g},\mathfrak{g}]] = [\mathbb{C}y,\mathbb{C}y] = \\{0\\}\\)

while \\(\mathfrak{g}^{k} = \mathbb{C}y\\) for all \\(k\geq 2\\). Hence, there are some properties particular for nilpotent Lie algberas that do not necessarily hold for solvable Lie algebras, but of course any result about solvable Lie algebras also holds for nilpotent Lie algebras. In particular, we have the following four properties on nilpotency, the first three of which have proofs in Humphreys (put a section/reference):

* If \\(\mathfrak{g}\\) is nilpotent, then so are all subalgebras and homomorphic images of \\(\mathfrak{g}\\).
    
* If \\(\mathfrak{g}/Z(\mathfrak{g})\\) is nilpotent, then so is \\(\mathfrak{g}\\).
    
* If \\(\mathfrak{g}\\) is nilpotent and nonzero, then \\(Z(\mathfrak{g})\neq\\{0\\}\\).

* If \\(I\\) and \\(J\\) are nilpotent ideals, so is \\(I + J\\).

The fourth property is an easy exercise, but just as with solvability, is a particularly important property since it implies that for any Lie algebra there is a maximal solvable ideal, where here maximal means it is not properly contained in a nilpotent ideal. The existence of this unique ideal is trivial: just add all nilpotent ideals! This is called the \\(\textbf{nilradical}\\) of \\(\mathfrak{g}\\) and is denoted by \\(\text{Nil}(\mathfrak{g})\\). 

Note that as \\(\text{Nil}(\mathfrak{g})\\) is nilpotent, it is solvable, and hence 

\\(\text{Nil}(\mathfrak{g})\subseteq \text{Rad}(\mathfrak{g})\\)

There is actually a nice nested chain of these ideals with a couple of other important ones, which I discuss [here](https://almosttrivial.github.io/posts/TheseIdeals/).

Returning to the present topic, there does not seem to be a name for Lie algebras with a zero nilradical. Nonetheless, given the result for solvable Lie algberas, one might expect that modding out a Lie algebra by its nilradical results in a Lie algebra with a zero nilradical. Unfortunately, this is not true! Indeed, consider the previous non-Abelian two dimensional Lie algebra example above. As any one-dimensional Lie algebra is Abelian, they are automatically nilpotent. Hence, if you set \\(\mathfrak{g}\\) for the aforementioned Lie algebra, \\(I = \mathbb{C}y\\) (or with \\(x\\)), then the corresponding quotient Lie algebra is one-dimensional, so nilpotent and thus equal to its nilradical i.e. it the quotient has a nontrivial nilradical!

Compared to the [Levi Decomposition](https://almosttrivial.github.io/posts/Levi-Decomposition/), this means that the corresponding short exact sequence with injecting and then projecting onto the nilradical does not split. 

Nonetheless, there are still several results one can prove about nilpotent Lie algebras. The first, which may not be surprising, is to consider the good ole adjoint representation! Namely:

\\(\textbf{Lemma}\\) If \\(\mathfrak{g}\\) is a nilpotent Lie algebra, then \\(\text{ad}(x)\\) is a \\(\textbf{nilpotent operator}\\) i.e. there exists an \\(n\\) such that \\(\text{ad}^{n}(x) = 0\\) as operators. 

\\(\textbf{Proof}\\) As \\(\mathfrak{g}\\) is nilpotent, suppose it is of nilpotent degree \\(k\\). Then for each \\(x,y\in\mathfrak{g}\\) one has \\(\text{ad}^{k - 1}(x)(y) \in L^{k} = \\{0\\}\\), which proves the result. \\(\Box\\)

Interestingly, the converse is also true! This is the content of [Engel's Theorem](https://almosttrivial.github.io/posts/EngelLieCartan/). This result is particularly interesting because these are two seemingly different notions of nilpotency. On the other side you have nilpotency for an abstract Lie algebra as defined here on the \\textbf{entire structure}, while the other form of nilpotency is something defined for \\(\textbf{each element (operator)}\\).

Allow me to preface [the proof](https://almosttrivial.github.io/posts/EngelLieCartan/) of Engel's theorem by proving a lemma that is interesting on its own right, but is used in the proof.

\\(\textbf{Lemma}\\) Let \\(\phi\in\mathfrak{gl}(V)\\) be a nilpotent endomorphism. Then \\(\text{ad}(\phi)\\) is nilpotent (an element of \\(\mathfrak{gl}(\mathfrak{gl}(V))\\)!).

\\(\textbf{Proof}\\) Consider the endomorphisms on \\(\mathfrak{gl}(mathfrak{gl}(V))\\) given by

\\(\lambda\_{\phi}(\psi) = \phi\circ\psi\\)

\\(\rho\_{\phi}(\psi) = \psi\circ\phi\\)

Since \\(\phi\\) is nilpotent, both \\(\lambda\_{\phi}\\) and \\(\rho\_{\phi}\\) are nilpotent oeprators on \\(\mathfrak{gl}(V)\\). However,

\\(\rho\_{\phi}(\lambda\_{\phi}(\psi)) = (\phi\circ\psi)\circ\phi = \phi\circ(\psi\circ\phi) = \lambda\_{\phi}(\rho\_{\phi}(\psi))\\)

i.e. left-composing and right-composing by \\(\phi\\) commute. Thus, as \\(\text{ad}(\phi) = \lambda\_{\phi} - \rho\_{\phi}\\), and the sum of nilpotent operators is nilpotent, the result follows. \\(\Box\\)
