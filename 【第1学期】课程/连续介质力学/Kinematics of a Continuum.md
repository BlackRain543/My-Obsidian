# 连续介质运动学

**Particle: ** 粒子

在粒子运动学中，粒子的路径线由时间t的矢量函数描述：$r=r(t)$

$\Theta,v,T$: 温度、速度、张量描述

$X$: 起点位置
$x$: 终点位置

刚体旋转：$v=w \times x$
$$
dx \cdot dx = (ds)^2
$$

$$
sin(\beta) = \frac{dx^{(1)} dx^{(2)}}{ds_1 ds_2}
$$
##### 位移场：
$u_1=x_1-X_1$
$u_2=x_2-X_2$
$u_3=x_3-X_3$

### 运动学方程：
##### （1）刚体平移：
$$
x = X + c(t)
$$
##### （2）刚体绕固定点旋转：
$$
x-b = R(t)(X-b)
$$
##### （3）一般刚体运动：
$$
x= R(t)(X-b) + c(t)
$$

### 微小形变：
##### 应变张量：
$$
[\nabla u]=
\begin{bmatrix}
	\frac{\partial u_1}{\partial X_1} & 
	\frac{\partial u_1}{\partial X_2} & 
	\frac{\partial u_1}{\partial X_3}\\
	\frac{\partial u_2}{\partial X_1} & 
	\frac{\partial u_2}{\partial X_2} & 
	\frac{\partial u_2}{\partial X_3}\\
	\frac{\partial u_3}{\partial X_1} & 
	\frac{\partial u_3}{\partial X_2} & 
	\frac{\partial u_3}{\partial X_3}\\
\end{bmatrix}
$$

$$
E=\frac{1}{2}[\nabla u + (\nabla u)^T]
$$

$$d\boldsymbol X^{(1)}=dX^{(1)}e_1$$

##### 主应变：
$$
[E_n]=
\begin{bmatrix}
	E_1 & 0 & 0 \\
	0 & E_2 & 0 \\
	0 & 0 & E_3 \\
\end{bmatrix}
$$

##### 速度梯度：
$$
\begin{aligned}
\nabla v &= D + W \\
D &= \frac{1}{2}[(\nabla v) + (\nabla v)^T] \\
W &= \frac{1}{2}[(\nabla v) - (\nabla v)^T]
\end{aligned}
$$

##### 变形梯度(Deformation  gradient)：
$F=\frac{\partial x_i}{\partial X_j}=RU$

##### Right STRETCH 张量：
$U=C^{\frac{1}{2}}$

##### Left STRETCH 张量：
$V=B^{\frac{1}{2}}=FR^T$

##### Right CAUCHY-GREEN 张量：
$C=F^TF=U^2$

##### Left CAUCHY-GREEN 张量：
$B=FF^T=V^2$

##### 旋转张量：
$R=FU^{-1}$

##### 拉格朗日应变张量：
$E^*=(C-I)/2$

##### 欧拉应变张量：
$e^*=\frac{1}{2}(I-B^{-1})$

##### 变形体积与初始体积之比：
$\frac{\Delta V}{\Delta V_o} = \sqrt{det(B)}$


$$
dA=dA_o(det\boldsymbol {F})(\boldsymbol {F}^{-1})^T\boldsymbol {n}_o
$$


$$
E = \frac{1}{2}(\nabla u + \nabla u^T)=\nabla u^S
$$


##### 加速度场：
$$
a_i = 
\frac{\partial v_i}{\partial t} + 
v_j \frac{\partial v_i}{\partial x_j}
$$

$$a_x = 
\frac{\partial v_x}{\partial t} + 
v_x \frac{\partial v_x}{\partial x} + 
v_y \frac{\partial v_x}{\partial y}$$
$$a_y = 
\frac{\partial v_y}{\partial t} + 
v_x \frac{\partial v_y}{\partial x} + 
v_y \frac{\partial v_y}{\partial y}$$


##### Pathline Equation：
$$
\int_{X}^{x} xdx = \int_{0}^{t} kdt
$$
$$
dx=FdX
$$
##### 归一化：
$$
e_1^2 + e_2^2 + e_3^2 = 1
$$


##### Compatibility Conditions(兼容性条件):
验证是否相等
$$
\frac{\partial^2 E_{11}}{\partial X_2^2}+
\frac{\partial^2 E_{22}}{\partial X_1^2}
=
2 \frac{\partial^2 E_{12}}{\partial X_1 X_2}
$$
$$
\frac{\partial^2 E_{22}}{\partial X_3^2}+
\frac{\partial^2 E_{33}}{\partial X_2^2}
=
2 \frac{\partial^2 E_{23}}{\partial X_2 X_3}
$$
$$
\frac{\partial^2 E_{33}}{\partial X_1^2}+
\frac{\partial^2 E_{11}}{\partial X_3^2}
=
2 \frac{\partial^2 E_{13}}{\partial X_1 X_3}
$$


**质量守恒：**
$$
\frac{\partial \rho} {\partial t} = \frac{\partial \rho v_i}{\partial x_i}
$$

**动量守恒：**
$$
\rho(\frac{\partial v_i} {\partial t} + \frac{\partial v_i} {\partial x_j}v_j)
=
\frac{\partial T_{ij}} {\partial x_j}
+ \rho b_i
$$

多选题：2 * 15（子标、矩阵）（30分）
证明题：2~3道（作业题）
计算题：4~5道（作业题）
