---
layout: post
title:  "Separation Axioms in Topological Spaces"
date:   2016-05-22 20:40:00
first-language: En
second-language: Fr
subdomain: fr 
activate-lan: yes
categories: post
---

In nowadays, an axiom of separation is a property that satisfies certain topological spaces. We are going to describe these axioms that are labeled
as $$T_{i}$$ but first let's recall some basic definitions.

<b>Separeted sets</b>
---
Let $$S$$ be a topological space and let $$x$$ and $$y$$ be points points such that $$x, y \in S$$. Let $$X, Y$$ be neighbourhoods of $$x$$
and $$y$$ respectively such that $$X, Y \subset S$$. Then, we say that:

- $$x$$ and $$y$$ are <i>distinguishable</i>, if there a neighborhood $$N \subset X$$ such that $$x \in N$$ but $$y \notin N$$, <br> 

- $$X$$ and $$Y$$ are <i>separated by a closed neighborhood</i>, if they have disjoints closed neighborhoods (<b>e.g.</b> $$X = [0, 1]$$ and $$Y = [4, 5]$$), <br>

- $$X$$ and $$Y$$ are <i>separated by a continuous function</i>, if there a map $$\phi$$ such that $$\phi: X \longrightarrow \mathbb{R}$$ and the
image $$\phi(X) = 0$$ and $$\phi(Y) = 1$$, <br>

- $$X$$ and $$Y$$ are <i>precisely separated by a continuous function</i>, if the preimage $$\phi^{-1}(\{0\}) = X$$ and $$\phi^{-1}(\{1\}) = Y$$.

<b>Axioms</b>
---

- <b>$$X$$ is $$T_{0}$$ (or <i>Kolmogorov</i>)</b>, the simplest axiom which satisfies that for any two distinct points $$x$$ and $$y$$ from $$S$$, then $$x$$ and $$y$$
are distinguishable.

- <b>$$X$$ is $$T_{1}$$ (or <i>Fréchet</i>)</b>, if satisfies $$T_{0}$$ and if any two dinstinguishable points in $$S$$ are separated. <br>

- <b>$$X$$ is $$T_{2}$$ (or <i>Hausdorff</i>)</b>, if satisfies $$T_{0}$$ and if any two dinstinguishable points in $$S$$ are separated by neighbourhoods. <br>

- <b>$$X$$ is $$T_{2 \frac{1}{2}}$$ (or <i>Urysohn</i>)</b>, if any two distinct points in $$S$$ are separated by closed neighbourhoods. $$T_{2 \frac{1}{2}}$$
implies $$T_{2}$$. <br>

- <b>$$X$$ is $$T_{3}$$ (or <i>regular Hausdorff</i>)</b>, if satisfies $$T_{0}$$ and if for any $$x \in S$$ and any closed set $$F \subset S$$ such that
$$x \notin F$$, then $$x$$ and $$F$$ are separated by neighbourhoods. <br>

- <b>$$X$$ is $$T_{3 \frac{1}{2}}$$ (or <i>Tychonoff,</i>)</b>, if satisfies $$T_{0}$$ and if for any $$x \in S$$ and any closed set $$F \subset S$$ such that
$$x \notin F$$, then $$x$$ and $$F$$ are separated by a continuous function. $$T_{3 \frac{1}{2}}$$ implies $$T_{3}$$. <br>


- <b>$$X$$ is $$T_{4}$$ (or <i>normal Hausdorff</i>)</b>, if satisfies $$T_{1}$$ and if any two disjoints closed subsets of S are separated by neighbourhoods. <br>

- <b>$$X$$ is $$T_{5}$$ (or <i>completely normal Hausdorff</i>)</b>, if satisfies $$T_{1}$$ and if for any two separated sets are separated by neighbourhoods. <br>

- <b>$$X$$ is $$T_{6}$$ (or <i>perfectly normal Hausdorff</i>)</b>, if satisfies $$T_{1}$$ and if any two disjoints closed sets are precisely separated
by a continuous function. <br>

Concluding:

$$
T_{0} \subset T_{1} \subset T_{2} \subset T_{2 \frac{1}{2}} \subset T_{3} \subset T_{3 \frac{1}{2}} \subset T_{4} \subset T_{5} \subset T_{6},
$$

since $$T_{i}$$ satisfies the properties of $$T_{j}$$ for a $$i > j$$.

<b>Example</b>
---

Let's make a very precise example. Let $$S = \mathbb{R}^{n}$$ be a topological space and let $$E, F$$ be any two differrent closed disjoints subsets
from $$\mathbb{R}^{n}$$ such that there a function $$x \mapsto \frac{d(x, E)}{d(x, E) + d(x, F)}$$ where $$d(x, E)$$ is the distance from a point $$x$$
to the subset $$E$$ defined as $$\inf_{y \in E}\{d(x, y)\}$$. Then,

- <b>$$\mathbb{R}^{n}$$ is $$T_{0}$$</b>, if we take any $$x \in E$$, then $$x \notin F$$ for any closed $$F \subset \mathbb{R}^{n}$$ since $$E, F$$ are
disjoints. Then for any $$y \in F$$, clearly $$x, y$$ are distinguishable.

- <b>$$\mathbb{R}^{n}$$ is $$T_{1}$$</b>, let $$X, Y$$ be closed subsets from $$\mathbb{R}^{n}$$ such that $$X \supset E$$ and $$Y \supset F$$, then
$$X, Y$$ are disjoints closed neighborhood from $$E$$ and $$F$$ respectively. Indeed, for any $$x \in X$$ and $$y \in Y$$, then $$x$$ and $$y$$ are separared.
Since $$\mathbb{R}^{n}$$ is $$T_{0}$$, then claim follows.

- <b>$$\mathbb{R}^{n}$$ is $$T_{2}$$</b>, as we described previously that for any $$x \in X$$ an $$y \in Y$$ are dinstinguishable points in $$\mathbb{R}^{n}$$
are separated by neighbourhoods $$E$$ and $$F$$ respectively, then claim follows.

- <b>$$\mathbb{R}^{n}$$ is $$T_{2 \frac{1}{2}}$$</b>, this is a little stronger than $$T_{2}$$ since follows that for any $$x, y \in \mathbb{R}^{n}$$
even if they are not dinstinguishable points, they are separated by closed neighbourhoods. Since already our example fulfills all the requirements about this,
then claim follows.

- <b>$$\mathbb{R}^{n}$$ is $$T_{3}$$</b>, if we taky any $$x \in \mathbb{R}^{n}$$ and we suppose that $$x \notin F$$, then $$x$$ and $$F$$ are separated
by neighbourhoods, this is easy to see if we suppose that $$x \in E$$, since $$E$$ and $$F$$ are disjoints subsets from $$\mathbb{R}^{n}$$ and since
it satisfies $$T_{0}$$ then claim follows.

- <b>$$\mathbb{R}^{n}$$ is $$T_{3 \frac{1}{2}}$$</b>, this is a little stronger than $$T_{3}$$, since requires that for any $$x \in \mathbb{R}^{n}$$
is separated by a closed subset $$F \subset \mathbb{R}^{n}$$, as previously we take $$E$$ and $$F$$ and they are closed disjoints subsets, then
claim follows.

- <b>$$\mathbb{R}^{n}$$ is $$T_{4}$$</b>, let $$X$$ and $$Y$$ be two disjoints closed subsets from $$\mathbb{R}^{n}$$ such that $$X \supset E$$ and $$Y \supset F$$,
then we can say that $$E$$ and $$F$$ are separated by neighbourhoods and since $$\mathbb{R}^{n}$$ satisfies $$T_{1}$$, then claim follows.

- <b>$$\mathbb{R}^{n}$$ is $$T_{5}$$</b>, this is a little stronger than $$T_{4}$$, since it satisfies that two any subsets from $$\mathbb{R}^{n}$$ are separated
even if they are not closed. As we have decomposed $$\mathbb{R}^{n}$$ in closed subsets and already our example fulfills all the requirements about this,
then claim follows.

- <b>$$\mathbb{R}^{n}$$ is $$T_{6}$$</b>, let $$\phi$$ be a continuous function such that $$\phi: x \longrightarrow \frac{d(x, E)}{d(x, E) + d(x, F)}$$ and as
we described previously $$d(x, E)$$ is the distance from a point $$x$$ to the subset $$E$$ defined as $$\inf_{y \in E}\{d(x, y)\}$$, then $$\phi$$ separates
$$E$$ and $$F$$ as closed subsets from $$\mathbb{R}^{n}$$. Note that we never divide by zero, that only could be possible if $$d(x, E)$$ and $$d(x, F)$$ are
both zero, but this is impossible since $$E$$ and $$F$$ are disjoints. Since $$\mathbb{R}^{n}$$ satisfies $$T_{1}$$, then claim follows.

This post is inspired by the question asked on [MathExchange][mathexchange] and the example was inspired by the user [Akiva][Akiva] about his [answer][math2]
to the question.

[mathexchange]: http://chat.stackexchange.com/transcript/message/29824757#29824757
[math2]: http://chat.stackexchange.com/transcript/message/29824929#29824929
[Akiva]: http://math.stackexchange.com/users/166353/akiva-weinberger
