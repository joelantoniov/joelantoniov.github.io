---
layout: post
title:  "Poisson Structure"
date:   2016-02-18 14:30:00
first-language: En
second-language: Fr
subdomain: fr 
activate-lan: yes
categories: post
---

In 1st January 2016 I submitted a paper on [Arxiv][ARXIV] about how to describe a Poisson structure on a manifold with corners, I'll write about it in a later post, now I'm going to talk about an introduction to understand what a poisson structure is.

<b>Introduction</b>
---

Suppose that we want to describe a system evolution, How can we do that? First, let's list elements of a system.

- Let $$M$$ be a smooth manifold (physical system). <br>
- Let $$x$$ be a point on $$M$$ (state of the system). <br>
- Let $$f$$ be a smooth function on $$M$$ (measuring device).

So, we can say that any state $$x_{i}$$ on $$M$$ can be measured by $$f(x_{i})$$. How the evolution works in this case?, we need to get a collection of measuring
devices (an $$\mathbb{R}$$-algebra homomorphism) and then the evolution depends about how is the the behaviour in this collection, thus $$f$$ can be viewed as a
hamiltonian function, more precisely a Poisson structure on a smooth manifold $$M$$ associates to every smooth function $$f$$ on $$M$$, a vector field
$$\pi_{f}$$ on $$M$$. After this short intuition, let's define formally some concepts.

<b>Definition</b>
---
Let $$M$$ be a smooth manifold and let a lie algebra bracket

$$
\{,\}: C^{\infty}(M) \times C^{\infty}(M) \rightarrow C^{\infty}(M)
$$

which is called a <b>Poisson bracket</b> on the vector space of smooth functions on $$M$$ and it's skew-symmetry 

$$
\label{a}\tag{1}
\{F \cdot G, H\} = F \cdot \{G, H\} + G \cdot \{F, H\}
$$

A poisson structure on $$M$$ is a smooth bivector field  $$\pi$$ on $$M$$ satisfying $$[\pi, \pi]_{s} = 0$$, where $$[\cdot, \cdot]_{s}$$ is the [Schouten bracket][SCHOUTER]. Let $$U$$ be an open subset of $$M$$ and let $$F, G \in C^{\infty}(U)$$ be smooth functions, the bilinear operation $$\{ \cdot, \cdot\}_{U}$$ is defined by 
$$
\{F, G\}_{U}(m) = \langle d_{m}F \wedge d_{m}G, \pi_{m} \rangle
$$
for all $$m \in M$$, which satisfies the [Jacobi Identity][JACOBI].

<b>Hamiltonian formalism</b>
---
To talk about Hamiltonian formalism, let's recall firstly the definition of a differential $$k$$-form.

$$\small\boxed{\text{Every differential $k$-form on the space $n$-dimension with a given coordinate system $x_{1}, \dots, x_{n}$ can be written uniquely in the form
$
\\ \\
\pi^{k} = \sum_{i_{i} < \dots < i_{k}} a_{i_{1}, \dots, i_{k}}(x)dx_{i_{1}} \wedge \dots \wedge dx_{i_{k}},
\\ \\
$
where the $a_{i_{1}, \dots, i_{k}}$ are smooth functions on $n$-dimension.
}}$$ 

If we take the 2-form $$\pi^{2}|_{x}$$ at a point $$x$$ of a manifold $$M$$ and it's differentiable, then we say that it's a 2-form on the tangent space
$$T_{x}M$$ (i.e. A 2-linear skew-symmetric function of 2 vectors $$P_{1}, P_{2}$$ tangent to $$M$$ at x).

Let $$A$$ be a $$\mathbb{R}$$-algebra, then $$\Delta: A \rightarrow A$$ is called a linear differential operator. Let Diff$$_{k}$$ the set of all
differential operator of order $$\leq k$$ acting on $$A$$ from $$A$$. Let $$S_{k}(A) = \frac{\text{Diff}_{k}(A)}{\text{Diff}_{k-1}(A)}$$ be a quotient module
which is called the $$k$$-symbols, now let us define the algebra of symbols for the algebra $$A$$ in the following way:

$$
\label{b}\tag{2}
\text{Smbl}(A) = \bigoplus_{n=0}^{\infty} S_{n}(A)
$$

Let $$\mathfrak{s} = \text{smbl}_{i}\Delta$$, where $$\text{smbl}_{i}\Delta \in S_{k}(A)$$ for $$i = 1, \dots, k$$ and thanks to \ref{a}, we can say that

$$
\label{c}\tag{3}
\{ \mathfrak{s_{\Delta}}, \mathfrak{s}_{\nabla} \} = \mathfrak{s}_{[\Delta, \nabla]}
$$

since $$[f, g] = [g, f] = 0$$ for $$f, g \in C^{\infty}(U)$$ where $$U \subset M$$. Applying \ref{c} to $$F = f(x)p^{\alpha}, G = g(x)p^{\beta}$$ where
$$\{p^{\alpha}, p^{\beta}\} = 0$$, we have

$$
\{F, G\} = \{f(x)p^{\alpha}, g(x)p^{\beta}\} \\
         \hspace{5cm} = \{f(x), g(x)\}p^{\alpha} p^{\beta} + \{f(x), p^{\alpha}\}g(x)p^{\beta} \\
\hspace{5.8cm}          + \{p^{\alpha}, g(x) \}f(x)p^{\beta} + \{p^{\alpha}, p^{\beta}\}f(x)g(x) \\
\hspace{5cm}         = \{p^{\alpha}, g(x)\}f(x)p^{\beta} - \{p^{\alpha}, f(x)\}g(x)p^{\beta} \\
$$

by the equality

$$
\{p^{\alpha}, g(x) \} = \sum_{i=1}^{n} \frac{\partial p^{\alpha}}{\partial p_{i}} \frac{\partial g}{\partial x_{i}}, 
\hspace{1cm} \{p^{\beta}, f(x) \} = \sum_{i=1}^{n} \frac{\partial p^{\beta}}{\partial p_{i}} \frac{\partial f}{\partial x_{i}}, 
$$

After some computations, we get

$$
\{F, G\} = \sum_{i=1}^{n} \left( \frac{\partial F}{\partial p_{i}}\frac{\partial G}{\partial x_{i}} - \frac{\partial G}{\partial p_{i}}\frac{\partial F}{\partial x_{i}}  \right)
$$

which is the standard Poisson bracket on $$T^{*}M$$, making $$X_{F} = \{F, G\}$$, then $$X_{F}$$ is the Hamiltonian vector field on $$T^{*}M$$ with the Hamiltonian $$F$$.

So, there a lot of work to do and study about Poisson structure, this is just a short introduction, however depending of the space over we work, it's not always easy to define a Poisson structure, next time we'll talk about how can we describe a Poisson structure on a manifold with singularities, this is thanks to the work of Miss <b>Maria Sorokina</b>: [Poisson structure on manifolds with singularities][SOROKINA].

[ARXIV]: http://arxiv.org/pdf/1601.00089v1.pdf
[SCHOUTER]: https://en.wikipedia.org/wiki/Schouten%E2%80%93Nijenhuis_bracket
[JACOBI]: https://en.wikipedia.org/wiki/Jacobi_identity
[SOROKINA]: http://arxiv.org/pdf/1312.6262v1.pdf
