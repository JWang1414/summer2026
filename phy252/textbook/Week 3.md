## Defeating the Carnot limit
People have tried to express TD2 in terms of mathematical theorems, but it turns out to be a troublesome thing to do. This shouldn’t surprise us: physical laws are founded on experimental measurements, not mathematical axioms.

Recall that the efficiency of the Carnot cycle is:
$$
	\eta _\text{Carnot} = 1-\frac{T_{c}}{T_{h}}
$$
One way to break the Carnot limit and achieve maximum efficiency would be to have the cold reservoir at 0 K. This is a cheat though, and in fact, also forbidden by the laws of thermodynamics.

However, $Q_{c}$ is the heat that needs to be exhausted into the cold reservoir during the isothermal compression step. This heat is accounting for the work $W_{c}$ required to compress the gas. That is, if this work is done isothermally, then there must be some heat exhausted into the reservoir.

How can we do less work during this step?

What if we track the locations of the particles, wait for most of them to be on the far side of the box, and then compress the box with minimal work. The particles are on the other side of the box after all, they cannot push back. In this case, we can complete a cycle with higher efficiency than the Carnot cycle. The cycle can be completed with 100% efficiency in this manner.

This means we have constructed an example where $\Delta S<0$. Just like with the alien process, we can move energy from a cold to a hot reservoir, with zero work.

This tells us something particularly strange: thermodynamics can be broken by tracking the dof. The laws of thermodynamics are valid only in the case of untracked dof.

All of thermodynamics, which can be expressed in terms of $S$, is the analysis of knowledge about untracked dof.
# Probability
Example: You are studying pigeon behaviour. There are 5 birdhouses, the pigeon chooses which one to rest in at random. You study this pigeon by marking numbers 1-5 to record which choices the pigeon makes.

Lets express this using the language of probability theory.
- Each time the pigeon flies into a birdhouse is a *trial*
- Each of the birdhouses is a possible *outcome* of the trial
- The set of all outcomes is the *sample space* $\Sigma$.
- Every subset of the sample space is called an *event* $e_{i}$. The collection of all possible events is the *event space* $\mathcal{E}$

The probability assigned to the events in the event space is a function that has to satisfy the following axioms:

Let $p:\mathcal{E}\to[0, 1]$ be the probability function.
- If $e_{1}$ and $e_{2}$ are disjoint sets, then $p(e_{1}\cup e_{2})=p(e_{1})+p(e_{2})$
- The probability of the entire sample space, $p(\Sigma)=1$
