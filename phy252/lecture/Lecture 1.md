
- Started off with a short segment introducing processes where thermal physics is relevant
	- Stuff like friction, is really just electromagnetic forces
	- Why we don't use quantum mechanics to predict the trajectory of classical objects

Basic Commandments of Physics:
0. (Absolute) adjectives don't make sense
	1. Stuff like "small" or "large" omit what the reference frame is
1. Quantify
2. Symmetry

Lets go back to our example with the incline plane with something rolling down it. This time, lets try to describe the full system, all the atoms in it. Well, you'd find that you would need an unfathomable number of variables, the degrees of freedom would approach infinity.

Generally speaking, we can split the energy in a system between the tracked and untracked degrees of freedom.
- The energy in the untracked degrees of freedom is called *internal energy*
# Particle in a box
Lets say we have a single particle bouncing around randomly in a box. The sides of the box aren't ideal, so it eventually explores the entire box. We cannot easily predict the trajectory of the particle.

Imagine we have a wall on this box we can measure. Something like a piston. Every time the particle bounces on this piston the change in momentum (for the particle) is:
$$
	\Delta p_{x} = 2mv_{x}
$$
The factor of two arises because it is a perfectly elastic collision. The particle begins moving in the opposite direction. What if we are instead interested in the average change in momentum over time?
$$
	\left< \frac{\Delta p_{x}}{\Delta t} \right> = \frac{2mv_{x}}{2L /v_{x}}= \frac{mv_{x}^{2}}{L} \equiv  \left< F_{x} \right>
$$
Where $2L /v_{x}$ is the average amount of time taken to travel to the back of the box, and back again.

Now, what if we begin tracking $N$ particles inside this box?
$$
	\left< F_{x} \right> = \left< \frac{Nmv_{x}^{2}}{L} \right> = \frac{1}{3} \frac{Nm}{L} \left< v^{2} \right>
$$
Where we have claimed,
$$
	\left< v_{x}^{2} \right> = \left< v_{y}^{2} \right> = \left< v_{z}^{2} \right> \implies \left< v_{x}^{2} \right> = \frac{1}{3} \left< v^{2} \right>
$$
Now, we can use the definition of kinetic energy to further simplify this into:
$$
	\left< F_{x} \right> = \frac{1}{2} mN\left< v^{2} \right> \times \frac{2}{3L} = \frac{2}{3} \frac{\left< K \right> }{L}
$$
So the average force is the average kinetic energy from all the particles multiplied by a constant.

Now, divide the force by the area of the surface, thus deriving the pressure,
$$
	\frac{\left< F_{x} \right> }{A}= \frac{2}{3} \frac{N\left< K \right> }{LA} \implies \left< P \right> = \frac{2}{3} \frac{N\left< K \right> }{ V}
$$
Where we have also swapped to measuring the average temperature of a single particle, extracting the $N$. Which gives us something that looks quite similar to the ideal gas law:
$$
	\left< P \right> V=  \frac{2}{3} N\left< K \right>
$$
# Temperature
We define the temperature, measured in kelvin as,
$$
	T_\text{system} = \alpha \left< K \right>
$$
Where $\alpha=2 /3k_{B}$ is a constant with united Kelvin/Joule, converting energy to temperature.

---
Aside:
If you want to measure temperature, like with a thermometer, you need both *thermal contact* and *thermal equilibrium*.

For example, if you were measuring your fever, you would need to keep the thermometer in your mouth for a while before getting an accurate measurement.

---

Ultimately, using our new definition for temperature, we now have a newer version of the equation from before:
$$
	\left< P \right> V = N k_{B}T
$$
Where $T$ is temperature, and $k_{B}$ is the Boltzmann constant.