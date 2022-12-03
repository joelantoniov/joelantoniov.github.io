---
layout: post
title:  "Chinese Dumbass Notation"
date:   2014-12-31 11:00:00
categories: pt post
---

Well, today is the last day of 2014 and we're just going take a look at non-standard notation called <b>Chinese Dumbass Notation</b>.
Actually this post is only a little description about it, since I have never used this one to prove a problem in math contest.

<b>Definition</b>
---

Chinese Dumbass Notation (CDN), is a way to write down three variable homogeneous expressions. It allows to keep like terms combined while not requiring
any sort of symmetry from the expression.

CDN uses a triangle to hold the coefficients of a three variable symmetric inequality in a way that is easy to visualize. By example: 

$$\sum_{sym} 8a^3b + \sum_{sym} 10a^2b^2 + \sum_{sym} 14a^2bc \\$$


$$

\newcommand\pad[1]{\rlap{#1}\phantom{274}}
\begin{matrix}
&&&&&0\\
&&&&8&&8\\
&&&20&&28&&20\\
&&8&&28&&28&&8\\
&0&&8&&20&&8&&0\\
\end{matrix}


=

\begin{matrix}
&&&&&[a^4]\\ 
&&&&[a^3b]&&[a^3c]\\
&&&[a^2b^2]&&[a^2bc]&&[a^2c^2]\\
&&[ab^3]&&[ab^2c]&&[abc^2]&&[ac^3]\\
&[b^4]&&[b^3c]&&[b^2c^2]&&[bc^3]&&[c^4]\\

\end{matrix}
$$

Here $$[x]$$ represents the coefficient of $$x$$. In general, a degree $$d$$ expression is represented by a triangle with side length $$d+1$$ and the
coefficient of $$a^{\alpha}b^{\beta}c^{\gamma}$$ is placed at Barycentric coordinates $$(\alpha, \beta, \gamma)$$.

<b>AM-GM and Schur Inequalities</b>
---

- The AM-GM inequality for two variables states that $$a^2 + b^2 \geq 2ab$$. In other words: 
$$
\begin{matrix}  
&&&1\\
&&-2&&0\\
&1&&0&&0
\end{matrix} \geq 0
$$


- The Schur's Inequality states that $$\sum_{sym} a^r(a-b)(a-c) \geq 0 $$ for all non-negative numbers $$a, b, c, r$$. The prototypical application of Schur's Inequality looks as follows:

$$
\begin{matrix}
&&&&&1\\ 
&&&&-1&&-1\\
&&&0&&1&&0\\
&&-1&&1&&1&&-1\\
&1&&-1&&0&&-1&&1\\
\end{matrix} 

\geq 0 
$$

As with AM-GM, the variables can be tweaked so that Schur's Inequality gives us $$\sum_{cyc}a^r(a^s-b^s)(a^s-c^2) \geq 0 $$

<b>Example</b>
---

Prove that $$\frac{bc}{2a+b+c} + \frac{ac}{a+2b+c} + \frac{ab}{a+b+2c} \leq \frac{1}{4}(a+b+c)$$

Proof. We clear denominators to obtain that this is equivalent to

$$
4\sum_{cyc} bc(a+2b+c)(a+b+2c) \leq (a+2b+c)(a+b+2c)(2a+b+c)(a+b+c)

\equiv

\\

4\sum_{cyc} \left(\begin{matrix}&&&0\\&&0&&0\\&0&&1&&0  \end{matrix}\right) \left(\begin{matrix}&&1\\&1&&2\\ \end{matrix}\right) \left(\begin{matrix}&&1\\&2&&1\\ \end{matrix}\right)  \leq \left(\begin{matrix}&&1\\&1&&2\\ \end{matrix}\right)   \left(\begin{matrix}&&1\\&2&&1\\ \end{matrix}\right)  \left(\begin{matrix}&&2\\&1&&1\\ \end{matrix}\right)  \left(\begin{matrix}&&1\\&1&&1\\ \end{matrix}\right)
$$

We'll expand the left hand side as

$$

4\sum_{cyc} \left(\begin{matrix}&&&0\\&&0&&0\\&0&&1&&0  \end{matrix}\right) \left(\begin{matrix}&&1\\&1&&2\\ \end{matrix}\right) \left(\begin{matrix}&&1\\&2&&1\\ \end{matrix}\right) \\

= 4\sum_{cyc} \left( \begin{matrix} 
&&&&&0\\ 
&&&&0&&0\\
&&&0&&1&&0\\
&&0&&3&&3&&0\\
&0&&2&&5&&2&&0\\
\end{matrix}\right)

\\

=
\begin{matrix}
&&&&&0\\
&&&&8&&8\\
&&&20&&28&&20\\
&&8&&28&&28&&8\\
&0&&8&&20&&8&&0\\
\end{matrix}
$$

We then expand the right hand side as


$$
\left(\begin{matrix}&&1\\&1&&2\\ \end{matrix}\right)   \left(\begin{matrix}&&1\\&2&&1\\ \end{matrix}\right)  \left(\begin{matrix}&&2\\&1&&1\\ \end{matrix}\right)  \left(\begin{matrix}&&1\\&1&&1\\ \end{matrix}\right)

\\

=
\begin{matrix}
&&&&&2\\
&&&&9&&9\\
&&&14&&30&&14\\
&&9&&30&&30&&9\\
&2&&9&&14&&9&&2\\
\end{matrix}
$$

The inequality is thus equivalent to showing that the difference in non-negative. But the difference is 

$$

\begin{matrix}
&&&&&2\\
&&&&1&&1\\
&&&-6&&2&&-6\\
&&1&&20&&20&&1\\
&2&&1&&-6&&1&&2\\
\end{matrix}

\geq

\begin{matrix}
&&&&&0\\
&&&&3&&3\\
&&&-6&&0&&-6\\
&&3&&0&&0&&3\\
&0&&3&&-6&&3&&0\\
\end{matrix}

\geq


0
$$

by Schur and AM-GM inequalities.

Well, all the information above is thanks to [Mr. Brian Hamrick][BH], this post is just to take a look at CDN. So, if you want to expand the knowledge about it, please visit: [The Art of Dumbassing][CDN]. 

I wonder, how many people have used this one in math contest? it's just curiosity. If you did it and want to share with me, please send me a mail.
Maybe we can resolve some problems together. Anyway. <b>The best wishes for everyone in 2015</b>


[CDN]: http://www.tjhsst.edu/~2010bhamrick/files/dumbassing.pdf
[BH]: http://www.tjhsst.edu/~2010bhamrick/
