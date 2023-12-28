# 辛形式初步

## 反对称双线性型

**D** (反对称双线性型) 记 $V$ 为 $m$-维 $\mathbb R$-线性空间. 称 $\Omega$ 是反对称的, 当且仅当
$$
\Omega (u,v)=-\Omega(v,u)\quad (\forall u,v\in V).
$$

**P** (Gram-Schmidt 正交化) 对线性空间 $V$ 与反对称双线性映射 $\Omega$, 存在 $V$ 的一组基
$$
\{e_i\}_{i=1}^n\cup \{f_i\}_{i=1}^n\cup\{u_i\}_{i=1}^k\quad (2n+k=m),
$$
满足
1. $\Omega(e_i,f_j)=\delta_{i,j}$,
2. $\Omega(e_i,e_j)=0=\Omega(f_i,f_j)$,
3. $\Omega(u_i,-):V\to \{0\}$. 

此时 $\Omega$ 对应矩阵
$$
\Omega(u,v)\mapsto 
u^T
\begin{pmatrix}
O_{k\times k}&O_{k\times n}&O_{k\times n}\\
O_{n\times k}&O_{n\times n}&I_{n\times n}\\
O_{n\times k}&-I_{n\times n}&O_{n\times n}
\end{pmatrix}
v.
$$

**D** (非退化反双线性型, 辛空间) 若对任意 $v\in V$, $\Omega(v,-)$ 的像均为 $\mathbb R$, 则称 $(V,\Omega)$ 是非退化的. 此时的矩阵形式为
$$
\begin{pmatrix}O&I\\-I&0\end{pmatrix}.
$$
记 $(V,\Omega)$ 为辛线性空间. 

**D** (特殊子空间) 对 $V$ 的子空间 $W$, 称

* $W$ 是辛子空间, 若 $(W,\Omega|_W)$ 是非退化的;
* $W$ 是迷向的, 若 $\Omega|_W$ 是零映射.  

**D** (零化子) 给定辛线性空间 $(V,\Omega)$, 任意线性子空间 $W\subset V$ 的零化子为线性空间
$$
W^\Omega:=\{u\in V:\Omega(u,-):W\to 0\}.
$$

**P** (零化子的维度) 辛子空间 $W\subseteq V$ 的零化子维度为 $\dim V-\dim W$. 对以下满射考虑第一同构定理即可
$$
T:V\to \mathrm{Hom}(W,\mathbb R),\quad v\mapsto \Omega (v,-).
$$

**P** (零化子作为对偶) 考虑维数定理, 则 $(W^\Omega)^\Omega=W$. 

**P** (辛子空间的等价刻画) 辛线性空间 $(V,\Omega)$ 的子空间 $W$ 是辛子空间, 等且仅当以下等价命题成立

1. $(W,\Omega|_{W\times W})$ 是辛线性空间;
2. $W\cap W^\Omega =\{0\}$, 即, $W\oplus W^\Omega =V$. 

**D** (迷向, 余迷向) 对辛线性空间 $(V,\Omega)$, 取 $W\subseteq V$, 

* 称 $W$ 是迷向的, 若 $W\subseteq W^\Omega$;
* 称 $W$ 是余迷向的,若 $W^\Omega\subseteq W$.

**P** 给定辛空间, 则迷向空间对应余迷向的零化子. 特别地, 一维子空间是迷向的, 余一维子空间是余迷向的. 

**D** (Lagrangian 子空间) 迷向且余迷向的子空间, 即, $\frac{\dim V}{2}$ 维子空间 $W=W^\Omega$. 

**P** lagrangian 子空间总是存在, 例如取辛线性空间标准基的所有 $\{e_i\}$ 或所有 $\{f_i\}$. 反之, Lagrangian 子空间的任意一组基可作为 $\{e_i\}$ 扩充至全空间. 

特别地, 对辛线性空间 $(V,\Omega)$ 与 Lagrangian 子空间 $W\subseteq V$​, 总有以下同构
$$
(V,\Omega)\to (W\oplus W^\ast,\Omega_0),\quad \Omega_0((u, \alpha),(v,\beta)):= \beta(u)-\alpha(v).
$$

**P** 对偶空间作为平凡丛具有的典范辛结构. 取有限维线性空间 $V$ 及其对偶空间 $V^\ast$, 存在典范辛形式
$$
\Omega:(V\oplus V^\ast)\times (V\oplus V^\ast)\to \mathbb R,\quad ((u,\alpha),(v,\beta))\mapsto \beta(u)-\alpha(v).
$$
取 $V$ 的基 $\{e_\lambda\}_{\lambda\in \Lambda}$ 以及 $V^\ast$ 的基 $\{f_\lambda\}_{\lambda}$, 则 $V\oplus V^\ast$ 的基写作 
$$
\{(e_\lambda,0)\}_{\lambda\in \Lambda}\cup\{(0,f_\lambda)\}_{\lambda\in \Lambda}.
$$

**D** (辛同态) 称 $\varphi: (V,\Omega)\to (V^\prime,\Omega^\prime)$ 是辛同态, 当且仅当 $\varphi:V\to V^\prime$ 是线性映射, 且
$$
\Omega(u,v)=\Omega(\varphi (u),\varphi(v))\quad (\forall u,v\in V).
$$

## 辛流形

**D** (流形上的辛形式) 称 $\omega\in \mathscr A^2(M)$ 是辛形式, 若 $\operatorname d\omega =0$ 且
$$
\omega_p:T_pM\times T_pM\to \mathbb R
$$
是非退化反对称双线性形.

**P** 辛流形是偶数维且可定向的, 这是因为辛形式 $\omega$ 诱导了体积形式 $\omega ^n$, 其中 $2n$ 是流形维度; 

**P** (紧致辛流形的 $2k$ 阶同调群非平凡) 若 $(M,\omega)$ 是 $2n$-维紧致辛流形, 则依照 Stocks 公式有 
$$
[0]\neq [\omega^n]\in H_{dR}^{2n}\neq 0.
$$
此时 $[\omega]\neq [0]$; 若不然, 记 $\omega=\operatorname{d}\eta$, 则 
$$
n!\operatorname{Vol}(M)=\int_{M}\operatorname{d}\eta\wedge\omega^{n-1}=\int_{\partial M}\eta\wedge\omega^{n-1}=0.
$$
因此对一切 $1\leq k\leq n$, $[0]\neq [\omega^k]\in H_{dR}^{2k}\neq 0$.

**D** (流形间的辛同态) 称 $\varphi :(M_1,\omega_1)\to (M_2,\omega_2)$ 是辛同态, 若 $\varphi :M_1\to M_2$ 是可微的, 且 $\varphi ^\ast \omega_2=\omega_1$. 此处
$$
(\varphi^\ast \omega_2)_p(u_p,v_p)=(\omega_2)_{\varphi(p)}(\operatorname d\varphi_p(u_p),\operatorname d\varphi_p(v_p))\quad (\forall u_p,v_p\in T_pM_1).
$$

## 余切丛的典范辛结构

**P** (余切丛) 余切丛是辛流形, 其辛形式为 Liouville $1$-形式的外微分(的相反数). 遵循约定取
$$
\omega :=-\operatorname{d}\pi^\ast (\eta_i\operatorname{d}x^i)=-\pi^\ast (\operatorname{d}(\eta_i\operatorname{d}x^i))=\operatorname{d}x^i\wedge\operatorname{d}\eta_i. 
$$

流形间可微映射保持 Liouville $1$-形式 $\pi^\ast (\eta_i\operatorname{d}x^i)$ 的拉回, 其诱导的余切丛间的同态是辛同态. 

**D** (Liouville 形式) 对 $n$ 维流形 $M$ 与切丛 $T^\ast M$ 定义
1. Liouville $1$-形式 $\alpha:=\pi^\ast (\eta_i\operatorname{d}x^i)$ 是 $T^\ast M$ 上的 $1$-形式;
2. Liouville $2$-形式 $\omega:=-\operatorname{d}\alpha$ 是 $T^\ast M$ 上的辛形式; 
3. Liouville 体积形式 $\frac 1{n!}\omega^n=\bigwedge_{i=1}^n(\operatorname{d}x^i\wedge\operatorname{d}\eta_i)$ 是非退化体积形式. 

**P** (Liouville $1$-形式的泛性质) 先前已证明, 余切丛 $T^\ast M$ 上的 Liouville $1$-形式 $\alpha$ 将任意 $1$-形式的拉回 $\mu^\ast:T^\ast (T^\ast M)\to T^\ast M$ 对应作 $\mu: M\to T^\ast M$ 其本身, 即, $\mu^\ast \alpha =\mu$. 

记顿范畴 $(\operatorname{Man}^\infty/M)$, 其对象是 $N\xrightarrow{f}M$, 态射即拉回
$$
\begin{matrix}
 & N_{1} & \xrightarrow{f_{1}} & M\\
\varphi  & \downarrow  & \circlearrowright  & \parallel \\
 & N_{2} & \xrightarrow[f_{2}]{} & M\\
. &  &  & 
\end{matrix}
$$
考虑反变函子
$$
F:(\operatorname{Man}^\infty/M)\to \mathbb R\operatorname{Vect}
$$
其中, $F(N\xrightarrow{f} M)=f^\ast\mathscr A^1(M)=C^{\infty}(N)\otimes_{C^\infty(M)}\mathscr A^1(M)$. 遂有
$$
\begin{matrix}
 & N & \xrightarrow{f} & M &  & f^{\ast }\mathscr{A}^{1}( M) & \\[6pt]
\varphi  & \downarrow  & \circlearrowright  & \parallel  & \xrightarrow{F} & \uparrow  & \varphi ^{\ast }\\[6pt]
 & T^{\ast } M & \xrightarrow[\pi ]{} & M &  & \pi ^{\ast }\mathscr{A}^{1}( M) & \\[6pt]
 .
\end{matrix}
$$
我们断言 $F$ 是可表函子. 实际上, 有相等的集合
$$
\operatorname{Hom}_{\operatorname{Man}^\infty/X}\left(\begin{matrix}
 & N &  & T^\ast M & \\
f & \downarrow  & , & \downarrow  & \pi \\
 & M &  & M & 
\end{matrix}\right)=\left\{\varphi :\begin{matrix}
 & N & \xrightarrow{\varphi } & T^\ast M & \\
f & \downarrow  & \circlearrowright  & \downarrow  & \pi \\
 & M & = & M & 
\end{matrix}\right\}.
$$
$F(-)\cong \operatorname{Hom}(-,\pi)$ 的(反变)自然性由拉回的自然性给出. Liouville $1$-形式 $\alpha$ 即 $\operatorname{id}_{\pi}$ 在自然同构下的像, 其泛性质说明如下: 对任意 $f^\ast\eta\in f^\ast \mathscr A^1(M)\subseteq \mathscr A^1(N)$, 存在唯一的 $\varphi :N\to T^\ast M$ 使得 $\varphi^\ast\alpha= f^\ast\eta$. 

**D** (Lagrangian 子流形) 称 $S$ 是 $(M,\omega)$ 的 Lagrangian 子流形, 当且仅当
1. $i_0:S\hookrightarrow M$ 是闭子流形; 
2. $(\iota_0)_\ast:TS\to TM$ 在每一点处是 Lagrangian 子空间向辛空间的嵌入. 

**P** (Lagrangian 子流形判定法则) $\iota_0:S\hookrightarrow(M,\omega)$ 是 Lagrangian 子流形当且仅当对任意 $X,Y\in TS$ 均有
$$
((\iota_0)^\ast \omega )(X,Y)=\omega((\iota_0)_\ast X,(\iota_0)_\ast Y)=0.
$$
当且仅当 $(\iota_0)^\ast \omega =0$. 

**P** (截面作为 Lagrangian 子流形) 考虑 $M$ 上 $1$-次微分形式 $\mu\in \mathscr A^1(M)$, 记截面 $S_\mu =\{(p,\mu_p):p\in M\}\in \Gamma(T^\ast M)$, 则有流形间同构 
$$
\psi_\mu:M\xrightarrow{\sim} S_\mu,p\mapsto (p,\mu_p).
$$
记嵌入 $\iota_\mu:S_\mu\to T^\ast M, p\mapsto (p,\mu_p)$. 因此 $S_\mu$ 是 Lagrangian 子流形当且仅当
$$
\begin{align*}
0&=(\iota_0)^\ast \operatorname{d}\alpha\\[6pt]
&=(\pi\circ \iota_0)^\ast\operatorname{d} (\eta_i\operatorname{d} x^i)\\[6pt]
&=\operatorname{d}((\pi\circ \iota_0)^\ast (\eta_i\operatorname{d} x^i))\\[6pt]
&=\operatorname{d}(\psi_\mu^\ast (\eta_i\operatorname{d} x^i))\\[6pt]
&=\operatorname{d}\mu.
\end{align*}
$$
这表明, $S_\mu\in \Gamma(T^\ast M)$ 是 Lagrangian 子流形当且仅当 $\mu$ 是闭形式. 

**P** (微分同胚的辛同构判别法) 给定 $2n$-维辛流形间的微分同胚 $\varphi :M_1\xrightarrow{\sim}M_2$, 则 $\varphi^\ast \omega_2=\omega_1$ 当且仅当图像
$$
\operatorname{Graph}(\varphi):\{(p,\varphi (p)):p\in M_1\}\subseteq M_1\times M_2
$$
是辛流形
$$
(M_1\times M_2,p_1^\ast \omega_1-p_2^\ast \omega _2)
$$
的 Lagrangian 子流形. 考虑嵌入
$$
i_0:M_1\cong \operatorname{Graph}(\varphi)\to M_1\times M_2,p\mapsto (p,\varphi (p))
$$
则 $\operatorname{Graph}(\varphi)$ 是 Lagrangian 子流形当且仅当
$$
\begin{align*}
0&=i_0^\ast (p_1^\ast \omega_1-p_2^\ast \omega _2)\\[6pt]
&= (p_1\circ i_0)^\ast \omega_1-(p_2\circ i_0)^\ast \omega_2\\[6pt]
&= \omega_1-\varphi^\ast \omega_2.
\end{align*}
$$


**P** 法丛是 Lagrangian 子流形. 对正则子流形 $i_0:S\hookrightarrow M$, 考虑 $\iota:N^\ast S\to T^\ast M$, 则在适应坐标下, $N^\ast S$ 的坐标形如
$$
(x^1,\ldots,x^k,0,\ldots,0,\eta_{k+1},\ldots,\eta_n).
$$
显然有 $\iota^\ast \alpha =0$. 

## 切触形式
**D** (局部切触结构, 局部切触形式, 切触流形) 给定 $2n+1$ 维流形 $M$ 与其上秩为 $2n$ 的向量场 $H$. 称 $(M,H)$ 为切触流形, 当且仅当存在 $\alpha\in \mathscr A^1(M)$ 使得
1. $\ker[\alpha_p:T_pM\to \mathbb R]=H_p$;
2. $\operatorname{d}\alpha$ 是辛形式. 

**D** (整体切触结构, 整体切触形式) 若局部切触结构 $(M,H,\alpha)$ 上有体积形式 $\alpha\wedge(\operatorname{d}\alpha)^n$, 则称 $(M,H,\alpha)$ 是一个整体切触结构, $\alpha$ 是整体切触形式. 称 $\alpha$ 为切触流形 $(M,H)$ 对应的局部切触形式, $(M,H,\alpha)$ 为一个局部切触结构. 

**P** (切空间的直和分解) 给定局部切触结构 $(M,H,\alpha)$, 辛形式 $\operatorname{d}\alpha$ 在每一 $2n+1$ 维切空间 $T_pM$ 上有 $2n$ 维非消失空间 $H_p$. 而奇数维反对称线性型总有零空间, 故有直和分解
$$
T_pM=\ker\alpha_p\oplus \ker \operatorname{d}\alpha_p.
$$

**P** 给定整体切触结构 $(M,H,\alpha)$, 则对任意局部切触结构 $\alpha^\prime$, $(M,H,\alpha^\prime)$ 仍是整体切触结构. 这是因为 $\alpha$ 与 $\alpha^\prime$ 相差一个非零连续函数的数乘. 

**P** (切触形式的辛形式化)


## Moser 方程, Darboux 定理


