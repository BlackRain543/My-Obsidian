(1)
$$
\begin{aligned}
	T(a+b) &= Ta + Tb \\
	T(\alpha a) &= \alpha T a
\end{aligned}
$$

（2）
$$
Te_i = T_{ij}e_j
$$

（3）
$$
T_{ij} = e_i \cdot Te_j
$$

（4）
$$
b_m=a_iT_{mi}=T_{mi}a_i
$$
（5）
$$
(T+S)a = Ta + Sa
$$
（6）
$$
(TS)_{ij}=T_{im}S_{mj}
$$
（7）
$$
T_{ji} = T_{ij}^T
$$
（8）
$$
(TS)^T = S^TT^T
$$
（9）
$$
tr T = T_{11} + T_{22} + T_{33}
$$
（10）
$$
tr (ab) = a \cdot b
$$
（11）
$$
Q_{mi}Q_{mj} = \delta_{ij}
$$
Eigenvalues and Eigenvectors：
$$
|T-\lambda I| = 0
$$

根据：
$$
\lambda^3 - I_1\lambda^2 + I_2\lambda - I_3 = 0
$$

Principal Scalar Invariants

$$
\begin{aligned}
I_1 &= T_{11} + T_{22} + T_{33} = T_{ii} = tr(T) \\
I_2 
&= 
\left |
\begin{matrix}
	T_{11} & T_{12} \\
	T_{11} & T_{12} \\
\end{matrix}
\right |
+
\left |
\begin{matrix}
	T_{22} & T_{23} \\
	T_{32} & T_{33} \\
\end{matrix}
\right |
+ \
\left |
\begin{matrix}
	T_{11} & T_{13} \\
	T_{31} & T_{33} \\
\end{matrix}
\right |
=
\frac{1}{2} (T_{ii}T_{jj} - T_{ij}T_{ji}) \\
I_3 &= det(T)
\end{aligned}
$$
