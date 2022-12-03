---
layout: post
title:  "Farey Sequences"
date:   2015-02-28 05:00:00
categories: pt post
---

February's last day and I wanna to write a little bit before to end this short month, so this time let's take a look at <b>Farey Sequence</b>
It's useful to find rational approximations of irrational numbers, for computer science applications is used as digital image processing and for
math contests, there some nice problems about it. So, here we go...


<b>Definition</b>
---

For any positive integer $$n$$, the Farey sequence $$F_{n}$$ is the sequence of rational numbers $$a/b$$ with $$0 \leq a \leq b \leq n$$
and $$(a, b) = 1$$ arranged in increasing order. For instance, $$F_{3} = \{ \frac{0}{1}, \frac{1}{3}, \frac{1}{2}, \frac{2}{3}, \frac{1}{1}  \}$$

By generalizing:

$$
|F_{n}| = |F_{n-1}| + \varphi(n)
$$

Where $$\varphi(n)$$ is the Euler's totient function, defined as the number of integers $$k$$ in range $$1 \leq k \leq n$$ for which the greatest
common divisor $$\gcd(n, k) = 1$$

<b>Theorem</b>
---

If $$p_{1}/q_{1}$$, $$p_{2}/q_{2}$$ and $$p_{3}/q_{3}$$ are three successive terms in a Farey sequence, then

$$ 
p_{2}q_{1} - p_{1}q_{2} = 1 

\ \ \ \ \ \ and  \ \ \ \ \ \ \

\frac{ p_{1} + p_{3} }{ q_{1} + q_{2} } = \frac{ p_{2} }{ q_{2} }
$$

<b>Example</b>
---

$$1.-$$ <b>(IMO 1967)</b> Which fraction $$p/q$$, where $$p, q$$ are positive integers less than $$100$$, is closest to $$\sqrt{2}$$? Find all
digits after the decimal point in the decimal representation of this fraction that coincide with digits in the decimal representation of $$\sqrt{2}$$.

$$
Solution
$$

We have that

$$
\left| \frac{p}{q} - \sqrt{2} \right| = \frac{|p - q\sqrt{2}|}{q} = \frac{|p^{2} - 2q^{2}|}{q(p + q\sqrt{2})} \geq \frac{1}{q(p + q\sqrt{2})} \tag{1}
$$

Because $$ \vert p^2 - 2q^2 \vert  \geq 1$$.

The greatest $$p, q \leq 100$$ satisfying the equation $$\vert p^2 - 2q^2 \vert = 1$$ are $$(p, q) = (99, 70)$$. It's easy to verify using $$(1)$$ that
$$\frac{99}{70}$$ best approximates $$\sqrt{2}$$ among the fractions $$p/q$$ with $$p, q \leq 100$$. The numbers $$\frac{99}{70} = 1.41428$$ and $$\sqrt{2}$$
coincide up to the fourth decimal digit: Indeed, $$(1)$$ gives $$7.10^{-5} < \frac{p}{q} - \sqrt{2} < 8.10^{-5}$$

What about Farey sequences?

By using some basic facts about Farey sequences, one can find that $$\frac{41}{29} < \sqrt{2} < \frac{99}{70}$$ implies  $$p \geq 41 + 99 > 100$$
because $$99.29 - 41.70 = 1$$. Of the two fractions $$\frac{41}{29}$$ and $$\frac{99}{70}$$, the later is closer to $$\sqrt{2}$$

Well, No there so much to talk about farey sequence (As part of math contests at least), but if you find problems about it please send me a message and maybe
we can try to solve it together. By the way, I found an interesting question in MathExchange, Check out: [What is the sum of the squares of the differences of consecutive element of a Farey Sequence?][ME]

[ME]: http://math.stackexchange.com/questions/41742/what-is-the-sum-of-the-squares-of-the-differences-of-consecutive-element-of-a-fa
