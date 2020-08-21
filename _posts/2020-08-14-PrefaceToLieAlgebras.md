---
title: 'Preface to Lie Algebras'
date: 2020-08-14
permalink: /posts/PrefaceToLieAlgebras
tags:
  - Lie Algebras
  - Representation Theory
  - sl2 theory
  - root systems
---


The first topic I pursued at the start of my doctoral studies was learning about the representation theory of complex semisimple Lie algebras. My main resource was HUMPHREYS, which, while relatively small given the complexity of the topic, was a very clear and concise treatment of the material. 

In this blog, I will highlight some of the main attractions of the theory e.g. the importance of \\(\mathfrak{sl}\_{2}\\), root systems, classifications, PBW, highest weights, etc. However, each of these examples and more will be properly explored and presented in their own respective blog posts. Thus, consider this as almost my rendition of Humphreys preface.

Before proceeding, I would also like to tease even more blog posts that are to come. Namely, after finishing Humphreys, I learned about Kac-Moody algebras from predominantly CARTER, and after that about Quantum Groups from JANTZEN. As I state theorems and propositions, I will appropriately comment on how some considerations in the Lie algebras case are crucial points that get reinterpreted and motivate analogous results in the studies of Kac-Moody algebras and Quantum Groups. I know Lie superalgebras are similarly motivated by techniques and observations in classical Lie algebras, but I am less familiar with this and would like to learn more about it. All I know is that Lie superalgebras are in fact Lie algebra objects in the category of super vector spaces, and that there is a similar classification of certain Lie superalgebras, but I am not familiar with the proof.


Without further ado, let us first consider what is a Lie algebra and what is their purpose. Well, a Lie algebra \\(\mathfrak{g}\\), typically over a field (and certainly for my considerations) \\(\mathbb{K}\\), is a \\(\mathbb{K}\\)-vector space with a bilinear operation \\([\cdot,\cdot]: \mathfrak{g}\times\mathfrak{g}\to\mathfrak{g}\\) satisfying the following equalities:

* \\([x,x] = 0\\)
* \\([x,[y,z]] + [y,[z,x]] + [z,[x,y]] = 0\\)

The operation is called the Lie bracket or just the bracket (of \\(\mathfrak{g}\\) if there is ambiguity). The first equality is called alternativity of the bracket and the second is called the Jacobi identity. However, I also said it is a bilinear operation, so this is part of its definition as well. Before proceeding with examples, I would just like to point out that while I said one commonly works over fields, I did not say that the fields had to have zero characteristic. In particular, if one considers the alternativity relation, then it readily implies \\([x,y] = -[y,x]\\), which is called skew-symmetry. Now, skew-symmetry also implies alternativity, but only if we assume \\(\text{char}(\mathbb{K})\neq 2\\). And indeed, for the bulk of what I have to say I will consider \\(\mathbb{K}\\) a characteristic zero field, and sometimes even algebraically closed when necessary.


Now that we have this abstract definition, well, where do we find Lie algebras? Why are they even considered in the first place? As it just so happens, everyone is likely familiar with a couple of important examples: endomorphisms of a vector space! In particular, if the vector space is finite-dimensional, then one can safely consider square matrices of a fixed size instead. The notation for these spaces are typically \\(\mathfrak{gl}(V)\\), especially when \\(V\\) is infinite-dimensional, and \\(\mathfrak{gl}(n), \text{ } \mathfrak{gl}\_{n},  \text{ } \mathfrak{gl}(V,n)\\) in the event that \\(V\\) is finite-dimensional. Of course, the reader is probably more familiar with the notation \\(\text{End}(V)\\), but the others are more common place when considering the Lie algebra structure on the space of endomorphisms. So, what exactly is its Lie algebra structure? Well, this actually will address why Lie algebras are studied as well.

For the sake of space I will use the linear maps formalism instead of matrices, but the reader is certainly encouraged to use whichever they prefer. Now, for two linear maps \\(\phi,\psi\in\mathfrak{gl}(V)\\), it is rarely the case that they commute i.e. \\(\phi\circ\psi = \psi\circ\phi\\) may or may not happen. However, both sides are certainly still endomorphisms of \\(V\\), and so too is their difference. Thus, one can consider \\(\phi\circ\psi - \psi\circ\phi\\) as a linear map, and this difference in fact blatantly captures how much \\(\phi\\) and \\(\psi\\) fail to commute. Indeed, if this difference acts trivially, then equivalently these maps do actually commute. To study the lack of commutativity between linear maps, one may define the following binary operation which is suggestively denoted as a bracket


\\( [\cdot,\cdot]:\mathfrak{gl}(V)\times\mathfrak{gl}(V)\to\mathfrak{gl}(V),\quad (\phi,\psi)\mapsto \phi\circ\psi - \psi\circ\phi\\)

which I strongly suggest the reader to confirm that this binary operation actually defines a Lie bracket on \\(\mathfrak{gl}(V)\\). One might have come across this as the "commutator" of linear maps. This moreover arises in the study of groups where one similarly has a notion of commutator, and in both cases these products capture how non-commutative the structure is.

Now, as I previously mentioned, there will be a series of blog posts to come that will explore the results below. With that in mind, I will not necessarily define everything. But even if I define something, I might not state all, or any, of the implications which might follow. Instead, I will tag it with the appropriate blog post as they become published.

For instance, one might wonder what some of the practically methods are in studying a Lie algebra? Perhaps unsurprisingly is by seeing how it acts on vector spaces! This is the idea of a representation of a Lie algebra. For the unfamiliar reader, if you know about group actions or \\(R\\)-modules, then it is the same thing except formulated with respect to Lie algebras instead of a group or a ring acting on something.

As it turns out, there is a particular Lie algebra, \\(\mathfrak{sl}\_{2}\\) consisting of all traceless linear maps in \\(\mathfrak{gl}\_{2}\\), and its' representation theory is pivotal in not only classifying complex simple Lie algebras and yielding a uniform presentation for them, but also in studying their corresponding representation theories. More precisely, the following theorem about \\(\mathfrak{sl}\_{2}\\) is crucial

INSERT THEOREM

And the aforementioned results are formally the following theorems

INSERT THEOREM
INSERT THEOREM
INSERT THEOREM

Each of these theorems are results of several other propositions and lemma culminating in their proofs. While the above \\(\mathfrak{sl}\_{2}\\) result is one such piece, there are results regarding two other structures that play essential roles as well: that is root systems and the universal enveloping algebra of a Lie algebra.

Root systems are a more geometric object which may be associated to a semisimple Lie algebra. This allows for more intuition about the Lie algebra by first saying something about root systems, and seeing the implication it has on the corresponding Lie algebra. Namely, the classification of simple Lie algebras is largely due in part to the classification of root systems associated to simple Lie algebras.

As for the universal enveloping algebra, it is definitely more algebraic. It too is associated to a Lie algebra, and whereas root systems aid in classifying simple Lie algebras, universal enveloping algebras aid in characterizing the representation theory of any semisimple Lie algebra. Root systems also play a role here by the presence of another object called a highest weight lattice, but it is really the universal enveloping algebra that allows for certain constructions altogether.

The enumerated theorems above will be the goal of a series of future blog posts. Moreover, I also mentioned throughout them I will elaborate on how the present material motivates considerations in the Kac-Moody algebra case and Quantum Group case. For now, what I can say is that the Serre presentation is at the crux of both Kac-Moody algebras and Quantum Groups. Moreover, the representation theory here in the classical setting motivates that of the other objects, and in a sense is in fact extended in both cases.

