电能 ---> 电磁能 ---> 机械能


直轴电流$I_d$: 励磁电流
交轴电流$I_q$: 转矩电流

# 1  BLDC / PMSM 数学模型
### 1.1  Q轴，D轴电压方程：
$$
\begin{align*}
u_{d}&= R i_{d}+L_{d} \frac{d}{dt} i_{d} - w_{e} L_{q} i_{q} \\
u_{q}&= R i_{q}+L_{q} \frac{d}{dt} i_{q} + w_{e}(L_{d}i_{d} + \psi_{f} ) 
\end{align*}
$$

### 1.2  磁链方程
$$
\begin{align*}
\psi_{d}&= L_{d}i_{d} + \psi_{f}\\
\psi_{q}&= L_{q}i_{q}
\end{align*}
$$

### 1.3  转矩方程
$$
T_{e}=\frac{3}{2}p_{n}[\psi_{f}i_{q}+i_{d}i_{q}(L_{d}-L_{q})]
$$
### 1.4  机械运动方程
$$
J\frac{dw_{m}}{dt} = T_{e}-T_{L}-Bw_{m}
$$







####  电机速度方程
$$
N_s = \frac{60f}{pp}
$$

$$
w_{rpm} = Kv \cdot EMF_{back}
$$

转矩系数 = 反电动势系数 * 电机电动势。
kv = 转速 / 电压


##### 耗损类型
* 铁芯耗损：铁损
* 电阻耗损：铜损

***后续测试任务：***
电角度标定
梯形轨迹
负载通信测试

$$
v_{S}=Ri_{S}+L \frac{d}{dt} i_{S} + e_{S}
$$

$$
e^{jw_{e}t}=cos(w_{e}t)+jsin(w_{e}t)
$$

$$
\varPhi_{S}=\varPhi_{S} \cdot e^{jw_{e}t}
$$
