---
layout: post
title:  "Structure de Poisson sur variétés avec singularités"
date:   2016-02-27 18:30:00
categories: fr post
---

Dans mom dernier post Je l'ai écrit d'une introduction á [Structure de Poisson][PS], maintenant Je vais expliquer comment nous pouvons décrire une 
structure de poisson sur variétés avec singularités, ce travail a été réalise par <b>Maria Sorokina</b> dans sa publication: [Poisson structure on manifolds with singularities][SOROKINA], donc si tu veux avoir des détails, tu devrais le lire, Je suis süre que ça va t'amuser.

Tout d'abord, nous rappelons la définition de la structure de poisson.

$$
\small\boxed{\text{Soit} \ M \ \text{une variété lisse, une structure de poisson sur } \ M \  
 \text{est un champ bi-vectuer lisse} \ \pi \ \text{sur} \ M \ \text{satisfaisant}
  \ [\pi, \pi]_{s} = 0, \\ \text{où} \ [\cdot, \cdot]_{s} \ \text{est le Crochet de Schouten. Soit} \ U \ \text{être une partie ouverte de} \ M \ \text{et soient } \ F, G \in C^{\infty}(U) \ \text{être des fonctions lisses} \\  \text{l'opération bilinéaire} \
  \{ \cdot, \cdot \}_{U} \ \text{est défini par } \ \{F, G\}_{U}(m) = \langle d_{m}F \wedge d_{m}G, \pi_{m} \rangle \ \text{pour tous} \ m \in M \text{, qui satisfait le identité de Jacobi } \\ \text{ et défini un algèbre de Lie sur} \ C^{\infty}(U).
}
$$

Comme Sorokina dit dans le papier, une singularité peut provoquer des charges lourdes sur les pièces de systèmes, dons la clé ici est considérer une algèbre dont le spectre coincide avec la espace de configuration avec singularités. En premier lieu, nous devons utiliser [la théorie de l'opérateur différentiel.][DFT].

<b>Opérateur différentiel</b>
---

Soit $$A$$ être un $$\mathbb{R}$$-algèbre, un opérateur différentiel linéaire d'ordre $$k$$ est un $$\mathbb{R}$$-homomorphisme $$\Delta: A \longrightarrow A$$ avec valeurs dans $$A$$ tel que

$$
(\delta_{a_{0}} \circ \dots \circ \delta_{a_{k}})(\Delta) = 0
$$

où $$a_{i} \in A$$, l'essemble de tous opérateur différentiel est représenté par  Diff$$_{k}$$. Maintenant, nous pouvons définir un module quotient par  $$S_{k} = \frac{\text{Diff}_{k}(A)}{\text{Diff}_{k-1}(A)}$$, qui est appelèe <b>le module de symboles d'ordre $$k$$</b>, de cette manière, nous pouvons définir l'algèbre des symboles pour une algèbre  $$A$$:

$$
\text{Smbl}(A) = \bigoplus_{n=0}^{\infty} S_{n}(A)
$$

Comme tout variété $$M$$ peut être déterminée par la lisse $$\mathbb{R}$$-algèbre $$A = C^{\infty}(M)$$ sur les fonctions de ce, pour chaque $$x$$ sur $$M$$ est la $$\mathbb{R}$$-algèbre homomorphisme $$:A \longrightarrow \mathbb{R}$$. ça attribue à chaque fonction $$f \in A$$ sa valeur $$f(x)$$ à un point $$x$$.

<b>Produit fibré d'algèbres</b>
---

Maintenant, Nous allons décrire l'algèbre désirée comme le produit fibre de deux algèbres connus. Soit $$A_{1} = C^{\infty}(M_{1}), A_{2} = C^{\infty}(M_{2})$$, pour variétés $$M_{i}, i= 1, 2$$. Le produit fibré est unique à isomorphisme unique, cela signifie

$$
A = A_{1} \oplus A_{2} = \{ (a_{1}, a_{2}) \in A_{1} \oplus A_{2}: p_{1}(a_{1}) = p_{2}(a_{2})  \}
$$

où $$p_{i}: A_{i} \longrightarrow C$$ est un homomorphisme pour certains $$\mathbb{R}$$-algèbre $$C$$.

<b>Construction des opérateurs différentiels</b>
---

Soit $$A$$ être une algèbre qui est le produit cartésien des algèbres $$A_{1}$$ et $$A_{2}$$ sur l'algèbre $$C$$. Soit $$\Delta \in \text{Diff}_{k}(A)$$, alors il existe une linéaire unique  $$\Delta_{i}: A_{i} \longrightarrow A_{i}$$, for $$i=1, 2$$ tel appartient à Diff$$_{k(A)}$$.

Dans l'étude de Sorokina, elle considère $$M = N = C = \mathbb{R}$$ comme exemple, nous allons considérer $$M = N = \mathbb{R}^{2}$$ et $$C = \mathbb{R}$$.

<b>Exemple</b>
---

Considérons le coordonner transversale sur le plan:

$$
\mathbb{K}_{0} = \{ (x_{1}, x_{2}), (y_{1}, y_{2}) \in \mathbb{R}^{2} | x_{i}y_{i} = 0, \text{for } i=1, 2  \}
$$

Algèbre des fonctions lisses sur la croix est donnée par la formule:

$$
A = C^{\infty}(\mathbb{K}_{0}) = C^{\infty}(\mathbb{R}^{2})|_{\mathbb{K}_{0}} = \{(f(x_{1}, x_{2}), g(y_{1}, y_{2}))| f(0, 0) = g(0, 0) \}
$$

En appliquant l'algorithme:

$$
A_{1} = A_{2} = C^{\infty}(\mathbb{R}), C = \mathbb{R}, p_{1}(f) = f(0, 0), p_{2}(g) = g(0, 0)
$$

Les opérateurs différentiels:

$$
\text{Diff}_{k}(A) = \{ (\Delta_{1}, \Delta_{2})| a_{i}(0, 0) = b_{i}(0, 0), i = 0, \dots, k  \}
$$


$$
\Delta_{1} = \sum_{i=0}^{k} a_{i}(x_{1}, x_{2}) \left( \frac{\partial}{\partial x}  \right)^{i},
$$


$$
\Delta_{2} = \sum_{i=0}^{k} b_{i}(y_{1}, y_{2}) \left( \frac{\partial}{\partial y}  \right)^{i}
$$

Pour un ordre no nulle:

$$
[\Delta]_{k} = ([\Delta_{1}], [\Delta_{2}]),
$$

plus, $$a_{0}(0, 0) = b_{0}(0, 0)$$ et $$a_{k}(0, 0) = 0 = b_{k}(0, 0)$$ if $$k \geq 1$$

Crochet de Poisson:

$$
\{[\Delta], [\nabla]\} = (\{[\Delta_{1}], [\nabla_{1}]\}, \{[\Delta_{2}], [\nabla_{2}]\})
$$

où

$$
\{[\Delta_{1}], [\nabla_{1}]\} = (la_{l_{\Delta}}(x_{1}, x_{2})a'_{n_{\nabla}}(x_{1}, x_{2}) - na_{n_{\nabla}}(x_{1}, x_{2})a'_{l_{\Delta}}(x_{1}, x_{2})) \left( \frac{\partial}{\partial x} \right)^{l+n-1}
$$

$$
\{[\Delta_{2}], [\nabla_{2}]\} = (lb_{l_{\Delta}}(y_{1}, y_{2})b'_{n_{\nabla}}(y_{1}, y_{2}) - nb_{n_{\nabla}}(y_{1}, y_{2})b'_{l_{\Delta}}(y_{1}, y_{2})) \left( \frac{\partial}{\partial y} \right)^{l+n-1}
$$

Ainsi, nous obtenons les conditions suivantes:

$$
a_{0}(0, 0) = b_{0}(0, 0), a_{i}(0, 0) = 0 = b_{i}(0, 0), i \geq 1, i = l_{\Delta}, b_{\nabla}.
$$

L'algèbre de symboles est Smbl$$(A) = S_{0} \oplus S_{1} \oplus \dots$$

<b>Lemme</b>
$$
\small\boxed{
\text{Pour la croix coordonner} \ |\text{Smbl}(A)| \ \text{est 0-dimensionnelle au le point de
singularité et une dimension à d'autres points.}
}
$$

<b>Démonstration:</b>
Définissons homomorphisme de l'algèbre des symboles à $$\mathbb{R}$$

$$
\text{Smbl}(A) = \text{Smbl}_{0}(A) \oplus \text{Smbl}_{1}(A) \oplus \dots
$$

$$H|_{S_{0}} = h_{0}$$, nous savons que $$S_{0} = A$$, soit $$(a_{k}, b_{k}) \in $$ Smbl$$_{k}$$
 par [Lemme de Hadamard][HL]:

$$
(a_{k}, b_{k}) = (a'(0, 0)x + x^{2} \tilde{a}, b'(0, 0)y + y^{2}\tilde{b}) = (a'(0, 0)x, b'(0, 0)y) + (x, y)(x\tilde{a}, y\tilde{b}),
$$

où

$$
(a'(0, 0)x, b'(0, 0)y) \in \text{Smbl}_{k}, (x, y) \in \text{Smbl}_{0}, (x\tilde{a}, y\tilde{b}) \in \text{Smbl}_{k}, (\tilde{a}, \tilde{b}) \in C^{\infty}(\mathbb{R})
$$

$$
H_{k}(a, b) = H_{k}(a'(0, 0)x, b'(0, 0)y), k > 0
$$

Comme $$a'(0, 0) = 0 = b'(0, 0), H_{k}(a, b) = 0$$

$$
(H_{k}(a, b))^{2} = H_{2k}((a. b)(a. b)) = H_{2k}(a^{2}, b^{2}) = 0,
$$

Donc, $$H_{k}(a, b) = 0$$.

Comme on peut le voir, travail sur les espaces avec singularités est gentil, dans mon prochain post Je vais parler de comment nous pouvons décrire une structure de poisson sur les variétés avec coins, la définition des variétés avec coins a été donnée par Mr. Dominic Joyce dans son papier: [On manifolds with corners][JOYCE].

[PS]: http://joelantonio.me/fr/post/2016/02/18/Poisson-sctructure/
[SOROKINA]: http://arxiv.org/pdf/1312.6262v1.pdf
[DFT]: https://fr.wikipedia.org/wiki/Op%C3%A9rateur_diff%C3%A9rentiel
[HL]: https://fr.wikipedia.org/wiki/Lemme_de_Hadamard
[JOYCE]: http://arxiv.org/pdf/0910.3518v2.pdf
