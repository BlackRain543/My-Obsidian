## 1 Netlist & Equations
	DRC:Design Rule Check
	LVS:Layout vs Schematic
	RC:RLC Extraction

* Parasitic R
* Parasitic L
* Parasitic C

**SPICE:** (Simulation Program with Integrated Circuit Emphasis)

**Netlist:** name, node, value

	KCL：Kirchhoff’s Current Law
	KVL：Kirchhoff’s Voltage Law

	BCE：Branch Constitutive Equations

### 2.1 Equation Formulation
$$
\begin{align*}
KCL: &  K_{v}v + K_{i}i &= i_s\\
KVL: &  Ai &=0 \\
BCE: &  v-A^{T}e&= 0
\end{align*}

$$

各节点中，流出的电流为+，流入的电流为-

### 2.2 Nodal Analysis(NA)

Nodal Matrix: $Y_{n}= i_{ns}$

### 2.3 Modified Nodal Analysis(MNA)
#### Step:
1. Write KCL
2. Use branch equations to eliminate as many branch currents as possible
3. Write down unused branch equations
4. Use KVL to eliminate branch voltages from previous equations

##### 电压控制电压源 VCVS
##### 电压控制电流源 VCCS

##### 电流控制电压源 CCVS
##### 电压控制电流源 CCCS

## 2 DC Solution

#### MNA Example
1. KCL+Node
2. KVL+Node
3. $Mx=b,x=M^{-1}b$


## 3 Nonlinear Circuit Simulation

1D Example

### Two Loops:
* ***outer loop:** time advancing
* ***inner loop:** NR iteration

I-V relation: $i = g(v)$

### MOSFET Model:
$I_{ds}=I_{ds}(V_{gs},V_{ds})$


### Dynamic Element Stamping
$$
\begin{align*}
v(t) &= C\frac{dv}{dt}\\
v(t) &= L\frac{di}{dt}
\end{align*}
$$

### FE and BE and TR:
* ***Forward Euler:*** $y(t_{n})=y(t_{n-1})+hf(y(t_{n-1}))$
* ***Backward Euler:** $y(t_{n})=y(t_{n-1})+hf(y(t_{n}))$
* ***Trapezioidal Rule:*** $y(t_{n})=y(t_{n-1})+\frac{h}{2}[f(y(t_{n}))+f(y(t_{n-1}))]$

稳定性，准确性


Capacitor Stamp
Inductor Stamp

Local Error、Global Error

#### NR:(Newton Raphson method)
Taylor Series --> Iteration function

Taylor Series
$$
f(x^{k+1})=f(x^{k})+ \frac{df(x^{k})}{dt}(x^{k+1}-x^{k})
$$
