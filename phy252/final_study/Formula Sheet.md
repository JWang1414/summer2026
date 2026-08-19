$$
	h\approx6.63 \times 10^{-34} \qquad \hbar \approx 1.05 \times 10^{-34} \qquad k_{B} \approx 1.38 \times 10^{-23}
$$
- 1000 litres is 1 cubic metre
- 1 bar is 100 000 pascal
- 1 atmospheres is 101 325 pascal
$$
	\left< P \right>_{\Delta V=0} = \frac{2N}{3V} \left< E_{K} \right>
$$
$$
	\left< V \right>_{\Delta P=0} = \frac{2N}{3P}\left< E_{K} \right>
$$
$$
	T \equiv  \frac{2}{3k_{B}}\left< E_{K} \right>
$$
$$
	P\left< V \right> = \frac{2}{3}N\left< E_{K} \right> = Nk_{B}T
$$
$$
	dW=-P \, d\left< V \right>
$$
$$
	d\left< E \right> =dW + dQ = T \, dS - P \, d\left< V \right>
$$
- Copy the table on page 21
$$
	\Delta Q = C\Delta T
$$
$$
	C=cm \implies \Delta Q = mc\Delta T
$$
$$
	C_{V} = \frac{3}{2}Nk_{B} \qquad C_{P} = C_{V} + Nk_{B}
$$
$$
	\gamma = \frac{C_{P}}{C_{V}} = 1+\frac{2}{f}
$$
Where $f$ is the number of active dof
$$
	W_\text{isothermal} = Nk_{B}T \log\left( \frac{V_{i}}{V_{f}} \right)
$$
$$
	W_\text{adiabatic} = \frac{P_{f}V_{f}-P_{i}V_{i}}{\gamma-1} = C_{V}(T_{f}-T_{i})
$$
$$
	\eta = \frac{W_\text{net}}{Q_{in}} = \frac{Q_{c}+Q_{h}}{Q_{h}}
$$
$$
	\eta _\text{Carnot} = \frac{T_{h}+T_{c}}{T_{h}} = 1-\frac{T_{c}}{T_{h}}
$$
$$
	\text{COP} = \frac{Q_\text{extracted}}{W_\text{input}} = -\frac{Q_{c}}{Q_{h}+Q_{c}}
$$
$$
	\text{COP}_\text{Carnot} = \frac{T_{c}}{T_{h}-T_{c}}
$$
$$
	dS = \frac{1}{T} \, d\left< E \right> + \frac{P}{T} \, d\left< V \right>
$$
$$
	\frac{1}{T} = \left( \frac{ \partial S }{ \partial \left< E \right>  }  \right)_{\left< V \right> }
$$
$$
	\frac{P}{T} = \left( \frac{ \partial S }{ \partial \left< V \right>  }  \right)_{\left< E \right> }
$$
$\Delta S=0$ at equilibrium. Generally speaking $\Delta S>0$.
# Math
$$
	\left< X \right> = \sum_{i \in\Sigma} p(i)X(i)
$$
$$
	\text{var}(X) = \sum_{i \in\Sigma} p(i) \left[ X(i)-\left< X \right>  \right] ^{2} = \left< X^{2} \right>  - \left< X \right> ^{2}
$$
$$
	\sigma(X) = \sqrt{ \text{var}(X) }
$$
$$
	\text{MGF}(t) = \left< e^{ -Xt } \right>  = \sum_{i \in\Sigma} p(i) e^{ -X(i)t }
$$
$$
	s(i) \equiv \log\left( \frac{1}{p(i)} \right)
$$
$$
	\left< s \right>  = s[p] =-\sum_{i \in\Sigma} p(i) \log p(i)
$$
$$
	\vec{\nabla}f = \lambda_{a} \vec{\nabla}g_{a} + \lambda_{b} \vec{\nabla}g_{b} + \lambda_{c} \vec{\nabla}g_{c}
$$
$$
	\left< f(T) \right> = \int_{-\infty}^{\infty} f(x)\rho_{T}(x) \, dx
$$
$$
	C_{T}(x) = \int_{-\infty}^{x} \rho_{T}(t) \, dt
$$
$$
	\left< s_{n} \right> = n\left< s_{1} \right>
$$
$$
	\left< x_{i}x_{j} \right> = \left< x_{i} \right> \left< x_{j} \right>
$$
# Equilibrium thermal physics
$$
	S=k_{B}\left< s \right>
$$
$$
	\mathcal{Z}(\beta) = \sum_{i} e^{ -\beta E_{i} }
$$
$$
	p^*_{i} = \frac{e^{ -\beta E_{i} }}{\mathcal{Z}}
$$
$$
	\left< s \right> _\text{max} = - \sum_{i} p^*_{i} \log p^*_{i} = \beta \left< E \right>  + \log \mathcal{Z}(\beta)
$$
$$
	\left< E \right> = -\frac{ \partial \log \mathcal{Z} }{ \partial \beta }
$$
$$
	\beta = \frac{1}{k_{B}T}
$$
$$
	\text{var}(E) = \frac{ \partial^2 \log \mathcal{Z} }{ \partial \beta^2 }
$$
$$
	C=k_{B} \beta^{2} \frac{ \partial^2  }{ \partial \beta^2 } \log \mathcal{Z}
$$
$$
	\frac{p^*_{a}}{p^*_{b}} = e^{ -(E_{a}-E_{B})/k_{B}T }
$$
- Copy the tables from page 72
$$
	\mathcal{Z} = \mathcal{Z}_{\mu}\mathcal{Z}_{\nu}
$$
$$
	\mathcal{Z}_{N} = \mathcal{Z}^N_{1} \implies \log\mathcal{Z}_{N} = N \log \mathcal{Z}_{1}
$$
$$
	\left< E \right> \to N\left< E \right> \qquad \left< s \right> _\text{max} \to N \left< s \right> _\text{max}
$$
$$
	\sigma(E) \to \sqrt{ N }\sigma(E)
$$
$$
	F \equiv  -\frac{1}{\beta} \log \mathcal{Z}
$$
$$
	d\left< W \right> = \left( \frac{ \partial F }{ \partial b }  \right)_{T} \, db
$$
$$
	\mathcal{Z}_{en}(\beta, \lambda) = \sum_{(i, j)} \lambda ^{j}e^{ -\beta E(i, j) }
$$
$$
	p^*(i, j) = \frac{\lambda ^{j}e^{ -\beta E(i, j) }}{\mathcal{Z}_{en}}
$$
$$
	\gamma=-\beta \mu \qquad \lambda=e^{ \beta \mu }
$$
$$
	\left< s \right> _\text{max} = \beta \left< E \right> - \beta \mu \left< N \right> + \log \mathcal{Z}_{en}(\beta, \mu)
$$
$$
	\left< N \right> = \lambda \frac{ \partial  }{ \partial \lambda } \log \mathcal{Z}_{en}
$$
$$
	\left< N^{2} \right> = \frac{\lambda^{2}}{\mathcal{Z}_{en}} \frac{ \partial^2 \mathcal{Z}_{en} }{ \partial \lambda^2 }
$$
$$
	dS = \frac{1}{T} \, d\left< E \right> - \frac{\mu}{T} \, d\left< N \right>
$$
$$
	p^*_{i} = \frac{e^{ -\beta(E_{i}-\mu ^{a}N^a_{i}-\mu^b N^b_{i}) }}{\mathcal{Z}_{en}}
$$
$$
	\left< s \right> _\text{max} = \beta \left< E \right> -\beta \mu^a \left< N^a \right>  - \beta \mu^b \left< N^b \right> +\log \mathcal{Z}_{en}(\beta, \mu^a, \mu^b)
$$
- Energy flows from higher to lower temperature
- Particles flow from higher to lower chemical potential
# Applications
$$
	\left< N(\epsilon) \right> = \frac{1}{e^{ \beta(\epsilon-\mu) }\pm 1} \to \lambda e^{ -\beta\epsilon }
$$
Small occupation limit
$$
	\left< N \right> = \sum_{i} \lambda e^{ -\beta E(i) }
$$
$$
	\left< E \right> = -\lambda \frac{ \partial  }{ \partial \beta } \frac{\left< N \right> }{\lambda}
$$
$$
	\lambda = e^{ \beta \mu } = \frac{\left< N \right> }{V} \left( \frac{h^{2}}{2\pi mk_{B}T} \right)^{3/2}
$$
$$
	\frac{S}{k_{B}} = \left< N \right> \left[ \log\left( \frac{V\left< E \right> ^{3/2}}{\left< N \right> ^{5/2}} \right) + \frac{3}{2}\log\left( \frac{4\pi m}{3h^{2}} \right) + \frac{5}{2} \right]
$$
Sackur-Tetrode Formula
$$
	\#F-\#C+\#P=2
$$
$$
	\frac{\Delta \left< S \right> }{M} = \frac{L}{T_{pt}}
$$
Where $M$ is the mass of the material, $L$ is latent heat, and $T_{pt}$ is the temperature of the phase transition.
$$
	\Delta S = Nk_{B} \log\left( \frac{V_{f}}{V_{i}} \right)
$$
---
$$
	\begin{matrix}
	e^{ \beta\epsilon/2 } & -\frac{\epsilon}{2} & 2\left( 1+\frac{\beta^{2}\epsilon^{2}}{8} \right) & -\frac{1}{4}\beta\epsilon^{2}\to 0 \\
	1+e^{ -\beta\epsilon } & \epsilon e^{ -\beta\epsilon } \to 0 & \frac{1}{\beta\epsilon} & \frac{1}{\beta} \\
	1+2e^{ -\beta\epsilon } & 2\epsilon e^{ -\beta\epsilon } \to 0 & \sqrt{ \frac{\pi}{\beta\epsilon} } & \frac{1}{2\beta} \\
	e^{ -\beta\epsilon } & \epsilon & \frac{1}{2}\sqrt{ \frac{\pi}{\beta\epsilon} } & \frac{1}{2\beta}
	\end{matrix}
$$
