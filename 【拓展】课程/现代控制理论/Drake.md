
**Tag:** #Drake #Python

---
# 1 Simulation
---
### 1.1 模型文件
* *.urdf
* *.sdf

### 1.2 Solver
* *Fast
* *Accurate

### 1.3 System
* *Static
* *Dynamic
   
>**MATLAB:** Simulink、Simscape

##### Cart-Pole Model
状态：4

##### DC Motor
**PI Block**

$$
\begin{aligned}
x(k+1) &= x(k)+Te(k) \\
y(k) &= K_Ix(k)+K_pe(k)
\end{aligned}
$$


