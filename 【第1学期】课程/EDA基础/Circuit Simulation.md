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

### Equation Formulation
$$
\begin{align*}
K_{v}v + K_{i}i &= i_s\\
Ai &=0\\
v-A^{T}e&= 0
\end{align*}

$$

### Nodal Analysis(NA)

Nodal Matrix:$Y_{n}= i_{ns}$
