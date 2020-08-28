---
title: 'Theorems of Engel, Lie, and Cartan'
date: 2020-06-17
permalink: /posts/EngelLieCartan/
tags:
  - Lie Algebras
---

The title of this blog post might be a bit ambitious, but I believe the results are related enough that I can present their proofs and discuss some of the implications therein with this blog post. In particular, these results are crucial statements regarding nilpotency and solvability. These theorems will then be used in future blog posts discussing some of their implications. 

To begin, recall that the adjoint representation of a Lie algebra presents equivalent conditions for a Lie algbera to be nilpotent or solvable:

\\(\mathfrak{g} \text{ is solvable (resp. nilpotent)} \Longleftrightarrow\text{ad}\mathfrak{g} \text{ is solvable (resp. nilpotent)}\\)

Thus, the proofs of Engel's Theorem, Lie's Theorem, and Cartan's Criterion in fact pertain to subalgebras of \\(\mathfrak{gl}(V)\\), from which one can then deduce results pertaining to an abstract Lie algebra by consider its image under the adjoint map. With this in mind, a preliminary result will be proven first that will serve to obtain Lie's Theorem, and indirectly obtain Engel's Theorem after reviewing its proof. However, this result is important in its own right so we call it a theorem instead of a lemma.


#An Important Theorem 

\\(\textbf{Theorem}\\) Let \\(\mathfrak{g}\\) be a solvable subalgebra of \\(\mathfrak{gl}(V)\\), \\(V\\) finite dimensional. If \\(V\neq \\{0\\}\\), then \\(V\\) contains a common eigenvector for all th endmorphisms in \\(\mathfrak{g}\\).

\\(\textbf{Proof}\\)

The proof is actually done by induction on the dimension of \\(\mathfrak{g}\\), the base case being trivial with \\(\text{dim}\mathfrak{g} = 0\\). Here is the schematic for proceeding with the proof:

1. Construct a codimension one ideal \\(I\\) of \\(\mathfrak{g}\\).
2. By induction, there exists common eigenvectors for \\(I\\).
3. Show that \\(\mathfrak{g}\\) stabilizes a space consisting of such eigenvectors from 2.
4. Find an eigenvecor in the previous space for a particular \\(z\in\mathfrak{g}\\) which satisifes the decomposition \\(\mathfrak{g} = I\oplus\mathbb{C}z\\), where the decomposition \\(\textbf{is as vector spaces, not Lie algebras!}\\)

For step one, as we are proceeding with induction and now assuming \\(\mathfrak{g}\\) is nontrivial and solvable, it properly contains its derived algebra i.e. \\([\mathfrak{g},\mathfrak{g}]\subsetneq \mathfrak{g}\\). Then the quotient algebra \\(\mathfrak{g}/[\mathfrak{g},\mathfrak{g}]\\) is Abelian, so any subspace is automatically an ideal. We thus take \\(I\\) to be the inverse image of any codimension one subspace; this is our codimension one ideal.

Next, by induction the following subspace \\(W\subseteq V\\)

\\(W := \\{w\in V\ \|\ x(w) = \lambda(x)w,\ \text{for all }x\in I\\}\\)

is nonzero, where \\(\lambda: I\to\mathbb{C}\\) is a linear function. If we then suppose that step 3 has been completed, then step 4 is quick too. Indeed, if \\(\mathfrak{g}\\) stabilizes \\(W\\), then as \\(\mathbb{C}\\) is algebraically closed, pick an eigenvector in \\(W\\) for \\(z\\) as in the decomposition. But since \\(W\\) consists of eigenvectors for all of \\(I\\), the proof is done by simply extending the weight \\(\lambda\\) onto \\(z\\). Hence, all that remains is to show that \\(\mathfrak{g}(W)\subseteq W\\).

Now, in order to prove this, let \\(x\in I\\) and \\(w\in W\\) and note that for all \\(y\in\mathfrak{g}\\), 

\\(\[x,y\](w) = x(y(w)) - y(x(w)) \Longrightarrow \lambda([x,y])w = x(y(w)) - \lambda(x)y(w)\\)

If it can be shown that \\(\lambda([x,y]) = 0\\), then

\\(x(y(w)) = \lambda(x)y(w)\\)

so that \\(y(w)\in W\\) and the result would follow. Hence, we are tasked with proving that for all \\(x\in I\\) and \\(y\in\mathfrak{g}\\) that \\(\lambda([x,y]) = 0\\). To this end, fix \\(w\\) and \\(y\in\mathfrak{g}\\). Next let \\(n\\) be the minimal positive integer such that the vectors

\\(w, y(w), \dots, y^{n}(w)\\)

are linearly dependent. Furthermore, define the subspaces

\\(W_{i} := \text{Span}\\{w,y(w),\dots,y^{i - 1}(w)\\}\\)

with \\(W_{0} = \\{0\\}\\). 

# Consequences

# The Connection to Engel's Theorem

# Cartan's Criterion

