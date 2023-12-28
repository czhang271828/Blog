---
title: 分析 HW5
date: 2023-10-24 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW5 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#5
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

**Ex 1** Prove the minimality of the positive measures $\nu^\pm$ obtained by the Jordan decomposition theorem. More precisely, suppose that $\nu$ is a signed measure and $\lambda$, $\mu$ are positive measures such that $\nu=\lambda-\mu$. Show that $\lambda\geq \nu^+$ and $\mu\geq \nu^-$. (Recall that $\nu^\pm$ are the unique positive measures such that $\nu=\nu^+-\nu^-$ and $\nu^+\perp\nu^-$.)

> **Proof** For arbitrary $E\in \mathscr F$, we have that
> $$
> \nu^+(E)=\nu (E\cap P)\leq \lambda(E\cap P)\leq \lambda(E).
> $$
> Conversely, the proof of $\nu^-(E)\leq \mu(E)$ is similar. 

**Ex 2** Assume that $\nu\ll \mu$, where $\nu$ is a signed measure and $\mu$ is a positive measure on $(X,\mathscr F)$. Let $f=\frac{\operatorname d\nu}{\operatorname d\mu}\in \mathscr L^1(\mu)$ be the Radon-Nikodym derivative. Describe the Hahn decompositions of $\nu$ (with respect to $\mu$) and the measures $\nu^+$, $\nu^-$, and $|\nu|$ in terms of $f$ and $\mu$. 

> **Proof** Set $f_+:=\max \{f,0\}$ and $f_-=f_+-f$. We claim that
> $$
> \nu^+:=f_+\operatorname d\mu,\quad \nu^-:=f_-\operatorname d\mu,\quad |\nu|:=|f|\operatorname d\mu.
> $$
> The first identity is due to $\operatorname{supp}(f_+)=P$ ($\nu$-a.e.), and thus 
> $$
> \nu^+(E)=\nu(E\cap P)=\int_X 1_{E\cap P}\cdot f\operatorname d\nu=\int_X 1_{E}\cdot f_+\operatorname d\nu.
> $$

**Ex 3** Let $\mu$ be a positive measure. A collection of functions $\{f_\alpha\}_{\alpha\in \mathcal I}\subset \mathscr L^1(\mu)$ is said to be uniformly integrable if for every $\varepsilon>0$ there exists $\delta>0$ such that $|\int_Ef_\alpha\operatorname d\mu|<\varepsilon$ for all $\alpha\in \mathcal I$ whenever $\mu(E)<\delta$. Prove that if a sequence $\{f_n\}\subset \mathscr L^1(\mu)$ converges to some $f\in \mathscr L^1(\mu)$ in the $\mathscr L^1$-norm, then $\{f_n\}$ is uniformly integrable. 

> **Proof** For arbitrary $\varepsilon>0$, there exists $M_i$​ such that
> $$
> \left|\int_{|f_i|\geq M_i} f_i\operatorname d\mu\right|<\varepsilon/4.
> $$
> Define $\delta_i^M:=\mu(|f_i|\geq M_i)$. Since $f_n\to f$ in $\mathscr L^1(\mu)$, there exists $N\in \mathbb N_+$ such that $\|f-f_n\|_{\mathscr L^1(\mu)}<\varepsilon/8$. Now we take $M_{N+i}=M$ for $i\in \mathbb N$ and obtain that
> $$
> \left|\int_{|f_i|>M_i}f_i\operatorname d\mu\right|<\varepsilon/2.
> $$
> Similarly, we take $\sup M_i=\max M_i=M_0$ and $\delta^\prime :=\frac{\varepsilon}{4 M_0}$. Set $\delta:=\min\{\delta^\prime,\sup \delta_i^M\}$, then
> $$
> \left|\int_E f_i\operatorname d\mu\right|<\varepsilon\quad (\forall E,\mu(E)<\delta).
> $$

**Ex 4** Let $(X,\mathscr F,\mu)$ be a finite measure space and let $\mathscr G\subset \mathscr F$ be a $\sigma$-subalgebra. Set $\nu:=\mu|_\mathscr G$. Prove that for each $f\in \mathscr L^1(X,\mathscr F,\mu)$ there exists $g\in \mathscr L^1(X,\mathscr G,\nu)$ such that 
$$
\int_Ef\operatorname d\mu=\int_Eg\operatorname d\nu\quad \text{for all }E\in \mathscr G.
$$
 Moreover, $g$ is unique in the $\nu$-a.e. sense. 

> **Proof** Consider $g=f$ in sense of set mappings. Then $g$ is what we desire. For uniqueness, we suppose that $f=0$ and conclude that $g=f$ $\nu$-a.e.. If not, then there exists a $\nu$-measurable set $F$ such that 
> $$
> 0=\int_Ff\operatorname d\mu\neq \int _Fg\operatorname d\nu.
> $$
> Therefore, $F$ is not $\nu$-null. Since $F\in \mathscr G\subset \mathscr F$, we have that $\mu(F)=\mu|_{\mathscr G}(F)=\nu(F)\neq 0$, a contradiction. 

**Ex 5** We call $g$ the conditional expectation of $f$ with respect to $\mathscr G$ and write $g=\mathbb E[f\mid \mathscr G]$. 

In the above setting, suppose in addition that $\mathscr H$ is a further $\sigma$-algebra of $\mathscr G$. Prove the towering property of conditional expectations: 
$$
\mathbb E[\mathbb E[f\mid \mathscr G]\mid \mathscr H]=\mathbb E[f\mid \mathscr H]\quad \mu|_\mathscr H\text{-a.e.}.
$$

> **Proof** The $\sigma$-subalgebras $\mathscr H\subseteq \mathscr G\subseteq \mathscr F$ gives 
> $$
> \mu|_{\mathscr H}=(\mu|_{\mathscr G})|_{\mathscr H}\quad \mu=\mu|_{\mathscr F}.
> $$
> Therefore, for any $F\in \mathscr H$ we have that
> $$
> \int_Ff\operatorname d\mu|_{\mathscr F}=\int_Ff\cdot \frac{\operatorname d \mu|_\mathscr H}{\operatorname d\mu|_\mathscr F}\operatorname d\mu |_{\mathscr F}=\int_Ff\cdot \frac{\operatorname d \mu|_\mathscr H}{\operatorname d\mu|_\mathscr G}\cdot \frac{\operatorname d \mu|_\mathscr G}{\operatorname d\mu|_\mathscr F}\operatorname d\mu |_{\mathscr F}. 
> $$

**Ex 6** Find $f\in \mathscr L^1(\mathbb R^d)$ such that there are $C,R>0$ satisfying
$$
\mathcal Mf(x)\geq C|x|^{-d}\quad \text{for all }|x|>R,
$$
where $\mathcal Mf$ is the Hardy-Littlewood maximal function of $f$. Prove that there exists $C^\prime >0$ such that for $\alpha>0$ small, it holds that 
$$
\mathscr L^d(\{\mathcal Mf>\alpha\})\geq \dfrac{C^\prime}{\alpha}.
$$
This shows the sharpness of the estimate in the Hardy-Littlewood maximal theorem. 

> **Proof** We claim that $f=\operatorname 1_{B_1(O)}$ is the desired function. For $|x|>1$, we have that 
> $$
> \mathcal Mf(x)\geq \dfrac{\omega_d}{(|x|+1)^d\omega_d}\geq \frac{1}{2^d\cdot |x|^d}，
> $$
> where $\omega_d=\mathscr L^d(B_1(O))$ is the volume of unit ball. 
>
> WLOG, let $f$ be such that $\int_{B_{r_0}(O)}|f|=I>0$. Then for arbitrary $0<\alpha\ll I$​, 
> $$
> \mathcal Mf(x)\geq F_{|x|+r_0}(x)\geq \frac{I}{(|x|+r_0)^d\cdot \omega_d}.
> $$
> Hence, $\{\mathcal Mf>\alpha\}$​ contains the set
> $$
> |x|<\sqrt[d]{\frac{I}{\alpha\cdot \omega_d}}-r_0.
> $$
> WLOG, suppose that $\alpha$ is small so that $2r_0<\sqrt[d]{\frac{I}{\alpha\cdot \omega_d}}$. Therefore, 
> $$
> \mathscr L^d(\{\mathcal Mf>\alpha\})\geq\omega_d\cdot \left(\frac{1}{2}\sqrt[d]{\frac{I}{\alpha\cdot \omega_d}}^d\right)=\dfrac{I}{2^d\cdot \alpha}.
> $$