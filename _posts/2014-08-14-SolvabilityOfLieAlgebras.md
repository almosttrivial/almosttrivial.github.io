---
title: 'Solvability Of Lie Algebras'
date: 2014-08-14
permalink: /posts/2014/08/blog-post-3/
tags:
  - cool posts
  - category1
  - category2
---

I wrote in an earlier blog post (HYPERLINK blog post) that the adjoint representation of a Lie algebra was a very informative representation. This blog post will explore one of the quintessential notions of a Lie algebra which is formulated in terms of the Lie bracket: solvability.

First, consider the following subspaces of a Lie algebra \\(\mathfrak{g}\\):

\\(    \mathfrak{g}^{(0)} := \mathfrak{g},\quad \mathfrak{g}^{(k + 1)} := \left[\mathfrak{g}^{(k)},\mathfrak{g}^{(k)}\right]\\)

Then the following two observations are readily proved

* \\(\mathfrak{g}^{(k+1)}\subseteq\mathfrak{g}^{(k)}\\) for each \\(k\\).
    
* \\(\mathfrak{g}^{(k)}\\) is an ideal for each \\(k\\).

The reader is encouraged to verify these statements themselves.

The series \\(\\{\mathfrak{g}^{(k)}\\}\_{k\in\mathbb{N}}\\) is called the derived series. The first term in this series \\(\mathfrak{g}^{(1)}\\). is called the derived algebra of \\(\mathfrak{g}\\). I discuss its importance with other ideals here, as well as its connection to solvability here.

Now, one may ask whether the derived series is infinite or if it eventually stabilizes in some sense for large enough \\(k\\). This leads to the notion of solvability:

\\(\textbf{Definition}\\) A Lie algebra is \\(\textbf{solvable}\\) if there exists \\(k\\) such that \\(\mathfrak{g}^{(k)} = \\{0\\}\\).

One sometimes says \\(\mathfrak{g}\\) is solvable of degree \\(k\\) if this is the minimal integer such that the derived series terminates. Clearly, the Lie algebras of solvable degree 0 are trivial. For Lie algebras of solvable degree 1, recall a Lie algebra is Abelian if it equals its center:

\\(\textbf{Proposition}\\) \\(\mathfrak{g}^{(1)} = \\{0\\} \\) if and only if \\(\mathfrak{g}\\) is Abelian.

\\(\textbf{Proof}\\)    If \\(\mathfrak{g}\\) is Abelian, then for all \\(x\in\mathfrak{g}\\) one has \\([x,y] = 0\\) for every \\(y\in\mathfrak{g}\\). However, these brackets span \\(\mathfrak{g}^{(1)}\\), so indeed \\(\mathfrak{g}^{(1)} = 0 \\). Conversely, if \\(\mathfrak{g}\\) is not Abelian, then there exists \\(x\in \mathfrak{g}\backslash Z(\mathfrak{g})\\). Hence, there exists a \\(y\in\mathfrak{g}\\) such that \\([x,y]\neq 0\\) but \\([x,y]\in\mathfrak{g}^{(1)}\\) and this completes the proof. \\(\Box\\)

Thus, all Abelian Lie algebras are certainly solvable, but the converse does not hold. There is also an intermediate notion between being Abelian and solvable called nilpotent, which I describe here. The smallest examples of a solvable Lie algebra that is not Abelian is the two dimensional \\(\mathfrak{g} = \text{Span}\_{\mathbb{C}}\\{x,y\\}\\) such that \\([x,y] = y\\). This example is actually more significant than this as there are actually only two possible two-dimensional Lie algebras: this once and the Abelian one.

That this example is solvable is obvious since \\(\mathfrak{g}^{(1)} = \mathbb{C}y,\\) and any one dimensional Lie algebra is Abelian. But by definition, the Lie algebra \\(\mathfrak{g}\\) is not Abelian. It is also not nilpotent! (HYPERLINK not nilpotent). Another example of a solvable Lie algebra is the collection of upper-triangular matrices (which is also not nilpotent!).

We now present some powerful properties of solvability, the proofs to which are nicely presented in Humphreys (put a section/reference):

* If \\(\mathfrak{g}\\) is solvable, then so are all subalgebras and homomorphic images of \\(\mathfrak{g}\\).
    
* If \\(I\\) is a solvable ideal of \\(\mathfrak{g}\\) such that \\(\mathfrak{g}/I\\) is solvable, then \\(\mathfrak{g}\\) is also solvable.
    
* If \\(I\\) and \\(J\\) are solvable ideals, then so is \\(I + J\\).

The last property is a particularly important one since it implies that for any Lie algebra, there is a maximal solvable ideal, where here maximal means it is not properly contained in a solvable ideal. The existence of this unique ideal is trivial: just add all solvable ideals! This is called the \\(\textbf{radical}\\) of \\(\mathfrak{g}\\) and is denoted by \\(\text{Rad}(\mathfrak{g})\\). In the event that there are no nontrivial solvable ideals, \\(\text{Rad}(\mathfrak{g}) = \\{0\\}\\) and the Lie algebra is called \\(\textbf{semisimple}\\).

The maximality of the radical paired with the second solvability property above readily implies that \\(\mathfrak{g}/\text{Rad}(\mathfrak{g})\\) is semisimple. Given how easy it is to obtain a semisimple Lie algebra, it might not be a big surprise that a bulk of the theory on Lie algebras is with regards to semisimple Lie algebras. I discuss a few of the main properties here, here, and here. However, as I said, semisimplicity is so common, and its properties are so powerful, that most future blog posts about Lie algebras will be with regards to semisimple Lie algebras.

There are two more results pertaining to solvability that I would like to mention here. The first is a remark I made in an earlier blog post (HYPERLINK to ad(g)) regarding the image of a Lie algebra under its adjoint map. That is, recall the map sending an element to its adjoint map:

\\(    \text{ad}: \mathfrak{g}\to \text{End}(\mathfrak{g}),\quad x\mapsto \text{ad}(x)\\)

This is a representation of \\(\mathfrak{g}\\). Moreover, it has the property that

\\(    \text{ad}(\mathfrak{g}) \cong \mathfrak{g}/Z(\mathfrak{g})\\)

The following lemma is trivial to prove:

\\(\textbf{Lemma}\\) \\(\mathfrak{g}\\) is solvable if and only if \\(\text{ad}(\mathfrak{g})\\) is solvable.

\\(\textbf{Proof}\\) The forward implication is obvious by the first property of solvability since it is precisely a homomorphic image of the Lie algebra. As for the reverse direction, it follows from the property. Indeed, if \\(\text{ad}(\mathfrak{g})\\) is assumed to be solvable, then the isomorphic image \\(\mathfrak{g}/Z(\mathfrak{g})\\) is also solvable. But \\(Z(\mathfrak{g})\\) is a solvable ideal, so the second property yields the desired result, thus completing the proof. \\(\Box\\)

There is an analogous result in terms of nilpotency (HYPERLINK on nilpotency). Both of these equivalences are particularly cool because one side you have an abstract Lie algebra, while the other is a collection of Lie algebra homomorphisms on the Lie algebra. This furthers a point I made in an earlier blog post that understanding the Lie bracket naturally provides insight on the structure of the Lie algebra.

The last result on solvability I want to state is a very nice theorem that is not in Humphreys and that some Lie algebra classes seem to not go over, if at all mention:

\\(\textbf{Theorem}\\)  If \\(\mathfrak{g}\\) is a finite dimensional Lie algebra over a characteristic zero field, then there exists a semisimple subalgebra \\(\mathfrak{s}\subset\mathfrak{g}\\), complementary to the radical \\(\text{Rad}(\mathfrak{g})\\) such that

\\(   \mathfrak{g} = \mathfrak{s}\ltimes\text{Rad}(\mathfrak{g})\\)

This is called the \\(\textbf{Levi decomposition}\\) of \\(\mathfrak{g}\\), and \\(\mathfrak{s}\\) is called a \\(\textbf{Levi factor}\\). For those unfamiliar with Lie theory or perhaps this notation, the direct sum of Lie algebras can always be made into a Lie algebra, but decomposing a particular Lie algebra into a direct sum of such is not necessarily possible. Namely, in order to decompose a Lie algebra, the factors must actually be ideals of the initial Lie algebra, not just subalgebras. This is similar to in ring theory and group theory where one can decompose rings and groups into ideals and normal subgroups, respectively. I think I might write about this in a future blog post since the reason for this is nicely presented categorically.

You might be wondering, well if this isn't a direct sum of ideals, what kind of decomposition is this? Well, the above decomposition is a semi-direct sum. For a discussion on semi-direct products and a proof on the Levi decomposition, see here. As for the rest of this blog post, I am about done. Taking the Levi decomposition for granted, it follows that to understand any finite dimensional Lie algebra, one can proceed to understand all solvable and semisimple Lie algebras. The latter will constitute a bulk of future blog posts, while the former is actually a very hard problem! Solvable Lie algebras behave poorly and get very complicated as you go up in dimensions. To my knowledge, the classification of solvable Lie algebras is only up to dimension 7 (REFERENCE). There are definitely some families and particular dimensions that one can make specific arguments for, but nothing as unifying as what is done for semisimple Lie algebras. Weird, right?
