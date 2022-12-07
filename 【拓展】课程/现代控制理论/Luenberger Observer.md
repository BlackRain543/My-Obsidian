**龙伯格观测器:** PLL

Stability is classical control



observer gain matrix：$L$

---
##### Key：
$$
\hat{x}(k+1)
=
A\hat{x}(k)+Bu(k)+L[y(k)-C \hat{x}(k)-Du(k)]
$$
##### State estimation error vector：状态估计误差向量
$$
e(k) = x(k) - \hat{x}(k)
$$
##### Error dynamics：动态误差
$$
e(k+1) = (A - LC)e(k)
$$

$$
eig(A-LC)=eig_{designed}
$$



