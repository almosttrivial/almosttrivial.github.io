---
title: 'The Road to Homological Algebra'
date: 2020-07-10
permalink: /posts/Road-To-Homological-Algebra/
tags:
  - Homological Algebra
  - Category Theory
---

I came across Homological Algebra like I think most do, which is as Simplicial Homology in Hatcher's Algebraic Topology. This becomes axiomatized in Hatcher a few sections later, but it certainly does not present homology in its full generality. Namely, in what types of categories can we construct a homology theory? I will address this in this blog post by exploring the progression of the structure on a category required to formulate a Homology Theory. One of the best resources on the field of Homological Algebra is a text by WEIBEL, which I will refer to as necessary.

(Ab-)Enriched Categories
======

Most working mathematicians assume their categories are such that the collection of morphisms between objects forms a set. However, consider \\(\textbf{Vect}\_{k}\\), the category whose objects are \\(k\\)-vector spaces and morphisms are \\(k\\)-linear maps. Then one may in fact imbue \\(\text{Hom}\_{\textbf{Vect}\_{k}}(V,W)\\) with the structure of a \\(k\\)-vector space by the natural pointwise addition and scalar multiplication. This holds more generally in the category \\(R-\text{mod}\\) of left \\(R\\)-modules with \\(R\\)-linear maps where \\(R\\) is some ring. These are all instances of enriched categories.

Suppose \\((\mathcal{C},\otimes,\mathbb{1}, \alpha,\lambda,\rho)\\) is a monoidal category. Then a \\(\mathcal{C}\\)-enriched category \\(\mathcal{A}\\) consists of the following datum
\begin{equation\*}
   \\left(\text{Obj}(\mathcal{A}), \\{C(a,b), \circ\_{a,b,c}, j\_{a}\\}\_{a,b,c\in\text{Obj}(\mathcal{A})}\\right)
\end{equation\*}
where \\(\text{Obj}(\mathcal{A})\\) is the set of objects, \\(C(a,b)\\) is in an object of \\(\mathcal{C}\\), and \\(\circ\_{a,b,c}, j\_{a}\\) are maps

\begin{align\*}
   & \circ_{a,b,c}: C(b,c)\otimes C(a,b) \rightarrow C(a,c),\\newline
   & j_{a}: 1 \\rightarrow C(a,a)
\end{align\*}

called composition and identity respectively, which make the following diagrams commute

INSERT ASSOCIATIVITY DIAGRAM

INSERT UNITAL DIAGRAMS

These diagrams generalize the notions in a usual category of the composition of morphisms being associative, and every object having an identity morphism that is unital in a sense, respectively.


For the purposes of formulating a Homology Theory, one begins with an \\(\textbf{Ab}\\)-enriched category. That is, the morphisms between two objects has the structure of an Abelian group. That \\(\textbf{Ab}\\) is a monoidal category is pretty clear: the tensor product is direct products (or sums!) of groups, the unit object is the trivial group \\(1 := \\{\ast\\}\\), the associator is the canonical isomorphism of a trinary direct product, and the left and right unitors are just the canonical projections. What is particularly nice is that in general the composition and identity morphisms \\(\circ\_{a,b,c}, j\_{a}\\) need not be unique, but the identity morphism is certainly unique here. This is because the unit object happens to be an initial (in fact zero!) object of \\(\textbf{Ab}\\). Thus, there is only one choice of morphism \\(j_{a}\\). But morphisms in \\(\textbf{Ab}\\) are group homomorphisms, so \\(j_{a}(\ast)\\) is the identity element of \\(C(a,a)\\).


