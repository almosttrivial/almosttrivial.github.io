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


My first exposure to category theory was back in my first undergraduate course on abstract algebra. It was certainly ambitious of my professor to introduce students to group theory through a categorical lens, but I was absolutely hooked. Even now my research interests are very categorical in nature. However, there was one definition above all else that seemed a little more complicated to grasp: the notion of a **limit**. I was always comfortable with universal properties, but for the longest time it did not sink in how limits were just instances of universal properties. Interestingly, the picture can be generalized to a slightly more involved setting, but it truly makes compactifies and captures the essence of what a limit really is.

In this post, I will present the usual definition of a limit, then recall some other categorical definitions and show from that perspective what a limit really is. I am of course assuming the reader has familiarity with basic notions of category theory. If you would like a review, I recommend taking a tour of the [nLab](https://ncatlab.org/nlab/show/HomePage), reading the classic book by [Mac Lane](https://www.springer.com/gp/book/9780387984032), or more briefly going through [these notes](https://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

Without further ado, what exactly is a limit?


