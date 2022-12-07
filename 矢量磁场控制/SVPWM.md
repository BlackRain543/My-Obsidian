#### 电压方程：
$$
\begin{aligned}
U_a &= U_m * cos\theta \\
U_b &= U_m * cos(\theta - \frac{2\pi}{3} ) \\
U_c &= U_m * cos(\theta + \frac{2\pi}{3} ) \\
\end{aligned}

$$

#### 反Park变换：
$$
\begin{aligned}

U_{\alpha} &= U_{ref} * cos\theta \\
U_{\beta}  &= U_{ref} * sin\theta \\
U_{ref}^2  &= U_{\alpha}^2 + U_{\beta}^2 \\
tan\theta  &= \frac{U_{\beta}}{U_{\alpha}}

\end{aligned}
$$

#### 持续时间：
$$
\begin{aligned}
T_s &= T_1 + T_2 + T_0 \\
U_sT_s &= U_1T_1 + U_2T_2 + T_0
\end{aligned}
$$


#### 扇区判断：
(1)
$$
\begin{aligned}
sector &= Angle_{el}*3 / \pi + 1 \\
T_1 &= \sqrt{3}sin(sector * \pi - Angle_{el})*U_{ref} \\
T_1 &= \sqrt{3}sin(Angle_{el} - (sector - 1.0) * \pi)*U_{ref} \\
T_0 &= 1 - T_1 - T_2
\end{aligned}
$$


（2）
$$
N=4C + 2B + A
$$

|   N    | 1   | 2   | 3   | 4   | 5   | 6   |
|:------:| --- | --- | --- | --- | --- | --- |
| Sector | 2   | 6   | 1   | 4   | 3   | 5   |

```python
import Drake
```

```C++
#include "math.h"

int main(){
	printf("Hello world!");
}
```

