---
title: 'Basics of Lie Algebras'
date: 2020-08-20
permalink: /posts/BasicsOfLieAlgebras/
tags:
  - Lie Algebras
---

The goal of this blog post is to present much of the inherit structure of a Lie algebra, as well as its corresponding representation theory; by "representation theory," I just mean the category of its respective modules. In particular, I will discuss substructures within a Lie algebra, how a Lie algebra acts on itself, and then specify a certain class of Lie algebras called semisimple Lie algebras. The representation theory for semisimple Lie algebras will be explored in another blog post.

Initially, a Lie algebra is just a (complex) vector space with a Lie bracket (MAKE HYPERLINK). As with most algebraic structures, there is a notion of a Lie subalgebra. Namely, if \\(\mathfrak{g}\\) is a Lie algebra with Lie bracket \\([\cdot,\cdot]\\), then a Lie subalgebra \\(\mathfrak{h}\\) of \\(\mathfrak{g}\\) is a subspace that is a Lie algebra by giving it the restricted Lie bracket of \\(\mathfrak{g}\\) i.e.

\\(    [\mathfrak{h},\mathfrak{h}]\subseteq\mathfrak{h}\subseteq\mathfrak{g}\\)



A stronger sub-object in a sense is that of an \textbf{ideal} of a Lie algebra. A subspace \\(I\\) of a Lie algebra \\(\mathfrak{g}\\) is an ideal if it is fixed by bracketing by the whole Lie algebra i.e.

\\(    [\mathfrak{g},I]\subseteq I\\)


Note that by the skew-symmetry of the Lie bracket, one does not need to distinguish between left- or right-ideals as in ring theory. The reason why being an ideal is stronger than a subalgebra is because all ideals are necessarily subalgebras. The converse need not be the case. Moreover, ideals allow us to define quotient Lie algebras. Namely, if \\(\mathfrak{g}\\) is a Lie algebra with \\(I\\) an ideal, then the quotient vector space \\(\mathfrak{g}/I\\) can be endowed with the structure of a Lie algebra by

\\( [x + I, y + I] := [x,y] + I\\)

This is indeed a (well-defined) Lie bracket on \\(\mathfrak{g}/I\\). In verifying this, it should also be clear why quotienting by a subalgebra does not necessarily yield a Lie algebra; consider the analogous situation in rings and groups where one needs ideals and normal subgroups as opposed to subrings and subgroups.

An important ideal I will point out is the center of a Lie algebra. It is denoted by \\(Z(\mathfrak{g})\\) and consists of all elements "commuting with the whole Lie algebra" i.e. \\(x\in Z(\mathfrak{g})\\) such that \\([x,y] = 0\\) for all \\(y\in\mathfrak{g}\\).

Now, in order to study Lie algebras, like most algebraic structures, one should also have a notion of morphism between them. To this end, the natural set of morphisms to consider are linear maps between Lie algebras which also preserve the Lie brackets i.e. a linear map \\(\phi:\mathfrak{g}\to\mathfrak{h}\\) between Lie algebras such that

\\(    \phi([x,y]\_{\mathfrak{g}}) = [\phi(x),\phi(y)]\_{\mathfrak{h}}\\)

Again being motivated by the study of other algebraic objects, there are two objects one can consider once the notion of morphisms has been introduced: the kernel and the image. Perhaps unsurprisingly, the kernel (resp. image) of any Lie algebra homomorphism is always an ideal (resp. a subalgebra). With this, there are three isomorphism theorems that parallel those which the reader might be familiar with in the context of groups or rings:

%LIST THE THEOREMS



Nonetheless, we use the interaction of a Lie algebra on itself through its own bracket to gain insight on its structure. To formalize this, consider the map

\\(    \text{ad}(x) :\mathfrak{g}\to\mathfrak{g},\quad y\mapsto[x,y]\\)

This is clearly a linear map for every \\(x\in\mathfrak{g}\\) by the bilinearity of the Lie bracket. This is called the adjoint map, or commonly "bracketing" by \\(x\\). One may then further consider the map sending an element to its adjoint map:

\\(    \text{ad}: \mathfrak{g}\to \text{End}(\mathfrak{g}),\quad x\mapsto \text{ad}(x)\\)

This map is also linear, again by the bilinearity of the Lie bracket. However, this map has a further interesting property: it preserves the Lie brackets! That is,

\\(    \text{ad}([x,y]) = [\text{ad}(x),\text{ad}(y)]\\)

Indeed, this is just the Jacobi identity! Thus, the Jacobi identity is equivalent to saying that the Lie bracket induces a representation of \\(\mathfrak{g}\\) on itself; more on this here (HYPERLINK).

The ideal \\(\text{ker}(\text{ad})\\) further emphasizes how significant the adjoint representation is: if \\(x\in\text{ker}(\text{ad})\\), then for all \\(y\in\mathfrak{g}\\) one has \\(0 = \text{ad}(x)(y) = [x,y]\\) i.e. \\(x\in Z(\mathfrak{g})\\). The converse is obvious, hence \\(\text{ker}(\text{ad}) = Z(\mathfrak{g})\\) and 

\\(    \text{ad}(\mathfrak{g}) \cong \mathfrak{g}/Z(\mathfrak{g})\\)

where the left-hand side is common notation for \\(\text{im}(\text{ad})\\). This isomorphism, while innocent, is very useful in proving several results about \\(\mathfrak{g}\\) itself. For instance, referring to the solvability and nilpotency blog posts, one clearly deduces that

\\(    \text{ad}(\mathfrak{g}) \text{ is solvable (resp. nilpotent)} \Longleftrightarrow \mathfrak{g} \text{ is solvable (resp. nilpotent)}\\)

This is particularly surprising because on one side we have an abstract Lie algebra, and on the other we have endomorphisms acting on it which is itself a Lie algebra, and the solvability and nilpotency is equivalent to that of the other. This equivalence is also used in the nilpotency blog post to prove Engel's theorem, which gives another equivalence for \\(\mathfrak{g}\\) being nilpotent.
