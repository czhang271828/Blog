---
title: 分析 HW6
date: 2023-10-31 11:40:00
category: 
- 学科笔记
- 博一(秋)
- 分析
tags: 
- 笔记
mathjax: true
---

## HW6 for Analysis

> ANALYSIS $\bullet$ MATH6105 $\bullet$ HOMEWORK \#6
> THE PROBLEM SHEETS ARE NOT TO BE HANDED IN

**Ex 1** Let $X$ be the topological space. Prove that for any subset $E\subseteq X$, we have 
$$
X\setminus \operatorname{int}(E)=\overline{X\setminus E}\quad \text{and}\quad X\setminus \overline E=\operatorname{int}(X\setminus E).
$$
Suppose furthermore that $X$ is a metric space. Prove that any closed subset of $X$ is a $G_\delta$-set. 

> **Proof** If $x\notin \operatorname {int}(E)$, then for any neighbourhood $x\in U_x$, there exists $x\in V_x\subseteq U_x$ s.t. $V_x\setminus E=\varnothing$. 
>
> * One on hand, $V_x$ has non-empty intersection with $X\setminus E$, thus 
>   $$
>   X\setminus \operatorname{int}(E)\subseteq \overline{X\setminus E}.
>   $$
>
> * On the other hand, since the set of points in $X\setminus E\subseteq X\setminus \operatorname{int}(E)$  and $X\setminus \operatorname{int}(E)$ is closed, we have that
>
> $$
> X\setminus \operatorname{int}(E)\supseteq \overline{X\setminus E}.
> $$
>
> We take $F:=X\setminus E$ in the identity $X\setminus \operatorname{int}(E)=\overline{X\setminus E}$, Hence, 
> $$
> X\setminus \operatorname{int}(X\setminus F)=\overline{F}.
> $$
> Hence, $X\setminus \overline F=\operatorname{int}(X\setminus F)$. 
>
> If $X$ is a metric space, then $X$ has countable topological basis. Given any fixed closed subset $F$, for any $x\in X\setminus F$, there exists an open neighbourhood $x\in V_x\subseteq X\setminus F$. WLOG, we can choose $V_x\in \mathscr F$ for $|\mathscr F|=|\mathbb N|$. Hence, 
> $$
> \mathscr G:=\{V_x:V_x\in \mathscr F\}
> $$
> is also countable. Define the closed set
> $$
> V^n:=V\setminus \bigcup_{x\notin V}B_{1/n}(x).
> $$
> Then $\bigcap (X\setminus V^n)=X\setminus V$. Finally, 
> $$
> F=\bigcap_{V\in \mathscr G}(X\setminus V)=\bigcap _{V\in \mathscr G}\bigcap_{n\in \mathbb N_+}(X\setminus V^n)
> $$
> is a $G_\delta$-set, since $\mathscr G$ and $\mathbb N_+$ are open. 

**Ex 2** Prove the following variant of the Baire category theorem: 

Any locally compact Hausdorff topological space is not a countable union of nowhere dense closed subsets. 

> **Proof** If not, then $\varnothing$ is a countable intersection of dense open sets, a contradiction. 

**Ex 3** We call $\mathcal C\subset\mathbb R$ a Cantor set if it is nonempty, compact, perfect (i.e., contains no isolated points), and totally disconnected (i.e., contains no intervals). Prove that every dense $G_\delta$-set in $[0, 1]$ contains a Cantor set.

Cantor sets are very good examples for meagre sets. The intuition is that meagre sets are obtained by taking away all possible subintervals from an interval. We shall use the above result to construct a set $\mathcal C\subset \mathbb R$ such that for any $a < b$, neither $X \cap [a, b]$ nor $[a,b]\setminus X$ is meagre. 

> **Proof** In fact, any perfect set contains a Cantor set. For $E\subset [0,1]$ the perfect set, we have the following the alternative 
>
> * if $\operatorname{int}(E)=\varnothing$, then $E$ is a Cantor set; 
> * if $E$ contains any interval, we can always construct a Cantor set in the closed interval. 

**Ex 4** Prove the following celebrated result due to Banach:

The set of nowhere differentiable continuous functions on $[0, 1]$ is residual in $\mathcal C([0, 1])$. That is, a generic continuous function is nowhere differentiable.

> **Proof** We define the subset of $\mathcal C([0,1])$ as follows
> $$
> E_n:=\left\{f\in \mathcal C([0,1]):\forall x\in [0,1],\exists y\in [0,1]\text{ s.t. }\frac{|f(x)-f(y)|}{|x-y|}>n\right\}.
> $$
> We claim that $E_n$ is open. First, we identify
> $$
> \mathcal C([0,1])\cong \mathcal C(\mathbb R),\quad f\mapsto f+f(0)\cdot 1_{x< 0}+f(1)\cdot 1_{x>1}.
> $$
> For any fixed $x\in [0,1]$, there exists $h\neq 0$ s.t.
> $$
> \frac{|f(x+h)-f(x)|}{|h|}=n+\varepsilon.
> $$
> Since $f$ is continuous, then there exists an open neighbourhood $x\in V_x$ such that
> $$
> \frac{|f(y+h)-f(y)|}{|h|}\geq n+\varepsilon/2
> $$
> for any $y\in V_x$. Hence, we have the following open cover of $[0,1]$. 
>
> * For $x\in [0,1]$, there exists $h_x$ and $V_x$ s.t. $\frac{|f(y+h_x)-f(y)|}{|h_x|}\geq n+\varepsilon_x$. Since $[0,1]$ is compact, we consider the finite subcover $\{V_x\}_{x\in X}$. We take
>   $$
>   \delta :=\frac{\min_{x\in X}\{|h_x|\}\cdot \min_{x\in X}\{\varepsilon_x\}}3,
>   $$
>   and deduce that for any $g\in \mathcal C([0,1])$ s.t. $\|f-g\|_\infty<\delta$, 
>   $$
>   \frac{|g(y+h_x)-g(y)|}{|h_x|}\geq \frac{|f(y+h_x)-f(y)|}{|h_x|}-\frac{2\delta}{|h_x|}\geq n+\varepsilon_x/3.
>   $$
>   Here there exists $x\in X$ s.t. $y\in V_x$. 
>
> We know that there exists some continuous but non-where differentiable functions due to the work of Weierstraß. Hence, $E_n$ is dense in $\mathcal C([0,1])$. 
>
> Finally, the dense $G_\delta$ set $\bigcap _{n\geq 1}E_n$ contains every non-where differentiable functions in $\mathcal C([0,1])$. Hence, a generic continuous function is nowhere differentiable.

**Ex 5** A number $0\leq x\leq 1$ ($x\notin \mathbb Q$) is said to be Liouville if for any $n > 0$ there is a rational number $p/q$ such that
$$
\left|x-\frac pq\right|<\frac1{q^n}.
$$
Prove that a generic number in $[0, 1]$ is Liouville. 

> **Proof** We define the open subset of $\mathbb [0,1]$​ as follows
> $$
> E_n:=\bigcup_{q\geq 2,p\in \mathbb Z}\left(\frac pq-\frac 1{q^n},\frac pq+\frac 1{q^n}\right)
> $$
> Then $E_n\cap [0,1]$ is dense, since it contains the set of rational numbers. Therefore, 
> $$
> \left(\bigcap_{n\geq 1}E_n\right)\cap ([0,1]\setminus  Q)
> $$
> is residual ($[0,1]\setminus \mathbb Q=\bigcap_{r\in \mathbb Q}[0,1]\setminus \{r\}$ is also residual.). 

**Ex 6** Prove the following variant of the uniform boundedness principle: Let $X$ be a Banach space and $Y$ be a normed vector space. Let $\{T_i\}_{i\in I}\subseteq \mathcal B(X,Y)$ (the set of continuous linear operators). Then either one of the following holds: 

1. $\sup_{i\in I}\|T_i\|<\infty$; or
2. there is a residual set $E\subseteq X$ s.t. $\sup_{i\in I}\|T_ix\|=\infty$ for all $x\in E$. 

> **Proof** We define the closed set 
> $$
> E_n:=\{x\in X:\sup_{i\in I}\|T_ix\|\leq n\}.
> $$
> In order to see that $E_n$ is closed, we take arbitrary $x_0\in X\setminus E_n$ and there exists $\varepsilon>0$ and $i=i_0$ s.t. $\|T_{i_0}x_0\|>n+\varepsilon$. Since $T_{i_0}$ is continuous, there exists $\delta_0>0$ s.t. for any $\|x-x'\|<\delta$, 
> $$
> \|T_{i_0}x\|\geq\|T_{i_0}x_0\|-\varepsilon/2> n+\varepsilon/2.
> $$
> Therefore, $x\in E_n$. 
>
> Now we assume $1$ ($\sup_{i\in I}\|T_i\|<\infty$) no longer holds, then there exists a sequence $\{x_k:\|x_k\|=1\}_{k\geq 1}$ and $\{T_k\}_{k\geq 1}\subseteq \{T_i\}_{i\in I}$ s.t.
> $$
> \|T_kx_k\|\geq k.
> $$
>  We claim that any
> $$
> E_\infty:=\{x\in X:\sup_{i\in I}\|T_ix\|=\infty\}
> $$
> is dense in $X$. In fact, for any $B_r(x_0)\subset X$, we see that
> $$
> \|T_k(x_0+x_k/2)\|\geq \frac 12\|T_kx_k\|-\|T_kx_0\|\overset{k\to\infty}\longrightarrow  \infty.
> $$
> It yields that $E_n$'s are no-where dense in $X$. Consequently, 
> $$
> E_\infty=X\setminus \bigcup_{n\geq 1}E_n
> $$
> is meagre. 