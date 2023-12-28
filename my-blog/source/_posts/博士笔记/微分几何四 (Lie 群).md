# Lie 群
## Lie 群与 Lie 代数初步

**D** (Lie 群) 若流形 $G$ 是群, 且连续映射 $\mu:G\times G\to G$ 是群的乘法, 则称 $G$ 是 Lie 群. 我们需验证 $\mu$ 是光滑映射, 考虑
$$
\Gamma_\mu:=\{(g,h,\mu(gh))\}\subseteq G\times G\times G.
$$
则以下复合映射 $p_{12}\circ i$ 是 Lie 群同构
$$
\begin{matrix}
\Gamma _{\mu } & \xrightarrow{i} & G\times G\times G & \xrightarrow{p_{12}} & G\times G\\[6pt]
\downarrow  &  & \downarrow  &  & \downarrow \\[6pt]
( g,h,\mu ( gh)) & \mapsto  & ( g,h,\mu ( gh)) & \rightarrow  & (g,h)\\[6pt]
. &  &  &  & 
\end{matrix}
$$

由于 $\mu(g,h)$ 是嵌入 $i\circ (p_{12}\circ i)^{-1}$ 的第三分量投影, 因此 $\mu$ 是可微的. 

**D** (左移, 右移) 定义微分同胚
* 左移映射 $L_g:G\xrightarrow{\sim} G,x\mapsto \mu(g,x)$;
* 右移映射 $R_h:G\xrightarrow{\sim} G,y\mapsto \mu(y,h)$. 

显然 $L_g$ 与 $R_h$ 可交换. 

**D** (切映射) 考虑 $\mu_{\ast (g,h)}:T_{(g,h)}(G\times G)\to T_{\mu(g,h)}G$, 对任意 $X,Y\in \Gamma(TG)$, 总有
$$
\begin{align*}
\mu_{\ast (g,h)}(X,Y)&=\frac{\operatorname{d}}{\operatorname{d}t}(\exp_g(tX)\exp_h(tY))|_{t=0}\\[6pt]
&=(L_g)_\ast Y_h+(R_h)_\ast X_g. 
\end{align*}
$$
以上利用了事实 $T_{(g,h)}(G\times G)=T_gG\oplus  T_hG$.

**P** 记 $e\in G$ 是群的单位元, 则
$$
T_{(e,e)}(X,Y)=X+Y. 
$$

**P** Lie 群的逆映射是光滑的. 特别地, 光滑曲线 $\exp_e(tX)$ 的逆为 $\exp_e(-tX)$. 

**P** (Lie 群上的左移不变向量场) 考虑单位元处的切向量 $X_e$, 定义 $X_g:=(L_g)_\ast X_e$, 从而
$$
(L_g)_\ast (X_h)=(L_g)_\ast (L_h)_\ast X_e=(L_{gh})_\ast X_e=X_{gh}. 
$$
反之, 任意左移不变向量场由向量场在 $e$ 处取值决定, 从而我们等同
$$
\{\text{左移不变向量场}\}\simeq T_eG.
$$

**P** (Lie 代数) 左移不变向量场在 Lie 括号下封闭. 因为
$$
h_\ast [X,Y]=[h_\ast X,h_\ast Y]. 
$$
此时, 称 $(T_eG,[,])$ 是 $G$ 的 Lie 代数, 记作 $\mathfrak g$. 

**D** (Lie 群同态) 称 $\varphi :G\to H$ 是 Lie 群同态, 当且仅当
* $\varphi :G\to H$ 是流形间光滑映射; 
* $\varphi:G\to H$ 是群同态. 

**P** Lie 群同态 $\varphi:G\to H$ 是常秩映射. 因为对任意 $g\in G$,
$$
\varphi_{\ast g}\circ (L_g)_\ast =(L_{\varphi(g)})_\ast \circ \varphi _{\ast e_G}. 
$$
而 $L_g$ 与 $L_{\varphi (g)}$ 是微分同胚, 从而 $\varphi_{\ast g}$ 与 $\varphi_{\ast e_G}$ 秩相同. 

**P** Lie 群同态 $\varphi :G\to H$ 诱导了
$$
(\varphi_{e_G})_\ast :\mathfrak{g}\to \mathfrak{h},X_{e_G}\mapsto (\varphi_\ast X)_{e_H}.
$$
这里 $\varepsilon_{e_G}$ 是 $\mathbb R$-线性且保持 Lie 括号的, 称之 Lie 代数同态.


**D** (Lie 群的伴随表示) 定义 Lie 群上的伴随映射为自同态
$$
c(g):G\to G,x\mapsto gxg^{-1}.
$$
定义其单位处切映射为伴随映射
$$
\operatorname{Ad}_g:=(c(g))_{\ast e} :T_eG\to T_eG,X\mapsto \frac{\operatorname d}{\operatorname dt}(g\exp_e(tX)g^{-1})|_{t=0}.
$$
特别地, 称 Lie 群的伴随表示为群同态 
$$
\operatorname{Ad}:G\to \operatorname{End}(T_eG),g\mapsto \operatorname{Ad}_g.
$$
**D** (Lie 代数的伴随表示) 对群同态 $\operatorname{Ad}:G\to T_eG$ 在单位处求导, 得 Lie 代数同态
$$
\operatorname{ad}:\mathfrak g\to \operatorname{Lie}(\operatorname{End}(T_eG)), X\mapsto [X,-].
$$
此处, 
$$
\begin{align*}
\operatorname{ad}_X(Y)&=\frac{\partial^2}{\partial s\partial t}(\exp_e(tX)\exp_e(sY)\exp_e(-tX))|_{s,t=0}\\[6pt]
&=\frac{\partial^2}{\partial s\partial t}(\exp_e(tX)\exp_e(sY)-\exp_e(sY)\exp_e(-tX))|_{s,t=0}\\[6pt]
&=[X,Y].
\end{align*}
$$

**P** (Ado 定理) 假定域特征为 $0$, 则有限维 Lie 群是矩阵群 $GL_n(-)$ 的子群.

## Lie 函子

**D** ($\operatorname{Lie}$ 函子) $\operatorname{Lie}$ 将 Lie 群对应作相应的 Lie 代数, 将 Lie 群同态对应做 Lie 代数同态. 容易验证 $\operatorname{Lie}$ 是 Lie 群范畴至 Lie 代数范畴的函子. 

**P** (Lie 函子保持直和) Lie 群的积对应 Lie 代数的直和, 即, 
$$
\operatorname{Lie}(G_1\times G_2)=\operatorname{Lie}(G_1)\oplus\operatorname{Lie}(G_2)
$$
上述直和视作内直和, 故记为等号.  

**P** (Lie 函子保持交) 对 Lie 群 $G$ 的 Lie 子群 $H_1$ 与 $H_2$, 有
$$
\operatorname{Lie}(H_1\cap H_2)=\operatorname{Lie}(H_1)\cap \operatorname{Lie}(H_2). 
$$

**P** (Lie 函子保持核) Lie 群同态 $\varphi:G\to H$ 常秩, 从而 $e_H$ 正则. 因此 $\varphi ^{-1}(e_H)$ 既是正则子流形又是闭子群. 因此
$$
\begin{matrix}
\operatorname{LieGrp} & \ker \varphi  & \xrightarrow{i_{0}} & G & \xrightarrow{\varphi } & H\\[6pt]
\operatorname{Lie} \downarrow \,\,\,\,\, & \downarrow  & \circlearrowleft  & \downarrow  & \circlearrowleft  & \downarrow \\[6pt]
\operatorname{LieAlg} & \ker \varphi _{\ast \ e} & \xrightarrow[( i_{0})_{\ast \ e}]{} & \mathfrak{g} & \xrightarrow[\varphi _{\ast \ e}]{} & \mathfrak{h}\\[6pt]
. &  &  &  &  & 
\end{matrix}
$$

**P** (指数映照的自然性) 记 $\exp_{\mathfrak{g}}(X_{e_G}):=\exp_{e_G}(tX_{e_G})|_{t=1}$, 则有如下交换图
$$
\begin{matrix}
 & G & \xrightarrow{\varphi } & H & \\[6pt]
T_{e_{G}} & \downarrow  & \circlearrowleft & \downarrow  & T_{e_{H}}\\[6pt]
 & \mathfrak{g} & \xrightarrow{\varphi _{\ast \ e_{G}}} & \mathfrak{h} & \\[6pt]
\exp_{\mathfrak{g}} & \downarrow  & \circlearrowleft  & \downarrow  & \exp_{\mathfrak{h}}\\[6pt]
 & G^\prime & \xrightarrow[\varphi |_{G^\prime}]{} & H^\prime & \\[6pt]
. &  &  &  & 
\end{matrix}
$$
这里, $(-)^\prime$ 是取包含单位元的连通分支. 更严格地, 定义函子 
$$
\begin{align*}
U:\text{Lie 群}&\to \text{光滑流形},\\[6pt]
G&\mapsto \text{包含单位元的连通分支},\\[6pt]
\varphi&\mapsto \varphi|_{U(G)}\text{ 忘却群同态结构}.
\end{align*}
$$
从而 $\exp:\operatorname{Lie}\to U$ 是函子间的自然变换. 



**P** (Lie 第三基本定理) 待补充.

**P** ($\Gamma$-$\operatorname{Lie}$ 伴随) 有限维 Lie 代数 $\mathfrak{g}$ 对应唯一的单联通 Lie 群, 记作 $\Gamma(\mathfrak{g})$. 此时存在连通 Lie 群范畴 $\operatorname{CLieGrp}$ 与 $\operatorname{LieAlg}$ 间的伴随
$$
\operatorname{Hom}_{\operatorname{CLieGrp}}(\Gamma(\mathfrak{g}),H)\cong\operatorname{Hom}_{\operatorname{LieAlg}}(\mathfrak{g},\operatorname{Lie}(H)).
$$
* 单位为 $\mathfrak{g}\to \operatorname{Lie}(\Gamma(\mathfrak{g}))$, 即, Lie 代数到自身的等同; 
* 余单位为 $\Gamma(\operatorname{Lie}(G))\to G$, 即万有覆盖 $\widetilde{G}$ 到 $G$ 的典范投影.

特别地, 
1. $\operatorname{Lie}$ 是忠实的;
2. $\Gamma$ 是全且忠实的;
3. 有限维 Lie 群 $G$ 的万有覆盖 $\widetilde G$ 存在且唯一.

## Lie 理论基本定理

**P** (Lie 子群) 若包含映射 $H\overset{i}\hookrightarrow G$ 是 Lie 群同态, 则称 $H$ 是 $G$ 的 Lie 子群. 特别地, 
1. 常秩单射总是浸入, $H$ 总是 $G$ 的子流形; 
2. 若 $i$ 是嵌入, 则 $H$ 是 $G$ 的正则子流形. 

**P** Lie 子群作为正则子流形是闭的. 适应坐标表明正则子流形是局部闭的, 结合 Lie 群的平移同构, 正则 Lie 子群是闭的. 

**P** (Cartan 闭子群定理) 反之, Lie 群的任何闭子群是正则子流形, 从而是闭的 Lie 子群. 

例如取 $H$ 为 Lie 群 $G$ 的闭子群, 并记 $e=e_G=e_H$. 今考虑
$$
V:=\{X:\exp_e(X)\in H\}\subseteq T_eG.
$$
我们断言 $V$ 关于加法封闭, 因为对任意 $X,Y\in V$,
$$
\exp_e(X+Y)=\lim_{n\to\infty}(\exp_e(n^{-1}X)\exp_e(n^{-1}Y))^n\in H.
$$
显然 $V$ 关于 $\mathbb R$-数乘封闭, 从而是 $T_eG$ 的线性子空间. 下验证 $V$ 关于 Lie 括号封闭. 只需注意到
$$
\exp_e(\sqrt tX)\exp_e(\sqrt tY)\exp_e(-\sqrt tX)\exp_e(-\sqrt tY)
$$
在 $t=0$ 时的导数为 $[X,Y]$. 



**P** Lie 代数满同态的若干性质如下. 
1. 若 $\varphi :G\to H$ 对应的 Lie 代数同态是满的, 则 $\varphi (G)$ 是 $H$ 的连通分支. 实际上, 记 $\varphi$ 将原点处小开集映至 $H$ 原点附近的某一开集 $V$, $\bigcup_{n\geq 1}V^n$ 是开且闭的子集, 从而是(包含单位元的)连通分支. 
2. 作为推论, 若 $H$ 是连通 Lie 子群, 则 $\varphi:G\to H$ 是满射当且仅当 $\operatorname{Lie}(\varphi)$ 是 Lie 代数上的满射.

**D** (覆叠空间) 拓扑空间间的连续映射 $f:X\to Y$ 是覆叠的, 当且仅当 $f$ 是满射, 且对任意 $y\in Y$, 存在小开邻域 $U_y\subseteq Y$ 使得 $f^{-1}(U_y)\cong S\times U_{f^{-1}(x)}$, $S$ 是离散集. 

**P** (Lie 代数同态意味着连通分支的覆叠映射) 若 $H$ 连通, 则 $\varphi:G\to H$ 覆叠映射, 当且仅当 $\operatorname{Lie}(\varphi)$ 是 Lie 代数同构. 
1. 若 $\varphi :G\to H$ 是覆叠映射. 一方面, 覆叠映射是满射, 从而 Lie 代数同态是满的; 另一方面, $\varphi^{-1}(e_H)$ 是零维流形, 从而 $\ker\operatorname{Lie}(\varphi)=0$. 故 $\operatorname{Lie}(\varphi)$ 是 Lie 代数的同构.
2. 若 $\operatorname{Lie}(\varphi)$ 是 Lie 代数同构, 则 $\varphi$ 限制在 $e_G$ 的某个开集 $U_{e_G}$ 上是微分同胚. 再取 $V_{e_G}$ 使得 $V_{e_G}\cdot V_{e_G}^{-1}\subset V_{e_G}$, 从而 $\varphi^{-1}(\varphi(V_{e_G}))=\varphi^{-1}(e_H)\times V_{e_G}$. 

