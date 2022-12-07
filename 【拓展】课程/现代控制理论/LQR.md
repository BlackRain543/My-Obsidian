LQR 线性二次规划器【Linear Quadratic Regulator】

倒立摆：

开环：

闭环:


$$ 
\begin{bmatrix} \dot x_1 \\ \dot x_2 \end{bmatrix} 
=
\begin{bmatrix} x_1 & 0 \\ 0 & x_2 \end{bmatrix} 
$$


LQR（Linear-Quadratic Regulator，线性二次型调节器）算法是一种常用的控制算法，用于设计满足线性和二次型限制条件的最优控制器。下面是LQR算法的推导过程：

1.  设定线性系统的状态转移方程为：

$$\dot{x}(t)=Ax(t)+Bu(t)$$

其中，$x(t)$表示系统的状态向量，$u(t)$表示控制输入，$A$和$B$是常数矩阵。

2.  设定控制器的结构为：

$$u(t)=-Kx(t)$$

其中，$K$是控制器的参数矩阵。

3.  根据状态转移方程和控制器的结构，得到系统的状态方程：

$$\dot{x}(t)=(A-BK)x(t)$$

4.  设定控制目标为：

$$J=\int_{0}^{\infty}[x(t)^TQx(t)+u(t)^TRu(t)]dt$$

其中，$Q$和$R$是正定矩阵，表示状态和控制输入的权重。

5.  对控制目标进行拉格朗日变换，得到对偶问题：

$$\min_{K}J_{LQR}=\min_{K}\max_{x,u}[x(t)^{TQ} ...$$$$