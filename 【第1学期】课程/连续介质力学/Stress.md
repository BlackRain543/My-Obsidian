$$
\begin{align*}
t &=   T \cdot n\\
T_{n} &=  n  \cdot t\\
T_{s} &= t - T_{n} \cdot n\\
T_{s} &= \sqrt{|t|^2-T_{n}^{2}}
\end{align*}
$$

$$
T=\left[ \begin{matrix}
	\sigma _x&		\tau _{xy}&		\tau _{xz}\\
	\tau _{yx}&		\sigma _y&		\tau _{yz}\\
	\tau _{zx}&		\tau _{zy}&		\sigma _z\\
\end{matrix} \right] 
$$

***The normal to the plane***：平面法线向量$n$
***Magnitude of shearing stress***：剪切应力$T_{s}$
***Normal stress***：法向应力，正应力$T_{n}$
***The stress vector on the plane***：平面上的应力矢量$t$

### Principle of moment of momentum:

应力分析：
$f_i(x,n) = f_i(x,e_j)n_j$

### Equilibrium Equations
平衡方程式：
$$
\frac{\partial T_{ij}}{\partial x_{j}} + \rho B_{i} = 0
$$


### Energy Equation


$$
\frac{D}{Dt} \int_{V_m}\rho dv = 0
$$




##### Balance of energy:
$$
\frac{d}{dt}\int{\rho dv \left( e+\frac{1}{2}v_iv_i \right)} =
\oint{f_iv_ida}+\int{\rho b_iv_idv}+\int{\rho dvR}+\oint{hda}
$$

##### Fourer's law:
$$
q_{i}= -k \frac{\partial \theta}{\partial x_i}
$$

$$
\begin{align*}
\hat{\rho} e + \rho v_{i} \hat{v_{i}} &= (T_{ij}v_i)_{ij} + \rho b_{i}v_{i}+ \rho R - q_i \\
(T_{ij}v_i)_{ij} &= v_{i} \frac{\partial T_{ij}}{\partial x_j}+ T_{ij} \frac{\partial v_i}{\partial x_j}
\end{align*}
$$


---

$$
T_{shear}^2=f_{i}f_{i}-(f \cdot n)^2
$$

---

$$
f=Tn=\lambda n
$$

---

##### 第二定律：
$$
\frac{d}{dt}\int{\rho \eta d\upsilon}\ge \int{\rho sd\upsilon}+\oint{\tilde{d}da}
$$


