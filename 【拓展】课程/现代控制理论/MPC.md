## MPC：模型预测控制
【Model Predictive Control】

Optimal Control ：在约束条件下达到最优系统表现



目标函数：
$$
J=\int_0^x (E^TQE+U^tRU)dt
$$

$$
\begin{aligned}
	\frac{d}{dt} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}
	&=
	A\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}
	+
	B\begin{bmatrix} u_1 \\ u_2 \end{bmatrix} 
	
	\\
	
	\begin{bmatrix} y_1 \\ y_2 \end{bmatrix}
	&=
	A\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}
\end{aligned}
$$

$$
E^TQE 
= 
\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}^T
\begin{bmatrix} q_1 & 0 \\ 0 & q_2 \end{bmatrix}
\begin{bmatrix} x_1 \\ x_2 \end{bmatrix}^T
=q_1x_1^2 + q_2x_2^2
$$

$$
U^TRU = r_1u_1^2 + r_2u_2^2
$$

$Q,R:$调节矩阵
$q_1,q_2,r_1,r_2:$权重系数

$$
X_{k+1}=AX_k + BU_k
$$

**步骤：**
在k时刻：
	step1：估计/测量当前系统状态
	step2：基于$u_k,u_{k+1},...,u_{k+n}$最优化
	step3：只施加$u_k$（滚动优化控制）


**推导：**

二次规划一般形式：
$$
min(Z^TQZ+C^TZ)
$$
最小二乘：
$$
q_1z_1^2+q_2z_2^2
$$

$$
X(k+1)=AX(k)+Bu(k)
$$

$u(k|k),u(k+1|k),u(k+2|k)，...，u(k+N-|k)$
预测区间

$x(k|k),x(k+1|k),x(k+2|k)，...，x(k+N|k)$

$$
X(k)=
\begin{bmatrix} 
x(k|k) \\ x(k+1|k) \\ x(k+2|k) \\ ... \\ x(k+N|k) 
\end{bmatrix}
$$
$$
U(k)=
\begin{bmatrix} 
u(k|k) \\ u(k+1|k) \\ u(k+2|k) \\ ... \\ u(k+N-1|k) 
\end{bmatrix}
$$


## Example：
$$
\begin{aligned}
x(k+1) & = Ax(k)+Bu(k) \\
\begin{bmatrix} x_1(k+1) \\ x_2(k+1) \end{bmatrix} 
& = 
\begin{bmatrix} 1 & 0.1 \\ 0 & 2 \end{bmatrix} 
\begin{bmatrix} x_1(k) \\ x_2(k) \end{bmatrix} 
+
\begin{bmatrix} 0 \\ 0.5 \end{bmatrix} 
u(k)
\end{aligned}
$$


$$
\begin{aligned}
	G&=M^T \bar Q M  \\
	E&=C^T \bar Q M  \\
	H&=C^T \bar Q C + \bar R
\end{aligned}
$$



MPC 算法（Model Predictive Control）是一种数学优化方法，可用来控制运动系统。它可以通过预测将来的输出，并计算当前应执行的控制动作，来优化长期的目标。

要用 C++ 代码实现 MPC 算法，首先需要了解其基本原理。MPC 通过对未来一段时间内系统的行为进行预测，并在满足一定限制条件的情况下，计算出当前时刻应执行的控制指令，以实现对系统进行优化。

实现 MPC 算法的 C++ 代码可能需要包含以下步骤：

1.  定义系统的状态变量和控制变量。
2.  建立系统的动力学模型，即系统的状态方程和输出方程。
3.  建立优化目标函数，并设定相应的限制条件。
4.  使用数学优化方法（如梯度下降法或非线性规划）求解优化问题，计算出当前时刻应执行的控制指令。
5.  将控制指令作为系统的输入，并根据系统的动力学模型更新状态变量。

在实际应用中，还可能需要进行更多的控制循环，以持续地优化系统