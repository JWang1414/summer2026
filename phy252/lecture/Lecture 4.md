Adiabatic processes only care about how efficient the energy transfer is. It does not have to happen in a specially made insulated box. For example, air is not a particularly good conductor of heat. This means that, in a lot of cases, if air is flowing quickly enough, it can be approximated as an adiabatic process.

This manifests in the speed of sound:
$$
	C_\text{sound} = \sqrt{ \frac{\gamma k_{B}T}{m} }
$$
The gamma ($\gamma=1+2 /f$) factor manifests here because it is an adiabatic process.
# Carnot Cycle
During the first step, the energy inside the box doesn't change at all, despite the volume inside increasing. This is because there is energy flowing inside from the hot reservoir, expanding the box. 
- Negative work. Energy goes out.
- Heat goes in

Now, we would like to move along an adiabat to decrease the temperature inside the box. In this case the volume of the box expands, but is isolated.
- Negative work. Energy goes out
- The box is insulated, so there is no heat transfer

We go back now. Place the box in contact with the cold reservoir, and compress the box. This is isothermal compression.
- Positive work. Energy goes in
- Heat goes out

Finally, we go back to our original point. Adiabatic compression.
- Positive work. Energy goes in
- No heat transfer, the box is insulated

Thermal efficiency is defined as:
$$
	\eta=\frac{W_\text{total}}{Q_\text{in}} \equiv  \frac{Q_\text{out}-Q_\text{in}}{Q_\text{in}}
$$
Which is essentially how much work you get for the heat required. $W_\text{total}$ is the work generated, and $Q_\text{in}$ is the heat input

The efficiency of the Carnot cycle is:
$$
	\eta _\text{Carnot} = 1-\frac{T_{c}}{T_{h}}
$$
It is the most efficient thermal cycle. You get the most energy for how much heat you put in.