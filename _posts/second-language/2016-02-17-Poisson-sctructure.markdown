---
layout: post
title:  "Structure de Poisson"
date:   2016-02-18 14:30:00
categories: fr post
---

Le 1er Janvier 2016, J'ai soumis un article sur [Arxiv][ARXIV] a propos de la façon de décrire une structure de poisson sur une varieté avec des coins, Je vais écrire à ce sujet dans un post plus tard, maintenant Je vais parler d'une introduction à comprendre ce qu'est une structure de poisson.

<b>Initiation</b>
---

Supposer que nous voulons décrire une évolution du système, Comment peut on faire ça? Premier, faisons la liste des éléments d'un système.

- Soit $$M$$ une varièté lisse (système physique). <br>
- Soit $$x$$ un point sur $$M$$ (état du système). <br>
- Soit $$f$$ une fonction lisse sur $$M$$ (appareil de mesure).

Donc, nou pouvons dire que qu'un état $$x_{i}$$ sur $$M$$ peut être mesurée par $$f(x_{i})$$. Comment l'évolution fonctionne dans ce cas?, nous avons besoin d'obtenir un ensemble de dispositifs 
de mesure (un $$\mathbb{R}$$-algèbre homomorphisme) et alors l'évolution dépend de la façon dont es le comportement dans celle collection, ainsi $$f$$ peut être considérée comme une 
hamiltonien fonction, plus prêcisément une structure de poisson sur une variétè lisse $$M$$ associe à chaque fonction lisse $$f$$ sur $$M$$, un champ vectoriel
$$\pi_{f}$$ sur $$M$$. Après cette courte intuition, nous allons définir formellement certains concepts.

<b>Définition</b>
---
Soit $$M$$ une variété lisse et soit un algèbre de Lie

$$
\{,\}: C^{\infty}(M) \times C^{\infty}(M) \rightarrow C^{\infty}(M)
$$

qui est appelé un <b>Crochet de Poisson</b> sur l'espace vectorial des fonctions lisses sur $$M$$ et il est antisymétrie

$$
\label{a}\tag{1}
\{F \cdot G, H\} = F \cdot \{G, H\} + G \cdot \{F, H\}
$$

Une structure de poisson sur $$M$$ est un champ bivecteur lisse $$\pi$$ sur $$M$$ satisfaisant $$[\pi, \pi]_{s} = 0$$, où $$[\cdot, \cdot]_{s}$$ est le [Crochet de Schouten][SCHOUTER]. Soit $$U$$ être une partie ouverte de $$M$$ et soit $$F, G \in C^{\infty}(U)$$ être des fonctions lisses, l'opération bilinéaire $$\{ \cdot, \cdot\}_{U}$$ est défini par
$$
\{F, G\}_{U}(m) = \langle d_{m}F \wedge d_{m}G, \pi_{m} \rangle
$$
pour tous $$m \in M$$, qui satisfait le [Identité de Jacobi][JACOBI].

<b>Formalisme Hamiltonien</b>
---
Pour parler de formalisme hamiltonien, rappelons la définition d'un $$k$$-forme différentielle.

$$\small\boxed{\text{Chaque $k$-forme différentielle sur l'espace $n$-dimension avec un système de coordonnées donné $x_{1}, \dots, x_{n}$ peut être écrit de manière unique
$
\\ \\
\pi^{k} = \sum_{i_{i} < \dots < i_{k}} a_{i_{1}, \dots, i_{k}}(x)dx_{i_{1}} \wedge \dots \wedge dx_{i_{k}},
\\ \\
$
où les $a_{i_{1}, \dots, i_{k}}$ sont fonctions lisses sur $n$-dimension.
}}$$ 

Si nous prenons le 2-forme $$\pi^{2}|_{x}$$ à un point $$x$$ d'une variété $$M$$ et il est différentiable, alors nous disons que c'est une 2-forme sur l'espace tangent 
$$T_{x}M$$ (i.e. Une fonction antisymétrique 2-linéaire de 2 vecteurs $$P_{1}, P_{2}$$ tangente au $$M$$ á x).

Soit $$A$$ une $$\mathbb{R}$$-algébre, alors $$\Delta: A \rightarrow A$$ est appelé un opérateur différentiel linéaire. Soient Diff$$_{k}$$ l'essemble de tous 
opérateur différentiel d'ordre $$\leq k$$ agissant sur $$A$$ à partir de $$A$$. Soient $$S_{k}(A) = \frac{\text{Diff}_{k}(A)}{\text{Diff}_{k-1}(A)}$$ un module quotient
qui est appelé les $$k$$-symboles, maintenant laissez-nous définir l'algèbre des symboles pour l'algèbre $$A$$ de la manière suivante:

$$
\label{b}\tag{2}
\text{Smbl}(A) = \bigoplus_{n=0}^{\infty} S_{n}(A)
$$

Soient $$\mathfrak{s} = \text{smbl}_{i}\Delta$$, où $$\text{smbl}_{i}\Delta \in S_{k}(A)$$ pour $$i = 1, \dots, k$$ et grâce à \ref{a}, on peut dire ça

$$
\label{c}\tag{3}
\{ \mathfrak{s_{\Delta}}, \mathfrak{s}_{\nabla} \} = \mathfrak{s}_{[\Delta, \nabla]}
$$

depuis $$[f, g] = [g, f] = 0$$ pour $$f, g \in C^{\infty}(U)$$ où $$U \subset M$$. Appliquant \ref{c} à $$F = f(x)p^{\alpha}, G = g(x)p^{\beta}$$ où
$$\{p^{\alpha}, p^{\beta}\} = 0$$, nous avons

$$
\{F, G\} = \{f(x)p^{\alpha}, g(x)p^{\beta}\} \\
         \hspace{5cm} = \{f(x), g(x)\}p^{\alpha} p^{\beta} + \{f(x), p^{\alpha}\}g(x)p^{\beta} \\
\hspace{5.8cm}          + \{p^{\alpha}, g(x) \}f(x)p^{\beta} + \{p^{\alpha}, p^{\beta}\}f(x)g(x) \\
\hspace{5cm}         = \{p^{\alpha}, g(x)\}f(x)p^{\beta} - \{p^{\alpha}, f(x)\}g(x)p^{\beta} \\
$$

par l'égalité

$$
\{p^{\alpha}, g(x) \} = \sum_{i=1}^{n} \frac{\partial p^{\alpha}}{\partial p_{i}} \frac{\partial g}{\partial x_{i}}, 
\hspace{1cm} \{p^{\beta}, f(x) \} = \sum_{i=1}^{n} \frac{\partial p^{\beta}}{\partial p_{i}} \frac{\partial f}{\partial x_{i}}, 
$$

Après quelques calculs, nous obtenons

$$
\{F, G\} = \sum_{i=1}^{n} \left( \frac{\partial F}{\partial p_{i}}\frac{\partial G}{\partial x_{i}} - \frac{\partial G}{\partial p_{i}}\frac{\partial F}{\partial x_{i}}  \right)
$$

qui est le standard crochet de poisson sur $$T^{*}M$$, forme $$X_{F} = \{F, G\}$$, alors $$X_{F}$$ est le champ de vecteurs hamiltonien sur $$T^{*}M$$ avec le hamiltonien $$F$$.

Donc, il y a beaucoup de travail à faire et étude sur la structure de poisson, ceci est seulement une courte introduction, toutefois selon de l'espace sur nous travaillons, il est pas toujours facile de définir une structure de poisson, la prochaine fois nous allons parler de comment nous pouvons décrire une structure de poisson sur une variété avec singularités, ceci grâce au travail de Miss <b>Maria Sorokina</b>: [Poisson structure on manifolds with singularities][SOROKINA].

[ARXIV]: http://arxiv.org/pdf/1601.00089v1.pdf
[SCHOUTER]: https://en.wikipedia.org/wiki/Schouten%E2%80%93Nijenhuis_bracket
[JACOBI]: https://en.wikipedia.org/wiki/Jacobi_identity
[SOROKINA]: http://arxiv.org/pdf/1312.6262v1.pdf
