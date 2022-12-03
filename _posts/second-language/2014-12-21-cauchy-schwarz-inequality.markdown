---
layout: post
title:  "Inégalité de Cauchy-Schwarz"
date:   2014-12-21 06:00:00
categories: fr post
---

Coucou tout le monde, ça va? Pendant cette opportunité nous allons parler a propos de le <b>Inégalité de Cauchy-Schwarz</b>, Il est une inégalité bien connue et utile entres les branches des matemátiques. En fait, Il est un cas particulier de <b>Inégalité de Hölder</b>. En concours de mathématiques, il est très utile. Donc, commençons avec la définition.

<b>Définition</b>
---

Soient $$a_{i}, b_{i}$$, pour $$ i = 1, 2, ..., n$$ être des nombres réels. Alors:

$$
\left( \sum_{i=1}^{n} a_{i}b_{i} \right)^2 \leq \left( \sum_{i=1}^{n} a_{i}^2 \right) \left( \sum_{i=1}^{n} b_{i}^2 \right)
$$

L'égalité se produit si et seulement si il existe $$ c \in \mathbb{R} $$ telle que $$ b_{i} = ca_{i} $$, pour $$ i=1, 2, ..., n$$

<b>Une preuve facile pour L'inégalité de Cauchy-Schwarz</b>
---

Il y a beaucoup de preuves à ce sujet. Je crois que le ci-dessous est la manierè plus facile.

Soit:

$$
F(x) = (a_{1}x - b_{1})^2 + (a_{2}x - b_{2})^2 + \cdots + (a_{n}x - b_{n})^2
$$

Étant une somme de carrés, $$F(x)$$ est toujours non négatif. Maintenant, nous élargissons et recueillons termes:

$$
F(x) = \left( \sum_{i=1}^{n} a_{i}^2 \right)x^2 - 2\left( \sum_{i=1}^{n} a_{i}b_{i} \right)x + \left( \sum_{i=1}^{n} b_{i}^2 \right)
$$

Le discriminant est $$\leq 0$$, le calcul du discriminant nous avons:

$$
4\left( \sum_{i=1}^{n}a_{i}b_{i} \right)^2 - 4\left( \sum_{i=1}^{n} a_{i}^2\right) \left( \sum_{i=1}^{n} b_{i}^2 \right) \leq 0
$$

Divisant par 4 et réarrangeant rendements L'inégalité de Cauchy-Schwarz. Il détient lorsque $$F$$ a une racine réelle (répété bien sûr). De la première forme de $$F$$
et en utilisant le fait que la somme des carrés égale à 0 seulement quand chaque carré est égal à 0, nous avons $$a_{i}x - b_{i} = 0 \Rightarrow a_{i}/b_{i} = x$$ pour tout
$$1 \leq i \leq n$$ qui est quand $$a_{i}/b_{i}$$ est constant pour tous $$i$$.

<b>Une preuve trigonométrique</b>
---

<img src="/bootstrap/images/right_triangle.png" align="right" height="210">
 
Pour le graphique nous connaissons la suit:

$$\sin(a) = \frac{y_{1}}{\sqrt{x_{1}^2 + y_{1}^2}}$$, $$\hspace{1.3cm}$$   $$\cos(a) = \frac{x_{1}}{\sqrt{x_{1}^2 + y_{1}^2}}$$


$$\sin(b) = \frac{y_{2}}{\sqrt{x_{2}^2 + y_{2}^2}}$$, $$\hspace{1.3cm}$$  $$\cos(b) = \frac{x_{2}}{\sqrt{x_{2}^2 + y_{2}^2}}$$

Application des identités trigonométriques:

$$\cos(a+b) = \cos(a)\cos(b) - \sin(a)\sin(b)$$
$$\sin(a+b) = \sin(a)\cos(b) + \cos(a)\sin(b)$$


Alors:

$$
\cos(a+b) = \frac{(x_{1}x_{2} - y_{1}y_{2})}{\sqrt{(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)}} \hspace{1.3cm} et \hspace{1.3cm}  \sin(a+b) = \frac{(x_{2}y_{1} + x_{1}y_{2})}{\sqrt{(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)}}
$$

Nous savons aussi que  $$\sin^2(a+b) + \cos^2(a+b) = 1$$

Donc:

$$
\frac{(x_{2}y_{1} + x_{1}y_{2})^2 + (x_{1}x_{2} - y_{1}y_{2})^2}{(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)} = 1 
$$


$$
(x_{2}y_{1} + x_{1}y_{2})^2 = (x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2) - (x_{1}x_{2} - y_{1}y_{2})^2
$$

$$
(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2) - (x_{1}x_{2} - y_{1}y_{2})^2 \leq (x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)
$$

Par conséquent

$$
(x_{1}y_{2} + x_{2}y_{1})^2 \leq (x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2), 
$$
qui est le deux variables de L'inégalité de Cauchy-Schwarz $$\ \ \  \mathbb{C.Q.F.D.}$$



<b>Résoudre les problèmes</b>
---

Commençons par un problème facile.

<b>$$1.-$$ Montrer que pour $$x, y, z > 0$$, nous avons</b>

$$
x + y + z \leq 2\left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right)
$$

$$Solution$$

Faisons

$$
\left( \frac{x\sqrt{y+z}}{\sqrt{y+z}} + \frac{y\sqrt{x+z}}{\sqrt{x+z}} + \frac{z\sqrt{x+y}}{\sqrt{x+y}} \right)^2
$$

Alors, pout L'inégalité de Cauchy-Schwarz

$$
\left( \frac{x\sqrt{y+z}}{\sqrt{y+z}} + \frac{y\sqrt{x+z}}{\sqrt{x+z}} + \frac{z\sqrt{x+y}}{\sqrt{x+y}} \right)^2 \leq \left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right) \left( 2x + 2y + 2z \right)
$$

$$
\left( x + y + z \right)^2 \leq 2\left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right) \left( x + y + z \right)
$$

$$
\left( x + y + z \right) \leq 2\left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right) \ \ \ \mathbb{C.Q.F.D.}
$$

<b>$$2.-$$ (APMO' 1991) Pour réels positifs $$\{ a_{i}, b_{i}\}$$ telles que $$a_{1} + a_{2} + \cdots + a_{n} = b_{1} + b_{2} + \cdots + b_{n}$$, montrer que</b>

$$
\frac{a_{1}^2}{a_{1} + b_{1}} + \frac{a_{2}^2}{a_{2} + b_{2}} + \cdots + \frac{a_{n}^2}{a_{n} + b_{n}}  \geq \frac{a_{1} + a_{2} + \cdots + a_{n}}{2}
$$

$$Solution$$

Nous supposons aussi vrai la dernière phrase et faisons un artifice.

$$
\frac{a_{1}^2}{a_{1} + b_{1}} + \frac{a_{2}^2}{a_{2} + b_{2}} + \cdots + \frac{a_{n}^2}{a_{n} + b_{n}}  \geq \frac{(a_{1} + a_{2} + \cdots + a_{n})(a_{1} + a_{2} + \cdots + a_{n})}{2(a_{1} + a_{2} + \cdots + a_{n})}
$$

Nous savons que $$a_{1} + \cdots + a_{n} = b_{1} + \cdots + b_{n}$$, alors au lieu de $$2(a_{1} + a_{2} + \cdots + a_{n})$$ nous écrivons $$ a_{1} + \cdots + a_{n} + b_{1} + \cdots + b_{n}$$ Aussi, nous allons faire $$a_{i} + b_{i} = c_{i}$$ for $$i = 1, \cdots, n$$

$$
\frac{a_{1}^2}{c_{1}} + \frac{a_{2}^2}{c_{2}} + \cdots + \frac{a_{n}^2}{c_{n}}  \geq \frac{(a_{1} + a_{2} + \cdots + a_{n})^2}{(c_{1} + c_{2} + \cdots + c_{n})}
$$

$$
\left( \frac{a_{1}^2}{c_{1}} + \frac{a_{2}^2}{c_{2}} + \cdots + \frac{a_{n}^2}{c_{n}} \right)(c_{1} + c_{2} + \cdots + c_{n}) \geq (a_{1} + a_{2} + \cdots + a_{n})^2
$$

Disons que avant la dernière phrase, il y avait un remplacement d'un $$a_{i} \rightarrow \frac{a_{i}}{\sqrt{c_{i}}}$$ and $$c_{i} \rightarrow \sqrt{c_{i}}$$ for $$1 \leq i \leq n$$, alors l'inégalité aurait pu se lire comme:

$$
(a_{1}^2 + a_{2}^2 + \cdots + a_{n}^2)(c_{1}^2 + c_{2}^2 \cdots + c_{n}^2) \geq (a_{1}c_{1} + a_{2}c_{2} + \cdots + a_{n}c_{n})
$$

Nous remarquons que la dernière phrase est en fait l'inégalité de Cauchy-Schwarz, alors nous
pouvons conclure que:

$$
\frac{a_{1}^2}{a_{1} + b_{1}} + \frac{a_{2}^2}{a_{2} + b_{2}} + \cdots + \frac{a_{n}^2}{a_{n} + b_{n}}  \geq \frac{a_{1} + a_{2} + \cdots + a_{n}}{2} \ \ \ \mathbb{C.Q.F.D.}
$$

Mais il ya autre chose, nous remarquons que:

$$
\huge\boxed{\frac{a_{1}^2}{c_{1}} + \frac{a_{2}^2}{c_{2}} + \cdots + \frac{a_{n}^2}{c_{n}}  \geq \frac{(a_{1} + a_{2} + \cdots + a_{n})^2}{(c_{1} + c_{2} + \cdots + c_{n})} }
$$

est une conséquence de l'inégalité de Cauchy-Schwarz, ce lemme est connu comme <b>Lemme de Titu</b>. Qui est une forme spéciale qui aide à lutter contre un grand nombre de problèmes d'optimisation impliquant des places dans le numérateur, immédiatement.

<b>$$3.-$$ (China Mathematical Olympiad 2004) Pour un nombre entier donné $$n \geq 2$$, supposons entiers positifs $$a_{i}(i=1, 2, \cdots, n)$$ satisfaire $$a_{1} \leq \cdots \leq a_{n}$$ et $$\sum_{i=1}^{n}\frac{1}{a_{i}} \leq 1$$. Prouver que, pour tout nombre réel $$x$$, l'inégalité suivante est,</b>

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right) \leq \frac{1}{2}\frac{1}{a_{1}(a_{1}-1) + x^2}
$$

$$
Solution
$$

Pour $$x^2 \geq a_{1}(a_{1}-1)$$, de $$\sum_{i=1}^{n} \frac{1}{a_{i}} \leq 1$$ nous avons 

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right) \leq \left( \sum_{i=1}^{n} \frac{1}{2a_{i}|x|} \right)^2 = \frac{1}{4x^2}\left( \sum_{i=1}^{n} \frac{1}{a_{i}} \right)^2
$$

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right) \leq \frac{1}{4x^2} \leq \frac{1}{2}\frac{1}{a_{1}(a_{1}-1) + x^2}
$$

Pour $$x^2 < a_{1}(a_{1}-1)$$, utilisant l'inégalité de Cauchy-Schwarz, nous avons

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right)^2 \leq \left( \sum_{i=1}^{n} \frac{1}{a_{i}} \right) \left( \sum_{i=1}^{n} \frac{a_{i}}{(a_{i}^2 + x^2)^2} \right)\leq  \sum_{i=1}^{n} \frac{a_{i}}{(a_{i}^2 + x^2)^2}
$$

Plus, pour des entiers positifs $$a_{1} < \cdots < a_{n}$$, nous avons $$a_{i+1} \geq a_{i}+1$$ et

$$
\frac{2a_{i}}{(a_{i}^2 + x^2)^2} \leq \frac{2a_{i}}{\left(a_{i}^2 + x^2 + \frac{1}{4}\right)^2 - a_{i}^2} = \frac{2a_{i}}{\left( \left( a_{i} - \frac{1}{2}\right)^2 + x^2 \right) \left( \left( a_{i} + \frac{1}{2}\right)^2 + x^2 \right)}
$$

$$
= \frac{1}{\left( a_{i} - \frac{1}{2}\right)^2 + x^2} - \frac{1}{\left( a_{i} + \frac{1}{2}\right)^2 + x^2} \leq \frac{1}{\left( a_{i} - \frac{1}{2}\right)^2 + x^2} - \frac{1}{\left( a_{i+1} - \frac{1}{2}\right)^2 + x^2}
$$

Pour $$i=1, \cdots, n-1$$. Donc

$$
\sum_{i=1}^{n} \frac{a_{i}}{(a_{i}^2 + x^2)^2} \leq \frac{1}{2} \sum_{i=1}^{n}\left[ \frac{1}{\left( a_{i} - \frac{1}{2}\right)^2 + x^2} - \frac{1}{\left( a_{i+1} - \frac{1}{2}\right)^2 + x^2} \right] \leq \frac{1}{2}\frac{1}{\left( a_{1} - \frac{1}{2} \right)^2 + x^2} \leq \frac{1}{2}\frac{1}{a_{1}(a_{1}-1)+x^2} \mathbb{C.Q.F.D.}
$$
