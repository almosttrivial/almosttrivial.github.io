---
title: 'What is a Hopf Algebra?'
date: 2020-07-02
permalink: /posts/Hopf-Algebras/
tags:
  - Hopf Algebras
---

The goal of this blog post is to present the definition and basic consequences therein of a Hopf algebra. For those that read more of my blog posts, this post and [this one](https://almosttrivial.github.io/posts/Tensor-Categories/) are some preliminary notions and results for some awesome blog posts to come. Without further ado, what is a Hopf algebra?

Now, to the best of my knowledge there are a few ways to introduce Hopf algebras. The one I will present here is sort of categorical, but not too demanding if the reader is uncomfortable with category theory. Moreover, the motivation for why one considers such objects at all is actually one of the points I emphasize [here](https://almosttrivial.github.io/posts/Hopf-Algebras-and-Tensor-Categories-a-love-story/). Otherwise, admittedly the structure I will define might seem sort of "forced;" as if I am constructing it just for fun with no purpose. Well for now, what's wrong with a little fun?

To get into it, let us first recall what an associative unital \\(R\\)-algebra is (I believe one should state whether their algebra is associative or unital!). Abstractly, an associative unital \\(R\\)-algebra is a [monoid object](https://almosttrivial.github.io/posts/OnMonoidAndModuleObjects/) in the category of left \\(R\\)-modules. Formulaically, one considers a left \\(R\\)-module \\(A\\) with an element (suggestively denoted by) \\(1\_{A}\in A\\) and an \\(R\\)-bilinear map \\(\mu\_{A}: A\times A\to A\\) (whose image is typically written just by juxtaposition) such that the following equalities hold

1. \\( (ab)c = a(bc)\\)
2. \\(1\_{A}a = a = a1\_{A}\\)

Notice that I am not requiring the algebra to be commutative! The reader might also be use to seeing the \\(R\\)-bilinearity of \\(\mu_{A}\\) written out formulaically as well among these two conditions. Now, the reason why I even introduced the notation \\(\mu_{A}\\) is so that we can rewrite 1 and 2 in a more enlightening way:

1. \\( \mu\_{A}(\mu_{A}(a,b),c) = \mu\_{A}(a,\mu\_{A}(b,c))\\)
2. \\( \mu\_{A}(1\_{A},a) = a = \mu\_{A}(a,1\_{A})\\)

Now, you might be wondering how is this more enlightening if these are saying the same thing? Well notice that we can view the first equation as a requirement for multiplication on a triple of elements, but there is a very big subtlety here!

Before I state what the subtlety is, recall that \\(\mu_{A}\\) is \\(R\\)-bilinear. By the universal property of tensor products, there is an induced \\(R\\)-linear map \\(\mu\_{A}': A\otimes A\to A\\) such that on a simple tensor \\(x\otimes y\mapsto \mu\_{A}(x,y)\\). This then allows one to define an \\(R\\)-linear map on \\((A\otimes A)\otimes A\\) and \\(A\otimes (A\otimes A)\\), both to \\(A\otimes A\\), given by \\(\mu'\_{A}\otimes\text{id}\_{A}\\) and \\(\text{id}\_{A}\otimes\mu'\_{A}\\). Then what 1. above says is equivalent to

\\(\mu\_{A}'\circ(\mu'\_{A}\otimes\text{id}\_{A})((a\otimes b)\otimes c)) = \mu\_{A}'\circ(\text{id}\_{A}\otimes\mu\_{A}')(a\otimes (b\otimes c))\\)

