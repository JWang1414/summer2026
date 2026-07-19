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
## Carnot cycle
Consider $N$ particles in a box with a movable wall. The Carnot cycle is a cyclical process we use to do work with this gas.

The first step is isothermal expansion. The box is kept in contact with a hot reservoir, and the volume of the gas expands from $V_{1}$ to $rV_{2}$,
$$
	W_{A} = Nk_{B}T_{h} \log\left( \frac{1}{r} \right) = -Nk_{B}T_{h} \log r
$$
The negative sign tells us work is being done against the external force pushing on it. That is, this is work we can use for some practical purpose
- Temperature does not change, therefore, internal energy is unchanged

Furthermore, because this is isothermic, the heat transferred from the gas to the reservoir is: $Q_{A}=-W_{A}$

Second is adiabatic expansion, accompanied by a temperature drop. The gas continues to expand, but the box is insulated. The gas cools down, and the total work done in this step is,
$$
	W_{B}=C_{V}(T_{c}-T_{h})
$$
Once again a negative quantity, because $T_{h}>T_{c}$.

Third, isothermal compression using a cold reservoir. The volume of the case is reduced while the gas is maintained at $T_{c}$. The work done during this step is,
$$
	W_{C}=Nk_{B}T_{c}\log r
$$
This time, it's positive. Note that, again, the internal energy of the gas is not changing her, and the heat transfer from the cold reservoir is: $Q_{C}=-W_{C}$. The negative sign here telling us energy is flowing from the gas into the reservoir.

Finally, we complete the cycle with adiabatic compression, and an accompanying temperature increase. The volume of the gas is compressed while the box is insulated again. Once its temperature has risen back to the original temperature, $T_{h}$, the amount of work done is:
$$
	W_{D}=C_{V}(T_{h}-T_{c})=-W_{B}
$$
And just like step B, alongside all adiabatic processes, there is no heat transfer during this step.

The total work from the full cycle is:
$$
	W_\text{net} = W_{A} + W_{B} + W_{C} + W_{D} = W_{A} + W_{C} =-Nk_{B}(T_{h}-T_{c})\log r
$$
A net negative quantity, telling us that we can use this cycle can be used to perform work.

The total change in the internal energy from the cycle is $\Delta \left< E \right>=0$. The ideal gas is left at the same temperature it started with. So, by TD1, the work output is accompanied by heat transfer from the hot reservoir to the cold reservoir.

A heat engine using the Carnot cycle is called a Carnot engine.

The efficiency of a heat engine is defined to be the ratio of net work output to the heat input,
$$
	\eta=-\frac{W_\text{net}}{Q_{h}}
$$
The efficiency of the Carnot cycle is,
$$
	\eta _\text{Carnot} = \frac{T_{h}-T_{c}}{T_{h}} = 1-\frac{T_{c}}{T_{h}}
$$
Unless the cold temperature is absolute zero, the Carnot cycle will never be perfectly efficient.

Generally speaking, for any cyclic heat engine with $\Delta \left< E \right> =0$, TD1 tells us that $-W_\text{net}=Q_{c}+Q_{h}$. So the efficiency can also be expressed as:
$$
	\eta=\frac{Q_{c}+Q_{h}}{Q_{h}}
$$
## Refrigerator
If a heat engine is run in reverse, it will instead use external work to extract heat from the cold reservoir, and exhaust heat into the hot reservoir. This is how a fridge works.

The coefficient of performance of a refrigerator is the ratio of heat extracted to the work input required:
$$
	\text{COP} = \frac{Q_\text{extracted}}{W_\text{input}}
$$
In the Carnot cycle, step $C$ extracts heat from the cold reservoir, and step $A$ deposits heat into the hot reservoir. The work input into the Carnot refrigerator is $W_\text{net}=Nk_{B}(T_{h}-T_{c})\log r$, and the heat extracted is $Q_{c}=Nk_{B}T_{c}\log r$.
$$
	\text{COP}_\text{Carnot} = \frac{T_{c}}{T_{h}-T_{c}}
$$
Like before, since $\Delta \left< E \right> =0$, TD1 tells us that, in general:
$$
	\text{COP}=-\frac{Q_{c}}{Q_{h}+Q_{c}}
$$
## Carnot vs. aliens
Imagine we have an alien cyclic process operating between two thermal reservoirs $T_{h}$ and $T_{c}$. This cycle has a higher efficiency than the Carnot cycle, with $Q_{h}$ extracted from the hot reservoir, and $Q_{c}$ exhausted from the cold reservoir.

Assuming $\eta_{X}>\eta _\text{Carnot}$ is equivalent to:
$$
	\eta _\text{X} > \eta _\text{Carnot} \implies \left( 1+\frac{Q_{c}}{Q_{h}} \right) > \left( 1-\frac{T_{c}}{T_{h}} \right) \iff \frac{Q_{h}}{T_{h}} + \frac{Q_{c}}{T_{c}} <0
$$
This condition is identical in the case of the COP as well. That is, for $\eta$ and COP:
$$
	\frac{Q_{h}}{T_{h}} + \frac{Q_{c}}{T_{c}} <0
$$
Thus telling us that the alien cycle is more efficient as a heat engine, and as a refrigerator.

For cycles worse than the Carnot cycle, we instead have:
$$
	\frac{Q_{h}}{T_{h}} + \frac{Q_{c}}{T_{c}} >0
$$
We will label this quantity:
$$
	\Delta S \equiv  \sum \frac{\Delta Q_{i}}{T_{i}} = \frac{Q_{h}}{T_{h}} + \frac{Q_{c}}{T_{c}}
$$
It is a convenient indicator of whether a cycle is better or worse than a Carnot cycle.

Now, if you place the alien cycle and the Carnot cycle next to each other, connected to the same two reservoirs, you will find that heat will flow from the cold to the hot reservoir. This should be impossible, and leads us to the second law of thermodynamics.

No Crazy Heat Flow Rule (TD2):
> No reversible cycle operating between two reservoirs at temperatures $T_{h}$ and $T_{c}$ can be more efficient than a Carnot cycle operating between the same reservoirs.

- The second law of thermodynamics isn't a quantitative statement, but one about the impossibility of building a certain type of machine
## Shifting focus
As it turns out, $S$ has been in the background of every thermal phenomenon that we have considered thus far.

Time reversal: $\Delta S$ is an indicator of time-reversal symmetry breaking. A process with $\Delta S>0$ can occur spontaneously, but $\Delta S<0$ cannot.

Thermal equilibrium: A system is at thermal equilibrium when $S$ is maximised, and $\Delta S=0$.

Using the definition $dS=dQ /T$ for small deviations from equilibrium, and $dW=-P \, d\left< V \right>$ for a gas, TD1 for particles inside a box can be rewritten as:
$$
	dS= \frac{1}{T} d\left< E \right> +\frac{P}{T} d\left< V \right>
$$
Now, from the above, temperature and pressure can both be expressed in terms of $S$:
$$
	\frac{1}{T} = \left( \frac{ \partial S }{ \partial \left< E \right>  }  \right)_{\left< V \right> } \qquad \frac{P}{T} = \left( \frac{ \partial S }{ \partial \left< V \right>  }  \right)_{\left< E \right> }
$$
In some ways, these can even be considered the definitions of temperature and pressure for a general system using the function $S(\left< E \right>, \left< V \right>)$

Clearly, $S$ is quite important, and we will be shifting our focus from $\left< E \right>$ to $S$. Dimensional analysis tells us that $S$ has units J/K. It is also a number such that we expect $S /Nk_{B}\sim 1$.

$S$ is called *entropy*.
