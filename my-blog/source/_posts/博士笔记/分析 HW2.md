---
title: 分析 HW2
date: 2023-09-26 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW2 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#2
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

**Ex 1** **(Differentiability under the integral sign)**. Let $f:(X,\mathscr F,\mu)\times [a,b]\to \mathbb C$ be a function such that $f(\bullet ,t)$ is integrable for each $t\in [a,b]$. Write $F(t)=\int_Xf(x,t)\mathrm d\mu(x)$. Suppose that $\frac{\partial f}{\partial t}$ exists and there exists some $g\in \mathscr L^1(X,\mathscr F,\mu)$​ such that
$$
\left|\dfrac{\partial f}{\partial t}(x,t)\right|\leq g(x)\quad \text{for every }(x,t)\in X\times [a,b]. 
$$
Then $F$ is differentiable with $F^\prime(t)=\int_X(\partial f/\partial t)(x,t)\mathrm d\mu(x)$. 

Using the above, or otherwise, show that
$$
\int_0^\infty x^ne^{-x}\mathrm dx=n!\quad \text{and}\quad \int_{\mathbb R}x^{2n}e^{-x^2}\mathrm dx=\dfrac{(2n)!\sqrt \pi}{4^nn!}.
$$
**Hint** consider $\int_0^\infty e^{-tx}\mathrm dx$ and $\int_{\mathbb R}e^{-tx^2}\mathrm dx$. 

> **Proof** 
>
> * (Former one) Take $f(x,t)=e^{-tx}$, $F(t)=\int_{\mathbb R} f\mathrm dx$. We have 
>   $$
>   -\int_{\mathbb R}xe^{-xt}\mathrm dx=F^\prime (t)=\dfrac{\mathrm d}{\mathrm dt}\dfrac 1t.
>   $$
>   Then we take $f_k(x,t)=x^{k}e^{-tx}$ and $F_k(t)=\int_{\mathbb R}f_k(x,t)\mathrm dx$​ to obtain that
>   $$
>   (-1)^k\int_{\mathbb R}x^{k}e^{-x t}\mathrm dx=\dfrac{\mathrm d^k}{\mathrm dt^k}\dfrac 1t=(-1)^k\cdot k!\cdot \dfrac 1{t^k}.
>   $$
>   Let $t=1$ on both sides, then $\int_0^\infty x^ne^{-x}\mathrm dx=n!$. 
>
> * (Latter one) Take $f(x,t)=e^{-tx^2}$, $F(t)=\int_{\mathbb R} f\mathrm dx$. We have 
>   $$
>   -\int_{\mathbb R}x^2e^{-x^2t}\mathrm dx=F^\prime (t)=\dfrac{\mathrm d}{\mathrm dt}\sqrt{\dfrac{\pi}{t}}.
>   $$
>   Then we take $f_k(x,t)=x^{2k}e^{-tx^2}$ and $F_k(t)=\int_{\mathbb R}f_k(x,t)\mathrm dx$​ to obtain that
>   $$
>   (-1)^k\int_{\mathbb R}x^{2k}e^{-x^2 t}\mathrm dx=\dfrac{\mathrm d^k}{\mathrm dt^k}\sqrt {\dfrac{\pi}{t}}=(-1)^k\dfrac{(2k)!}{4^kk!}\sqrt{\dfrac{\pi}{t^{2k+1}}}.
>   $$
>   Let $t=1$ on both sides, then $\int_{\mathbb R}x^{2n}e^{-x^2}\mathrm dx=\dfrac{(2n)!\sqrt \pi}{4^nn!}$. 

**Ex 2** Let $f_n$, $g_n$, $f$, $g$ be integrable functions such that $f_n\to f$, $g_n\to g$ a.e.. $|f_n|\leq g_n$, and $\int g_n\to \int g$. Deduce that $\int f_n\to \int f$. 

> **Proof** On one hand, 
> $$
> \int f+g=\int \liminf (f_n+g_n)\leq \liminf\int f_n+\int g.
> $$
> On the other hand, 
> $$
> \int -f+g=\int\liminf (-f_n+g_n)\leq \liminf\int -f_n+g_n= \int g-\limsup\int f_n.
> $$
> It yields that $\liminf\int f_n\geq \int f\geq \limsup\int f_n$. Consequently, $\int f_n\to \int f$. 

**Ex 3** Let $f_n(x)=ae^{-nax}-be^{-nbx}$ where $0<a<b$. Find $\sum_{n=1}^\infty \int_0^\infty|f_n(x)|\mathrm dx$, $\sum_{n=1}^\infty \int_0^\infty f_n(x)\mathrm dx$, and $\int_0^\infty\sum_{n=1}^\infty f_n(x)\mathrm dx$. 

> **Proof** 
>
> 1. Let $C=\dfrac{\ln b-\ln a}{b-a}$, then $f_n(C/n)=0$ and $f_n(x)>0$ for $x>C$. Thus 
>    $$
>    \sum_{n=1}^\infty \int_0^\infty|f_n(x)|\mathrm dx\geq \sum_{n=1}^\infty \int_{C/n}^\infty f_n(x)\mathrm dx=\sum_{n=1}^\infty \dfrac{e^{-Ca}-e^{-Cb}}{n}=\infty.
>    $$
>
> 2. It is clear that
>    $$
>    \sum_{n=1}^\infty \int_0^\infty f_n(x)\mathrm dx=\sum_{n=1}^\infty \dfrac{e^{-nax}-e^{-nbx}}{n}|_{x=0}^\infty=\sum_{n=1}^\infty0=0.
>    $$
>
> 3. The sum of power series is evaluated as
>
> $$
> \sum_{n=1}^\infty ae^{-anx}=\dfrac{ae^{-ax}}{1-e^{-ax}}=[\ln (1-e^{-ax})]^\prime.
> $$
>
> Thus 
> $$
> \int_0^\infty\sum_{n=1}^\infty f_n(x)\mathrm dx=\int_0^\infty\left(\ln\dfrac{1-e^{-ax}}{1-e^{-bx}}\right)^\prime\mathrm dx=0-\ln\dfrac{ax-\frac 1{2!}a^2x^2-\cdots}{bx-\frac 1{2!}b^2x^2-\cdots}=\ln \dfrac ba.
> $$

**Ex 4** Find $\lim_{k\to\infty}\int_0^kx^n(1-\frac xk)^k\mathrm dx$. 

> **Proof** We claim that $(1-x/k)^k\leq e^{-x}$ for $|x/k|<1$. Taking logarithm on both sides, we have $k\ln (1-x/k)\leq -x$. Since $\ln (1-t)\leq -t$ for $t=x/k\in (-1,1)$, the claim is proved. 
>
> Set $g_n=x^n(1-x/k)^k\cdot 1_{]0,k[}$ on $\mathbb R$ and $g= x^ne^{-x}\cdot 1_{]0,\infty[}$. We know that $|g_n|\leq g$ and $g\in \mathscr L^1(\mathbb R)$. It is known that for fixed $x$ and arbitrary large $k$, 
> $$
> \lim_{k\to+\infty}(1-x/k)^k=\left(\lim_{k\to+\infty}(1-x/k)^{-k/x}\right)^{-x}=e^{-x}.
> $$
> Therefore, $g_n\to g$ a.e.. By [DCT] we have that
> $$
> \lim_{k\to\infty}\int_0^kx^n(1-\frac xk)^k\mathrm dx=\int_0^\infty x^ne^{-x}\mathrm dx=n!\quad (\text{see }\textbf{Ex 1}).
> $$

**Ex 5** Prove that $\lim_{n\to\infty}\int_0^{n^2}n\left(\sin\frac xn\right)e^{-x^2}\mathrm dx=\frac 12$. 

> **Proof** Set $g_n(x)= n(\sin \frac xn)e^{-x^2} 1_{[0,n^2]}$ and $g(x)=xe^{-x^2}$. We have that $g_n\to g$ a.e. and $|g_n|\leq g$. By [DCT]
> $$
> \lim_{n\to\infty}\int_0^{n^2}n\left(\sin\frac xn\right)e^{-x^2}\mathrm dx=\int_0^\infty xe^{-x^2}\mathrm dx=\frac 12
> $$

**Ex 6** Show that for $n\geq 2$ and $0\leq y\leq n$, it holds that 
$$
\left(1-\dfrac yn\right)^{-n}\geq \left(1-\dfrac y{n+1}\right)^{-(n+1)}.
$$
Hence, or otherwise, show that for $\alpha>0$ and $\beta >-1$, 
$$
\lim_{n\to\infty}n^\alpha\int_0^1x^{\alpha-1}e^{-n\beta x} (1-x)^n\mathrm dx=(\beta+1)^{-\alpha}\Gamma(\alpha),
$$
where $\Gamma$ is the Gamma function. 

> **Proof** In order to prove the first inequality, we take logarithm on both sides to obtain
> $$
> -n\ln (1-y/n)\leq -(n+1)\ln (1-y/(n+1)).
> $$
> Equivalently, we have that 
> $$
> (-y/n)\ln (1-y/n)\leq (-y/(n+1))\ln (1-y/(n+1)).
> $$
> Set $f(x):=x\ln (1+x)$. Then $f^{\prime\prime}(x)=\dfrac{x+2}{(1+x)^2}$. Hence, $f^\prime$ is strictly increasing for $x>-1$. Since $f^\prime (0)=0$, the inequality is proved. 
>
> Substitute $x\mapsto y/n$​, we have that
> $$
> n^\alpha\int_0^1x^{\alpha-1}e^{-n\beta x} (1-x)^n\mathrm dx=
> \int_0^ny^{\alpha-1}e^{-\beta y} (1-y/n)^n\mathrm dy.
> $$
> Now set $g_n(y)=y^{\alpha-1}e^{-\beta y} (1-y/n)^n 1_{[0,n]}$, we have that
> $$
> g_n(y)\leq y^{\alpha-1}e^{-\beta y}e^{-y}=:g(y).
> $$
> By [DCT], the limit is
> $$
> \int_0^\infty g(y)\mathrm dy=\int_0^\infty y^{\alpha-1}e^{-y(\beta+1)}\mathrm dy=\int_0^\infty \left(\dfrac{z}{\beta+1}\right)^{\alpha-1}e^{-y}\,\mathrm d\,\dfrac{z}{\beta+1}=(\beta+1)^{-\alpha}\Gamma(\alpha).
> $$

**Ex 7** Let $\alpha >-1$. Show that $f(x):=x^\alpha\log x$ is integrable on $]0,1[$, and that
$$
\int_0^1f(x)\mathrm dx=-(1+\alpha)^{-2}.
$$
Then, deduce for $\beta >-1$ that $g(x)=x^\beta (1-x)^{-1}\log x$ is integrable over $]0,1[$, and that 
$$
\int_0^1g(x)\mathrm dx=-\sum_{n=1}^\infty (n+\beta)^{-2}.
$$

> **Proof** Set $\varepsilon:=\dfrac{\alpha-(-1)}2$. We know that $\lim_{x\to 0^+}x\log x=0$. Therefore, 
> $$
> \lim_{x\to 0^+}x^\varepsilon\log x=\varepsilon^{-1}\lim_{x\to 0^+}x^\varepsilon\log x^\varepsilon=0.
> $$
> Consequently, $x^\varepsilon \log x$ is bounded on $]0,1[$, thus $x^\alpha\log x=x^{1-\varepsilon} x^\varepsilon\log x\in \mathscr L^1(]0,1[)$. 
>
> Set $u_n(x):=x^{\beta+n}\log x$ for $n\in \mathbb N$. Since $\lim_{x\to 1^-}g(x)=-1$, $g(x)$ is integrable on $]0,1]$ and thus $g\in \mathscr L^1([0,1])$. We notice that $g_N:=\sum_{0\leq n\leq N}u_n\to g$ a.e., and $g\in \mathscr L^1([0,1])$. By [DCT] we have that
> $$
> \int_0^1g(x)\mathrm dx=-\sum_{n=1}^\infty (n+\beta)^{-2}.
> $$
