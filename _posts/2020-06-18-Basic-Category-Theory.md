---
title: 'Push it to the Limit!'
date: 2020-06-18
permalink: /posts/Push-It-To-The-Limit/
tags:
  - Category Theory
---

* Definie (co)limints
* Define (co)products and (co)equalizers
* Mention (co)complete and the equivalences
* Natural Transformations
* Higher Category Theory
* Monoidal, Rigid, Braided, Ribbon, and Modular Categories


My first exposure to category theory was back in my first undergraduate course on abstract algebra. It was certainly ambitious of my professor to introduce students to group theory through a categorical lens, but I was absolutely hooked. Even now my research interests are very categorical in nature. However, there was one definition above all else that seemed a little more complicated to grasp: the notion of a **limit**. I was always comfortable with universal properties, but for the longest time it did not sink in how limits were just instances of universal properties. Interestingly, the picture can be generalized to a slightly more involved setting, but it truly makes compactifies and captures the essence of what a limit really is.

In this post, I will present the usual definition of a limit, then recall some other categorical definitions and show from that perspective what a limit really is. I am of course assuming the reader has familiarity with basic notions of category theory. If you would like a review, I recommend taking a tour of the [nLab](https://ncatlab.org/nlab/show/HomePage), reading the classic book by [Mac Lane](https://www.springer.com/gp/book/9780387984032), or more briefly going through [these notes](https://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

Without further ado, what exactly is a limit? To define limits we first need to define *digrams of shape \\(J\\)* and *cones over a functor*. Formally, a **diagram of shape \\(J\\) in a category \\(\mathcal{C}\\)** is just a functor \\(F:J\to\mathcal{C}\\). The reader might then wonder what's the point of calling a functor by any other name? Well, one is typically interested in the case when \\(J\\) is a small or even finite category. Recall that a category is called **small** if its collection of objects is in fact a set; it is called **finite** is the objects are a finite set. But at the end of the day, yes, a digram is just another term for a functor. In these two particular cases of interest, especially the latter, the *image of the functor* can be neatly seen as just a diagram in \\(\mathcal{C}\\). By the defining properties of a functor, this diagram is clearly *the same shape at \\(J\\)*.

Next, given \\(F:J\to\mathcal{C}\\) a digram of shape \\(J\\) in a category \\(\mathcal{C}\\), a **cone to \\(F\\)** is a pair consisting of an object \\(A\\) of \\(\mathcal{C}\\) and a family of morphisms \\(\\{\phi\_{X}:A\to F(X)\\}\_{X\in\text{Ob}(J)}\\) with the property that \\(\phi\_{Y} = F(f)\circ\phi\_{X}\\) for all morphisms \\(f:X\to Y\\). One typically denotes such a pair by \\((A,\phi)\\) with the assumption that \\(\phi\\) denotes the aforementioned family of morphisms.

Now that we have cones, we can define a limit! A **limit** of the diagram \\(F:J\to\mathcal{C}\\) is a cone \\((L,\psi)\\) to \\(F\\) such that for every other cone \\((A,\phi)\\) to \\(F\\) there exists a *unique* morphism \\(\theta:A\to L\\) such that \\(\phi\_{X} = \psi\_{X}\circ\theta\\). That is, a limit of a diagram \\(F\\) is a cone to \\(F\\) such that *all other cones to \\(F\\) factor through it*. This can be expressed as stating the following diagram commutes in all triangles

INSERT DIAGRAM

Of course one can then dualize this notion and define **cocones** and analogously **colimits,** but these are just cones and limits in the opposite category, so I will solely consider these latter terms. 

So what was so confusing to me about limits? Well more unsettling than confusing was actually the family of morphisms. I understand that one wants an object of \\(\mathcal{C}\\) that is *as close as possible* to the shape of \\(J\\), hence why we have maps at all. But the requirement that these components \\(\phi\_{X}\\) must satisfy the compatibility relation \\(\phi\_{Y} = F(f)\circ\phi\_{X}\\) seemed odd yet familiar. It took me a while to realize where I had seen such a relation before: natural transformations!

Recall that a natural transformation is in fact a morphism between functors which satisfy a compatibliity relation. Namely, if \\(F,G:\mathcal{C}\to\mathcal{D}\\) are functors, then a natural transformation \\(\eta:F\to G\\) is simply a family of morphisms \\(\eta\_{X}:F(X)\to G(X)\\) for every object \\(X\\) of \\(\mathcal{C}\\) such that \\(\eta\_{Y}\circ F(f) = G(f)\circ\eta\_{X}\\) for all morphisms \\(f:X\to Y\\). The compatiblity is equivalent to the following diagram commuting:

INSERT DIAGRAM

The similarity to the compatibility relation in the definition of a limit should be rather striking. The problem is now how can I realize any cone \\((A,\phi)\\) as some sort of natural transformation? The way to do this is actually really trivial and the obvious thing to do once you know it...care to guess? Well let's take a look at the compatibility relation once more: \\((A,\phi)\\) is a cone to \\(F\\) if \\(\phi\_{Y} = F(f)\circ\phi\_{X}\\) for all \\(f:X\to Y\\). I am now going to perform a wonderful trick:

\begin{equation\*}
  F(f)\circ\phi\_{X} = \phi\_{Y} = \phi\_{Y}\circ \text{id}\_{A}
\end{equation\*}

As trivial as this insertion of the identity morphism might appear, it immediately presents the udnerlying natural transformation structure going on here. Namely, if I want this to be a statement about a natural transformation, I obviously need another functor besides the diagram \\(F: J\to\mathcal{C}\\). Given the above equality, I will define the following functor \\(G:J\to\mathcal{C}\\) where I assign every object of \\(J\\) to *the same object* \\(A\\) and to every morphism of \\(J\\) I will just map them all to the identity morphism of \\(A\\). This is commonly called the **constant functor** and denoted by \\(\Delta(A)\\). 

Well this is it! Now every cone is in fact nothing more than a natural transformation from a choice of a constant functor! That is, \\((A,\phi)\\) is a cone to \\(F\\) if and only if \\(\phi:\Delta(A)\to F\\) is a natural transformation. If every cone is simply a natural transformation, then what does this say about limits? 

Now that we have natural transformations, let us take one step further in this generalization and define the following functor: \\(\Delta:\mathcal{C}\to\mathcal{C}^{J}\\), where the codomain category is the category of functors from \\(J\\) to \\(\mathcal{C}\\), and \\(\Delta: A\mapsto \Delta(A)\\). One might be wondering why would I create such a functor? Weren't the \\(\Delta(A)\\) functors enough? Now I have a functor into functors??? Yes, this is exactly what we're missing! One must recall that functors do not simply associate objects between categories, they must also map morphisms in a *compatible* way!

In particular, in order for my proposed functor \\(\Delta\\) to actually be a functor, I need to define what happens to any morphism \\(\varphi:A\to B\\). Well, the target category is a category of functors, so \\(\Delta(\varphi):\Delta(A)\to \Delta(B)\\) must be a *natural transformation*. Thus, it is equivalent to define a family of component morpshisms that satisfy the definition of natural transformation. To this end, if \\(X\\) and \\(Y\\) are objects of \\(J\\), then \\(\Delta(A)(X) = A = \Delta(A)(Y)\\) and \\(\Delta(B)(X) = B = \Delta(B)(Y)\\). Moreover, for any morphism \\(f:X\to Y\\) we have \\(\Delta(A)(f) = \text{id}\_{A}\\) and \\(\Delta(B)(f) = \text{id}\_{B}\\). Hence, the components \\(\Delta(\varphi)\_{X}\\) must satisfy

\begin{equation\*}
   \text{id}\_{B}\circ\Delta(\varphi)\_{X} = \Delta(\varphi)\_{Y}\circ\text{id}\_{A}
\end{equation\*}
which is to say, every component morphism *needs to be the same*! Well, given that we started with a morphism \\(\varphi:A\to B\\), we can just take the natural transformation whose components are all \\(\varphi\\)! Thus, \\(\Delta\\) is a functor defined by mapping each object of \\(\mathcal{C}\\) to the corresponding constant functor, as well as mapping each morphism in \\(\mathcal{C}\\) to the constant natural transformation whose components are all the input morphism!

We are now at the crux of compactly expressing what a limit is. To recap, a cone to \\(F\\) is just a natural transformation from a constant functor to \\(F\\). Moreover, there is a functor \\(\Delta:\mathcal{C}\to\mathca{C}^{J}\\) which maps every object to their respective constant functor, and sends every morphism to an analogous constant natural transformation. Now, the initial functor \\(F\\) is simply *an object* in \\(\mathcalC{C}^{J}\\). 



