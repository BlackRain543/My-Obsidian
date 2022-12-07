### Probability Space【概率空间】
* Sampling space$\Omega$：
* Event space$F$：
* Probability measure$P$：


### Conditional probability【条件概率】
$$
P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(B | A)P(A)}{P(B)}
$$

* Random Variables【随机变量】
* Random Vectors【随机矢量】


$$
\begin{aligned}
E(AX) &= AE(X) \\
E(X)  &= \sum_x x \cdot Prob(X = x)
\end{aligned}
$$








卡尔曼滤波是一种用于处理随机过程的技术，用于估计随机变量的最优线性估计。它是根据线性最小均方估计理论推导出来的。

线性最小均方估计理论是一种用于计算最优线性估计的技术。它通过对系统进行线性化，并对每个随机变量建立一个线性模型来实现估计。

假设有一个随机变量 $x$，它的最优线性估计为 $\hat{x}$。通过线性最小均方估计理论，我们可以写出以下方程来描述 $\hat{x}$：

$$ \hat{x} = E[x] + K(y - E[x]) $$

其中，$E[x]$ 表示随机变量 $x$ 的期望值，$K$ 表示卡尔曼增益，$y$ 表示观测值。

通过解析上述方程，我们可以得出卡尔曼滤波的推导过程。首先，我们需要对随机变量 $x$ 进行线性化，并建立一个线性模型来描述它的变化。然后，我们可以通过计算随机变量 $x$ 的期望值 $E[x]$，以及观测值 $y$，来计算卡尔曼增益 $K$。最后，我们可以通过将 $E[x]$ 与 $K$ 相乘
