Q: 给定实数 $k>1$, 设 $0<a_1<1$, $a_{n+1}=a_n+\dfrac{a_n^k}{n^k}$, $n=1,2,3,\ldots$. 证明 $\{a_n\}$ 有下界.

Q: 置 $\dfrac{a_{n+1}}{a_n}=1+\dfrac{a_n^{k-1}}{n^k}$, 从而得
$$
a_{n+1}=a_1\cdot \prod_{1\leq k\leq n}\left(1+\dfrac{a_n^{k-1}}{n^k}\right)\leq a_1\exp\sum_{1\leq k\leq n}\dfrac{a_n^{k-1}}{n^k}.
$$
为证明 $a_n$ 之有界性, 只需证明 $a_n$ 的增长速率小于等于 $\mathcal O(n^{1-\varepsilon})$ 即可(存在给定的 $\varepsilon $). 既证 $a_n=\mathcal O(1)$ 和 $a_n=\mathcal O(n^{1-\varepsilon})$ 等价, **后面其实没必要写了. [知乎回答](https://www.zhihu.com/question/608732625/answer/3092157076)的思路已足够简单.** 

置 $a_1=1$, 则通解为 $a_n=n$. 根据单调性, 不难得出结论: 对 $a_1<a_1'<1$, 总有
$$
a_n<a_n'<n\qquad (\forall n\in \mathbb N_+).
$$
并且我们有理由相信, $\{(n,a_n)\}_{n\in \mathbb N_+}$ 的图像在某条凹曲线上(二阶导负). 并据此猜想 $a_n\leq n^{1-\varepsilon(a_1,k)}$, 其中 $\varepsilon (a_1,k)$ 是由 $a_1$ 与 $k$ 共同决定的小量, 且
$$
\begin{align*}
&\lim_{a_1\to 1^-}\varepsilon (a_1,k)=\lim_{k\to 0^+}\varepsilon(a_1,k)=0,\\[8pt]
&\lim_{a_1\to 0^+}\varepsilon (a_1,k)=\lim_{k\to +\infty}\varepsilon(a_1,k)=1.
\end{align*}
$$
显然 $n=1$ 时成立. 归纳假设为 $a_n\leq n^{1-\varepsilon}$, 从而
$$
a_{n+1}\leq n^{1-\varepsilon}+n^{-\varepsilon k}.
$$
为使得归纳假设成立, 则应有
$$
n^{-1-\varepsilon (k-1)}+1\leq (n+1)^{1-\varepsilon}. 
$$
我们希望 $(n+1)^{1-\varepsilon }\geq 1+n^{1-\varepsilon }$ 足以应付上界, 从而
$$
n^{-1-\varepsilon (k-1)}\leq n^{1-\varepsilon}, 
$$
即, $n^{2-2\varepsilon +\varepsilon k}\geq 1$. 到这里就显然了. 

