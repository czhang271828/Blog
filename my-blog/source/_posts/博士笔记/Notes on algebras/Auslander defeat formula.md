---
title: A short proof of Auslander defeat formula  
date: 2023-10-26 16：00：00
category: 
- 代数笔记
- AR 理论
tags: 笔记
mathjax: true
---

# A short proof of Auslander defeat formula  

## Notations

**Notation** Set $k\in\mathrm{CommRing}$, $R\in k\mathrm{Alg}$. Let $I$ be any injective modules. Define the dual functor 
$$
D:=(-,I)_k:=\operatorname{Hom}_k(-,I).
$$

**Definition** The dual functor is the following covariant functor 
$$
\ast: \mathrm{Hom}_R(P,R).
$$

**Definition** Say $X$ is a finitely presented module, if there exists some finitely generated projective module $P_0$ and $P_1$, such that
$$
P_1\to P_0\to X\to 0
$$
is exact. Since projective module is a summand of free module, $P_0$ and $P_1$ can be substitude by finitely generated free modules. 

**Definition** For $P_1\to P_0\to X\to 0$ finitely presented module, we define the transposition (Auslander dual) of $X$ as the cokernel of $P_0^\ast \to P_1^\ast$, that is, the following sequence in the category of $R^{\mathrm {op}}$-modules is exact
$$
P_0^\ast \to P_1^\ast \to \operatorname {Tr}(X)\to 0.
$$

## The proof

**Notation** From now on, $\mathscr A$ is locally small Abelian category. The $\text{米田}$ embedding writes $\text{よ}_X:\operatorname{Hom}_{\mathscr A}(-,X)$ and $\text{よ}^X:\mathrm{Hom}_{\mathscr A}(X,-)$. 

**Definition** Given short exact sequence $0\to A\to B\to C\to 0$, set
* $\delta_\ast$ as the functor such that 
$$
0\to \text{よ}^C(X)\to \text{よ}^B(X)\to \text{よ}^A(X)\to \delta_\ast(X)\to 0
$$
is exact in the category of $\mathbb Z$-modules;
* $\delta^\ast$ as the functor such that 
$$
0\to \text{よ}_A(X)\to \text{よ}_B(X)\to \text{よ}_C(X)\to \delta^\ast(X)\to 0
$$
is exact in the category of $\mathbb Z$-modules 

for every $X\in \mathsf{Ob}(\mathscr A)$. 

**Proposition** For $A\in \mathsf{Ob}({}_R\mathrm{Mod})$ and $Y\in \mathsf{Ob}(\mathrm{Mod}_R)$, wehave that
$$
D(Y\otimes A)\cong \mathrm{Hom}_R(A,DY)
$$
which is functorial in $Y$ and $A$.
> **Proof** Consider the natural isomorphism induced by the adjunction
> $$
> (Y\otimes_R A,I)_k\cong (A,(Y,I)_k)_R. 
> $$

**Proposition** For finitely generated projective module $P$, we have that
$$
P^\ast\otimes_R A\cong (P,A)_R,
$$
which is functorial in $P$ and $A$. 
> **Proof** Let $Q$ be projective module such that $P\oplus Q\cong R^n$. Then $Q\cong \ker(R^n\to P)$ is also finitely generated. 
> >In fact, finitely generated projective modules, finitely presented modules, finitely presented flat modules are the same for any rings. 
> 
> Consider the natural isomorphism 
> $$
> (R^n)^\ast \otimes _RA\cong \text{よ}_A(R^n)\cong \text{よ}_A(R)^n\cong (R^\ast \otimes _RA)^n,
> $$
> we have the following commutative diagram 
> $$
> \begin{matrix}
 &  & 0 & \leftarrow  & P & \leftarrow  & R^{n} & \leftarrow  & R^{m}\\
 &  & \downarrow  &  & \downarrow  &  & \downarrow  &  & \downarrow \\
0 & \rightarrow  & 0 & \rightarrow  & \text{よ}_{A}( P) & \rightarrow  & \text{よ}_{A}\left( R^{n}\right) & \rightarrow  & \text{よ}_{A}\left( R^{m}\right)\\
\downarrow  &  & \downarrow  &  & \boxed\downarrow  &  & \ \ \parallel \sim  &  & \ \ \parallel \sim \\
0 & \rightarrow  & 0 & \rightarrow  & P^{\ast } \otimes _{R} A & \rightarrow  & R{^{n}}^{\ast } \otimes _{R} A & \rightarrow  & R{^{m}}^{\ast } \otimes _{R} A\\
 &  & \uparrow  &  & \uparrow  &  & \uparrow  &  & \uparrow \\
 &  & 0 & \rightarrow  & P^{\ast } & \rightarrow  & R{^{n}}^{\ast } & \rightarrow  & R{^{m}}^{\ast }\\
 &  & \uparrow  &  & \uparrow  &  & \uparrow  &  & \uparrow \\
 &  & 0 & \leftarrow  & P & \leftarrow  & R^{n} & \leftarrow  & R^{m} &.
\end{matrix}
> $$
> Here the boxed morphism is given by 
> $$
> \text{よ}_A(P)\ni f\mapsto \sum_i \{r_j\mapsto \delta_{i,j}\}\otimes_R f(r_i)\in P^\ast\otimes _RA.
> $$
> Here $r_j$ are generators of $P$. By five lemma, $\boxed \downarrow$ is an isomorphism. 

**Theorem** $D\delta^\ast (X)\cong \delta_\ast(D\operatorname{Tr}X)$ is functorial in $\delta$ and finitely presented module $X$. 
> **Proof** We note that
> $$
> \begin{matrix}
 &  & P_{0}^{\ast } \otimes A & \rightarrow  & P_{1}^{\ast } \otimes A & \twoheadrightarrow  & \mathrm{Tr}( X) \otimes A\\
 &  & \ \ \parallel \sim  &  & \ \ \parallel \sim  &  & \\
\text{よ}_{A}( X) & \hookrightarrow  & \text{よ}_{A}( P_{0}) & \rightarrow  & \text{よ}_{A}( P_{1}) &  & .
\end{matrix}
> $$
> Then there is a pattern of exact sequence
> $$
> \begin{matrix}
 &  &  &  &  &  & 0\\
 &  &  &  &  &  & \downarrow \\
0 &  & 0 &  & 0 &  & K\\
\downarrow  &  & \downarrow  &  & \uparrow  &  & \ \ \downarrow b\\
\text{よ}_{A}( X) & \hookrightarrow  & \text{よ}_{A}( P_{0}) & \rightarrow  & \text{よ}_{A}( P_{1}) & \twoheadrightarrow  & \mathrm{Tr}( X) \otimes A\\
\downarrow  &  & \downarrow  &  & \downarrow  &  & \downarrow \\
\text{よ}_{B}( X) & \hookrightarrow  & \text{よ}_{B}( P_{0}) & \rightarrow  & \text{よ}_{B}( P_{1}) & \twoheadrightarrow  & \mathrm{Tr}( X) \otimes B\\
\downarrow  &  & \downarrow  &  & \downarrow  &  & \downarrow \\
\text{よ}_{C}( X) & \hookrightarrow  & \text{よ}_{C}( P_{0}) & \rightarrow  & \text{よ}_{C}( P_{1}) & \twoheadrightarrow  & \mathrm{Tr}( X) \otimes C\\
\ \ \downarrow a &  & \downarrow  &  & \downarrow  &  & \downarrow \\
\delta ^{\ast }( X) &  & 0 &  & 0 &  & 0\\
\downarrow  &  &  &  &  &  & \\
0 &  &  &  &  &  & .
\end{matrix}
> $$
> By snake lemma, we have the isomorphism $\operatorname{ker}(b)\cong \operatorname{coker}(a)$ which is also functorial. Hence, 
> $$
> D\delta^\ast (X)\cong DK=D(\operatorname{Tr}(X)\otimes \ker(A\to B)).
> $$
> We learn by functorial isomorphism in the proposition a priori that 
> $$
> D(\operatorname{Tr}(X)\otimes \ker(A\to B))\cong \text{よ}_{D\operatorname{Tr}(X)}(\ker(A\to B)).
> $$
> The right hand side equals $\delta_\ast (D\operatorname{Tr}(X))$ by definition. 

## Uniqueness of $\operatorname {Tr}(-)$. 

**Definition** Say $M$ and $N$ are projective equivalent, whenever there exists finitely generated projective modules $P$ and $Q$ such that $M\oplus P\cong N\oplus Q$. 

**Theorem** $\operatorname {Tr}(M)$ is unique in the manner of projective equivalence. 
> **Proof** We split the proof into the following parts. 
> 1. For any presentation $Q_1\to Q_0\to M\to 0$, there exists another presentation $P_1\to P_0\to M\to 0$ such that the following rows and columns are exact. We say $Q_1\to Q_0\to M\to 0$ is dominated by $P_1\to P_0\to M\to 0$. 
> $$
> \begin{matrix}
0 & \rightarrow  & K_{1} & \rightarrow  & P_{1} & \rightarrow  & Q_{1} & \rightarrow  & 0\\
 &  & \downarrow  &  & \downarrow  &  & \downarrow  &  & \\
0 & \rightarrow  & K_{0} & \rightarrow  & P_{0} & \rightarrow  & Q_{0} & \rightarrow  & 0\\
 &  & \downarrow  &  & \downarrow  &  & \downarrow  &  & \\
 &  & 0 & \rightarrow  & M & = & M & \rightarrow  & 0\\
 &  &  &  & \downarrow  &  & \downarrow  &  & \\
 &  &  &  & 0 &  & 0 &  & .
\end{matrix} 
> $$
>
> 2. Write $\operatorname{Tr}(M)_X:=\operatorname{coker}(X_0^\ast \to X_1^\ast)$ for $X=P,Q$. Then $\operatorname{Tr}(M)_P$ and $\operatorname{Tr}(M)_Q$ are projective equivalent. 

**Proposition** (Part I) Every two presentations $Q_1\to Q_0\to M\to 0$ and $P_1\to P_0\to M\to 0$ are dominated by some presentations. 
> **Proof** First, we extend the projective resolution 
> $$
> \begin{matrix}
P_{2} & \xrightarrow{u^{\prime }} & P_{1} & \xrightarrow{u} & P_{0} & \xrightarrow{f} & M & \rightarrow  & 0&,\\
 &  &  &  &  &  &  &  & & \\
Q_{2} & \xrightarrow{v^{\prime }} & Q_{1} & \xrightarrow{v} & Q_{0} & \xrightarrow{g} & M & \rightarrow  & 0 &.
\end{matrix}
> $$
> Write $(E,\alpha)$ as the kernel of $(f,g)$, i.e., 
> $$
> \begin{matrix}
0 & \rightarrow  & E & \xrightarrow{\alpha } & P_{0} \oplus Q_{0} & \xrightarrow{( f,g)} & M & \rightarrow  & 0\\[6pt]
 &  &  &  & ( p,q) & \mapsto  & f( p) +g( q) &  & .
\end{matrix}
> $$
> Now we claim that 
> $$
> \begin{matrix}
 E\oplus P_2\oplus Q_2 & \xrightarrow{(\alpha,0,0 )} & P_{0} \oplus Q_{0} & \xrightarrow{( f,g)} & M & \rightarrow  & 0\\[6pt]
  (e,p,q) & \mapsto  & \alpha(e) &  & &&.
\end{matrix}
> $$
> dominates the $P$-presentation. The claim for $Q$-presentation is symmetric. The proof of the claim is given as follows.
>
> 1. By lifting property of projective modules, take $\phi_0: P_0\to Q_0$ such that 
> $$
> \begin{matrix}
 & P_{0} & \xrightarrow{f} & M & \rightarrow  & 0\\
\phi _{0} & \downarrow  & \circlearrowleft  & \parallel  &  & &\\
 & Q_{0} & \xrightarrow[g]{} & M & \rightarrow  & 0 &.
\end{matrix}
> $$
> Then we consider the following commutative diagram
> $$
> \begin{matrix}
 &  &  & ( p,q) &  & f( p) +g( q) &  & \\[8pt]
 & E & \xrightarrow{\alpha } & P_{0} \oplus Q_{0} & \xrightarrow{( f,g)} & M & \rightarrow  & 0\\
\delta  & \downarrow  & \circlearrowleft  & \downarrow  &  & \parallel  &  & \\
 & Q_{1} & \xrightarrow[v]{} & Q_{0} & \xrightarrow[g]{} & M & \rightarrow  & 0\\[8pt]
 &  &  & \phi _{0}( p) +q &  & f( p) +g( q) &  & .
\end{matrix}
> $$
> Here the existence of $\delta$ is given by lifting property. Finally we define
> $$
> \begin{matrix}
 & ( e,p_{0} ,q_{0}) &  & ( p,q) &  &  &  & \\[8pt]
 & E\oplus P_{2} \oplus Q_{2} & \xrightarrow{( \alpha ,0,0)} & P_{0} \oplus Q_{0} & \xrightarrow{( f,g)} & M & \rightarrow  & 0\\
( \delta ,0,v^\prime) & \downarrow  &  & \downarrow  &  & \parallel  &  & \\
 & Q_{1} & \xrightarrow[v]{} & Q_{0} & \xrightarrow[g]{} & M & \rightarrow  & 0\\[8pt]
 & \delta ( e) +v^\prime( q_{0}) &  & \phi _{0}( p) +q &  &  &  & .
\end{matrix}
> $$
> Here $v(\delta(e)+v^\prime(q_0))=v\delta(e)=\phi_0(p)+q$, thus the diagram commutes. It remains to show that 
> * $(\delta,0,v^\prime)$ is surjective;
> * $\ker(\delta,0,v^\prime)\to \ker(\phi,1)$ is also surjective.
> 
> For the first proposition, we take any $q\in Q_1$ and obtain 
> $$
> (0,v(q))\in \ker(f,g)=\operatorname {im}(\alpha,0,0). 
> $$
> Now we take $e$ such that $\alpha (e)=(0,v(q))$. Therefore, 
> $$
> (\delta,0,v^\prime)(e,p_0,q_0)=\delta(e)+v^\prime (q_0).
> $$
> Since $v(\delta(e)-q)=(\phi_0,1)\alpha(e)-v(q)=0+v(q)-v(q)=0$, we see that 
> $$
> (\delta(e)-q)\in\ker (v)=\operatorname{im}(v^\prime).  
> $$
> Hence, we can find $q_0$ such that $\delta (e)-q=v^\prime(q_0)$. 
>
> For the latter proposition, to see that
> $$
> \ker(\delta,0,v^\prime)\xrightarrow{\widetilde{(\alpha,0,0)}}\ker(\phi_0,1)
> $$
> is surjective, we take $(p,q)\in \ker(\phi_0,1)$ and have that $\phi_0(p)+q=0$. Consider
> $$
> \ker(\phi_0,1)\subseteq \ker(f,g)=\operatorname{im}(\alpha,0,0).
> $$
> Then there exists $e\in E$ such that $\alpha(e)=(p,q)$. From the proof that $(\delta,0,v^\prime)$ is an epimorphism, there exists $q_0$ such that $\delta(e)-v^\prime(q_0)=0$. Then $(e,0,q_0)$ lies in the preimage of $(p,q)$. 

**Proposition** (Part II) For any presentation $Q_1\to Q_0\to M\to 0$, if there exists another presentation $P_1\to P_0\to M\to 0$ such that the following rows and columns are exact
$$
\begin{matrix}
0 & \rightarrow  & K_{1} & \rightarrow  & P_{1} & \rightarrow  & Q_{1} & \rightarrow  & 0\\
 &  & \downarrow  &  & \downarrow  &  & \downarrow  &  & \\
0 & \rightarrow  & K_{0} & \rightarrow  & P_{0} & \rightarrow  & Q_{0} & \rightarrow  & 0\\
 &  & \downarrow  &  & \downarrow  &  & \downarrow  &  & \\
 &  & 0 & \rightarrow  & M & = & M & \rightarrow  & 0\\
 &  &  &  & \downarrow  &  & \downarrow  &  & \\
 &  &  &  & 0 &  & 0 &  & .
\end{matrix}
$$
Then $\operatorname{Tr}(M)_P$ and $\operatorname{Tr}(M)_Q$ are projective equivalent. 
> **Proof** For $i\in \{0,1\}$, $K_i$ is projective since $K_i\oplus Q_i\cong P_i$. Therefore $K_1\to K_0$ is a split epimorphism. 
> Then we consider the dual diagram 
> $$
> \begin{matrix}
 &  & 0 &  & 0 &  & 0 &  & \\
 &  & \uparrow  &  & \uparrow  &  & \uparrow  &  & \\
0 & \leftarrow  & K & \leftarrow  & \operatorname{Tr}( M)_{P} & \leftarrow  & \operatorname{Tr}( M)_{Q} & \leftarrow  & 0\\
 &  & \uparrow  &  & \uparrow  &  & \uparrow  &  & \\
0 & \leftarrow  & K_{1}^{\ast } & \leftarrow  & P_{1}^{\ast } & \leftarrow  & Q_{1}^{\ast } & \leftarrow  & 0\\
 &  & \uparrow  &  & \uparrow  &  & \uparrow  &  & \\
0 & \leftarrow  & K_{0}^{\ast } & \leftarrow  & P_{0}^{\ast } & \leftarrow  & Q_{0}^{\ast } & \leftarrow  & 0\\
 &  & \uparrow  &  & \uparrow  &  & \uparrow  &  & \\
 &  & 0 & \leftarrow  & M^{\ast } & = & M^{\ast } & \leftarrow  & 0\\
 &  &  &  & \uparrow  &  & \uparrow  &  & \\
 &  &  &  & 0 &  & 0 &  & .
\end{matrix}
> $$
> Here $K$ is given by $\operatorname{coker}(K_0^\ast \to K_1^\ast )$. By snake lemma, the first row is exact. Since $K_0^\ast \to K_1^\ast$ is a split monomorphism, $K$ is projective. Therefore, $\operatorname{Tr}(M)_P\cong \operatorname{Tr}(M)_Q\oplus K$. 

## Proof of AR-formula

**Definition** For $\text{よ}^A(B)$, we define the quotient group (subgroup) 
$$
\underline{\text{よ}^A(B)}:=\frac{\text{よ}^A(B)}{\{f:f\text{ factors through some proj. mod..}\}}.
$$

**Proposition** For $0\to K\to P\to B\to 0$, we have that 
$$
0\to \text{よ}_K\to\text{よ}_P\overset {\text{よ}_g}\to \text{よ}_B\to \underline{\text{よ}_B}\to 0,
$$
which is functorially exact. 
> **Proof** For arbitrary $A$, we claim that every $A\xrightarrow f B$ factoring through a projective module $P^\prime$ factors through $P$. The claim is due to 
> $$
>\begin{matrix}
A & \xrightarrow{f} &\!\! B \\
\downarrow  & \nearrow  & \,\,\uparrow g\\
P^{\prime } & \xrightarrow[u]{} &\!\! P &.
\end{matrix}
> $$
> Here $u$ is given by lifting property of projective module for the epimorphism $P\xrightarrow{g}B$. Therefore, 
> $$
> \left[\ker(\text{よ}_B(A)\to \underline{\ker(\text{よ}_B(A))})\right]\subseteq \operatorname{im}(\text{よ}_g(A)). 
> $$

**Theorem** (AR formula) $D\underline{\text{よ}_C(X)}\cong \operatorname{Ext}^1(C,D\operatorname{Tr}(X))$ is functorial in $X$ and $C$. 
> **Proof** $D\underline{\text{よ}_C(X)}\cong D\delta^\ast(X)\cong \delta_\ast(D\operatorname{Tr}(X))\cong \operatorname{Ext}^1(C,D\operatorname{Tr}(X))$.

**Example** For $k$ a field, $I=k$, $R$ the finite $k$-algebra, we have
$$
\operatorname{Ext}^1_R(X,D\operatorname{Tr}(X))= 0,
$$
whenever $X$ is projective. 
> **Proof** Consider the AR formula, we have the isomorphism
> $$
> D\underline{\operatorname{End}_R(X)}\cong \operatorname{Ext}^1_R(X,D\operatorname{Tr}(X)).
> $$
> If $X$ is projective, then the identity takes zero. Conversely, if $X$ is not projective, then $1_X:X\to X$ no longer factors through any projective modules; otherwise, if there is any factorisation
> $$
> \left[X\xrightarrow{\iota}P\xrightarrow{\pi}X\right]=\operatorname{1_X}.
> $$
> Then $\iota$ is split monomorphism and thus $X$ is a direct summand of $P$, which contradicts our assumption. 

**Example** With $[\delta^\ast (X)=0]\Leftrightarrow [\delta_\ast(D\operatorname{Tr}(X))=0]$, we have that
$$
\left[\text{よ}^X(B)\twoheadrightarrow \text{よ}^X(C)\right]\Leftrightarrow \left[\text{よ}_{D\operatorname{Tr}(X)}(B)\twoheadrightarrow \text{よ}_{D\operatorname{Tr}(X)}(A)\right].
$$
In other words, the following are equivalent
* any $X\to C$ factor through $X\to B$;
* any $A\to D\operatorname{Tr}X$ factor through $B\to D\operatorname{Tr}X$. 

$$
\begin{matrix}
 &  &  &  &  &  & X &  & \\
 &  &  &  &  & \swarrow  & \downarrow  &  & \\
0 & \rightarrow  & A & \rightarrow  & B & \rightarrow  & C & \rightarrow  & 0\\
 &  & \downarrow  & \swarrow  &  &  &  &  & \\
 &  & D\operatorname{Tr} X &  &  &  &  &  & .
\end{matrix}
$$
