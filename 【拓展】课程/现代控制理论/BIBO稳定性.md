**有界输入有界输出稳定性**

Bounded Input Bounded Output
Continuous time：连续时间

零状态响应的稳定性：

Transfor function：
$$
H(z)=C(ZI-A)^{-1}B+D
$$

内稳定一定外稳定，反之不成立：

$$
\begin{aligned}
det(\lambda I - A) &= 0 \\

&=
(\lambda - \lambda_1)
(\lambda - \lambda_2)
...
(\lambda - \lambda_n)
\end{aligned}
$$

判断BIBO：check H(z)