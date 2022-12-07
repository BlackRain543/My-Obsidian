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

### 2.2 Nodal Analysis(NA)

Nodal Matrix: $Y_{n}= i_{ns}$

### 2.3 Modified Nodal Analysis(MNA)
#### Step:
1. Write KCL
2. Use branch equations to eliminate as many branch currents as possible
3. Write down unused branch equations
4. Use KVL to eliminate branch voltages from previous equations

## 2 DC Solution

## 3 I don not know
