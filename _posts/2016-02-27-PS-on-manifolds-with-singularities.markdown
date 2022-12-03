---
layout: post
title:  "Poisson Structure on manifolds with singularities"
date:   2016-02-27 18:30:00
first-language: En
second-language: Fr
subdomain: fr 
activate-lan: yes
categories: post
---

In my last post I wrote about an introduction to [Poisson Structure][PS], now I'm going to explain how we can describe a poisson structure
on a manifold with singularities, this work was made by <b>Maria Sorokina</b> in her paper: [Poisson structure on manifolds with singularities][SOROKINA], so if you want details you should read it, I'm sure you will get fun.

Firstly we recall the definition of poisson structure.

$$
\small\boxed{\text{Let} \ M \ \text{be a smooth manifold, a poisson structure on } \ M \  
 \text{is a smooth bivector field} \ \pi \ \text{on} \ M \ \text{satisfying}
  \ [\pi, \pi]_{s} = 0, \\ \text{where} \ [\cdot, \cdot]_{s} \ \text{is the Schouten bracket. Let} \ U \ \text{be an open subset of} \ M \ \text{and let } \ F, G \in C^{\infty}(U) \ \text{be smooth functions,} \\  \text{the bilinear operation} \
  \{ \cdot, \cdot \}_{U} \ \text{is defined by } \ \{F, G\}_{U}(m) = \langle d_{m}F \wedge d_{m}G, \pi_{m} \rangle \ \text{for all} \ m \in M \text{, which satisfies the Jacobi Identity} \\ \text{ and define a Lie algebra structure on } \ C^{\infty}(U).
}
$$

As Sorokina says in the paper, a singularity can cause heavy loads on systems parts, so the key here is consider an algebra whose spectrum coincides with la configuration space with singularities. In first place we need to use the [Differential operator theory][DFT].

<b>Differential Operator</b>
---

Let $$A$$ be a $$\mathbb{R}$$-algebra, a linear differential operator of order $$k$$ is a $$\mathbb{R}$$-homomorphism $$\Delta: A \longrightarrow A$$ with values in $$A$$ such that

$$
(\delta_{a_{0}} \circ \dots \circ \delta_{a_{k}})(\Delta) = 0
$$

where $$a_{i} \in A$$, the set of all differential operator is denoted by Diff$$_{k}$$. Now, we can define an quotient module by $$S_{k} = \frac{\text{Diff}_{k}(A)}{\text{Diff}_{k-1}(A)}$$, which is called <b>the module of symbols of order $$k$$</b>, in this way we can define the algebra of symbols for an algebra $$A$$:

$$
\text{Smbl}(A) = \bigoplus_{n=0}^{\infty} S_{n}(A)
$$

Since any manifold $$M$$ can be determined by the smooth $$\mathbb{R}$$-algebra $$A = C^{\infty}(M)$$ on functions on it, for each $$x$$ on $$M$$ is the $$\mathbb{R}$$-algebra homomorphism $$:A \longrightarrow \mathbb{R}$$. that assigns to every function $$f \in A$$ its value $$f(x)$$ at a point $$x$$.

<b>Pullback of algebras</b>
---

Now, we're going to describe the algebra desired as the pullback of two known algebras. Let $$A_{1} = C^{\infty}(M_{1}), A_{2} = C^{\infty}(M_{2})$$, for manifolds $$M_{i}, i= 1, 2$$. The pullback is unique up to a unique isomorphism, this means

$$
A = A_{1} \oplus A_{2} = \{ (a_{1}, a_{2}) \in A_{1} \oplus A_{2}: p_{1}(a_{1}) = p_{2}(a_{2})  \}
$$

where $$p_{i}: A_{i} \longrightarrow C$$ is a homomorphism for  certain $$\mathbb{R}$$-algebra $$C$$.

<b>Construction of differential operators</b>
---

Let $$A$$ be an algebra which is the cartesian product of the algebras $$A_{1}$$ and $$A_{2}$$ over the algebra $$C$$. Let $$\Delta \in \text{Diff}_{k}(A)$$, then there exists a unique linear map $$\Delta_{i}: A_{i} \longrightarrow A_{i}$$, for $$i=1, 2$$ such belongs to Diff$$_{k(A)}$$.

In Sorokina's paper, she considers $$M = N = C = \mathbb{R}$$ as example, we're going to consider $$M = N = \mathbb{R}^{2}$$ and $$C = \mathbb{R}$$.

<b>Example</b>
---

Let us consider coordinate cross on the plane:

$$
\mathbb{K}_{0} = \{ (x_{1}, x_{2}), (y_{1}, y_{2}) \in \mathbb{R}^{2} | x_{i}y_{i} = 0, \text{for } i=1, 2  \}
$$

Algebra of smooth functions on the cross is given by the formula:

$$
A = C^{\infty}(\mathbb{K}_{0}) = C^{\infty}(\mathbb{R}^{2})|_{\mathbb{K}_{0}} = \{(f(x_{1}, x_{2}), g(y_{1}, y_{2}))| f(0, 0) = g(0, 0) \}
$$

Applying the algorithm:

$$
A_{1} = A_{2} = C^{\infty}(\mathbb{R}), C = \mathbb{R}, p_{1}(f) = f(0, 0), p_{2}(g) = g(0, 0)
$$

The differential operators:

$$
\text{Diff}_{k}(A) = \{ (\Delta_{1}, \Delta_{2})| a_{i}(0, 0) = b_{i}(0, 0), i = 0, \dots, k  \}
$$


$$
\Delta_{1} = \sum_{i=0}^{k} a_{i}(x_{1}, x_{2}) \left( \frac{\partial}{\partial x}  \right)^{i},
$$


$$
\Delta_{2} = \sum_{i=0}^{k} b_{i}(y_{1}, y_{2}) \left( \frac{\partial}{\partial y}  \right)^{i}
$$

For a non-zero order:

$$
[\Delta]_{k} = ([\Delta_{1}], [\Delta_{2}]),
$$

plus, $$a_{0}(0, 0) = b_{0}(0, 0)$$ and $$a_{k}(0, 0) = 0 = b_{k}(0, 0)$$ if $$k \geq 1$$

Poisson bracket:

$$
\{[\Delta], [\nabla]\} = (\{[\Delta_{1}], [\nabla_{1}]\}, \{[\Delta_{2}], [\nabla_{2}]\})
$$

where

$$
\{[\Delta_{1}], [\nabla_{1}]\} = (la_{l_{\Delta}}(x_{1}, x_{2})a'_{n_{\nabla}}(x_{1}, x_{2}) - na_{n_{\nabla}}(x_{1}, x_{2})a'_{l_{\Delta}}(x_{1}, x_{2})) \left( \frac{\partial}{\partial x} \right)^{l+n-1}
$$

$$
\{[\Delta_{2}], [\nabla_{2}]\} = (lb_{l_{\Delta}}(y_{1}, y_{2})b'_{n_{\nabla}}(y_{1}, y_{2}) - nb_{n_{\nabla}}(y_{1}, y_{2})b'_{l_{\Delta}}(y_{1}, y_{2})) \left( \frac{\partial}{\partial y} \right)^{l+n-1}
$$

So, we get the following conditions:

$$
a_{0}(0, 0) = b_{0}(0, 0), a_{i}(0, 0) = 0 = b_{i}(0, 0), i \geq 1, i = l_{\Delta}, b_{\nabla}.
$$

The algebra of symbols is Smbl$$(A) = S_{0} \oplus S_{1} \oplus \dots$$

<b>Lemma</b>
$$
\small\boxed{
\text{For the coordinate cross} \ |\text{Smbl}(A)| \ \text{is 0-dimensional at the point of
singularity and one-dimensional at other points.}
}
$$

<b>Proof:</b>
Let us define homomorphism from the algebra of symbols to $$\mathbb{R}$$

$$
\text{Smbl}(A) = \text{Smbl}_{0}(A) \oplus \text{Smbl}_{1}(A) \oplus \dots
$$

$$H|_{S_{0}} = h_{0}$$, we know that $$S_{0} = A$$, let $$(a_{k}, b_{k}) \in $$ Smbl$$_{k}$$
 by [Hadamard's Lemma][HL]:

$$
(a_{k}, b_{k}) = (a'(0, 0)x + x^{2} \tilde{a}, b'(0, 0)y + y^{2}\tilde{b}) = (a'(0, 0)x, b'(0, 0)y) + (x, y)(x\tilde{a}, y\tilde{b}),
$$

where

$$
(a'(0, 0)x, b'(0, 0)y) \in \text{Smbl}_{k}, (x, y) \in \text{Smbl}_{0}, (x\tilde{a}, y\tilde{b}) \in \text{Smbl}_{k}, (\tilde{a}, \tilde{b}) \in C^{\infty}(\mathbb{R})
$$

$$
H_{k}(a, b) = H_{k}(a'(0, 0)x, b'(0, 0)y), k > 0
$$

Since $$a'(0, 0) = 0 = b'(0, 0), H_{k}(a, b) = 0$$

$$
(H_{k}(a, b))^{2} = H_{2k}((a. b)(a. b)) = H_{2k}(a^{2}, b^{2}) = 0,
$$

Therefore, $$H_{k}(a, b) = 0$$.

As we can see, work on spaces with singularities is nice, in my next post I'll talk about how we can describe a poisson structure on manifolds with corners, the definition of manifolds with corners was given by Mr. Dominic Joyce in his paper: [On manifolds with corners][JOYCE].

[PS]: http://joelantonio.me/post/2016/02/18/Poisson-sctructure/
[SOROKINA]: http://arxiv.org/pdf/1312.6262v1.pdf
[DFT]: https://en.wikipedia.org/wiki/Differential_operator
[HL]: https://en.wikipedia.org/wiki/Hadamard%27s_lemma
[JOYCE]: http://arxiv.org/pdf/0910.3518v2.pdf
