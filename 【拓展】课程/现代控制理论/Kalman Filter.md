### 1.Probability Space【概率空间】
* Sampling space$\Omega$：
* Event space$F$：
* Probability measure$P$：


### 2.Conditional probability【条件概率】
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

### 3.MMSE: Minimum Mean Squared Estimation
$$
X_{MMSE}= \varPhi_{MMSE}(y)=E(X|Y=y)
$$

### 4.Gaussian Random Vectors
1D Gaussian: $X - N(\mu, \sigma)$

$$
f_x\left( x \right) =\frac{1}{\sqrt{2\pi \sigma ^2}}e^{-\frac{\left( x-\mu \right) ^2}{2\sigma ^2}}
$$

* **Fact 1:** Independence between two Gaussians
$$
\begin{align*}
E(XX^{T})&= E(X) \cdot E(Y)^{T}\\\\
Cov(X,Y) &= 0
\end{align*}
$$
* **Fact 2:** Affine transformation of Gaussian is still Gaussian
$$
Z=AX+b - N(A\mu + b,A \sum\limits{A^T})
$$
* **Fact 3:** Conditional Gaussian is Gaussian
$$
\begin{bmatrix}X  \\  y\end{bmatrix} - N
(\begin{bmatrix}u_{X} \\ u_{Y}\end{bmatrix},
\begin{bmatrix} \sum_{X} & \sum_{XY} \\ \sum_{YX} & \sum_{Y}\end{bmatrix})
$$
Hence,
$$
\begin{align*}
\mu_{X|Y=y}  &= \mu_{X} + \sum_{XY} \sum_{Y}^{-1}(y-\mu_Y)\\
\sum_{X|Y=y} &= \sum_{X} - \sum_{XY} \sum_{Y}^{-1}\sum_{YX}
\end{align*}
$$


### 5. Kalman Filter Derivations
$$
\begin{align*}
x_{k+1} &= A_kx_k+B_ku_k+w_k\\
y_{k}&= C_kx_k+D_ku_k+v_k
\end{align*}
$$
$x_k$: System state at time k
$y_k$: measurement vector at time k
$Y_k$: collection of measurements up to time k

$u_k$: system input at time k (deterministic input)
$w_k$: process noise ~ $N(0,Q_k)$
$v_k$: measurement noise ~ $N(0,R_k)$





卡尔曼滤波是一种用于处理随机过程的技术，用于估计随机变量的最优线性估计。它是根据线性最小均方估计理论推导出来的。

线性最小均方估计理论是一种用于计算最优线性估计的技术。它通过对系统进行线性化，并对每个随机变量建立一个线性模型来实现估计。

假设有一个随机变量 $x$，它的最优线性估计为 $\hat{x}$。通过线性最小均方估计理论，我们可以写出以下方程来描述 $\hat{x}$：

$$ \hat{x} = E[x] + K(y - E[x]) $$

其中，$E[x]$ 表示随机变量 $x$ 的期望值，$K$ 表示卡尔曼增益，$y$ 表示观测值。

通过解析上述方程，我们可以得出卡尔曼滤波的推导过程。首先，我们需要对随机变量 $x$ 进行线性化，并建立一个线性模型来描述它的变化。然后，我们可以通过计算随机变量 $x$ 的期望值 $E[x]$，以及观测值 $y$，来计算卡尔曼增益 $K$。最后，我们可以通过将 $E[x]$ 与 $K$ 相乘
