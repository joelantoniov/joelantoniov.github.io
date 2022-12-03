---
layout: post
title:  "Cauchy-Schwarz Inequality"
date:   2014-12-21 06:00:00
first-language: En
second-language: Fr 
subdomain: fr
activate-lan: yes
categories: post
---

Hello guys, how you doing? This time let's talk about <b>Cauchy-Schwarz inequality</b>, it's a well known inequality and useful across multiple branches of mathematics. Actually, it's a special case of <b>Hölder's inequality</b>. In math contest, it's really useful, so let's start with the definition.

<b>Definition</b>
---

Let $$a_{i}, b_{i}$$, for $$ i = 1, 2, ..., n$$ be real numbers. Then:

$$
\left( \sum_{i=1}^{n} a_{i}b_{i} \right)^2 \leq \left( \sum_{i=1}^{n} a_{i}^2 \right) \left( \sum_{i=1}^{n} b_{i}^2 \right)
$$

Equality occurs if and only if there exists $$ c \in \mathbb{R} $$ such that $$ b_{i} = ca_{i} $$, for $$ i=1, 2, ..., n$$

<b>An easy proof for Cauchy-Schwarz Inequality</b>
---

There a lot of proofs about it, I think that below is the easiest way.

Let:

$$
F(x) = (a_{1}x - b_{1})^2 + (a_{2}x - b_{2})^2 + \cdots + (a_{n}x - b_{n})^2
$$

Being a sum of squares, $$F(x)$$ is always non-negative. Now we expand it and collect terms:

$$
F(x) = \left( \sum_{i=1}^{n} a_{i}^2 \right)x^2 - 2\left( \sum_{i=1}^{n} a_{i}b_{i} \right)x + \left( \sum_{i=1}^{n} b_{i}^2 \right)
$$

The discriminant is $$\leq 0$$, computing the discriminant we have:

$$
4\left( \sum_{i=1}^{n}a_{i}b_{i} \right)^2 - 4\left( \sum_{i=1}^{n} a_{i}^2\right) \left( \sum_{i=1}^{n} b_{i}^2 \right) \leq 0
$$

Dividing by 4 and rearranging yields Cauchy-Schwarz Inequality. It holds when $$F$$ has a real root (repeated of course). From the first form of $$F$$
and using the fact that the sum of squares equal to 0 only when each square equals to 0, we have $$a_{i}x - b_{i} = 0 \Rightarrow a_{i}/b_{i} = x$$ for all
$$1 \leq i \leq n$$ that is when $$a_{i}/b_{i}$$ is constant for all $$i$$.

<b>A Trigonometric Proof</b>
---

<img src="/bootstrap/images/right_triangle.png" align="right" height="210">
 
For the graph we know the following:

$$\sin(a) = \frac{y_{1}}{\sqrt{x_{1}^2 + y_{1}^2}}$$, $$\hspace{1.3cm}$$   $$\cos(a) = \frac{x_{1}}{\sqrt{x_{1}^2 + y_{1}^2}}$$


$$\sin(b) = \frac{y_{2}}{\sqrt{x_{2}^2 + y_{2}^2}}$$, $$\hspace{1.3cm}$$  $$\cos(b) = \frac{x_{2}}{\sqrt{x_{2}^2 + y_{2}^2}}$$

Applying trigonometric identities:

$$\cos(a+b) = \cos(a)\cos(b) - \sin(a)\sin(b)$$
$$\sin(a+b) = \sin(a)\cos(b) + \cos(a)\sin(b)$$


Then:

$$
\cos(a+b) = \frac{(x_{1}x_{2} - y_{1}y_{2})}{\sqrt{(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)}} \hspace{1.3cm} and \hspace{1.3cm}  \sin(a+b) = \frac{(x_{2}y_{1} + x_{1}y_{2})}{\sqrt{(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)}}
$$

We know also that $$\sin^2(a+b) + \cos^2(a+b) = 1$$

So:

$$
\frac{(x_{2}y_{1} + x_{1}y_{2})^2 + (x_{1}x_{2} - y_{1}y_{2})^2}{(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)} = 1 
$$


$$
(x_{2}y_{1} + x_{1}y_{2})^2 = (x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2) - (x_{1}x_{2} - y_{1}y_{2})^2
$$

$$
(x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2) - (x_{1}x_{2} - y_{1}y_{2})^2 \leq (x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2)
$$

Therefore

$$
(x_{1}y_{2} + x_{2}y_{1})^2 \leq (x_{1}^2 + y_{1}^2)(x_{2}^2 + y_{2}^2), 
$$
which is the two-variable Cauchy-Schwarz Inequality  $$\ \ \  \mathbb{Q.E.D}$$



<b>Solving problems</b>
---

Lets begin with an easy problem.

<b>$$1.-$$ Show that for $$x, y, z > 0$$, we have</b>

$$
x + y + z \leq 2\left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right)
$$

$$Solution$$

Let's make

$$
\left( \frac{x\sqrt{y+z}}{\sqrt{y+z}} + \frac{y\sqrt{x+z}}{\sqrt{x+z}} + \frac{z\sqrt{x+y}}{\sqrt{x+y}} \right)^2
$$

Then, for Cauchy-Schwarz Inequality

$$
\left( \frac{x\sqrt{y+z}}{\sqrt{y+z}} + \frac{y\sqrt{x+z}}{\sqrt{x+z}} + \frac{z\sqrt{x+y}}{\sqrt{x+y}} \right)^2 \leq \left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right) \left( 2x + 2y + 2z \right)
$$

$$
\left( x + y + z \right)^2 \leq 2\left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right) \left( x + y + z \right)
$$

$$
\left( x + y + z \right) \leq 2\left( \frac{x^2}{y+z} + \frac{y^2}{x+z} + \frac{z^2}{x+y} \right) \ \ \ \mathbb{Q.E.D}
$$

<b>$$2.-$$ (APMO' 1991) For positive reals $$\{ a_{i}, b_{i}\}$$ such that $$a_{1} + a_{2} + \cdots + a_{n} = b_{1} + b_{2} + \cdots + b_{n}$$, show that</b>

$$
\frac{a_{1}^2}{a_{1} + b_{1}} + \frac{a_{2}^2}{a_{2} + b_{2}} + \cdots + \frac{a_{n}^2}{a_{n} + b_{n}}  \geq \frac{a_{1} + a_{2} + \cdots + a_{n}}{2}
$$

$$Solution$$

We assume as true the last sentence and make an artifice.

$$
\frac{a_{1}^2}{a_{1} + b_{1}} + \frac{a_{2}^2}{a_{2} + b_{2}} + \cdots + \frac{a_{n}^2}{a_{n} + b_{n}}  \geq \frac{(a_{1} + a_{2} + \cdots + a_{n})(a_{1} + a_{2} + \cdots + a_{n})}{2(a_{1} + a_{2} + \cdots + a_{n})}
$$

We know that $$a_{1} + \cdots + a_{n} = b_{1} + \cdots + b_{n}$$, then instead of $$2(a_{1} + a_{2} + \cdots + a_{n})$$ we write $$ a_{1} + \cdots + a_{n} + b_{1} + \cdots + b_{n}$$ Also, let's make $$a_{i} + b_{i} = c_{i}$$ for $$i = 1, \cdots, n$$

$$
\frac{a_{1}^2}{c_{1}} + \frac{a_{2}^2}{c_{2}} + \cdots + \frac{a_{n}^2}{c_{n}}  \geq \frac{(a_{1} + a_{2} + \cdots + a_{n})^2}{(c_{1} + c_{2} + \cdots + c_{n})}
$$

$$
\left( \frac{a_{1}^2}{c_{1}} + \frac{a_{2}^2}{c_{2}} + \cdots + \frac{a_{n}^2}{c_{n}} \right)(c_{1} + c_{2} + \cdots + c_{n}) \geq (a_{1} + a_{2} + \cdots + a_{n})^2
$$

Let's say that before the last sentence, there was a replacement of $$a_{i} \rightarrow \frac{a_{i}}{\sqrt{c_{i}}}$$ and $$c_{i} \rightarrow \sqrt{c_{i}}$$ for $$1 \leq i \leq n$$, then the inequality could have been read as:

$$
(a_{1}^2 + a_{2}^2 + \cdots + a_{n}^2)(c_{1}^2 + c_{2}^2 \cdots + c_{n}^2) \geq (a_{1}c_{1} + a_{2}c_{2} + \cdots + a_{n}c_{n})
$$

We notice that the last sentence is in fact the Cauchy-Schwarz Inequality, then we can conclude that:

$$
\frac{a_{1}^2}{a_{1} + b_{1}} + \frac{a_{2}^2}{a_{2} + b_{2}} + \cdots + \frac{a_{n}^2}{a_{n} + b_{n}}  \geq \frac{a_{1} + a_{2} + \cdots + a_{n}}{2} \ \ \ \mathbb{Q.E.D}
$$

But there is something else, we notice that

$$
\huge\boxed{\frac{a_{1}^2}{c_{1}} + \frac{a_{2}^2}{c_{2}} + \cdots + \frac{a_{n}^2}{c_{n}}  \geq \frac{(a_{1} + a_{2} + \cdots + a_{n})^2}{(c_{1} + c_{2} + \cdots + c_{n})} }
$$

is a consequence of Cauchy-Schwarz Inequality, this lemma is known as <b>Titu's Lemma</b>. Which is a special form helps tackle a lot of optimization problems involving squares in the numerator, immediately.

<b>$$3.-$$ (China Mathematical Olympiad 2004) For a given integer $$n \geq 2$$, suppose positive integers $$a_{i}(i=1, 2, \cdots, n)$$ satisfy $$a_{1} \leq \cdots \leq a_{n}$$ and $$\sum_{i=1}^{n}\frac{1}{a_{i}} \leq 1$$. Prove that, for any real number $$x$$, the following inequality holds,</b>

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right) \leq \frac{1}{2}\frac{1}{a_{1}(a_{1}-1) + x^2}
$$

$$
Solution
$$

For $$x^2 \geq a_{1}(a_{1}-1)$$, from $$\sum_{i=1}^{n} \frac{1}{a_{i}} \leq 1$$ we have

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right) \leq \left( \sum_{i=1}^{n} \frac{1}{2a_{i}|x|} \right)^2 = \frac{1}{4x^2}\left( \sum_{i=1}^{n} \frac{1}{a_{i}} \right)^2
$$

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right) \leq \frac{1}{4x^2} \leq \frac{1}{2}\frac{1}{a_{1}(a_{1}-1) + x^2}
$$

For $$x^2 < a_{1}(a_{1}-1)$$, using Cauchy-Schwarz Inequality, we have

$$
\left( \sum_{i=1}^{n} \frac{1}{a_{i}^2 + x^2} \right)^2 \leq \left( \sum_{i=1}^{n} \frac{1}{a_{i}} \right) \left( \sum_{i=1}^{n} \frac{a_{i}}{(a_{i}^2 + x^2)^2} \right)\leq  \sum_{i=1}^{n} \frac{a_{i}}{(a_{i}^2 + x^2)^2}
$$

Futher, for positive integers $$a_{1} < \cdots < a_{n}$$, we have $$a_{i+1} \geq a_{i}+1$$ and

$$
\frac{2a_{i}}{(a_{i}^2 + x^2)^2} \leq \frac{2a_{i}}{\left(a_{i}^2 + x^2 + \frac{1}{4}\right)^2 - a_{i}^2} = \frac{2a_{i}}{\left( \left( a_{i} - \frac{1}{2}\right)^2 + x^2 \right) \left( \left( a_{i} + \frac{1}{2}\right)^2 + x^2 \right)}
$$

$$
= \frac{1}{\left( a_{i} - \frac{1}{2}\right)^2 + x^2} - \frac{1}{\left( a_{i} + \frac{1}{2}\right)^2 + x^2} \leq \frac{1}{\left( a_{i} - \frac{1}{2}\right)^2 + x^2} - \frac{1}{\left( a_{i+1} - \frac{1}{2}\right)^2 + x^2}
$$

For $$i=1, \cdots, n-1$$. So

$$
\sum_{i=1}^{n} \frac{a_{i}}{(a_{i}^2 + x^2)^2} \leq \frac{1}{2} \sum_{i=1}^{n}\left[ \frac{1}{\left( a_{i} - \frac{1}{2}\right)^2 + x^2} - \frac{1}{\left( a_{i+1} - \frac{1}{2}\right)^2 + x^2} \right] \leq \frac{1}{2}\frac{1}{\left( a_{1} - \frac{1}{2} \right)^2 + x^2} \leq \frac{1}{2}\frac{1}{a_{1}(a_{1}-1)+x^2} \mathbb{Q.E.D}
$$
