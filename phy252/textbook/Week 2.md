# Active and frozen degrees of freedom
In any given situation, only some of the energetic dof are active. Each energetic dof has a characteristic energy associated with it, which can be used to determine if it is active or frozen.

For example, for the electron motion dof in a helium atom, the characteristic energy is roughly an electron volt. Converting this energy into a temperature,
$$
	T_{c} \propto \frac{E_{c}}{k_{B}} \approx 10^{4}
$$
Generally speaking, for some system temperature $T$, if $T\ll T_{c}$, the dof is frozen, if $T\gg T_{c}$, the dof is active.

This is why we can treat helium gas at room temperature as a collection of point particles.

Equipartition theorem:
> Every active dof contributes $k_{B}T /2$ to the internal energy.
- Each active dof must be in thermal equilibrium, at the same temperature

As a corollary, a system with $f$ active dof has internal energy and heat capacity:
$$
	\left< E \right> = \frac{f}{2} k_{B}T \qquad C_{V}=\frac{f}{2}k_{B}
$$
Notably, for an idea gas, $C_{P}$ is always $C_{V}+Nk_{B}$. We define the *heat capacity ratio* of an ideal gas to be:
$$
	\gamma=\frac{C_{P}}{C_{V}} = 1+\frac{2}{f}
$$
Which is an important quantity in gas dynamics. We will come back to it later.
- Also, notice that $\gamma>1$, always
# Heat engine
A heat engine is a repeated cyclic process that converted internal energy into work using a *working substance* (like a gas)

Work for particles in a box is $W=-P(\Delta V)$. Notice that, if the volume stays constant, then there is no work done. Lets say we are trying to bring an ideal gas from a higher temperature $T_{h}$ to a lower temperature $T_{c}$. Its pressure and volume must satisfy,
$$
	P_{h}V_{h} = Nk_{B}T_{h}
$$
Consider two ways of cooling down our gas.
1. Constant-pressure expansion from $V_{h}\to V_{c}$, and then constant-volume cooling from $P_{h}\to P_{c}$
2. Constant-volume cooling from $P_{h}\to P_{c}$, and constant-pressure expansion from $V_{h}\to V_{c}$
As already established, the constant-volume cooling takes no work. The work in the first case is $W_{1}=P_{h}(V_{h}-V_{c})$, and the work in the second case is $W_{2}=P_{c}(V_{h}-V_{c})$. Despite achieving the same final temperature, the work done is different.

Therefore, work is not path independent, and neither is heat.

There are two classic pathways $(P_{h}, V_{h})\to(P_{c}, V_{c})$ on a $(P, V)$ diagram. The isothermal path, and the adiabatic path.
$$
	W_\text{isothermal} = Nk_{B}T \log\left( \frac{V_{c}}{V_{h}} \right)
$$
$$
	W_\text{adiabatic} = \frac{P_{c}V_{c}-P_{h}V_{h}}{\gamma-1} = C_{V}(T_{c}-T_{h})
$$
- Assume we maintain thermal equilibrium at all times
- Physically, imagine the isothermal system as one where our box is always attached to a conductive thermal reservoir
- The adiabatic system is one where our box is insulated from all external elements
