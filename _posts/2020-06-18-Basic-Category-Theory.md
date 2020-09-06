---
title: 'Basics of Category Theory'
date: 2020-06-18
permalink: /posts/Basics-of-Category-Theory/
tags:
  - Category Theory
---

* Definition of a category
* (Locally) small categories
* Opposite categories
* Functors, contravariant and covariant
* Discrete categories for the sake of limits
* Definie (co)limints
* Define (co)products and (co)equalizers
* Mention (co)complete and the equivalences
* Natural Transformations
* Higher Category Theory
* Monoidal, Rigid, Braided, Ribbon, and Modular Categories


My first exposure to Category Theory was in my first undergraduate course on abstract algebra. My professor presented several constructions of group theory in categorical terms and it admittedly confused several students, but it had me hooked. In hindsight it is rather ambitious to teach category theory simultaneously with a first exposure to algebra. However, it rationalized certain constructions and definitions that would otherwise be more abstract nonsense. It became one of my favorite topics since then, to now where I find myself working with monoidal categories with more structure e.g. ribbon categories, modular categories, etc.

So what exactly is a category? In short, it is a pair consisting of a collection of objects and a collection of arrows between these objects satisfying some relations. In more detail, one calls \\(\mathcal{C} = (\text{Ob}(\mathcal{C}),\text{Mor}(\mathcal{C}))\\) a category if

* For every morphism \\(\phi\\), there is are a pair of objects \\(\text{s}(\phi)\\) and \\(\text{t}(\phi)\\) called the **source** and **target** objects.
* For every pair of morphisms \\(\phi,\psi\\) such that \\(t(\phi) = s(\psi)\\), there is a third morphism, denoted by \\(\psi\circ\phi\\) called their **composition**, which satisfies \\(s(\psi\circ\phi) = s(\phi)\\) and \\(t(\psi\circ\phi) = t(\psi)\\) and an associtivity law \\((\psi\circ\phi)\circ\eta = \psi\circ(\phi\circ\eta)\\) whenever the compositions are defined.
* For every object \\(X\\) there is a morphism \\(\text{id}\_{X}\\) called the **identity morphism of \\(X\\)**, which satisfies \\(\text{id}\_{t(\phi)}\circ\phi = \phi = \phi\circ\text{id}\_{s(\phi)}\\)

I SHOULD REPHRASE THE MORPHISMS AS A FAMILY OF COLLECTION OF MORPHISMS. 

The diligent might have noticed I used the word *collection* when discussing objects and morphisms. This word choice is intentional since typically the objects we are looking at collectively do not form a set e.g. consider the collection of all sets. However, the objects themselves may be sets, and certainly the morphisms between objects will be sets, typically with more structure. Whent the collection of morphisms for any two objects is a set, the category is called **locally small**. I will assume further categories are locally small, but certain definitions do not necessarily require this.

At the start I mentioned that a category consists of *arrows.* The reason for this is morphisms can be visualized by directed arrows from the source to the target of the morphism much like sets maps or any function. In fact, since the morphisms are aware of the source and target objects, and every object at least has the identity morphism, some mathematicians would argue that a category is all about the morphisms. And indeed, I take this perspective and believe this is particularly crucial when discussing later topics like universal objects and *coobjects*.

Now, before exploring the versatility of categories and giving them more structures, just as in the study of other mathematical objects one should define a notion of *map between categories.* This is the premise of a **functor.** Specifically, given two categories \\(\mathcal{C}\\) and \\(\mathcal{D}\\), a functor \\(F:\mathcal{C}\to\mathcal{D}\\) is an association of objects and morphisms, with the morphisms *preserving the categorical structure;* consider the definition of group or ring homomorphisms. Thus,

\begin{equation\*}
F(\text{id}\_{X}) = \text{id}\_{F(X)},\quad F(\psi\circ\phi) = F(\psi)\circ F(\phi)
\end{equation\*}

where by an abuse of notation the compositions of the two categories are denoted by the same composition.

