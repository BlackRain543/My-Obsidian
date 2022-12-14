### 1.Probability Space【概率空间】
---
* Sampling space$\Omega$：
* Event space$F$：
* Probability measure$P$：


### 2.Conditional probability【条件概率】
---
$$
P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(B | A)P(A)}{P(B)}
$$

* Random Variables【随机变量】
* Random Vectors【随机矢量】

$$
\begin{aligned}
E(AX) &= AE(X) \\
E(X)  &= \varSigma_x x \cdot Prob(X = x)
\end{aligned}
$$

### 3.MMSE: Minimum Mean Squared Estimation
---

最小均方差估计：
$$
X_{MMSE}= \varPhi_{MMSE}(y)=E(X|Y=y)
$$

$$
E(||\varPhi(Y)-X||^2)
$$

### 4.Gaussian Random Vectors
---
1D Gaussian: $X - N(\mu, \sigma)$

$$
f_x\left( x \right) =\frac{1}{\sqrt{2\pi \sigma ^2}}e^{-\frac{\left( x-\mu \right) ^2}{2\sigma ^2}}
$$

* ##### Fact 1: Independence between two Gaussians
$$
\begin{align*}
E(XX^{T})&= E(X) \cdot E(Y)^{T}\\\\
Cov(X,Y) &= 0
\end{align*}
$$
* ##### Fact 2: Affine transformation of Gaussian is still Gaussian
$$
Z=AX+b - N(A\mu + b,A \varSigma {A^T})
$$
* ##### Fact 3: Conditional Gaussian is Gaussian
$$
\begin{bmatrix}X  \\  y\end{bmatrix} - N
(\begin{bmatrix}u_{X} \\ u_{Y}\end{bmatrix},
\begin{bmatrix} \varSigma _{X} & \varSigma _{XY} \\ \varSigma _{YX} & \varSigma _{Y}\end{bmatrix})
$$
Hence,

$$
\begin{align*}
\mu_{X|Y=y}  &= \mu_{X} + \varSigma _{XY} \varSigma _{Y}^{-1}(y-\mu_Y)\\
\varSigma _{X|Y=y} &= \varSigma _{X} - \varSigma _{XY} \varSigma _{Y}^{-1}\varSigma _{YX}
\end{align*}
$$

### 5. Kalman Filter Derivations
---
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

##### State estimation problem: Find the MMSE of $x_k$ given $Y_k$

$$
\begin{align*}
\hat{x}_{k|k} &= E(x_k|Y_k)\\
\hat{x}_{k|k-1} &= E(x_k|Y_k-1)\\
P_{(k|k)}&=  E((x_{k}- \hat{x}_{k|k})(x_{k}- \hat{x}_{k|k})^T|Y_{k})\\
P_{(k|k-1)}&=  E((x_{k}- \hat{x}_{k|k-1})(x_{k}- \hat{x}_{k|k-1})^T|Y_{k-1})
\end{align*}
$$


##### Goal of Kalman Filter: obtain recursive formula
$$
\begin{bmatrix} \hat x_{k }   \\ P_{k}\end{bmatrix} --->
\begin{bmatrix} \hat x_{k+1}   \\ P_{k+1}\end{bmatrix} 
$$

$E(x_{k}|Y_{k})$与$Cov(x_k,x_{k}|Y_{k})$

$\hat{x}_{0},P_{0}$，得

$\hat{x}_{k},P_{k}$与$\hat{x}_{k+1},P_{k+1}$

prediction -> measurement update
$\hat{x}_{k|k} ==> \hat{x}_{k+1|k} ==> \hat{x}_{k+1|k+1}$
$\hat{P}_{k|k} ==> \hat{P}_{k+1|k} ==> \hat{P}_{k+1|k+1}$