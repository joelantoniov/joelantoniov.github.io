---
layout: post
title:  "Differentiating under the integral sign"
date:   2015-03-20 05:00:00
first-language: En
second-language: Pt 
subdomain: pt 
activate-lan: yes
categories: post
---

Let's talk about a formula created by Leibniz to resolve integrals well known as "Differentiating under the integral sign", otherwise name:
<b>"Feyman's favorite trick"</b> or <b>"differentiation with respect to a parameter"</b>

<b>Definition</b>
---

We have the integral:

$$
I(\alpha) = \int_{a(\alpha)}^{b(\alpha)} f(x, \alpha) \ \mbox{dx}
$$

Where $$\alpha$$ is the parameter of the integral, then we calculate the derivate of $$I$$ with respect to $$\alpha$$ by definition of the derivative

<b>Proof</b>
---

$$
\frac{\mbox{d}I}{\mbox{d}\alpha} = \lim_{\Delta \alpha \rightarrow 0} \frac{I(\alpha + \Delta \alpha) - I(\alpha)}{\Delta \alpha}
$$

Then:

$$
I(\alpha + \Delta \alpha) - I(\alpha) =  \int_{a + \Delta a}^{b + \Delta b} f(x, \alpha + \Delta \alpha) \ \mbox{dx} - \int_{a}^{b} f(x, \alpha) \ \mbox{dx} \\
= \left( \int_{a + \Delta a}^{a}  + \int_{a}^{b} + \int_{b}^{b + \Delta b} \right) f(x, \alpha + \Delta \alpha) \ \mbox{dx} - \int_{a}^{b} f(x, \alpha) \ \mbox{dx} \\
 = \int_{a}^{b} \{ f(x, \alpha + \Delta \alpha) - f(x, \alpha) \} \ \mbox{dx} + \int_{b}^{b + \Delta b}
f(x, \alpha + \Delta \alpha) \ \mbox{dx} - \int_{a}^{a + \Delta a} f(x, \alpha + \Delta \alpha) \ \mbox{dx}
$$

As $$\Delta \alpha \rightarrow 0 $$, then we have as well $$\Delta a \rightarrow 0$$ and $$\Delta b \rightarrow 0$$, so

$$
\lim_{\Delta \alpha \rightarrow 0} \{ I(\alpha + \Delta \alpha) - I(\alpha)\} \\
= \lim_{\Delta \alpha \rightarrow 0} \int_{a}^{b} \{ f(x, \alpha + \Delta \alpha) - f(x, \alpha) \} \ \mbox{dx} + f(b, \alpha) \Delta b - f(a, \alpha) \Delta a
$$

Thus, 

$$
\frac{ \mbox{d} I}{ \mbox{d} \alpha} \lim_{\Delta \alpha \rightarrow 0} \frac{I(\alpha + \Delta \alpha) - I(\alpha)}{\Delta \alpha}
= \lim_{\Delta \alpha \rightarrow 0 } \frac{1}{\Delta \alpha} \int_{b}^{a} \{ f(x, \alpha + \Delta \alpha) - f(x, \alpha)  \} \ \mbox{dx} + \lim_{\Delta \alpha \rightarrow 0 } f(b, \alpha) \frac{\Delta b}{\Delta \alpha}  - \lim_{\Delta \alpha \rightarrow 0 } f(a, \alpha) \frac{\Delta a}{\Delta \alpha} \\ \\ \\

\\

\huge\boxed{ \frac{dI}{d\alpha} = \int_{a}^{b} \frac{\partial f}{\partial \alpha} \ dx +  f(b, \alpha)\frac{db}{d\alpha} - f(a, \alpha)\frac{da}{d\alpha}}
$$

A sight at the integral
---

For understand the claim above, let's compute the following intgral:

$$
I = \int_{0}^{\infty} \frac{\sin{ax}}{x} \ dx
$$

The first thing to develop is <b>introduce a parameter</b> in the integral such that we allow us generalize the integral and when we get the answer, we'll find
a family solutions. Sometimes is not too easy know what parameter it is, for this example we put: $$\exp(-xy)$$ in our integral:


$$
I(y) = \int_{0}^{\infty} \exp(-xy) \left( \frac{\sin{ax}}{x} \right) \ dx
$$

$$y$$ has the initial value 1, next let's proceed to <b>derivate with respect to the parameter that we introduced</b>

$$
\frac{dI}{dy} = \int_{0}^{\infty} \frac{\partial}{\partial y}  \Big\{  \exp(-xy) \frac{\sin{ax}}{x} \Big\} \ dx = - \int_{0}^{\infty} \exp(-xy) \sin{ax} \ dx
$$

After, we intregrated-by-parts twice, and we get this:

$$
\frac{dI}{dy} = -\frac{a}{a^2 + y^2}
$$

Now we need to <b>integrate with respect to $$y$$</b>

$$
\frac{dI}{dy} = -\frac{a}{a^2 + y^2} = - \arctan{\frac{y}{a}} + C
$$

We can calculate $$C$$ assuming $$I(\infty) = 0$$ because $$e^{-xy}$$ factor goes to zero everywhere as $$y \rightarrow \infty$$, thus:

$$
0 = C - \arctan(\pm \infty) \\ 
C = \pm \frac{\pi}{2} \\
I(y) = \pm \frac{\pi}{2} - \arctan{\frac{y}{a}}
$$

and we are done!

<b>Leibniz's Flip-side formula</b>
---

Now, let's see the Flip-side of the formula, we have the following integral:

$$
I(a, b) = \int_{0}^{\pi} \frac{\cos{ax} -  \cos{bx}}{x\sin{x}} \ dx
$$

For the flip-side, we don't should derivate, we need to backward to integrate, if we look atention:

$$
\frac{\cos{ax} - \cos{bx}}{x}  = \frac{\cos{yx}}{x} \biggr\rvert_{b}^{a} \ \ \ \ \mbox{because} \ \ \ \ \int_{b}^{a} sin(yx) \ dy 
$$

Now we know this, we proceed:

$$
\int_{0}^{\pi} \int_{b}^{a} \frac{\sin{yx}}{\sin{x}} \ dy \ dx
$$

Now just flip the integral order and we have:

$$
\int_{b}^{a} \int_{0}^{\pi} \frac{\sin{yx}}{\sin{x}} \ dx \ dy \ \ \mbox{, The integral is well known                }    \ \ \ \ \ \int_{0}^{\pi} \frac{\sin{yx}}{\sin{x}}   = \left\{ \begin{array}{rcl} 0 & \mbox{, for y even}\\ \pi & \mbox{, for y odd} \end{array}\right.
$$

If $$y$$ is even, the final answer will be 0, but if not the final answer will be $$\pi[a-b]$$, and we are done.
