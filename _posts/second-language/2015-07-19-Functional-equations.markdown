---
layout: post
title:  "Functional equations"
date:   2015-07-19 17:00:00
categories: fr post
---

The last month I asked to [Nataliia][Nataliia] who participated in [IMO-2015][IMO2015]: Which is your favorite topic in math contest?. Then she told me: "Functional equations", so I decided to make a post about it with her support (<b>Thank you Nataliia!</b>).

<b>Definition</b>
---

Functional equations are kind equations where the unknowns are the functions, mostly it gives us information about the functions whom are important
to solve the problem given, let's see this better with an example:

<b>Determine all the functions $$f: \mathbb{R} \rightarrow \mathbb{R}$$ such that:</b>

$$
f(x^3) - f(y^3) = (x^2 + xy + y^2)(f(x) - f(y)), \forall (x, y) \in \mathbb{R}
$$

The problem give us:

Domain and CoDomain: $$f: \mathbb{R} \rightarrow \mathbb{R}$$

The main functional equation: $$f(x^3) - f(y^3) = (x^2 + xy + y^2)(f(x) - f(y))$$

Sometimes, it can provide us values of $$f$$ at some number.

Now, WLOG assume $$f(0) = 0$$, otherwise let $$f(x) = f(x) - f(0)$$, putting $$y=0$$ we get $$f(x^3) = (x^2)f(x)$$ Substituting in the main
equation we get $$f(x) = xf(1)$$, so the answer is $$f(x) = xf(1) + f(0)$$

<b>Methods for solving Functional equations:</b>
---

As you can see we can use a lot methods for solving functional equations, let's listing some of them.

<b>Mathematical induction:</b> We use the value $$f(1)$$ to find all $$f(n)$$ (for $$n$$ integer). After we find $$f(\frac{1}{n})$$ and $$f(r)$$ for rational $$r$$. This method is used mostly when the function is defined on $$\mathbb{Q}$$.

<b>Looking for injectivity or surjectivity of functions involved in the equation:</b> If the function is injective, we can get an equality $$f(g(x,y)) = f(h(x,y))$$
and conclude that: $$g(x,y) = h(x,y)$$. If the function is surjective, there will be a constant such that $$f(k)=0$$.

<b>Looking for the monotonicity and continuity of function:</b> Sometimes the continuity is given as additional condition and the monotonicity is usually for reducing the problem. Actually if the function is periodic, that could help us a lot.

<b>Making recurrent relations:</b> If the range of the function is bounded, maybe we can be able to find a relationship between $$f(f(n)), f(n) \mbox{ and } n$$.

<b>Expressing function as sums of odd and even:</b> This could be help in treat some linear functional equations.

<b>Treating numbers in a system with basis different than 10:</b> Only we can use this if the domain is $$\mathbb{N}$$.

<b>Cauchy equation</b>
---

Now, let's focus in the equation $$f(x+y) = f(x) + f(y)$$, which is called The Cauchy equation, there are a lot problems which can solved by
this method. If a function $$f$$ satisfies any of the conditions:


- Monotonicity on some interval of the real line. <br>
- Continuity at least 1 point. <br>
- Boundedness on some interval. <br>
- Positivity on the ray $$x \geq 0$$.

Then the general solution to the Cauchy equation $$f:\mathbb{R} \rightarrow S$$ has to be $$f(x) = xf(1)$$. The following equations can be
reduced to the Cauchy equation.

- All continuous functions $$f:\mathbb{R} \rightarrow (0, +\infty)$$ satisfying $$f(x+y) = f(x)f(y)$$ are of the form $$f(x)=a^x$$. Namely
the function $$g(x)=\log{f(x)}$$ is continuous and satisfies the Cauchy equation.

- All continuous functions $$f:(0, +\infty) \rightarrow \mathbb{R}$$ satisfying $$f(xy) = f(x) + f(y)$$ are of the form $$f(x) = \log_{a}{x}$$. 
Now the function $$g(x) = f(a^{x})$$ is continuous and satisfies the Cauchy equation.

- All continuous functions $$f:(0, +\infty) \rightarrow (0, +\infty)$$ satisfying $$f(xy) = f(x)f(y)$$ are $$f(x) = x^t$$, where $$t=\log_{a}{b}$$
and $$f(a)=b$$. Indeed the function $$g(x)=log{f(a^x)}$$ is continuous and satisfies the Cauchy equation.

Let's see some examples:

<b>- Find all the functions $$f,g,h: \mathbb{R} \rightarrow \mathbb{R}$$ that satisfy</b> 

$$
f(x+y) + g(x-y) = 2h(x) + 2h(y)
$$
 
First, let's putting $$x=y \mbox{ and } g(0)=a$$, then we get: $$f(2x) = 4h(x) - a$$.

Putting $$y=0$$, we get: $$g(x) = 2h(x) + 2b - 4h(\frac{x}{2}) + a$$, where $$h(0)=b$$, the original equation can be written as:

$$
2 \Bigg[ h\left( \frac{x+y}{2} \right) + h\left( \frac{x-y}{2} \right) \Bigg] + h(x-y) + b = h(x) + h(y)
$$

In this way, we express $$f \mbox{ and } g$$ in terms of $$h$$.

Now, Do you remember the method <b>expressing function as sums of odd an even</b>? Well, we can use here: $$H(x) = H_{e}(x) + H_{o}(x)$$, furthermore
we write the same expressions for $$(-x,y) \mbox{ and } (x,-y)$$, then

$$
2 \Bigg[ H_e\left( \frac{x-y}{2} \right) + H_e\left( \frac{x+y}{2} \right) \Bigg] + H_e(x-y) = H_e(x) + H_e(y)
$$

If we set $$H_e(y) = H_e(-y)$$ and we add it to the last equation:

$$
H_e(x+y) - H_e(x-y) = 2H_e(x) + 2H_e(y)
$$

Using Mathematical induction yields $$H_e(x) = \alpha x^2$$. Similar method gives the relation for $$H_o$$:

$$
H_o(x+y) + H_o(x-y) = 2H_o(x)
$$

This is a Cauchy equation hence $$H_o(x) = \beta x$$. Thus $$h(x) = \alpha x^2 + \beta x + b$$ and substituting for $$f \mbox{ and } g$$
we get:

$$
f(x) = \alpha x^2 + 2\beta x + 4b - a, \ \ \ \ \ g(x) = \alpha x^2 + a
$$

<b>- (IMO 2015) Let $$\mathbb{R}$$ be the set of real numbers. Determine all functions $$f:\mathbb{R} \rightarrow \mathbb{R}$$ that satisfy the
equation, for all real numbers $$x \mbox{ and } y$$</b>.

$$
f(x + f(x + y)) + f(xy) = x + f(x + y) + yf(x)
$$

<b>- Find all functions $$f:\mathbb{R}^+ \rightarrow \mathbb{R}^+$$ such that:</b>

$$
(f(x))^2 + 2yf(x) + f(y) = f(y + f(x)), \ \ \ \ \ \forall (y,x) \in \mathbb{R}^+
$$

The equation can be written as:

$$  
f(y + f(x)) - (y + f(x))^2 = f(y) - y^2
$$

We say that $$g(x) := f(x) - x^2$$ is periodic, and every $$f(x)$$ is its period. We equal $$f(x)=0$$, which satisfies the initial equation,
otherwise, $$f(x)$$ takes the value of the form $$k\alpha$$, where $$k$$ is a positive integer and $$\alpha$$ the minimal non-zero period of $$g$$.

Hence the natural $$k, l$$ such that $$k > l$$ we have

$$
f(x + k\alpha) - (x + k\alpha)^2 = f(x + l\alpha) - (x + l\alpha)^2
$$

$$
f(x + k\alpha) - (x + l\alpha)^2 = \alpha(k - l)(2x + (k + l)\alpha)
$$

The LHS is equal to $$m\alpha$$ for some natural $$m$$, which yields

$$
\alpha = \frac{1}{k + l} \left( \frac{m}{k - l} - 2x \right)
$$

The period of the function depends of $$x$$, hence any real number can be the period, then the function is constant. So, the solutions are $$f(x) = 0 \mbox{ and } f(x) = x^2 + C, C \in \mathbb{R}$$

Well, there a lot of fun in solving functional equations. I found the following question on MathExchange, so it's a good idea if you check out:
[Continuous function $$f:\mathbb{R} \rightarrow \mathbb{R}$$ such that $$f(f(x)) = -x$$?][MES2]

If you are interested in practice some problems, you can find a list [here][FE].

[IMO2015]: https://www.imo-official.org/year_info.aspx?year=2015
[Nataliia]: http://imo-official.org/participant_r.aspx?id=25118
[FE]: http://imomath.com/index.php?options=342&lmm=0
[MES2]: http://math.stackexchange.com/questions/312385/continuous-function-f-mathbbr-to-mathbbr-such-that-ffx-x
