### Math 4423 Assignment 1
\* I submit as LaTeX for the bonus points XD

$Q1)$

$H_0: m = 5$

$H_1: m> 5$

$\alpha = 0.05$

$Sorted\space Statistics: 1,2,3,4,4,7,9,10,12,15$

$a)$ Sign Test

$S=\sum_{i=1}^{10}I\{X_i>m\}=5$ 

$S \sim Bin(10, \frac{1}{2})$

$\text{P-Value}$

$P(S\geq 5\mid H_0)$

$=P(Bin(10, \frac{1}{2})\geq5)$

$=\binom{10}{5}(\frac{1}{2})^{10}+\binom{10}{5}(\frac{1}{2})^{10}+\binom{10}{7}(\frac{1}{2})^{10}+\binom{10}{8}(\frac{1}{2})^{10}+\binom{10}{9}(\frac{1}{2})^{10}+\binom{10}{10}(\frac{1}{2})^{10}$

$=(\frac{1}{2})^{10}\times{(252+210+120+45+10+1)}$

$=0.623046875$

$\gt 0.05$

We do not have enough evidence to reject the null hypothesis

$b)$ Sign Test with Normal Approximation

$S=\sum_{i=1}^{10}I\{X_i>m\}=5$ 

$S \sim Bin(10, \frac{1}{2})$

$\text{By Central Limit Theorem:}$
$$\frac{S-np}{\sqrt{np(1-p)}}\to N(0,1)\space \text{for Large n}$$

$\text{P-Value}$

$P(S\geq 5\mid H_0)$

$=P(Bin(10, \frac{1}{2})\geq5)$

$\approx 1-\Phi(\frac{5+\frac{1}{2}-\frac{10}{2}}{\sqrt{10}/2})$

$\approx 1-\Phi(0.316227766)$

$\approx 0.1255$

$\gt 0.05$

We do not have enough evidence to reject the null hypothesis

$c)$ Wilxocon Sign Rank Text

| $X_i$                      | $X_1$           | $X_2$           | $X_3$           | $X_4$ | $X_5$           | $X_6$ | $X_7$           | $X_8$           | $X_9$ | $X_{10}$ |
|--------------------------|---------------|---------------|---------------|-----|---------------|-----|---------------|---------------|-----|--------|
| obs                      | 3             | 4             | 7             | 10  | 4             | 12  | 1             | 9             | 2   | 15     |
| $X_i-m_0$                  | -2            | 1             | 2             | 5   | -1            | 7   | -4            | 4             | -3  | 10     |
| $\text{abs of }{X_i-m_0}$            | 2             | 1             | 2             | 5   | 1             | 7   | 4             | 4             | 3   | 10     |
| $\text{R of } X_i-m_0$     | $\frac{3+4}{2}$ | $\frac{1+2}{2}$ | $\frac{3+4}{2}$ | 8   | $\frac{1+2}{2}$ | 9   | $\frac{6+7}{2}$ | $\frac{6+7}{2}$ | 5   | 10     |
| $\text{Signs of } X_i-m_0$ | -             | +             | +             | +   | -             | +   | -             | +             | -   | +      |
| $R_i$                      | -3.5          | 1.5           | 3.5           | 8   | -1.5          | 9   | -6.5          | 6.5           | -5  | 10     |



$W+=\sum_{i=1}^{10}R_iI_i$

$=1.5+3.5+8+9+6.5+10$

$=38.5$

$W-=3.5+1.5+6.5+5$

$=16.5$

By looking up the table: We know that the critical value is 10 when n=10, $\alpha$=0.05

$\because 16.5>10$

$\therefore$ We do not have enough evidence to reject the null hypothesis

$d)$ Wilxocon Sign Rank Test with Normal Approximation

$W=\sum_{i=1}^{10}R_iI_i$

$=1.5+3.5+8+9+6.5+10$

$=38.5$

$\text{P-Value}$

$P(W\geq 38.5)$

$\approx 1-\Phi(\frac{38.5-\frac{10(10+1)}{2}-0.5}{\sqrt{\frac{1}{24}(10)(10+1)(2\times10+1)}})$

$\approx0.6423\gt0.05$

$\therefore$ We do not have enough evidence to reject the null hypothesis

$e)$ Parametric t-test

We Assume the data follows Normal Distribution

$X_1..X_{10} \sim i.i.d\space N(\mu, \sigma ^ 2)$

$H_0: m = 5$

$H_1: m> 5$

$\text{T-Statistics}$

$$T=\frac{\sqrt{n}(\bar{X}-5)}{\sigma}$$

$$\hat{\sigma}=\sqrt{\frac{1}{n-1}\sum{(X_i-\bar{X})^2}}$$

$t_{obs}=\frac{\sqrt{10}(6.7-5)}{4.667856991}=1.151678818$

$T\sim t(n-1)\sim t(9)$

$\text{P-Value}$

$P(T\geq1.1517)$

$\approx 0.13956$

$\gt0.05$

$\therefore$ We do not have enough evidence to reject the null hypothesis

$f)$ Yes, five approaches reach the same conclusion of not rejecting the null hypothesis of the median being 5 among the population

$Q2)$ Exact Distribution of Wilcoxon Sign Rank Test

| n=5            |   |   |   |   |   | W  | Prob |
|----------------|---|---|---|---|---|----|------|
| signs of $R_i$ | 1 | 2 | 3 | 4 | 5 |    |      |
|                | + | + | + | + | + | 15 | 1/32 |
|                | - | + | + | + | + | 14 | 1/32 |
|                | + | - | + | + | + | 13 | 1/32 |
|                | - | - | + | + | + | 12 | 1/32 |
|                | + | + | - | + | + | 12 | 1/32 |
|                | - | + | - | + | + | 11 | 1/32 |
|                | + | - | - | + | + | 10 | 1/32 |
|                | - | - | - | + | + | 9  | 1/32 |
|                | + | + | + | - | + | 11 | 1/32 |
|                | - | + | + | - | + | 10 | 1/32 |
|                | + | - | + | - | + | 9  | 1/32 |
|                | - | - | + | - | + | 8  | 1/32 |
|                | + | + | - | - | + | 8  | 1/32 |
|                | - | + | - | - | + | 7  | 1/32 |
|                | + | - | - | - | + | 6  | 1/32 |
|                | - | - | - | - | + | 5  | 1/32 |
|                | + | + | + | + | - | 10 | 1/32 |
|                | - | + | + | + | - | 9  | 1/32 |
|                | + | - | + | + | - | 8  | 1/32 |
|                | - | - | + | + | - | 7  | 1/32 |
|                | + | + | - | + | - | 7  | 1/32 |
|                | - | + | - | + | - | 6  | 1/32 |
|                | + | - | - | + | - | 5  | 1/32 |
|                | - | - | - | + | - | 4  | 1/32 |
|                | + | + | + | - | - | 6  | 1/32 |
|                | - | + | + | - | - | 5  | 1/32 |
|                | + | - | + | - | - | 4  | 1/32 |
|                | - | - | + | - | - | 3  | 1/32 |
|                | + | + | - | - | - | 3  | 1/32 |
|                | - | + | - | - | - | 2  | 1/32 |
|                | + | - | - | - | - | 1  | 1/32 |
|                | - | - | - | - | - | 0  | 1/32 |

From the Derived Exact Distribution:

$P(W\leq3)=5/32=0.15625$

$P(W\geq8)=16/32=0.5$

$Q3)$
| Statistics ||||||
|-------|------|------|------|------|------|
| X     | 17.2 | 21.6 | 19.5 | 19.0 | 22.0 |
| Y     | 18.3 | 20.8 | 20.9 | 21.2 | 22.7 |
| Z=X-Y | -1.1 | 0.8  | -1.4 | -2.2 | -0.7 |

$a)$ By Order Statistics,

$\hat{m_0}=z_{(3)}=-1.1$

$P(S<K_{\alpha})=\frac{0.05}{2}-0.025$

$\sum_{i=0}^{k_{\alpha}-1}\binom{5}{i}=0.025$

$k_{\alpha}=1 \text{ is closest to 0.025}$

$\therefore \text{CI of median=}[z_{(1)}, z_{(5-1+1)}]=[-2.2, 0.8]$

$b)$ Hodgers-Lehmann estimator

$\hat{m_{HL}}=$ MD of all Walsh Average

Walsh Average for \{-2.2, -1.4, -1.1, -0.7, 0.8\}:

$\{-2.2, -1.8, -1.65, -1.45, -1.4, -1.25, -1.1, -1.05, 
-0.9, -0.7, -0.7, -0.3, -0.15, 0.05, 0.8\}$

$\hat{m_{HL}}=X_{(\frac{15+1}{2})}=X_{(8)}=-1.05$

By Tukey's method of CI

$P(W<K_{\alpha})=0.05/2$

when $k_{\alpha}$ is 1, it is closest to 0.025,

$\therefore$ the median 95\% CI is [-2.2, 0.8]