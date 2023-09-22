Q: 若 $x,y,z$ 是至多有一个为 $0$ 的非负实数, 证明: $\sqrt{\dfrac{x^2+8yz}{y^2+z^2}}+\sqrt{\dfrac{y^2+8zx}{z^2+x^2}}+\sqrt{\dfrac{z^2+8xy}{x^2+y^2}}\geqslant 4$. 

***

A: 不妨设 $x\geq y\geq z$, 则

$$
\sqrt{\dfrac{x^2+8yz}{y^2+z^2}}+\sqrt{\dfrac{y^2+8zx}{z^2+x^2}}+\sqrt{\dfrac{z^2+8xy}{x^2+y^2}}\geq \sqrt{\dfrac{x^2+8z^2}{y^2+z^2}}+\sqrt{\dfrac{y^2+z^2}{8z^2+x^2}}+\sqrt{\dfrac{8xy}{x^2+y^2}}.
$$
然后证明对 $0<\alpha\leq 0.8$ 总有
$$
\sqrt{\dfrac{x^2+8z^2}{y^2+z^2}}+\sqrt{\dfrac{y^2+z^2}{x^2+8z^2}}\geq (x/y)^\alpha+(y/x)^\alpha.
$$
等价地, 证明 $\dfrac{x^2+8z^2}{y^2+z^2}\geq (x^2/y^2)^\alpha$ 即可. 分别取左式 $\dfrac{x^2+8y^2}{2y^2}$ 与 $\dfrac{x^2}{y^2}$, 不等式显然. 

回到原式, 只需证明存在 $0<\alpha \leq 0.8$ 使得
$$
(x/y)^\alpha+(y/x)^\alpha+\sqrt{\dfrac{8xy}{x^2+y^2}}\geq 4.
$$
记 $t=x/y\geq 1$, 下证明 $f_\alpha(t):=t^\alpha+t^{-\alpha}+\sqrt{8/(t+t^{-1})}\geq 4$. 分析单调性知, 只需证明 $f_\alpha''(1)>0$ 即可. 此时 $2\alpha^2-1>0$, 即, $\alpha > 1/\sqrt 2$. 

> 依照[延申阅读](https://approach0.xyz/search/?q=OR%20content%3A%24%5Csqrt%7B%5Cdfrac%7Bx%5E2%2B8yz%7D%7By%5E2%2Bz%5E2%7D%7D%2B%5Csqrt%7B%5Cdfrac%7By%5E2%2B8zx%7D%7Bz%5E2%2Bx%5E2%7D%7D%2B%5Csqrt%7B%5Cdfrac%7Bz%5E2%2B8xy%7D%7Bx%5E2%2By%5E2%7D%7D%5Cgeqslant%204%24&p=1)中的几个特例, 不难发现对 $k\geq 1$ 总有
> $$
> \sqrt{\dfrac{x^2+kyz}{y^2+z^2}}+\sqrt{\dfrac{y^2+kzx}{z^2+x^2}}+\sqrt{\dfrac{z^2+kxy}{x^2+y^2}}\geqslant \min \left(2+\sqrt{\dfrac k2},3\sqrt[3]{\dfrac{k}{4}}\right).
> $$

