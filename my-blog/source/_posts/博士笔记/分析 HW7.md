---
title: 分析 HW7
date: 2023-11-7 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW7 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#7
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

**Ex 1** Let $X$ be a Banach space and $Y$ be normed vector space. Let $T\in \mathcal B(X,Y)$ be such that there exists $\delta >0$ s.t. $\|Tx\|\geq \delta\|x\|$ for all $x\in X$. Prove that $T$ has closed range. 

> **Proof** In fact, we have the following proposition: Let $T\in \mathcal B(X,Y)$ be any linear operator between Banach spaces. Then $T$ is injective with closed range, whenever there exists $c>0$ s.t. $\|Tx\|\geq c\|x\|$. 
>
> $\Leftarrow$ (We shall not use the Banach condition here for $Y$) The injectivity is due to $\|Tx\|=0\Leftrightarrow x=0$. For any $\{y_\lambda\}\to y_0\in \overline Y$, there exists $\{x_\lambda\}\subseteq X$ s.t. $Tx_\lambda=y_\lambda$. Since
> $$
> \|x_\lambda-x_\mu\|\leq c^{-1}\cdot \|y_\lambda-y_\mu\|,
> $$
> $\{x_\lambda\}$ converges in $X$ and thus converges to some $x_0\in X$. We take $Tx_0=y_0\in Y$ and thus $TX$ is closed in $Y$. 
>
> $\Rightarrow$ If $T$ is injective with closed range, then $T:X\to TX$ is a continuous bijective linear operator between Banach spaces, yielding that $T^{-1}$ is continuous. Then there exists $c$ s.t. 
> $$
> \|y\|\leq c^{-1}\cdot \|T^{-1}y\|\quad (\forall y\in TX).
> $$

**Ex 2** Let $K:=\{z\in \mathbb C:1\leq |z|\leq 2\}$ and
$$
\Phi:C^0(K)\to \mathbb C,\quad f\mapsto \int_{|z|=3/2}f(z)\operatorname dz.
$$

1. Show that $\Phi$ is a bounded linear functional.
2. Hence, or otherwise, prove that $\mathbb C[z]$ (the space of complex-coefficient polynomials) is not dense in $C^0(K;\mathbb C)$. That is, the direct analogue of Stone Weierstraß fails in $\mathbb C$. 

> **Proof** It is clear that $\Phi$ is linear functional with norm $3\pi$. Since $\mathbb C[z]$ is contained in the space of holomorphic functions, then
> $$
> \mathbb C[z]\subseteq \ker(\Phi). 
> $$
> For any $f_0\notin \ker(\Phi)$, there exists $\delta>0$ s.t. $\Phi(f)\neq 0$ ($\|f-f_0\|<\delta$). Hence the analogue of Stone Weierstraß fails in $\mathbb C$. 

**Ex 3** Let $X$ be a normed vector space and let $Z$ be a closed (why is it necessary?) subspace of $X$. Dene the quotient norm on $X/Z$ by $\|x+Z\|:=\operatorname{dist}(x,Z)$. Prove that it indeed denes a norm. Moreover, if $X$ is a Banach space, then so is $X/Z$ under the quotient norm.

> **Proof** To see that the quotient norm $\operatorname{dist}(-,Z)$ is a norm, we see that
>
> * $\operatorname {dist}(x,Z)=0$ whenever there exists $\{x_\lambda\}$ s.t. $\{x_\lambda\}\to x$, whenever $x\in Z$ (since $Z$ is closed);
>
> * $\operatorname{dist}(ax,Z)=\operatorname{dist}(ax,aZ)=|a|\operatorname{dist}(x,Z)$;
>
> * by definition, 
>   $$
>   \begin{align*}
>   \operatorname{dist}(x+y,Z)&=\sup_{z}\operatorname{dist}(x+y,z)\\[6pt]
>   &\leq \sup_{z}\operatorname{dist}(x,z)+\sup_{z}\operatorname{dist}(y,z)\\[6pt]
>   &\leq \operatorname{dist}(x,Z)+\operatorname{dist}(y,Z).
>   \end{align*}
>   $$
>
> Here it is highlighted that $Z$ is closed; otherwise, let $Y$ be any non-completed vector linear space (hence, $Y\subsetneq\overline Y$), then $x\in \overline Y\setminus Y$ has quotient norm $0$, which contradicts the definition of norm. 
>
> Since $\operatorname{dist}(x,Z)\leq\operatorname{dist}(x,0)=\|x\|$, we see that $\{x_\lambda\}\to x_0$ implies $\{x_\lambda+Z\}\to x_\lambda+Z$. Therefore, if $X$ is a Banach space, then so is $X/Z$ under the quotient norm.

**Ex 4** Let $X$ be a normed vector space and let $T\in \mathcal B(X,Y)$. Prove that the operator $T_0:X/\ker T\to \operatorname{ran}T$ given by $T_0(x+\ker T)=Tx$ for every $x\in X$ satisfies $\|T_0\|=\|T\|$. 

> Let $\pi:X\to X/\ker T$ be the canonical projection and $\iota:\operatorname{ran}T\hookrightarrow Y$ be the natural inclusion. Then we can factorise $T=\iota\circ T_0\circ \pi$. This is a factorisation over bounded maps; it is known as the canonical factorisation of $T$. Note that $(T_0)^{-1}$ may fail to be bounded; i.e., $T_0$ is not necessarily an NVS-isomorphism. Compare with the rank-nullity theorem in (finite-dimensional) linear algebra and the first isomorphism theorem in group theory.

> **Proof** First, $T^{-1}(\{0\})=\ker T$ is closed in $X$. We only need to prove that
> $$
> \sup_{\|x\|=1}\|Tx\|=\sup_{\operatorname{dist}(x,\ker T)=1}\|T_0(x+\ker T)\|.
> $$
> Since $0\in \ker T$, it directly follows that LHS $\geq$ RHS. Since 
> $$
> \sup_{\operatorname{dist}(x,\ker T)=1}\|T_0(x+\ker T)\|=\sup_{\|x-z\|=1,z\in \ker T}\|T(x+z)\|=\sup_{\|x\|=1}\|Tx\|,
> $$
> the equality is proved. 

**Ex 5** Let $X$ be an infinite-dimensional Banach space. Using Baire Category Theorem, show that $X$ cannot have countable Hamel bases. 

> **Proof** If not, then let $\{x_n\}_{n\geq 1}$ be the collection of Hamel basis of $X$. Then $X$ is isomorphic (in manner of linear space) to 
> $$
> \bigcup_{n\geq 1}\left\{\sum_{1\leq k\leq n} c_kx_k:c_k\in \mathbb F\right\}.
> $$
> It yields that $X$ is a countable union of non-where dense closed set, which is not Banach. 

**Ex 6** Let $X$ be a normed vector space. A series $\sum x_n$ is said to be absolutely convergent if $\sum_{n=1}^\infty\|x_n\|<\infty$. Prove that $X$ is a Banach space if and only if every absolutely convergent series in $X$ also converges in $X$.

> **Proof** $\Rightarrow$ If $X$ is Banach, then every Cauchy sequence converges to $X$. 
>
> $\Leftarrow$ Since every Cauchy sequence is written as the sum of absolutely sequence, the convergence of absolutely convergent sequence implies that $X$ is Banach.



