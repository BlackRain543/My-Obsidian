# Back - End:

## 1 illustrative View
---

### Step:
* Design Import
* Power Planning(Floorplanning)
* Placement
* Clock Tree Synthesis(CTS)
* Detailed Route
* Prepare Tape

## 2 Foorplanning
---

	between the logical description and physical description

### 2.1 Overview:
* Chip size
* Number of Gates
* Number of Metal layers
* Interface to the outside
* Hard IPs/Macros
* Power Delivery
* Multiple Voltages
* Clocking Scheme
* Flat or Hierarchical

	**Utilization:利用率

#### Chip Size Choose:
* Core Limited
* Pad Limited

#### Placement regions:
1. Soft guide
2. Guide
3. Region
4. Fence

#### Placement Blockages and Halos:
1. Hard Blockage
2. Soft Blockage
3. Partial  Blockage
4. Halo

#### Placement Flow:
* Global
* Detailed

### 2.2  布局分析方法：
#### Simple Placer:(EXAM)

$$
HPWL = \Delta X + \Delta Y
$$

**Probability of a move:** $P = exp(\frac{-\Delta L}{T})$
**Quadratic wirelength:** $L = (x_1-x_2)^2+(y_1-y_2)^2$

$$
\begin{aligned}
\frac{\partial f}{\partial x} = 0， \frac{\partial f}{\partial y} = 0
\end{aligned}
$$

**Calculate the Distance**

## 3 Routing
---

### 3.1 Maze Routers
**Basic Idea:** Expand → Backtrace → Cleanup
