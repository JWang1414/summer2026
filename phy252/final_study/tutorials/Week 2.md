# Question 1
$$
	\Delta Q=C(\Delta T)
$$
Constant volume for an ideal gas:
$$
	C_{V} = \frac{3}{2} Nk_{B}
$$
Change in temperature is therefore:
$$
	\Delta T = \frac{\Delta Q}{C} = \frac{2}{3} \frac{\Delta Q}{Nk_{B}} \approx 0.48
$$
So the final temperature is 400.48 K

At constant pressure:
$$
	\Delta Q = C(\Delta T) = \frac{5}{2} Nk_{B}(\Delta T) = 3450
$$
So 3450 J of heat is required. No work is done during this process
# Question 2
Based on the graphical understanding of isotherms and adiabats, it would take a greater external pressure different to compress the adiabatic system (A).
# Question 3
Convert energy to temperature:
$$
	T \equiv  \frac{2}{3k_{B}}\left< E_{K} \right>
$$
---
a.
Characteristic temperature for vibrational dof:
$$
	T = \frac{2}{3k_{B}}(\hbar \omega) \approx 2029
$$
So below 2029 K. Translation and rotation account for 3+2 dof (since nitrogen is diatomic)
$$
	C_{V} = \frac{5}{2}Nk_{B}
$$
---
b.
Characteristic temperature for rotational dof:
$$
	T=\frac{2}{3k_{B}}\left( \frac{\hbar^{2}}{2mR^{2}} \right) \approx 0.57
$$
So below 0.57 K both rotational and vibrational dof can be ignored.
$$
	C_{V} = \frac{3}{2}Nk_{B}
$$
Because there is just translational dof remaining.

---
c.
Characteristic temperature for translational dof:
$$
	T=\frac{2}{3k_{B}} \left( \frac{\hbar^{2}}{2mL^{2}} \right) \approx 5.7 \times 10^{-19}
$$
Below $5.7\times 10^{-19}$ the heat capacity may be entirely neglected
# Question 4
Characteristic temperature will be:
$$
	T=\frac{2}{3k_{B}} \left( \frac{\hbar^{2}}{2mL^{2}} \right)
$$
Solve for $L$
$$
	L^{2} = \frac{2}{3k_{B}} \left( \frac{\hbar^{2}}{2mT} \right) \implies L = \sqrt{ \frac{2}{3k_{B}} \left( \frac{\hbar^{2}}{2mT} \right) } \approx 6.31 \times 10^{-11}
$$
So the box must be roughly 0.06 nm across
# Question 5
---
a.
Ideal gas law:
$$
	PV = Nk_{B}T \implies P = \frac{Nk_{B}T}{V}
$$
Therefore:
$$
	-P \, dV = - \frac{Nk_{B}T}{V} \, dV
$$
Valid since $T$ is constant in an isothermal setting.

---
b.
$\Delta T=0$ therefore $\Delta E=0$. Therefore we have:
$$
	0=dQ+dW \implies dQ =-dW = \frac{Nk_{B}T}{V} \, dV
$$
Integrate:
$$
	Q = \int_{V_{i}}^{V_{f}} \frac{Nk_{B}T}{V} \, dV = Nk_{B}T \int_{V_{i}}^{V_{f}} \frac{1}{V} \, dV = Nk_{B}T \log\left( \frac{V_{f}}{V_{i}} \right)
$$
---
c.
Expansion means $V_{f}>V_{i}$ and therefore $V_{f} /V_{i}>1$. Hence $\log(V_{f} /V_{i})$ is positive. Everything else in this quantity is a positive constant. So $Q$ is positive during isothermal expansion. Implying heat input, as needed.
# Question 7
---
a.
$\Delta V=0$ therefore $W=0$.

Heat:
$$
	Q=C(\Delta T) = \frac{3}{2}Nk_{B}\Delta T = \frac{3}{2} V(P_{f}-P_{i}) \approx 607.95
$$
No work done, 608 J of heat transferred into the box.

---
b.
Ideal gas law:
$$
	T=\frac{PV}{Nk_{B}}
$$
Definition adiabatic:
$$
	T_{i}V^{\gamma-1}_{i} = T_{f}V^{\gamma-1}_{f} \implies P_{i}V^{\gamma}_{i} = P_{f}V_{f}^{\gamma}
$$
The final pressure is:
$$
	\frac{P_{i}V_{i}^{\gamma}}{V_{f}^{\gamma}} = 2.15 \times 10^{-2} \text{ atm}
$$
Solve for work:
$$
	W_\text{adiabatic} = \frac{P_{f}V_{f}-P_{i}V_{i}}{\gamma-1} \approx -119.24
$$
So about 119 J of work is extracted from the gas. There is no heat exchange because this is adiabatic.

---
c.
Compression ratio:
$$
	r=\frac{V_{i}}{V_{f}} = \frac{10}{1} = 10
$$
Work:
$$
	W_\text{isothermal} = Nk_{B}T \log r = PV \log r = 1(10) \log(10) \approx 23.03
$$
In an isothermal setting, $\Delta W=-\Delta Q$. So 23 J of work is done to compress the gas, and 23 J of heat is extracted from the gas.

---
d.
$$
	Q=C(\Delta T) = \frac{3}{2}Nk_{B}(\Delta T) \approx -2070
$$
So 2070 J of heat is extracted from the gas, and no work is done.
# Question 8
---
b.
Work when $\Delta V=0$ is 0.

Compute work:
$$
	W_{1} = -P (10V_{0} - V_{0} ) = -9P_{0}V_{0}
$$
$$
	W_{2} = -\frac{P_{0}}{2}(V_{0}-10V_{0}) = \frac{9}{2}P_{0}V_{0}
$$
So the net work is:
$$
	W_\text{net} = -9P_{0}V_{0} + \frac{9}{2}P_{0}V_{0} = -\frac{9}{2}P_{0}V_{0}
$$
Compute the temperature between the steps:
$$
	T_{0} = \frac{P_{0}V_{0}}{Nk_{B}}
$$
$$
	T_{1} = \frac{10P_{0}V_{0}}{Nk_{B}}
$$
$$
	T_{2} = \frac{5P_{0}V_{0}}{Nk_{B}}
$$
$$
	T_{3} = \frac{P_{0}V_{0}}{2Nk_{B}}
$$
Changes in temperature:
$$
	\Delta T_{1} = \frac{P_{0}V_{0}}{Nk_{B}}(10-1) = 9T_{0}
$$
$$
	\Delta T_{2} = -5T_{0}
$$
$$
	\Delta T_{3} = -\frac{9}{2}T_{0}
$$
$$
	\Delta T_{4} = \frac{1}{2}T_{0}
$$
Changes in heat:
$$
	Q_{1} = C_{P}(\Delta T_{1}) = \frac{5}{2}Nk_{B}(9T_{0}) = \frac{45}{2}P_{0}V_{0}
$$
$$
	Q_{2} = C_{V}(\Delta T_{2}) = \frac{3}{2}Nk_{B}(-5T_{0}) = -\frac{15}{2} P_{0}V_{0}
$$
$$
	Q_{3} = C_{P}(\Delta T_{3}) = -\frac{45}{4}P_{0}V_{0}
$$
$$
	Q_{4} = C_{V}(\Delta T_{4}) = \frac{3}{4}P_{0}V_{0}
$$
Net heat:
$$
	Q_\text{net} = \frac{9}{2}P_{0}V_{0}
$$
---
c.
$$
	\eta = \frac{W_\text{net}}{Q_\text{in}} = \frac{9 /2}{93 /4} = \frac{6}{31} \approx 0.19
$$
So its not really all that efficient.
