## 逻辑综合——Logic Synthesis

综合=翻译+优化+映射
Synthesis = translation + optimization + mapping

---
#### Objective Function：目标函数
* Minimize area:最小化区域
* Minimize power:最小化电源
* Maximize performance:最大限度地提高性能
* Any combination of the above:以上任意组合
* More global objectives:更多向的目标

---
#### DeMorgan’s Theorem：
德摩根定理（对偶）
$$
Y=\overline{AB}=\overline{A}+\overline{B}
$$

$$
Y=\overline{A+B}=\overline{A} \cdot \overline{B}
$$

---
#### Sum-of-Products (SOP) Form：
* Minterm：最小项

#### Product-of-Sum(POS) Form:
* Maxterm：最大项

#### Quine-McCluskey Method:
（麦克卢斯基法）

---
#### 布尔定理：
**加法：**
$$ B + 1=1 $$
$$ B + 0=B $$
$$ B + B=B $$

$$ B + \overline{B}=1 $$
**数乘：**
$$ B \cdot 1=B $$
$$ B \cdot 0=0 $$
$$ B \cdot B=B $$
$$ B \cdot \overline{B}=0 $$


---
#### Quine-Mccluskey Method：（必考）
**step:**
1. 找到所有一次蕴含项
2. 一次合并
3. 二次合并
4. 素项表

---
#### Technology Mapping：技术图谱


#### Minimum Tree算法

**SRC ==> SNK**

**ATs**：Arrival Time
**RATs**：Required Arrival Time

$Slack(n) = RAT(n) –AT(n)$