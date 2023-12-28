# Hodge 理论初步

## 实线性空间的 Hodge 理论

**D** (外形式上的双线性型) 记 $V=\mathbb R^n$, $B:V\times V\to \mathbb R$ 是双线性型, 定义
$$
\begin{align*}
\widetilde B:V^{\otimes s}\times V^{\otimes s}&\to \mathbb R,\\[6pt]
(v_1^I\otimes\cdots \otimes v_n^I,u_1^J\otimes\cdots \otimes u_n^J) &\mapsto \det (B(v_i^I,u_j^J)).  
\end{align*}
$$
以上 $I$ 与 $J$ 是关于有限指标的求和. 

**D** (反对称化算子的泛性质) 对任意反对称线性映射, 即
$$
\widetilde \varphi:V^{\otimes s}\to A,\widetilde\varphi\circ \sigma=(-1)^\sigma\cdot \widetilde \varphi.
$$
存在唯一的线性映射 $\varphi :V^{\wedge s}\to A$ 使得 $\widetilde \varphi=\varphi \circ \mathscr A$. 这里 $\mathscr A$ 是张量积到外微分的典范映射(反线性化). 

**P** $\widetilde B|_{(V^{\otimes s}\times V^{\otimes s})/\ker \widetilde B}\cong B|_{\mathscr A^s(V)\times\mathscr A^s(V)}$, 是非退化的, 且以上同构是自然同构. 

**D** 往后将 $B:V\times V\to \mathbb R$ 拓宽至 $\bigoplus_{s\geq 0}(\mathscr A^s(V)\times \mathscr A^s(V))$ 上. 

**D** (Hodge 算子) 记 $\mathscr A^s$ 是 $s$-次外微分形式, $\Omega$ 是 $V$ 的体积形式(非退化 $n$-次反对称型), 则定义 Hodge $\star$-算子是如下由 $(B,\Omega)$ 决定的算子
$$
\star: \mathscr A^s(V)\to \mathscr A^{n-s}(V),\quad \alpha\wedge (\star \omega )=B(\alpha,\omega)\Omega. 
$$
特别地, 当 $\Omega$ 与 $B$ 改变时, 
* $\alpha\wedge (\star_{\lambda \Omega,B}\omega)=B(\alpha,\omega)\lambda \Omega =\alpha\wedge (\lambda\star \omega)$; 
* $\alpha\wedge(\star_{\Omega,B(-,T-)})=B(\alpha,T\omega)\Omega=\alpha\wedge (\star T\omega)$. 

**D** (直和分解) 给定 $V=V_1\oplus V_2$, $\dim V_1=r$, $\dim V_2=s$. 若双线性型存在相应的分解 $B=B_1\oplus B_2:=\begin{pmatrix}
    B_1\\&B_2
\end{pmatrix}$, 则对 $\alpha_1,\omega_1\in \mathscr A^r(V_1)$, $\alpha_2,\beta_2\in \mathscr A^s(V_2)$, 总有
$$
B(\alpha_1\wedge\alpha_2,\omega_1\wedge \omega_2)=B_1(\alpha_1,\omega_1)\cdot B_2(\alpha_2,\omega_2). 
$$
给定对应的体积形式 $\Omega=\Omega_1\wedge \Omega_2$, 则
$$
\begin{align*}
&\quad \,\,(\alpha_1\wedge \alpha_2)\wedge(\star(\omega_1\wedge \omega_2))\\[6pt]
&=B_1(\alpha_1,\omega_1)\cdot B_2(\alpha_2,\omega_2)\Omega\\[6pt]
&=B_1(\alpha_1,\omega_1)\Omega_1\wedge B_2(\alpha_2,\omega_2)\Omega_2\\[6pt]
&=(\alpha_1\wedge\star_1\omega_1)\wedge (\alpha_2\wedge\star_2\omega_2)\\[6pt]
&=(-1)^{rs}(\alpha_1\wedge\alpha_2)\wedge (\star_1\omega_1\wedge\star_2\omega_2)\\[6pt]
&=(\alpha_1\wedge\alpha_2)\wedge (\star_2\omega_2\wedge\star_1\omega_1)\\[6pt]
\end{align*}
$$
这表明对有限直和 $V=\bigoplus_{s=1}^k V_s$, 有
$$
\star(\omega_1\wedge\cdots \wedge \omega_k)=(\star_k\omega_k)\wedge \cdots \wedge (\star_1\omega_1).
$$

**D** (内积, 外积) 给定 $V=\mathbb R^n$ 与 $1\leq s\leq n-1$, 对向量场 $X$ 与 $1$-形式 $\gamma$ 定义
* (内积) $i_X:\mathscr A^s(V)\to \mathscr A^{s-1}(V),\alpha\mapsto \iota_X(\alpha)$;
* (外积) $e_\gamma:\mathscr A^{s}(V)\to \mathscr A^{s+1}(V),\alpha\mapsto \gamma\wedge\alpha$. 

**D** ((右)伴随算子) 给定双线性型 $B$, 称 $\kappa$ 与 $\kappa^\dag$ 是左右伴随, 当且仅当有等式
$$
B(\kappa(u),v)=B(u,\kappa^\dag(v)). 
$$

**P** (内外积的右伴随) 对 $\alpha,\beta\in \mathscr A^s(V)$, $\alpha\wedge \star \beta:=B(\alpha,\beta)\Omega$. 给定体积形式 $\Omega\in \mathscr A^n(V)$. 则, 对 $\omega \in \mathscr A^{s+1}(V)$ 总有
$$
\begin{align*}
B(e_\gamma\alpha,\omega)\Omega&=(e_\gamma\alpha)\wedge(\star\omega)\\[6pt]
&=(-1)^s\alpha\wedge(\gamma\wedge \star\omega)\\[6pt]
&=(-1)^s\alpha\wedge(e_\gamma \star\omega)\\[6pt]
&=(-1)^s\alpha\wedge \star(\star^{-1}e_\gamma \star\omega)\\[6pt]
&=B(\alpha,(-1)^s\star^{-1}e_\gamma\star \omega)\Omega\\[6pt]
&=B(\alpha,e_\gamma^\dag \omega)\Omega.
\end{align*}
$$
同理, 对 $\omega\in \mathscr A^{s-1}(V)$ 总有
$$
\begin{align*}
B(i_X\alpha,\omega)\Omega&=(i_X\alpha)\wedge (\star\omega)\\[6pt]
&=i_X(\alpha\wedge \star\omega)+(-1)^s\alpha\wedge i_X(\star\omega)\\[6pt]
&=(-1)^s\alpha\wedge \star(\star^{-1}i_X\star\omega)\\[6pt]
&=B(\alpha,(-1)^s(\star^{-1}i_X\star\omega))\Omega\\[6pt]
&=B(\alpha,i_X^\dag \omega)\Omega.
\end{align*}
$$
这表明, 对定义在 $\mathscr A^s(V)$ 上的算子 $i_X$ 与 $e_\gamma$, 总有
$$
i_X^\dag =(-1)^s\star^{-1}i_X\star,\quad e_\gamma^\dag =(-1)^s\star^{-1}e_\gamma\star.
$$

**P** (求导公式) 对向量场 $X$ 与 $1$-形式 $\gamma$, 
$$
i_X e_\gamma +e_\gamma i_X=\gamma(X)\cdot \operatorname{id}. 
$$

**P** 特别地, 记 $$
$$
B(e_\gamma e_\delta^\dag+e_\gamma^\dag e_\delta)
$$