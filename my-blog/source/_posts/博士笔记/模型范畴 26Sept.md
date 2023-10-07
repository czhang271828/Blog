---
title: Model structure
category: 
- 学科笔记
- Zhang 组会
tags: 
- 模型范畴
mathjax: true
---

## Basic about the model structure 

### Model structure

**Definition** Given category $\mathcal M$, (How large?), the model structure consists of the triple $(\mathrm{Cofib}(\mathcal M), \mathrm{Fib}(\mathcal M), \mathrm{Weq}(\mathcal M))$ of classes of morphisms. 

* $\mathrm{Cofib}$ consists of the collection of cofibrations, "monomorphism" ($\hookrightarrow $);
* $\mathrm{Fib}$ consists of the collection of fibrations, "epimorphism" ($\twoheadrightarrow$);
* $\mathrm{Weq}$ consists of the collection of weak equivalence (neither fibration nor cofibration in general);
* $\mathrm{Weq}\cap \mathrm{Cofib}$ consists of trivial cofibration ($\,\,\,\,\mid\!\!\!\!\hookrightarrow$); 
* $\mathrm{Weq}\cap \mathrm{Fib}$ consists of trivial fibration ($\,\,\,\,\mid\!\!\!\!\twoheadrightarrow$);
and satisfy the following: 
1. [M1] (Lifting property) Every commutative square <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20230926184101669.png" style="zoom: 33%;" /> induces a morphism $s$ if either $i$ or $p$ in $\mathrm{Weq}$, that is, 

   <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006215454398.png" style="zoom:33%;" />
2. [M2] (Factorisation property) $\forall \left[X\overset f\to Y\right]\in \mathsf{Mor}(\mathcal M)$ has the (mono-sur) factorisation <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006215622915.png" style="zoom:33%;" />, that is, 
   $$
   \mathsf{Mor}=\mathrm{Fib}\circ (\mathrm{Cofib}\cap \mathrm{Weq})=(\mathrm{Fib}\cap \mathrm{Weq})\circ \mathrm{Cofib}.
   $$
3. [M3] When there exists any, both $\mathrm{Cofib}(\mathcal M)$ and $\mathrm{Fib}(\mathcal M)$ are closed under compositions. Fibration (resp. cofibrations) are closed under pullback (reps. pushforward), that is, 
   
   <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006220042481.png" style="zoom: 33%;" />.
> Isomorphisms are both fibration and cofibration.  
4. [M4] In the square above, the pullback (resp. pushforward) of trivial fibration (resp. trivial cofibration) is still trivial fibration (resp. trivial cofibration).
5. [M5] ($2\to 3$ property) In $X\overset g\to Y\overset f\to Z$, if two of $\{f,g,fg\}$ are in $\mathrm{Weq}$, then so is the third. 

**Proposition** Consider [M2] and [M5], we have that
$$
\mathrm{Weq}=(\mathrm{Fib}\cap \mathrm{Weq})\circ (\mathrm{Cofib}\cap \mathrm{Weq}).
$$

<img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006220205789.png" style="zoom:33%;" />.

**Proposition** [M2] is functorial. Given the 2-morphism $(f,f^\prime):\varphi\to \psi$, or morphism in the morphism category, there exists $s$ such that 

1. there exists $(i,i^\prime):\varphi\to s$ in $\mathrm{Cofib}\cap \mathrm{Weq}$ and $(p,p^\prime):s\to \psi$ in $\mathrm{Fib}$;
2. there exists $(i,i^\prime):\varphi\to s$ in $\mathrm{Cofib}$ and $(p,p^\prime):s\to \psi$ in $\mathrm{Fib}\cap \mathrm{Weq}$. 

<img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20230926195816444.png" style="zoom:33%;" />.

> **Proof** Taking 
>
> * either $i$, $i^\prime$ in $\mathrm{Cofib}\cap \mathrm{Weq}$ and $p$, $p^\prime$ in $\mathrm{Fib}$, 
> * or $i$, $i^\prime$ in $\mathrm{Cofib}$ and $p$, $p^\prime$ in $\mathrm{Fib}\cap \mathrm{Weq}$, 
>
> then there exists $s$ such that the centroid square commutes
>
> <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20230926200656435.png"  style="zoom:33%;" />.

**Definition** $\mathcal M$ is a model category iff it is equipped with the model structure, and satisfies

* [M0] $\mathcal M$ is closed under finite limit and colimit. 

**Proposition** A model category is equipped with initial objects, terminal objects, kernels, cokernels, finite products, finite coproducts, finite pushforwards and fintie pullbacks. 

**Convention** From now on we assume $\mathcal M$ is a model category with zero object $0$. 

**Definition** (left/right lifting property, abbr., LLF/RLF). we say $i$ has LLP w.r.t. $p$ (eq., $p$ has RLP w.r.t. $i$), whenever the dashed arrow exists for arbitrary commutative square <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20230926192724026.png" style="zoom:33%;" />. Denote $l(S)=\{f\text{ has LLP w.r.t. }g\mid \forall g\in S\}$ and $r(S)=\{f\text{ has RLP w.r.t. }g\mid \forall g\in S\}$. Here $\{\mid \}$ stands for classes. 

**Proposition** $\mathrm{Cofib}\subseteq l(\mathrm{Fib}\cap\mathrm{Weq})$ and $\mathrm{Fib}\subseteq r(\mathrm{Cofib}\cap \mathrm{Weq})$, see [M1]. 

**Definition** (fibrant/cofibrant objects) $X$ is fibrant (resp., cofibrant) whenever $X\to 0$ is a fibration (resp., $0\to X$ is a cofibration). 

**Definition** (trivial object) $X$ is trivial whenever $X\to 0$ is a weak equivalence. 

**Convention** we denote the class (or the full subcategory) of fibrant/cofibrant/trivial objects by $\mathcal F$/$\mathcal C$/$\mathcal W$, respectively. 

**Proposition** By [M5], $\mathsf{Mor}(\mathcal W)$ consists of weak equivaleces. 
> Hint: consider the composition $0\to A\overset f\to B$ for arbitrary $\left[A\overset f\to B\right]\in \mathcal W$. 

## Closed model structure

**Definition** We say $f$ is a retract of $g$, whenever there exists any morphisms making the following diagram commutative 

<img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20230926192341890.png" style="zoom: 33%;" />.

**Definition** (closed model structure) We say $(\mathrm{Cofib}, \mathrm{Fib}, \mathrm{Weq})$ admits a closed model structure on $\mathcal M$, whenever the following are satisfied
1. [CM1]=[M5] ($2\to 3$ property) . 
2. [CM2] $\mathcal C$, $\mathcal F$ and $\mathcal W$ are closed under retraction. 
3. [CM3]=[M1] (Lifting property) .
4. [CM4]=[M2] (Factorisation property) .

**Definition** (closed model category) A closed model category is a category admits closed model structure, and satisfies 
* [CM0]=[M0].

**Proposition** A model structure is closed if it satisfies [CM2]. This is trivial.

**Proposition** A closed model category is indeed a model category. 

**Proposition** (lifting property + [CM2] = lifting equalities) We learn from [M1] that
$$
\begin{align*}
\mathrm{Cofib}&\subseteq l(\mathrm{Fib}\cap\mathrm{Weq}),\\[6pt]
r(\mathrm{Cofib})&\supseteq (\mathrm{Fib}\cap\mathrm{Weq}),\\[6pt]
\mathrm{Fib}&\subseteq r(\mathrm{Cofib}\cap \mathrm{Weq}),\\[6pt]
l(\mathrm{Fib})&\supseteq (\mathrm{Cofib}\cap \mathrm{Weq}). 
\end{align*}
$$
When [CM2], the equalities holds. 
> **Proof** To see that $\mathrm{Cofib}\supseteq l(\mathrm{Fib}\cap \mathrm{Weq})$, we take arbitrary $f\in (\mathrm{Fib}\cap \mathrm{Weq})$. By [CM4]=[M2], one has the factorisation
> $$
> f=p'\circ i'\in (\mathrm{Fib}\cap \mathrm{Weq})\circ \mathrm{Cofib},
> $$
> yielding the following commutative diagram 
>
> <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006220703144.png" style="zoom:33%;" />. Here the dashed $s$ exists due to [M1]. Therefore we have the retraction
>
> <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006194228868.png" style="zoom:33%;" />. Since $i'\in \mathrm{Cofib}$ and [CM2], $f\in \mathrm{Cofib}$. Conversely, we shall prove that $r(\mathrm{Cofib})\subseteq(\mathrm{Fib}\cap\mathrm{Weq})$. Take arbitrary $g\in r(\mathrm{Cofib})$ an factorise it into ([CM2])
> $$
> g=p\circ i\in (\mathrm{Fib}\cap \mathrm{Weq})\circ  \mathrm{Cofib}.
> $$
> By [CM1], there exists $t$ such that the following diagram commutes
>
> <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006195029108.png" style="zoom:33%;" />. It yields the retraction 
>
> <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006195909194.png" style="zoom:33%;" />. Since $p\in (\mathrm{Fib}\cap \mathrm{Weq})$ and [CM2], we have that $g\in (\mathrm{Fib}\cap \mathrm{Weq})$. The rest two statements are similar. 

**Proposition** A closed model category satisfies [M3], that is, 

1. $\mathrm{Fib}$ and $\mathrm{Fib}\cap \mathrm{Weq}$ are closed under compositions;
2. $\mathrm{Fib}$ and $\mathrm{Fib}\cap \mathrm{Weq}$ are closed under pullbacks;
3. $\mathrm{Cofib}$ and $\mathrm{Cofib}\cap \mathrm{Weq}$ are closed under compositions;
4. $\mathrm{Cofib}$ and $\mathrm{Cofib}\cap \mathrm{Weq}$ are closed under pushforwards. 

> **Proof** The proof of $n+2$ is similar to $n$ ($n=1,2$). Now we focus on 1 and $2$. 
>
> 1. Since $f\in \mathrm{Fib}$ whenever $f$ has RLP w.r.t. $\mathrm{Cofib}\cap\mathrm{Weq}$. Now we take $p$ and $p^\prime$ in $\mathrm{Fib}$. For arbitrary $i\in \mathrm{Cofib}\cap \mathrm{Weq}$, both $p$ and $p'$ have the LLP, i.e., the following diagram commutes. For commutative square $(pp^\prime)a=bi$, we first recover $s$ in the square $p(p^\prime a)=bi$ and then recover $t$ in the square $p^\prime a=si$. $s$ is what splits $(pp^\prime)a=bi$ into two triangles. Therefore, $\mathrm{Fib}$ is closed under compositions. 
>
>    Since $\mathrm{Weq}$ is also closed under compositions ([CM1]=[M5]), the trivial fibres are closed under compositions. <img src="https://cdn.jsdelivr.net/gh/czhang271828/imgs/test/image-20231006221718477.png" alt="image-20231006221718477" style="zoom:33%;" />.
>
> 2. 
