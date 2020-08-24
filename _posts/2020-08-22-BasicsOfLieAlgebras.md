---
title: 'Basics of Lie Algebras'
date: 2020-08-20
permalink: /posts/BasicsOfLieAlgebras/
tags:
  - Lie Algebras
---

THe goal of this blog post is to present some of the basic definitions and consequences of the structure of a Lie algebra. Some statements will be given with a citation to a proof in Humphreys. Others might be straightforward enough for the reader to work out, but if the proof is enlightening or interesting enough, then I will present a proof regardless of whether it is in Humphreys or not. 

Initially, a Lie algebra is just a (complex) vector space with a Lie bracket (MAKE HYPERLINK). As with most algebraic structures, there is a notion of sub object and quotient object. For instance, in groups one has subgroups and quotient groups by normal subgroups; rings have subrings and quotient rings by ideals; and Lie algebras have \textbf{subalgebras} and \textbf{quotient algberas} by \textbf{ideals} (not to be confused with ring ideals!). Specifically, if \\(\mathfrak{g}\\) is a Lie algebra with Lie bracket \\([\cdot,\cdot]\\), then a Lie subalgebra \\(\mathfrak{h}\\) of \\(\mathfrak{g}\\) is a subspace that is a Lie algebra by giving it the restricted Lie bracket of \\(\mathfrak{g}\\) i.e.

\\(    [\mathfrak{h},\mathfrak{h}]\subseteq\mathfrak{h}\subseteq\mathfrak{g}\\)



A stronger sub-object in a sense is that of an \textbf{ideal} of a Lie algebra. A subspace \\(I\\) of a Lie algebra \\(\mathfrak{g}\\) is an ideal if it is fixed by bracketing by the whole Lie algebra i.e.

\\(    [\mathfrak{g},I]\subseteq I\\)


Note that by the skew-symmetry of the Lie bracket, one does not need to distinguish between left- or right-ideals as in ring theory! The reason why being an ideal is stronger than a subalgebra is because all ideals are necessarily subalgebras. The converse need not be the case. Moreover, ideals allow us to define quotient Lie algebras. Namely, if \\(\mathfrak{g}\\) is a Lie algebra with \\(I\\) an ideal, then the quotient vector space \\(\mathfrak{g}/I\\) can be endowed with the structure of a Lie algebra by

\\( [x + I, y + I] := [x,y] + I\\)

This is indeed a (well-defined) Lie bracket on \\(\mathfrak{g}/I\\). In verifying this, it should also be clear why quotienting by a subalgebra does not necessarily yield a Lie algebra; consider the analogous situation in rings and groups.

Now, as in the other categories, subobjects and quotient objects are not just an object, but an object with a map! That is, again in the context of groups and rings, one has some sort of embedding and projection with these objects respectively. However, what should be the notion of Lie algebra homomorphism? Perhaps unsurprisingly, a \textbf{Lie algbera homomorphism} is a linear map between Lie algebras that preserves their corresponding Lie brackets i.e. a linear map \\(\phi:\mathfrak{g}\to\mathfrak{h}\\) between Lie algebras such that

\\(    \phi([x,y]\_{\mathfrak{g}}) = [\phi(x),\phi(y)]\_{\mathfrak{h}}\\)

Now given a Lie algebra homomorphism \\(\phi\\), one can define two corresponding objects: the \textbf{kernel} \\(\text{ker}(\phi)\\) and \textbf{image} \\(\text{im}(\phi)\\). It is clear to see that the former is always an ideal while the latter is always a subalgebra. Moreover, with these notions one can analogously define what it means for a Lie algebra homomorphism to be a monomorphism, epimorphism, and an isomorphism: a trivial kernel, the image is the whole codomain, and the homomorphism has both properties.

As with groups and rings, there are three isomorphism theorems that parallel those which the reader might be familiar with in the context of groups or rings:

%LIST THE THEOREMS


Homomorphisms of particular interests are those from a Lie algbera to the endomorphisms of a vector space. In particular, if \\(V\\) is a complex vector space, then a Lie algera homomorphism 

\\(\phi:\mathfrak{g}\to\\text{End}(V)\\)

is called a \textbf{representation} of \\(\mathfrak{g}\\). A representation is called finite-dimensional if the corresponding vector space is.

Representations of a Lie algebra play a particularly important role in classifying all complex semisimple Lie algebras (HYPERLINK SEMISIMPLE TO SOLVABILITY POST) due to the fact that a Lie algebra comes equipped with a representation on itself! This should not be too surprising; groups act on themselves by multiplication and conjugation, and rings similarly act by multiplication. Here, a Lie algebra only has its Lie bracket, so that is what we use. Namely, for any \\(x\in\mathfrak{g}\\) consider the map

\\(    \text{ad}(x) :\mathfrak{g}\to\mathfrak{g},\quad y\mapsto[x,y]\\)

This is clearly a linear map for every due to the bilinearity of the Lie bracket. This is commonly called "bracketing" by \\(x\\). One may then further consider the map sending an element to its adjoint map:

\\(    \text{ad}: \mathfrak{g}\to \text{End}(\mathfrak{g}),\quad x\mapsto \text{ad}(x)\\)

This map is also linear, again by the bilinearity of the Lie bracket. However, this map further preserves the Lie brackets! That is,

\\(    \text{ad}([x,y]) = [\text{ad}(x),\text{ad}(y)]\\)

Indeed, this is just the Jacobi identity! Thus, the Jacobi identity is equivalent to saying that the Lie bracket induces a representation of \\(\mathfrak{g}\\) on itself. This is called the \textbf{adjoint representation} of \\(\mathfrak{g}\\). It is a prolific representation that I will use in several futuer blog posts. One particularly nice property that I explore here (HYPERLINK TO NILPOTENCY) is that the adjoint representation in fact maps specifically into the derivations of \\(\textbf{g}\\), denoted \\(\text{Der}(\mathfrak{g})\\), where recall an endomorphism \\(\delta\\) of an algebra \\(A\\) (of course not necessarily associative!) is a \textbf{derivation} if 

\\(\delta(ab) = \delta(a)b + a\delta(b)\\)

for all \\(a,b\in A\\). Here, the juxtaposition denotes the multiplication in the algebra. Returning back to Lie algebras, the claim that each \\(\text{ad}(x)\\) is a deriviation is in fact simply another reformulation of the Jacobi identity! See here (HYPERLINK) for more about the derivations of a Lie algebra.

Now, if the adjoint representation wasn't cool enough, it will also serve as our first instance of an ideal. That is, recall that the kernel of any Lie algebra homomorphism is always an ideal. While \\(\text{ker}(\text{ad})\\) is no different, it is a significant ideal. Written out, it is easy to check that this ideal contains all \\(x\in\mathfrak{g}\\) such that for all \\(y\in\mathfrak{g}\\) one has \\(0 = \text{ad}(x)(y) = [x,y]\\). One commonly says that these are all of the elements of \\(\mathfrak{g}\\) that commute with the rest of the Lie algbera - some reasnoning can be found here. This ideal is hence denoted by \\(\text{ker}(\text{ad}) =: Z(\mathfrak{g})\\). By the first isomorphism theorem above, one thus has 

\\(    \text{ad}(\mathfrak{g}) \cong \mathfrak{g}/Z(\mathfrak{g})\\)

where the left-hand side is common notation for \\(\text{im}(\text{ad})\\). This isomorphism, while innocent, is very useful in proving several results about \\(\mathfrak{g}\\) itself - see here and here (HYPERLINK TO SOLVABILITY AND NILPOTENCY).

All in all, it might not be surprising that the Lie bracket provides so much information about the Lie algebra; consider how groups and rings acting on themselves yield tremendous resutls. But what is surprising is that there is a rather large bounty of results from just considering the adjoint action. I encourage you to check the hyperlinked blog posts above for exploration of these consequences.
