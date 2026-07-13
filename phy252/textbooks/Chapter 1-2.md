# Degrees of Freedom
Given some physical system, if you need to specify $N$ real numbers to communicate the configuration of your system, then your system has $N$ degrees of freedom.

Generally speaking, in a given physical system, there are typically some easy dof to track, and some that are harder to track. For example, it is easier to track the motion of a pendulum bob, than the motion of the air.

The dof that are easier to track are our tracked dof, and the parts that we struggle to track, are called untracked dof. Thermal physics is a collection of methods to deal with the energy in the untracked dof.

$$
	\text{Energy of system} = \text{Energy in tracked dof} + \text{Energy in untracked dof}
$$
Notably, energy can be transferred between the tracked and untracked dof.

Not all dof in a system contribute to its energy. The dof that do contribute to the energy are called *energetic dof*
# Internal Energy
Monoatomic gases have just one particle per molecule. So, there are no vibrations or rotations to track.
## Fixed Volume, fluctuating force
Our model of gas inside of a box will have $N$ particles with mass $m$. There are no external forces, and the gas has been unperturbed for long enough that it is in *thermal equilibrium*. That is, the untracked dof have reached a *steady state*. The average values of all the properties of the untracked dof are no longer changing in time.

Consider an elastic collision in one dimension, between a particle moving to the right with velocity $v_{x}$ bouncing off the $+x$ wall of the box. The change in momentum after bouncing is $\Delta p_{x}=2mv_{x}$. And the collisions happen on average every $\tau=2L_{x} /v_{x}$.

The average force on the wall, exerted by $N$ particles is,
$$
	\left< F_{x} \right> = \frac{\Delta p_{x}}{\tau} = Nm \frac{\left< v^{2}_{x} \right> }{L_{x}}
$$
Now, using symmetry, we will suppose that $\left< v^{2}_{x} \right> = \left< v^{2}_{y} \right> = \left< v^{2}_{z} \right>$. Furthermore, we have that,
$$
	\left< v^{2} \right>  = \left< v^{2}_{x} \right>  + \left< v^{2}_{y} \right>  + \left< v^{2}_{z} \right> \implies \left< v^{2}_{x} \right>  = \frac{1}{3} \left< v^{2} \right>
$$
Yielding,
$$
	\left< F_{x} \right>  = N \frac{m\left< v^{2} \right> }{3L_{x}} = \frac{2}{3}N \frac{\left< E_{K} \right> }{L_{x}}
$$
Where $\left< E_{K} \right> = \frac{1}{2}m\left< v^{2} \right>$

Notice that, if we have some way to measure the force exerted by the particles in the box on the walls, we can measure the energy in the untracked dof.

The easiest way to measure this force is to measure the *pressure* on the walls of the box. That is, the force per unit area on the walls.
$$
	\left< P \right> = \frac{2N}{3V} \left< E_{K} \right>
$$
Where $n=N /V$ is called the number density.

- If the volume of the box is fixed, we can measure the average kinetic energy inside by attaching a pressure gauge to our box
## Fixed force, fluctuating volume
Consider a situation where a constant force $F^{\text{ext}}_{x}$ is exerted from the outside on a box whose $x$ wall is free to move. As the length of the box is reduced by the force, there are more impacts from the particles. At a steady state, the force is balanced such that,
$$
	\left< L_{x} \right> = \frac{1}{3} \frac{Nm\left< v^{2} \right> }{F_{x}^{\text{ext}}}
$$
Casting this in terms of the pressure and volume relationship with:
$$
	P= \frac{F_{x}^{\text{ext}}}{L_{y}L_{z}} \qquad V=L_{x}L_{y}L_{z}
$$
Yields:
$$
	\left< V \right> = \frac{2N}{3P} \left< E_{K} \right>
$$
So the volume of the box, measured at a fixed particle number and external pressure, is a measure of the energy in the untracked dof.
## Remarks
From this point, the average energy in the untracked dof of a system will be called the *internal energy*

In our simple system, the only contribution to the internal energy is the total kinetic energy of the particles. In other systems, internal energy may include contributions from the potential energy, vibrations, rotations etc.
- Only for an ideal gas is the internal energy a function of temperature alone

The physics of dilute, or ideal gases describes a simple, and universal method to measuring internal energies. It works reasonably well for most gases.

Recall that the assumptions used to develop the theory are:
1. No long-range forces between particles
2. Dimensions of the box are large compared to the particles
# Temperature
We can use the internal energy of an ideal gas to construct an ideal gas *thermometer* (IGT). This is a fixed-volume box filled with a known quantity of molecules, and equipped with a pressure gauge. This pressure tells us the internal energy of the gas.

To measure the temperature of an object, we place it in *thermal contact* with an IGT. Thermal contact means the two are free to exchange energy. Energy transfer occurs between the untracked dof of the two, and once both have attained thermal equilibrium, we may read off the temperature. That being:
$$
	T \equiv \alpha \left< E_{K} \right> 
$$
Where $\alpha=4.83\times 10^{22}$ K/J is a universal constant. In terms of the Boltzmann constant,
$$
	\alpha = \frac{2}{3k_{B}} \qquad k_{B} = 1.38\times 10^{-23} \text{ J/K}
$$
One of our previous equations may also be re-written as:
$$
	P\left< V \right>  = \frac{2}{3} N \left< E_{K} \right>  = Nk_{B}T
$$
Often called the ideal gas law.

In chemistry this is often written as,
$$
	P\left< V \right> = nk_{B}N_{A}T
$$
Where $n$ is the amount of gas in moles, and $N_{A}=6.022\times 10^{23}$ mol$^{-1}$ is Avogadro's constant.
# Work and Heat
## Mechanical Method
Recall that when an external force is applied to a gas in a box with a movable $+x$ wall, the wall is displaced to an average position $\left< x \right>$ at equilibrium. The average force from the gas inside balances the external forces such that $\left< F_{x} \right>=-F_{eq}$.

Imagine this force is increased to $F$. There is a change in the equilibrium position by a distance $d\left< x \right>$. There is therefore work done on the wall according to,
$$
	dW=Fd\left< x \right>
$$
The work-energy theorem claims that work done on an object changes its kinetic energy, but the kinetic energy of the wall has not changed. This is because the work has been done on the particles inside the box. The change in internal energy is,
$$
	d\left< E \right> =dW=Fd\left< x \right>
$$
The work is positive or negative, depending on the signs of the force and displacement. Using the volume of a box full of particles, and an external pressure $P$, the work is,
$$
	dW=-P \, d\left< V \right>
$$
![[Pasted image 20260712225742.png]]
## Thermal Method
In this case, energy is transferred from one object to another through a conducting wall. The energy is transferred from internal energy sources to other internal energy sources.

For example, by placing two conducting boxes in thermal contact with each other, after enough time, they will reach thermal equilibrium. These two boxes are therefore at the same temperature, with the same average kinetic energy.

Energy transferred between systems at different temperatures is what we will call *heat*. A quantity of heat $dQ$ transferred into our box is another way in which we can change its average internal energy,
$$
	d\left< E \right> =dQ
$$
## First Law of Thermodynamics
So, the internal energy can change through the mechanical method (work), or the thermal method (heat). Both are methods of energy transfer.

The change in internal energy of a system in general is,
$$
	d\left< E \right> = dW+dQ
$$
Which is the First Law of Thermodynamics (TD1)

Jargon used to describe various kinds of energy transformations:
![[Pasted image 20260712230951.png]]
