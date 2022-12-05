**Park变换：**
 静止的$\alpha \beta$坐标系 —> 旋转的$dq$坐标系
$$
\begin{bmatrix}
i_d \\
i_q \\
\end{bmatrix}
=
\begin{bmatrix}
cos\theta & sin\theta\\ 
-sin\theta & cos\theta\\ 
\end{bmatrix}
\begin{bmatrix}
i_\alpha \\
i_\beta \\
\end{bmatrix}
$$

**Inverse Park变换：**
 静止的$\alpha \beta$坐标系 <— 旋转的$dq$坐标系
$$
\begin{bmatrix}
i_\alpha \\
i_\beta \\
\end{bmatrix}
=
\begin{bmatrix}
cos\theta & -sin\theta\\ 
sin\theta & cos\theta\\ 
\end{bmatrix}
\begin{bmatrix}
i_d \\
i_q \\
\end{bmatrix}
$$

$I_q$ 代表期望力矩
$I_d$ 代表励磁分量，期望为0

$$
\begin{bmatrix}
cos\theta & sin\theta\\ 
-sin\theta & cos\theta\\ 
\end{bmatrix}
\begin{bmatrix}
i_\alpha \\
i_\beta \\
\end{bmatrix}
=
\begin{bmatrix}
i_d \\
i_q \\
\end{bmatrix}
$$
