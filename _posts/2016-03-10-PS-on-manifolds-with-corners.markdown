---
layout: post
title:  "Poisson Structure on manifolds with corners"
date:   2016-03-10 14:40:00
first-language: En
second-language: Fr
subdomain: fr 
activate-lan: yes
categories: post
---

In my last post I wrote about [Poisson Structure on manifolds with singularities][PS]. Sorokina's research (See her [published][SOROKINA]) motivated me to do research
in this topic and thanks to her support I sent a paper to [arXiv][PSWC] about how can we describe a Poisson Structure on manifolds with corners. As you can see by the title, is really important to define What it is a manifold with corners, but all this work was defined by Mr. Joyce on his papers [On manifolds with corners][JOYa] and [A generalization of manifolds with corners][JOYb], so let's just recall some definitions.

<b>Manifolds with corners</b>
---
What it is the intuition behind manifolds with corners? First, we need to remember what does a manifold with boundary is. Suppose we are on $$\mathbb{R}^{n}$$, then let $$B^{n}$$ be a $$n$$-ball such that $$B^{n} = \{(x_{1}, \dots, x_{n}) \in \mathbb{R}^{n} | x_{1}^{2} + \dots + x_{n}^{2} < 1 \}$$, this closed set is the manifold with boundary since $$x_{1}^{2} + \dots x_{n}^{2} < 1$$, meantime $$x_{1}^{2} + \dots + x_{n}^{2} = 1$$ is the unit hyper-sphere. This is indeed a manifold, since every second countable Hausdorff space is locally homeomorphic to Euclidean space. Now, we need to generalize the previous concept, if we take a $$n$$-manifold
$$M$$ with boundary $$\partial M$$, then this is a $$(n-1)$$-manifold with corners. Formally


<b>Definition:</b>
$$
\small\boxed{\text{Let} \ \mathbb{R}_{k}^{n} = [0, \infty)^{k} \times \mathbb{R}^{n-k} \ \text{. The singular space} \ M \  
 \text{is a second countable Hausdorff topological space in} \ n \ \text{dimensions, modeled on} \ \mathbb{R}_{k}^{n}  \text{.}
}
$$

Let $$U$$ be an open subset in $$\mathbb{R}_{k}^{n} = [0, \infty)^{k} \times \mathbb{R}^{n-k}$$ for some $$0 \leq k \leq n$$, and let $$\phi: U \longrightarrow M$$
be a homeomorphism with a nonempty set $$\phi(U)$$, then the pair $$(U, \phi)$$ is a $$n$$-dimensional chart on $$M$$.

Until here, we know what it is a manifold with corners and how we can define a $$n$$-dimensional chart on it. In order to define a Poisson structure on a manifold with corners, we need to know how we can describe a sheaf structure on it.

<b>Sheaves</b>
---
In order to define sheaves, first we need to define pre-sheaves. Let $$M$$ be a manifold with corners, then a presheaf consists of two sets of data:

-<b>Sections over open sets</b>, for each open set $$U \subseteq M$$ an abelian group $$\Gamma(U)$$.

-<b>Restriction maps</b>, for every inclusion $$V \subseteq U$$ of open sets in $$M$$ a group homomorpshim $$p_{V}^{U}:F(U) \longrightarrow F(V)$$ subjected
to the conditions

$$
p_{W}^{U} = p_{W}^{V} \circ p_{W}^{U}
$$

for all sequences $$W \subseteq V \subseteq U$$ of inclusions of open sets in $$M$$, where $$F(R)$$ are called <b>sections</b> of $$F$$ over $$R$$
  and  $$p_{V}^{U}$$ are called <b>restriction maps</b>.

Now, we are able to define sheaves. A sheaf on $$M$$ is a presheaf of abelian groups on $$M$$ satisfying the following properties:

-<b>Locally axiom</b>, let $$\{U_{i}\}_{i \in I}$$ be an open cover of the open set $$U$$ and let $$s$$ be a sectionof $$F$$ over $$U$$.

-<b>Gluing axiom</b>, let $$\{U_{i}\}_{i \in I}$$ be an open cover of the open set $$U$$. Given sections $$s_{i}$$ over $$U_{i}$$ matching on the intersections
$$U_{ij} = U_{i} \cap U_{j}$$, then there is a section $$s$$ of $$F$$ over $$U$$ satisfying $$s|_{U_{i}} = s_{i}$$.

What does this mean? It means that there is a locall homeomorphism structure (sheaf) $$F$$ into $$M$$ where we can define a Poisson Structure where given
a ring-valued sheaf $$\mathcal{O}_{M}$$ on manifold with corners $$M$$.

<b>Poisson Structure</b>
---
A poisson structure on $$(M, \mathcal{O})$$, where $$M$$ is a manifold with corners, is a sheaf morphism

$$
\{-, -\} = \mathcal{O} \times \mathcal{O} \longrightarrow \mathcal{O}
$$

that is a derivation (satisfies the Leibniz rule) in each argument and also satisfies the Jacobi identity (See my [previous post][PSS] for details). The proof is short, but since we need to recall some lemmas, please take your time to [read it][PSC].


[PS]: http://joelantonio.me/post/2016/02/27/PS-on-manifolds-with-singularities/
[PSS]: http://joelantonio.me/post/2016/02/18/Poisson-sctructure/
[PSC]: http://arxiv.org/pdf/1601.00089v1.pdf
[SOROKINA]: http://arxiv.org/pdf/1312.6262v1.pdf
[PSWC]: http://arxiv.org/pdf/1601.00089v1.pdf
[DFT]: https://en.wikipedia.org/wiki/Differential_operator
[JOYa]: http://arxiv.org/pdf/0910.3518v2.pdf
[JOYb]: http://arxiv.org/pdf/1501.00401v2.pdf
