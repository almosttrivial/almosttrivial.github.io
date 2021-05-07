---
title: 'Preface to Lie Algebras'
date: 2020-06-15
permalink: /posts/PrefaceToLieAlgebras
tags:
  - Lie Algebras
  - Representation Theory
  - sl2 theory
  - root systems
---


The first topic I pursued at the start of my doctoral studies was learning about the representation theory of complex semisimple Lie algebras. My main resource was [Humphreys](https://books.google.com/books/about/Introduction_to_Lie_Algebras_and_Represe.html?id=gCUlAQAAIAAJ), which, while relatively small given the complexity of the topic, was a very clear and concise treatment of the material[.](https://l.facebook.com/l.php?u=https%3A%2F%2Fdrive.google.com%2Ffile%2Fd%2F1sbxLuVlFT-y8O5hIGBm1N-VQB2gKD34S%2Fview%3Fusp%3Dsharing%26fbclid%3DIwAR0azy_RJP279RfsQ1m-ZwkVthdXh1uoIsQNB3dMi8uMxpkDpAiV6xYVqPM&h=AT0-Ds1HdU9Rm2pQ-_m58dUF0lsAfMzPVHd0SJvy-bUEsUJiVEbPt_XzAUVYowCliMIjEGsB1L4owkqxbC2iMwLZ1c9bLCIYQANYkswTDh75M3BYSxuuxqXXdMg_jJY2ABY) 

In this post I will highlight some of the main attractions of the theory: the classification of complex-simple Lie algebras, their Serre presentation, and their representation theory. However, each of these examples and more will be properly explored and presented in their own respective blog posts. Thus, consider this as almost my rendition of Humphreys preface.

Before proceeding, I would also like to tease even more blog posts that are to come. Namely, after finishing Humphreys, I learned about Kac-Moody algebras from predominantly [Carter](https://books.google.com/books/about/Lie_Algebras_of_Finite_and_Affine_Type.html?id=gv2Xf8VVi2MC), and after that about Quantum Groups from [Jantzen](https://books.google.com/books/about/Lectures_on_Quantum_Groups.html?id=uOGqPjjVt0AC). As I state theorems and propositions, I will appropriately comment on how some considerations in the Lie algebras case are crucial points that get reinterpreted and motivate analogous results in the studies of Kac-Moody algebras and Quantum Groups. I know Lie superalgebras are similarly motivated by techniques and observations in classical Lie algebras, but I am less familiar with this and would like to learn more about it. All I know is that Lie superalgebras are in fact Lie algebra objects in the category of super vector spaces, and that there is a similar classification of certain Lie superalgebras, but I am not familiar with the proof by [Kac](https://pdf.sciencedirectassets.com/272585/1-s2.0-S0001870800X03398/1-s2.0-0001870877900172/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEM%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIQDiTF4OdK2N0R6upzihQOFq8LWoWa5nEOXMomhyqf%2Fm%2FgIgNtw28j9pHTdu08Zr28YWpw%2F%2BAGsOY%2FoSQzcO5kUnQ8EqvQMIyP%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARADGgwwNTkwMDM1NDY4NjUiDCsMIY2JvYqAy%2B6T4iqRA4mc0ojCarnGcNnFFwJTDsfmCDMmfDDQuGBaK0YVKdwwAjSdunhKxkIPz5W8zjgGMA6icloqMotzxAVfJuhZ7nJrEaPzFsADuyK3Qwks2uYbuzadVSxrwaCrZbacS0QWCjdJkGrfED8td7hOqog%2Ft1TfpfApSn5Owg2Kx0EtsLP0dIkxMEKTDTpi%2FRVNVjoYgTaukowaThn0sX%2FEdSq7n5CFUa%2FAns5GJfwwl6Aei9qNH7Yo7fkJ7ZOttjtpO0AOCFYcWBbhO5n60EhCXo7LDPzfjEtOl0%2Bb4EKPs8Xfn20yGHgZxDsfpezxMAC7dmxt%2FtX3qhHkZBBK9jH4rEbUSFdV7V0k%2FmoFgYoAabqadcLDDoGOGtOIpZz7GUOBAfW5WxvsqmtqB%2BDmxdZEPpsYmf44RpAGuUSOWiJEnOQVPwkTydyhT3ZSh%2FSfCxZcL9dmEHFMJhppO7rKnrjXt4U3%2FQigXBcHF9wEDWsTRG9wSWP4z75PsWYk8KpJxbCVr4N2NE5rbSLg%2FoDoAKr%2BDu9z4Wv6MM%2BLy%2FoFOusBSBHRb8Z5K5k1yDm9AhQfM5n%2F96KPZ%2B8aNxwyZ%2FRMy%2BianFcu19BOWZJKnclZudekwat%2BKavMOQrgZSL3M6%2F4lpLtMW91BZWWMxOdEls%2BFSoYg0qGKiDd7PIzaOyq0Ul22P0zsY03wXGf41jagX0l%2BvAkGgiF9CBN2Y1CzgLdXoUJLa2szoWT2J%2FeaheZ3h31ZsMxrzQOznX9PtgUIV5Kvum3HC9a5R6nbBGdCaKOKUqAY15N5eP%2FYfvvetqrgaWthvRryKLuIdOdI%2FiMxbvTFySRV0%2B0mcv%2FPjxzHEO8N%2B7uo6vLCg2R30JwAg%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20200904T235535Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYT45LNTI7%2F20200904%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=5c9396340543a74ce2aba292db92cbaf79a19e1c830025a09f97172337cfe633&hash=9a1bbf5f6520fc914dd0c7f9d4e9c78e233e43a0f8a61e7b00ff69a26f034b74&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=0001870877900172&tid=spdf-e91ecbaa-78ff-4214-b31d-8f94ce3edb08&sid=4e5b60117ff81947bc59dff982280b7a6a8bgxrqa&type=client).


Without further ado, let us first consider what is a Lie algebra and what is their purpose. Well, a Lie algebra \\(\mathfrak{g}\\), typically over a field (and certainly for my considerations) \\(\mathbb{K}\\), is a \\(\mathbb{K}\\)-vector space with a bilinear operation \\([\cdot,\cdot]: \mathfrak{g}\times\mathfrak{g}\to\mathfrak{g}\\) satisfying the following equalities:

* \\([x,x] = 0\\)
* \\([x,[y,z]] + [y,[z,x]] + [z,[x,y]] = 0\\)

The operation is called the **Lie bracket** or just the bracket (of \\(\mathfrak{g}\\) if there is ambiguity). The first equality is called **alternativity** of the bracket and the second is called the **Jacobi identity**. However, I also said it is a bilinear operation, so this is part of its definition as well. Before proceeding with examples, I would just like to point out that while I said one commonly works over fields, I did not say that the fields had to have zero characteristic. In particular, if one considers the alternativity relation, then it readily implies \\([x,y] = -[y,x]\\), which is called **skew-symmetry**. Now, skew-symmetry also implies alternativity, but only if we assume \\(\text{char}(\mathbb{K})\neq 2\\). And indeed, for the bulk of what I have to say I will consider \\(\mathbb{K}\\) a characteristic zero field, and sometimes algebraically closed, when necessary.


Now that we have this abstract definition, well, where do we find Lie algebras? Why are they even considered in the first place? As it just so happens, everyone is likely familiar with a couple of important examples: endomorphisms of a vector space! In particular, if the vector space is finite-dimensional, then one can safely consider square matrices of a fixed size instead. The notation for these spaces are typically \\(\mathfrak{gl}(V)\\), especially when \\(V\\) is infinite-dimensional, and \\(\mathfrak{gl}(n), \text{ } \mathfrak{gl}\_{n},  \text{ } \mathfrak{gl}(V,n)\\) in the event that \\(V\\) is finite-dimensional. Of course, the reader is probably more familiar with the notation \\(\text{End}(V)\\), but the others are more common place when considering the Lie algebra structure on the space of endomorphisms. So, what exactly is its Lie algebra structure? This will actually address why Lie algebras are studied as well.

For the sake of space I will use the linear maps formalism instead of matrices, but the reader is certainly encouraged to use whichever they prefer. Now, for two linear maps \\(\phi,\psi\in\mathfrak{gl}(V)\\), it is rarely the case that they commute i.e. \\(\phi\circ\psi = \psi\circ\phi\\) may or may not happen. However, both sides are certainly still endomorphisms of \\(V\\), and so too is their difference. Thus, one can consider \\(\phi\circ\psi - \psi\circ\phi\\) as a linear map, and this difference in fact blatantly captures how much \\(\phi\\) and \\(\psi\\) fail to commute. Indeed, if this difference acts trivially, then equivalently these maps do actually commute. To study the lack of commutativity between linear maps, one may define the following binary operation which is suggestively denoted as a bracket


\\( [\cdot,\cdot]:\mathfrak{gl}(V)\times\mathfrak{gl}(V)\to\mathfrak{gl}(V),\quad (\phi,\psi)\mapsto \phi\circ\psi - \psi\circ\phi\\)

which I strongly suggest the reader to confirm that this binary operation actually defines a Lie bracket on \\(\mathfrak{gl}(V)\\). One might have come across this as the "commutator" of linear maps. This moreover arises in the study of groups where one similarly has a notion of commutator, and in both cases these products capture how non-commutative the structure is, but it is quite distinct from our current situation.

Now, as I previously mentioned, there will be a series of blog posts to come that will explore the results below. With that in mind, I will not necessarily define everything. But even if I define something, I might not state all, or any, of the implications which might follow. Instead, I will tag it with the appropriate blog post as they become published.

For instance, one might wonder what are some ways of studying a Lie algebra? Perhaps unsurprisingly is by seeing how it acts on vector spaces! This is the idea of a representation of a Lie algebra. For the unfamiliar reader, if you know about group actions or \\(R\\)-modules, then it is the same thing except formulated with respect to Lie algebras instead of a group or a ring acting on something.

As it turns out, there is a particular Lie algebra, \\(\mathfrak{sl}\_{2}\\) consisting of all traceless linear maps in \\(\mathfrak{gl}\_{2}\\), and its' representation theory is pivotal in proving the three theorems mentioned at the beginning of this post. The aforementioned results are formally the following theorems

**Theorem** _Fix a root system \\(\Phi\\) with base \\(\Delta = \\{\alpha\_{1},\dots,\alpha\_{l}\\}\\). Let \\(L\\) be the Lie algebra generated by \\(3l\\) elements \\(\\{x\_{i}, y\_{i}, h\_{i} \| 1\leq i\leq l\\}\\), subject to the Serre relations. Then \\(L\\) is a finite-dimensional semisimple Lie algebra, with Cartan subalgebra spanned by the \\(h\_{i}\\) and with corresponding root system \\(\Phi\\)._


INSERT THEOREM

INSERT THEOREM

Each of these theorems are results of several other propositions and lemmas culminating in their proofs. While the above \\(\mathfrak{sl}\_{2}\\) result is one such piece, there are results regarding two other structures that play essential roles as well: they are root systems and the universal enveloping algebra of a Lie algebra.

Root systems are a more geometric object which may be associated to a semisimple Lie algebra. This allows for more intuition about the Lie algebra by first saying something about root systems, and seeing the implication it has on the corresponding Lie algebra. Namely, the classification of simple Lie algebras is largely due in part to the classification of irreducible (crystallographic) root systems.

As for the universal enveloping algebra, it is definitely more algebraic. It too is associated to a Lie algebra, and whereas root systems aid in classifying simple Lie algebras, universal enveloping algebras aid in characterizing the representation theory of any semisimple Lie algebra. Nonetheless, root systems also play a role here by the presence of another object called a weight lattice, but it is really the universal enveloping algebra that allows for certain constructions e.g. Verma modules.

The enumerated theorems above will be the goal of a series of future blog posts. Moreover, throughout each blog post I will elaborate on how the present material motivates considerations in the Kac-Moody algebra case and Quantum Group case. For now, what I can say is that the Serre presentation is at the crux of both these other topics. Also, the representation theory in the classical setting motivates that of the others, and in a sense is extended in both cases.

