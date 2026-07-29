# Question 5
---
a.
Uniform distribution for $m=\pm 1 /2$. That is, the probability for both will be 50/50

---
b.
Start from the stat-sum
$$
	\mathcal{Z}(\beta) = \sum_{i} e^{ -\beta E_{i} } = \sum_{m} e^{ \beta m\mu B } = e^{ -\beta \mu B/2 } + e^{ \beta \mu B/2 }
$$
Solve for $\left< E \right>$
$$
	\left< E \right> = -\frac{1}{\mathcal{Z}} \frac{ \partial \mathcal{Z} }{ \partial \beta } = -\frac{1}{e^{ -\beta \mu B/2 } + e^{ \beta \mu B/2 }} \left[ \frac{\mu B}{2}(e^{ \beta \mu B/2 } - e^{ -\beta \mu B/2 }) \right]
$$
$$
	\left< E \right> = \frac{\mu B}{2} \frac{e^{ \beta \mu B/2 } - e^{ -\beta \mu B/2 }}{e^{ -\beta \mu B/2 } + e^{ \beta \mu B/2 }} = \frac{\mu B}{2} \tanh\left( \frac{\mu B}{2k_{B}T} \right)
$$
![[Pasted image 20260729152127.png]]
Graph of $\left< E \right>$ as a function of $T$

![[Pasted image 20260729152224.png]]
Graph of $d\left< E \right> /dT$ as a function of $T$

---
c.
