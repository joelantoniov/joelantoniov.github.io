---
layout: post
title:  "Vieta Root Jumping"
date:   2014-09-21 16:00:00
categories: pt post
---

Olá pessoal, esta publicaçäo é sobre uma boa técnica de prova a teoria dos números úteis no concurso de matemática como [IMO][IMO], [IMC][IMC], etc.
O chamado <b>Vieta Root Jumping</b>.
O Vieta jumping, que tem um tema comum de uma prova por descendência infinita, por exemplo graças a Vieta jumping, podemos ter um <b>Árvore de Markov</b>, que é gerado por <b>Números de Markov</b>


<b>Números de Markov</b>
---

Um número de Markov é um número inteiro positivo $$x$$, $$y$$ ou $$z$$ que faz parte de uma soluçao para a equação diofantina de Markov:
$$ x^{2} + y^{2} + z^{2} = 3xyz$$. Assim, através de equação anterior temos a seqüência  [$$ 1, 2, 5, 13, 29... $$][OEIS-A002559].

Em particular se pode normalizar os triplos para que  $$ x \leqslant y \leqslant z$$. Então se $$(x, y, z)$$ é um triple de Markov então por
Vieta jumping é assim $$(x, y, 3xy-z)$$. Lindo, não é?

Mas como chegamos a $$(x, y, 3xy-z)$$? Bem, nós podemos fazer isso através de <b>Fórmulas de Vieta</b>

<b>Fórmulas de Vieta</b>
---

Fórmulas de Vieta são fórmulas que relacionam os coeficientes de um polinômio de somas e produtos de suas raízes.
Qualquer polinômio geral de grau $$n$$

$$
P(x) = a_{n}x^{n} + a_{n-1}x^{n-1} + ... + a_{1}x + a_{0}
$$

(com os coeficientes de ser números reais ou complexos e $$a_{n} \neq 0$$) é conhecido pela <b>Teorema fundamental da álgebra</b> ter $$n$$ raízes complexas 
$$x_{1}, x_{2}, ..., x_{n}$$. Fórmulas de Vieta relacionam os coeficientes do polinômio {$$a_{k}$$} a somas e produtos de suas raízes assinados {$$x_{i}$$}
do seguinte modo:


$$
\left\{ \begin{array}{llll} 
x_{1} + x_{2} + ... + x_{n-1} + x_{n} = -\frac{a_{n-1}}{a_{n}} \\
(x_{1}x_{2} + x_{1}x_{3} + ... + x_{1}x_{n}) + (x_{2}x_{3} + x_{2}x_{4} + ... + x_{2}x_{n}) + ... + x_{n-1}x_{n} = \frac{a_{n-2}}{a_{n}} \\
\vdots \\
x_{1}x_{2} ...x_{n} = (-1)^{n}\frac{a_{0}}{a_{n}},
\end{array}\right.
$$

De forma equivalente, afirmou o ($$n-k$$)º coeficiente $$a_{n-k}$$ está relacionada com uma soma de todos os possíveis assinado sub-produtos de raízes, tomado $$k$$ por vez:

$$
\sum_{1 \leq i_{i} < i_{2} < ... < i_{k} \leq n}{x_{i_{1}}x_{i_{2}} ...x_{i_{k}} = (-1)^{k}\frac{a_{n-k}}{a_{n}}}
$$

Por exemplo:

Para o polinômio $$P(x) = ax^{3} + bx^{2} + cx + d$$, as raízes $$x_{1}, x_{2}, x_{3}$$ da equação $$P(x) = 0$$ satisfazem

$$x_{1} + x_{2} + x_{3} = -\frac{b}{a}, \ \ \ x_{1}x_{2} +x_{1}x_{3} + x_{2}x_{3} = \frac{c}{a}, \ \ \ x_{1}x_{2}x_{3} = -\frac{d}{a}$$

<b>Resolvendo problemas</b>
---

Já temos as definições básicas para provar algumas afirmações, então vamos començar com o problema clásico de IMO 1998:

<b>$$1.-$$ Seja $$a$$ e $$b$$ inteiros positivos de modo que $$ab + 1$$ divide $$a^{2} + b^{2}$$. Provar que $$\frac{a^{2}+b^{2}}{ab+1}$$ é um quadrado perfeito.</b>

$$Solução$$

Seja $$k = \frac{a^{2}+b^{2}}{ab+1}$$, consideramos todos os pares $$(a, b)$$ não negativos que sastifazem a equação: 

$$\frac{a^{2}+b^{2}}{ab+1} = k,$$ então  $$s =$$ {$$(a, b): a, b  \ \ \epsilon \ \ \mathbb{Z}^{+} \wedge \frac{a^{2}+b^2}{ab+1} = k$$}

Existe um par $$(a, b)$$ onde $$b=0$$, neste caso temos:

$$
\frac{a^{2}+0}{a(0)+1} = k \\
a^{2} = k
$$

Assim, para este caso a nossa prova está completa. Para comprovar esta afirmação, suponha-se que $$k$$ não é um quadrado perfeito e que $$(A, B \ \epsilon \ \  S)$$
é o par que minimizem $$a+b$$ sobre todos os pares $$(a, b) \ \epsilon \ \ S$$. Assim, assumimos que: $$A \geqslant B > 0$$, temos a equação:

$$
\frac{X^{2} + B^{2}}{XB + 1} = k,
$$

O que equivale a:

$$
X^{2} - KBX + B^{2} - k = 0
$$

Como uma equação  quadrática em $$X$$. Sabemos que $$X_{1} = A$$ é uma raiz desta equação, pela Vieta's formula a outra raiz da equação é:

$$
X_{2} = \frac{(-1)^{2}(B^{2}-k)}{A} = \frac{B^{2}-k}{A}
$$

Percebemos que $$X_{2}$$ é um inteiro e $$X_{2}\neq0$$ caso contrário, $$k=B^{2}$$ seria um quadrado perfeito, contradizendo nossa suposição.
Também, $$X_{2}$$ não pode ser negativa, pois de outra forma:

$$
X_{2}^{2} - kBX_{2} + B^{2} - k \geqslant X_{2}^{2} + k + B^{2} - k > 0,
$$

uma contradição, daí, $$X_{2} \geqslant 0$$ e portanto $$(a, b) \  \epsilon \ \ S$$. No entanto, porque $$A \geqslant B$$, temos:

$$
X_{2} = \frac{B^{2}-k}{A} < A,
$$

Assim $$X_{2}+B < A+B$$, contradiciendo la minimalidad de $$A+B \ \$$ C.Q.D. 


<b>$$2.-$$ (IMO 2007) Seja $$a, b$$ números inteiros positivos. Mostre que se $$4ab-1$$ divide $$(4a^{2}-1)^{2}$$, então $$a=b$$</b>


$$
Solução
$$

Seja $$k = \frac{(4a^{2}-1)^{2}}{(4ab-1)}$$, consideramos o par $$(a, b)$$ não negativo que satisfazem esta equação:

$$\frac{(4a^{2}-1)^{2}}{(4ab-1)} = k$$, Então $$s = $$ {$$(a,b): a, b \ \epsilon \ \ \mathbb{Z}^{+} \wedge \frac{(4a^{2}-1)^{2}}{(4ab-1)} = k$$},

Existe um par $$(a, b)$$ onde $$a=b$$, neste caso temos:

<b>Primeiro caso:</b>

$$
\frac{(4a^{2}-1)^{2}}{4a^{2}-1} = k 
$$

$$
(4a^{2}-1) = k
$$

Vamos fazer $$2a=x$$, então $$(x^{2}-1) = k$$

<b>Segundo caso:</b>

$$
\frac{(4b^{2}-1)^{2}}{4b^{2}-1} = k 
$$

$$
(4b^{2}-1) = k
$$

Vamos fazer $$2b=y$$, então $$y^{2}-1 = k$$

Então,

$$
y^{2}-1 = x^{2}-1  \\

y = x
$$

Substituindo 

$$
2a=2b
$$

$$
a=b
$$

Assim, para este caso a nossa prova está completa. Para provar essa afirmação, supomos que $$a \neq b$$ e que $$(A, B) \ \epsilon \ \ s$$ é o par 
onde $$a$$ and $$b$$ nunca são iguais para todos os pares $$(a, b) \ \ \epsilon \ s$$. Assim, assumimos que $$(A > B > 0) \vee (0 < A < B)$$

Vamos fazer  $$2A = X$$

$$
\frac{(X-1)^{2}}{XB - 1} = k
$$

O que equivale a dizer:

$$
X^{2} - 2X + 1 = XBK - K = 0 \\
x^{2}  - XBX - 2X + (1 + k) = 0
$$

Como uma equação quadrática em $$X$$. Através de fórmulas de Vieta sabemos que $$X_{1}=2A$$ é uma das raízes dessa equação, a outra é:

$$
X_{2} = \frac{-2X + (1+k)}{2A}
$$

Percebemos que $$X_{2}$$ é um nùmero inteiro e $$(A>B) \vee (B<A)$$, a outra forma $$A$$ poderia ser igual a $$B$$, contrariando nossa suposição. 
Também nota-se que para qualquer $$k \ \epsilon \ \ \mathbb{Z}^{+}$$, nem $$A>B$$ ou $$B<A$$ não é estritamente necessário. Assim,

$$
X_{2}^{2} - kBX_{2} - 2X_{2} + (1 + k) \geqslant X_{2}^{2} - X_{2} - 2X_{2} + (1 + k) \\

\\

\vee \\

\\

X_{2}^{2} - kBX_{2} - 2X_{2} + (1 + k) \leqslant X_{2}^{2} - X_{2} - 2X_{2} + (1 + k) \\
$$

Uma contradição, portanto $$a \neq b$$. Assim $$X_{2} + B \leqslant A + B$$, contradizendo a declaração de $$A \neq B$$. C.Q.D


[IMO]: http://imo-official.org/ 
[IMC]: http://www.imc-math.org.uk/
[OEIS-A002559]: https://oeis.org/A002559
