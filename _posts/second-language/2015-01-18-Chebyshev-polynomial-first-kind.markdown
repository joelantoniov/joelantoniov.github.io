---
layout: post
title:  "Polynôme de Tchebychev (De première espèce)"
date:   2015-01-19 17:00:00
categories: fr post
---

Nous commençons l'année 2015 avec un bon suje de polynômes, dans ce cas nous allons parler de <b>Le polynôme de Tchebychev</b>, seulement nous prenons le première espèce, nous avons laissé la seconde espèce pour une autre occasion. Alors, qu'est-il?

<b>Définition</b>
---

Les Polynôme de Tchebychev sont des polynômes avec le plus grand coefficient tête possible, avec la condition que leur valeur absolute dans l'intervalle $$[-1, 1]$$ est délimité pour $$1$$. Le polynôme de Tchebychev de première espèce sont définis par la relation de récurrence. <br>

$$T_{0}(x) = 1 $$ <br> $$T_{1}(x) = x $$ <br> $$T_{n+1}(x) = 2xT_{n}(x) - T_{n-1}(x)$$

Ils sont caractérises par la propriété:

$$
T_{n}(\cos{\theta}) = \cos{(n\theta)}
$$

Nous pouvons soulever la question suivante

<b>Montrer que pour chaque $$n \in \mathbb{N}$$ il y a un polynôme $$T_{n}$$ à coefficients entiers et $$2^{n-1}$$ est premier, tel que $$T_{n}(\cos{x}) = \cos{nx}$$ pour tous $$x$$</b>.

<b>Solution</b>

Nous sauvons que $$T_{0}(x)=1$$ et $$T_{1}(x)=x$$. Pour $$n>1$$ nous utilisons induction sur $$n$$. 

Comme $$\cos{(n+1)}x = 2\cos{x}\cos{(nx)} - \cos{(n-1)}x$$, Nous pouvons définir $$T_{n+1} = 2T_{1}T_{n} - T_{n-1}$$ depuis $$T_{1}T_{n}$$ et $$T_{n-1}$$ sont de degré $$n+1$$ et $$n-1$$ respectivement, $$T_{n+1}$$ est de degré $$n+1$$ et a le coefficient $$2\times2^{n} = 2^{n+1}$$ tête. Il résulte que la construction que tous ses coefficients est des nombres entiers.

En fait, les polynômes orthogonaux de séquence sont líes à la <b>Formule de Moivre</b>.

<b>Formule de Moivre</b>
---

Pour tout nombre complexe $$x$$ et tout nombre entier $$n$$.

$$
(\cos{x} + i\sin{x})^{n} = \cos{(nx)} + i\sin{(nx)}
$$

<b>Prouve:</b>

Nous prouvons cette formule par induction sur $$n$$ et appliquant la somme trigonométrique et les formules de produit. Nous considérons d'abord les entiers non négatifs. Le cas de base $$n=0$$ est clairement vrai. Pour l'etape d'induction, observez que:

$$
(\cos{n} + i\sin{x})^{k+1} = (\cos{x} + i\sin{x})^{k} \times (\cos{x} + i\sin{x}) \\ 
\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ = (\cos{kx} + i\sin{kx})(\cos{x} + i\sin{x}) \\ 
\ \ \ \ \ \ \ \ \ \ \ \ \ \ \  \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ = \cos{kx}\cos{x} - \sin{kx}\sin{x} + i[\sin{kx}\cos{x} + \cos{kx}\sin{x}] \\ 
\  \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \  \ \ = \cos{[(k+1)x]} + i\sin{[(k+1)x]} \\
$$

Ici, on a un problème à propos le Polynôme de Tchebychev.

<b>Prouver que la valuer maximum en absolue de tout polynôme unitaire de $$n$$-ième degrè sur $$[-1, 1]$$ n'est pas moins de $$\frac{1}{2^{n-1}}$$</b>

<b>Solution</b>


Notez que l'ègalité est valable pour un multiple de nième du Polynôme de Tchebychev $$T_{n}(X)$$
Le coefficient de $$T_{n}$$ tête est égal à $$2^{n-1}$$, alors $$C_{n}(X) = \frac{1}{2^{n-1}}T_{n}(X)$$ est un polynôme unitaire et

$$
|T_{n}(X)| = \frac{1}{2^{n-1}}|\cos{(n\arccos{x}})| \leq \frac{1}{2^{n-1}} \ \ \ \ za \ \ x \in [-1,1]
$$

En outre, les valeurs de $$T_{n}$$ dans les points $$1, \cos{\frac{\pi}{n}}, \cos{\frac{2\pi}{n}}, \dots ,  \cos{\frac{(n-1)\pi}{n}}, -1$$ sont alternativement $$\frac{1}{2^{n-1}}$$ et $$-\frac{1}{2^{n-1}}$$

Supposons maintenant que $$P \neq T_{n}$$ est un polynôme unitaire telle que $$ \max_{-1\leq x \leq 1} |P(x)| < \frac{1}{2^{n-1}}$$ 
Alors $$P(X)-C_{n}(X)$$ dans les points $$1, \cos{\frac{\pi}{n}},  \dots ,  \cos{\frac{(n-1)\pi}{n}}, -1$$ prend alternativement les valeurs positives et négatives. Par conséquent, le polynôme $$P-C_{n}$$ présente au moins $$n$$ zéros, à savoir, au moins une est très intervalle entre deux points adjacents. Cependant, $$P-C_{n}$$ est un polynôme de degré $$n-1$$ comme $$x^n$$ monôme est anunlé, Alors nous avons arrivè à une contradiction.

Au fait, Je voudrais savoir d'autres solutions pour le dernier, donc [Je demandé sur MathStackExchange][MES]. Si vous voulez partager quelque chose avec moi, s'il vous plaît envoyez-moi un message.

Maintenant, nous décrivons un théoreme engendrè par les Polynômes de Tchebychev.

<b>Le théorème de Chebyshev</b>
---

Pour $$n\geq1$$ fixe, le polynôme $$2^{-n+1}T_{n}(x)$$ est le uniqué $$n$$-ième degré polynôme Monique, satisfassent

$$
\max_{-1 \leq x \leq 1} {|2^{-n+1}T(x)|}\leq \max_{-1 \leq x \leq 1}{|P(x)|},
$$

Pour tout autre nième degré du polynôme monique $$P(x)$$. Nous allons voir un example.

<b>Soient $$A_{1}, A_{2}, \dots, A_{n}$$ points dans le plan. Prouver que sur un segment de longuour $$l$$
il y a un point $$M$$ tel que</b> 

$$
MA_{1}.MA_{2} \dots MA_{n} \geq 2 \left( \frac{1}{4} \right)^n
$$

<b>Solution</b>

Nous pouvons supposer que $$l=2$$. Coordonnèes complexe associé à des points d'une manière telle que le segment coïncide
avec l'intervalle $$[-1, 1]$$. Alors

$$
MA_{1}.MA_{2} \dots MA_{n} = |z-z_1||z-z_2| \dots |z-z_n| = |P(z)|,
$$

Où $$P(z)$$ est un polynôme monique avec coefficients complexes, et $$z \in [-1, 1]$$. 

Nous pouvons écrite $$P(z) = R(z) + iQ(z)$$, où $$R(z)$$ est la partie réelle et $$Q(z)$$ est la partie imaginaire du polynôme.
Comme $$z$$ est réel, on a $$|P(z)| \geq |R(z)|$$. Le polynôme $$R(z)$$ est monique,
ainsi sur l'intervalle [-1, 1] il varie de zéro à une distance d'au moins autant que le polynôme de Tchebychev. Ainsi,
nous pouvons trouver $$z$$ dans cet intervalle de telle sorte que $$|R(z)| \geq \frac{1}{2^{n-1}}$$. Cela implique $$|P(z)| \geq 2\frac{1}{2^n}$$, et mise à l'echelle de de retour en déduit l'existence dans le cas géneral d'un point $$M$$ satisfaisant à l'inégalite de l'énonce.

Un pas de côté de l'image classique, nous considérons aussi les familles de polynômes $$T_{n}(x)$$ définie par $$T_{0}(x) = 2, T_{1}(x) = x, T_{n+1}(x) = xT_{n}(x) - T_{n-1}(x)$$. C'est déterminé par l'égalite:

$$
T_{n}\left( z + \frac{1}{z} \right) = z^n + \frac{1}{z^n}
$$

Aussi, Je suggère de visiter la réponse étonnante pour:

<b>Soit $$a_{i} \in \mathbb{R} (i=1, 2, \dots, n)$$ et $$f(x) = \sum_{i=0}^{n}a_{i}x^{i}$$ de telle sorte que si $$ |x| \leq 1$$, alors $$|f(x)| \leq 1 $$</b> 
sur [MathStackExchange][MES2]

[MES]: http://math.stackexchange.com/q/1105882/161851
[MES2]: http://math.stackexchange.com/a/532170/161851
