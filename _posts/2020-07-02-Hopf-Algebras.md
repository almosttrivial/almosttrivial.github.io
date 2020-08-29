---
title: 'What is a Hopf Algebra?'
date: 2020-07-02
permalink: /posts/Hopf-Algebras/
tags:
  - Hopf Algebras
---

The goal of this blog post is to present the definition and basic consequences therein of a Hopf algebra. For those that read more of my blog posts, this post and [this one](https://almosttrivial.github.io/posts/Tensor-Categories/) are some preliminary notions and results for some awesome blog posts to come. Without further ado, what is a Hopf algebra?

Now, to the best of my knowledge there are a few ways to introduce Hopf algebras. The one I will present here is sort of categorical, but not too demanding if the reader is uncomfortable with category theory. Moreover, the motivation for why one considers such objects at all is actually one of the points I emphasize [here](https://almosttrivial.github.io/posts/Hopf-Algebras-and-Tensor-Categories-a-love-story/). Otherwise, admittedly the structure I will define might seem sort of "forced;" as if I am constructing it just for fun with no purpose. Well for now, what's wrong with a little fun?

The tl;dr is that a Hopf algebra is a bialgebra with an antipode, where moreover a bialgebra is an algebra and coalgebra with a compatibility condition.

To flesh out the details, let us first recall what is an associative unital \\(R\\)-algebra over a commutative (associative and unital) ring \\(R\\). In particular, as \\(R\\) is assumed to be commutative, there is no distinction between left and right \\(R\\)-modules. Then abstractly, an associative unital \\(R\\)-algebra is a [monoid object](https://almosttrivial.github.io/posts/OnMonoidAndModuleObjects/) in the category of \\(R\\)-modules. Formulaically, an \\(R\\)-algebra is a triple \\((A,\mu\_{A},\iota\_{A})\\) consisting of an \\(R\\)-module \\(A\\) with an \\(R\\)-bilienar map \\(\mu\_{A}: A\otimes A\to A\\) and an element \\(1\_{A}\\) such that

1. \\( \mu\_{A}(\mu_{A}(a,b),c) = \mu\_{A}(a,\mu\_{A}(b,c))\\)
2. \\( \mu\_{A}(1\_{A},a) = a = \mu\_{A}(a,1\_{R})\\)

Some readers might be familiar with a slightly different formulation of an associative unital \\(R\\)-algebra, but I'm sure your notion is equivalent to this. The reason why I like this formulation is that it makes it really easy to define a coalgebra. To do this, we need to point out a couple of subtleties with these two conditions.

For the first, recall that \\(\mu_{A}\\) is required to be \\(R\\)-bilinear. By the universal property of tensor products, there is an induced \\(R\\)-linear map \\(\mu\_{A}': A\otimes A\to A\\) such that on a simple tensor \\(x\otimes y\mapsto \mu\_{A}(x,y)\\). This then allows one to define an \\(R\\)-linear map on \\((A\otimes A)\otimes A\\) and \\(A\otimes (A\otimes A)\\), both to \\(A\otimes A\\), given by \\(\mu'\_{A}\otimes\text{id}\_{A}\\) and \\(\text{id}\_{A}\otimes\mu'\_{A}\\). Then the associativity is equivalent to

\\((\mu\_{A}'\circ(\mu'\_{A}\otimes\text{id}\_{A}))((a\otimes b)\otimes c) = (\mu\_{A}'\circ(\text{id}\_{A}\otimes\mu\_{A}'))(a\otimes (b\otimes c))\\)

Since linear maps from a tensor product are equivalent to bilinear maps from the underlying direct product, clearly \\(\mu\_{A}'\\) uniquely determines \\(\mu\_{A}\\), so I will drop the prime notation. 

Now, going back to the subtlety I was promising: the equality in 1 is not on **the same triple of elements!** Indeed, the above expression in terms of tensor maps shows the domain of the left hand side and right hand side are \\((A\otimes A)\otimes A\\) and \\(A\otimes (A\otimes A)\\), respectively. These spaces are **not the same** spaces, they are **isomorphic as \\(R\\)-modules!** If we turn to the language of diagrams, the associativity of our multiplication is equivalent to the commutativity in the following diagram

PUT THE DIAGRAM

For the second condition, recall that having this unit allows one to define the following \\(R\\)-linear map \\(\iota\_{A}: R\to A\\) given by \\(r\mapsto \phi(r)(1\_{A})\\) where \\(\phi: R\to\text{End}(A)\\) is the \\(R\\)-module structure on \\(A\\). In particular, note that since \\(\phi\\) is a ring homomrphism and preserves the identity

\\(\iota\_{A}(1\_{R}) = \phi(1\_{R})(1\_{A}) = \text{id}\_{A}(1\_{A}) = 1\_{A}\\)

From this, it follows that \\(\iota\_{A}\\) has its image contained in the center of \\(A\\):

\\(\mu\_{A}(\iota\_{A}(r),x) = \mu\_{A}(\phi(r)(\iota\_{A}(1\_{R})),x) = \phi(r)(\mu\_{A}(1\_{A},x)) = \phi(r)(x)\\)

where the equalities come from the \\(R\\)-linearity of \\(\iota\_{A}\\), the \\(R\\)-bilinearity of \\(\mu\_{A}\\), and that \\(1\_{A}\\) is a unit. Similarly

\\(\mu\_{A}(x,\iota\_{A}(r)) = \mu\_{A}(x,\phi(r)(\iota\_{A}(1\_{R}))) = \phi(r)(\mu\_{A}(x,1\_{A})) = \phi(r)(x)\\)

Thus, the image is in the center and in particular

\begin{equation}
\mu_{A}(\iota_{A}(r),x) = \phi(r)(x) = \mu_{A}(x,\iota_{A}(r))
\end{equation}
Suppose instead that one started with t

