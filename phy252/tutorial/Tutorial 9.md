# Question 1
Recall that in a harmonic oscillator:
$$
	\mathcal{Z} = \frac{1}{1-e^{ -\beta \hbar \omega }}
$$
And,
$$
	\left< E \right> = - \frac{ \partial  }{ \partial \beta } \log \mathcal{Z}
$$
---
a.
The average energy in this system is:
$$
	\frac{\hbar \omega}{e^{\beta \hbar \omega}-1}
$$
Compute $\left< E^{2} \right>$,
$$
	\left< E^{2} \right> = \frac{1}{\mathcal{Z}} \frac{ \partial^{2}\mathcal{Z} }{ \partial \beta^{2} } = \frac{\hbar^{2}\omega^{2}(e^{ \beta \hbar \omega }+1)}{(e^{ \beta \hbar \omega }-1)^{2}}
$$
The variance is therefore:
$$
	\text{var}(E) = \left< E^{2} \right>  - \left< E \right> ^{2} = \frac{\hbar^{2}\omega^{2}(e^{ \beta \hbar \omega }+1)}{(e^{ \beta \hbar \omega }-1)^{2}} - \left[ \frac{\hbar \omega}{e^{\beta \hbar \omega}-1} \right] ^{2} = \frac{\hbar^{2}\omega^{2} e^{ \beta \hbar \omega }}{(e^{ \beta \hbar \omega }-1)^{2}}
$$
The standard deviation is the square root of this:
$$
	\sigma(E) = \frac{\hbar \omega e^{ \beta \hbar \omega/2 }}{e^{ \beta \hbar \omega }-1}
$$
---
b.
Increasing the number of particles is easy because $\left< E \right>\to N \left< E \right>$ and $\sigma(E)\to \sqrt{ N } \sigma(E)$.

So when $N=10^{6}$ we have:
$$
	\left< E \right> = \frac{10^{6}\hbar \omega}{e^{ \beta \hbar \omega }-1} \qquad \sigma(E) = \frac{10^{3}\hbar \omega e^{ \beta \hbar \omega/2 }}{e^{ \beta \hbar \omega }-1}
$$
---
c.
Do the same thing as above.
$$
	\left< E \right> = \frac{10^{20}\hbar \omega}{e^{\beta \hbar \omega}-1} \qquad \sigma(E) = \frac{10^{10}\hbar \omega e^{ \beta \hbar \omega/2 }}{e^{ \beta \hbar \omega }-1}
$$
For the sketch, you should notice that the normal curve grows progressively more "peaked" over time.
- Law of large numbers
# Question 3
---
a.
Definition of the free energy:
$$
	F \equiv  -\frac{1}{\beta} \log \mathcal{Z}
$$
Recall that:
$$
	\mathcal{Z}(\beta) = \sum e^{ -\beta E_{i} } = e^{ -\beta(-\mu B) } + e^{ -\beta(E_{0}+\mu B) } = e^{ \beta \mu B } + e^{ -\beta E_{0} } e^{ -\beta \mu B }
$$
Therefore we have:
$$
	F = -\frac{1}{\beta} \log \left[ e^{ \beta \mu B } + e^{ -\beta E_{0} } e^{ -\beta \mu B } \right]
$$
Where $\beta=1 /k_{B}T$

---
b.
We are interested in the quantity:
$$
	d\left< W \right> = \left( \frac{ \partial F }{ \partial b }  \right)_{T} \, db
$$
For some quantity $b$. In our case, $B$.
$$
	\frac{ \partial F }{ \partial B } = -\frac{1}{\beta} \frac{ \partial  }{ \partial B } \log \left[ e^{ \beta \mu B } + e^{ -\beta E_{0} } e^{ -\beta \mu B } \right] = - \frac{\mu(e^{ \beta(2\mu B+E_{0}) }-1)}{e^{ \beta(2\mu B+E_{0}) }+1}
$$
And therefore we have:
$$
	d\left< W \right> = - \frac{\mu(e^{ \beta(2\mu B+E_{0}) }-1)}{e^{ \beta(2\mu B+E_{0}) }+1} \, dB
$$
# Question 2
