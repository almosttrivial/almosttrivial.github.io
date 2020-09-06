---
title: 'Basics of Category Theory'
date: 2020-06-18
permalink: /posts/Basics-of-Category-Theory/
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

Next, given \\(F:J\to\mathcal{C}\\) a digram of shape \\(J\\) in a category \\(\mathcal{C}\\), a **cone to \\(F\\)** is a pair consisting of an object \\(A\\) of \\(\mathcal{C}\\) and a family of morphisms \\(\{\phi\_{X}:A\to F(X)\}\_{X\in\text{Ob}(J)}\\) with the property that \\(\phi\_{Y} = F(f)\circ\phi\_{X}\\) for all morphisms \\(f:X\to Y\\).


