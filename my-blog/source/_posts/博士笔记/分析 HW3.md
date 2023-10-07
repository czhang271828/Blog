---
title: 分析 HW3
date: 2023-10-03 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW3 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#3
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

One important theorem we shall use frequently throughout the course is the Fubini (Tonelli) theorem, which allows us to interchange the order of iterated integrals under the assumption that the integrand is either nonnegative or integrable. However, unfortunately, we won't go over the proof in lectures due to the limited time. Please refer to the texts (e.g., [Folland, $\S$ 2.5]) to understand the statement and proof of the following. 

**Theorem 1** (Fubini-Tonelli) Let $(X,\mathscr F,\mu)$ and $(Y,\mathscr G,\nu)$ be $\sigma$-finite measure spaces. 

* If $f:(X\times Y,\mathscr F\otimes \mathscr G,\mu\otimes \nu)\to \mathbb R$ is a non-negative measurable function, then $g(x):=\int_Yf(x,y)\mathrm d\nu(y)$ and $h(y):=\int_X f(x,y)\mathrm d\mu(x)$ are both measurable, and 
  $$
  \iint_{X\times Y}f\mathrm d (\mu\otimes \nu)=\int_Xg(x)\mathrm d\mu(x)=\int_Y h(y)\mathrm d\nu(y)\qquad (1).
  $$

* If $f\in \mathscr L^1(X\times Y,\mathscr F\otimes \mathscr G,\mu\otimes \nu)$, then for $\mu$-a.e. $x\in X$ the function $y\mapsto f(x,y)$ is in $\mathscr L^1(Y,\mathscr G,\nu)$, and for $\nu$-a.e. $y\in Y$ the function $x\mapsto f(x,y)$ is in $\mathscr L^1(X,\mathscr F,\mu)$. Moreover, the a.e.-defined functions $g$ and $h$ as above are in $\mathscr L^1(X,\mathscr F,\mu)$ and $\mathscr L^1(Y,\mathscr G,\nu)$, respectively, and **Equation (1)** holds. 

Then, work out the following problem ([Folland, p.77, Q55]): Let $Q=[0,1]^2$​. Investigate the existence and equality of
$$
\int_Qf\mathrm d\mathscr L\otimes \mathscr L,\quad \int_0^1\int_0^1 f(x,y)\mathrm dx\mathrm dy,\quad \text{and }\int_0^1\int_0^1 f(x,y)\mathrm dy\mathrm dx
$$
for following $f$: 

* $f(x,y)=\dfrac{x^2-y^2}{(x^2+y^2)^2}$;
* $f(x,y)=(1-xy)^{-\alpha}$ for some $\alpha>0$;
* $f(x,y)=(x-1/2)^{-3}\cdot 1_{\{0<y<|x-1/2|\}}$. 

> **Proof** 
>
> 1. Set $F=\{x\in Q:\|x\|_2\leq 1\}$. It is clear that $f\in \mathscr L(Q\setminus F)$. To see that $f\notin \mathscr L (Q)$, we notice that
>    $$
>    \int_0^{\pi/4}\int_0^1\left|\dfrac{\sin 2\theta}{r^2}\right|\mathrm dr\mathrm d\theta=\infty.
>    $$
>    Since 
>    $$
>    \dfrac{\partial^2}{\partial y\partial x}\arctan \dfrac{x}{y}=\dfrac{\partial ^2}{\partial x\partial y}(-\arctan \dfrac{y}{x}),
>    $$
>    we have that
>    $$
>    \begin{align*}
>    \int_0^1\int_0^1 f(x,y)\mathrm dx\mathrm dy&=\int_0^1-\dfrac{1}{1+y^2}\mathrm dy=-\dfrac\pi 4,\\[6pt]
>    \int_0^1\int_0^1 f(x,y)\mathrm dy\mathrm dx&=\int_0^1\dfrac{1}{x^2+1}\mathrm dx=\dfrac\pi 4.
>    \end{align*}
>    $$
>
> 2. Similarly, we take 
>    $$
>    f(x,y)=(x+y-xy)^{-\alpha}=(r\cos \theta+r\sin\theta+r^2\sin\theta\cos\theta).
>    $$
>    Then $f\in \mathscr L(Q)$ whenever $\alpha<2$. Since $f(x,y)\geq 0$, three integrals exists and are equal whenever $\alpha<2$; otherwise, neither exists. 
>
> 3. Since $f\geq 0$, the three integrals are equal. For instance, one can evaluate
>    $$
>    \begin{align*}
>    \int_0^1\int_0^1 f(x,y)\mathrm dx\mathrm dy&=\int_0^{1/2}(y^{-2}-4)\mathrm dy=\infty,\\[6pt]
>    \int_0^1\int_0^1 f(x,y)\mathrm dy\mathrm dx&=\int_{1/2}^1(x-1/2)^{-2}\mathrm dx=\infty.
>    \end{align*}
>    $$
