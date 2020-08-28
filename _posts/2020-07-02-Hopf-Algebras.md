---
title: 'What is a Hopf Algebra?'
date: 2020-07-02
permalink: /posts/Hopf-Algebras/
tags:
  - Hopf Algebras
---

The goal of this blog post is to present the definition and basic consequences therein of a Hopf algebra. For those that read more of my blog posts, this post and [this one](https://almosttrivial.github.io/posts/Tensor-Categories/) are some preliminary notions and results for some awesome blog posts to come. Without further ado, what is a Hopf algebra?

Now, to the best of my knowledge there are a few ways to introduce Hopf algebras. The one I will present here is sort of categorical, but not too demanding if the reader is uncomfortable with category theory. Moreover, the motivation for why one considers such objects at all is actually one of the points I emphasize [here](https://almosttrivial.github.io/posts/Hopf-Algebras-and-Tensor-Categories-a-love-story/). Otherwise, admittedly the structure I will define might seem sort of "forced;" as if I am constructing it just for fun with no purpose. Well for now, what's wrong with a little fun?

To get into it, let us first recall what an associative unital \\(R\\)-algebra is (I believe one should state whether their algebra is associative or unital!). Abstractly, an associative unital \\(R\\)-algebra is a [monoid object](https://almosttrivial.github.io/posts/OnMonoidAndModuleObjects/) in the category of left \\(R\\)-modules. Formulaically, one considers a left \\(R\\)-module \\(A\\) with an element (suggestively denoted by) \\(1\_{A}\in A\\) and an \\(R\\)-bilinear map \\(\mu_{A}: A\times A\to A\\) (whose image is typically written just by juxtaposition) such that the following equalities hold

1. \\( (ab)c = a(bc)\\)
2. \\(1_{A}a = a = a1_{A}\\)

Notice that I am not requiring the algebra to be commutative! The reader might also be use to seeing the \\(R\\)-bilinearity of \\(\mu_{A}\\) written out formulaically as well among these two conditions. Now, the reason why I even introduced the notation \\(\mu_{A}\\) is so that we can rewrite 1 and 2 in a more enlightening way:

1'. \\( \mu_{A}(\mu_{A}(a,b),c) = \mu_{A}(a,\mu_{A}(b,c))\\)
2'. \\( \mu_{A}(1_{A},a) = a = \mu_{A}(a,1_{A})\\)

Okay.
