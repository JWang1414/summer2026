# Question 1
---
a.
Recall that $\Delta V=0\implies W=0$.

Work done:
$$
	W_{1} = -P_{1}(V_{2}-V_{1}) = -P_{1}(2V_{1}-V_{1}) = -P_{1}V_{1}
$$
$$
	W_{2} = -P_{2}(V_{1}-V_{2})=-\frac{P_{1}}{2}(V_{1}-2V_{1}) = \frac{1}{2}P_{1}V_{1}
$$
Net work:
$$
	W_\text{net} = \left( -1+\frac{1}{2} \right)P_{1}V_{1} = -\frac{1}{2}P_{1}V_{1}
$$
The area of the box is:
$$
	A = \left( P_{1}-\frac{P_{1}}{2} \right)(2V_{1}-V_{1}) = \frac{1}{2}P_{1}V_{1}
$$
Which is equivalent to the absolute value of the work extracted from the gas.
- It's true because you can split any cycle into a number of infinitesimally small squares. Since it's true for this square, we can just apply this to everything
---
b.
Calculate the temperature:
$$
	T_{0} = \frac{P_{1}V_{1}}{Nk_{B}} \qquad T_{1} = \frac{P_{1}V_{2}}{Nk_{B}} = \frac{2P_{1}V_{1}}{Nk_{B}} = 2T_{0}
$$
$$
	T_{2} = \frac{P_{2}V_{2}}{Nk_{B}} = \frac{1}{2} \times 2 \times \frac{P_{1}V_{1}}{Nk_{B}} = T_{0}
$$
$$
	T_{3} = \frac{P_{2}V_{1}}{Nk_{B}} = \frac{T_{0}}{2}
$$
Changes in temperature:
$$
	\Delta T_{1} = T_{0} \qquad \Delta T_{2} = -T_{0} \qquad \Delta T_{3} = -\frac{T_{0}}{2} \qquad \Delta T_{4} = \frac{T_{0}}{2}
$$
Heat:
$$
	Q_{1} = C_{P}(\Delta T_{1}) = \frac{5}{2} Nk_{B}T_{0} = \frac{5}{2}P_{1}V_{1}
$$
$$
	Q_{2} = C_{V}(\Delta T_{2}) = \frac{3}{2}Nk_{B}(-T_{0}) = -\frac{3}{2}P_{1}V_{1}
$$
$$
	Q_{3} = C_{P}(\Delta T_{3}) = -\frac{5}{4} P_{1}V_{1}
$$
$$
	Q_{4} = C_{V}(\Delta T_{4}) = \frac{3}{4}P_{1}V_{1}
$$
Heat in and out:
$$
	Q_\text{in} = \frac{13}{4}P_{1}V_{1} \qquad Q_\text{out} = \frac{11}{4}P_{1}V_{1}
$$
Therefore:
$$
	\eta = \frac{W_\text{net}}{Q_\text{in}} = \frac{1 /2}{13 /4} = \frac{2}{13} \approx 0.15
$$
$$
	\text{COP} = \frac{Q_\text{out}}{W_\text{in}} = \frac{11 /4}{1 /2} = \frac{11}{2} = 5.5
$$
# Question 2
Isothermal so $\Delta W=-\Delta Q$
$$
	W = Nk_{B}T \log r
$$
$$
	\Delta S = -Nk_{B}\log r \approx -24.7
$$
# Question 3
---
a.
$$
	\frac{ \partial S }{ \partial \left< E \right>  } = A \left< V \right> ^{1/4} \left( \frac{3}{4} \right) \left< E \right> ^{-1/4} = \frac{1}{T}
$$
$$
	\left( \frac{3A}{4} \right)^{4} \frac{V}{E} = \frac{1}{T^{4}} \implies \left< E \right> = \left( \frac{3A}{4} \right)^{4} V T^{4}
$$
As needed.

---
b.
$$
	\frac{ \partial S }{ \partial \left< V \right>  } = \frac{A}{4} \left< V \right> ^{-3/4} \left< E \right> ^{3/4} = \frac{P}{T} = P \left[ A \left< V \right> ^{1/4} \left( \frac{3}{4} \right) \left< E \right> ^{-1/4} \right]
$$
$$
	\frac{1}{4} \left< E \right> = P \left< V \right> \left( \frac{3}{4} \right) \implies \left< E \right> = P\left< V \right> (3)
$$
$$
	P\left< V \right> = \frac{1}{3}\left< E \right>
$$
---
c.
$$
	P = \frac{1}{3} \frac{\left< E \right> }{\left< V \right> } \approx \frac{10^{6}}{3}
$$
So about 3.29 atm of pressure
# Question 4
---
a.
$$
	A=\frac{1}{n}
$$
---
b.
$$
	\left< s \right> =- \sum p(i) \log p(i) = - \sum \frac{1}{n} \log\left( \frac{1}{n} \right)
$$
$$
	\frac{1}{n} \log n \sum_{i=1}^{n} 1 = \log n
$$
---
c.
$$
	\left< x(k) \right> = \sum p(k)x(k) = \frac{1}{n} \sum_{k=1}^{n} k = \frac{1}{n} \frac{n(n+1)}{2} = \frac{n+1}{2}
$$
---
d.
$$
	\left< x^{2} \right> = \sum_{k=1}^{n} k^{2} \left( \frac{1}{n} \right) = \frac{1}{n} \sum_{k=1}^{n} k^{2} = \frac{1}{n} \frac{n(n+1)(2n+1)}{6}
$$
$$
	\left< x^{2} \right> = \frac{(n+1)(2n+1)}{6}
$$
$$
	\text{var}(x) = \left< x^{2} \right> - \left< x \right> ^{2} = \frac{(n+1)(2n+1)}{6} - \left[ \frac{n+1}{2} \right] ^{2}
$$
# Question 5
---
a.
$$
	\sum_{k=0}^{\infty} A \frac{r^{k}}{k!} = A e^{ r } = 1 \implies A = \frac{1}{e^{ r }}
$$
---
b.
$$
	\left< x \right> = \sum_{k=0}^{\infty} k \frac{1}{e^{ r }} \frac{r^{k}}{k!} = \frac{1}{e^{ r }} \sum_{k=0}^{\infty} \frac{r^{k}}{(k-1)!} = \frac{1}{e^{ r }} (e^{ r }r) = r
$$
---
c.
$$
	\left< s \right> =- \sum_{k=0}^{\infty} \frac{1}{e^{ r }} \frac{r^{k}}{k!} \log \left( e^{ r } \frac{k!}{r^{k}} \right)
$$
$$
	\log e^{ r } + (\log k! - \log r^{k}) = r + \log k! - k\log r
$$
$$
	-\frac{1}{e^{ r }} \left[ \sum_{k=0}^{\infty} \frac{r^{k+1}}{k!} + \sum_{k=0}^{\infty} \frac{r^{k}}{k!}\log k! - \log r \sum_{k=0}^{\infty} \frac{r^{k}}{(k-1)!} \right]
$$
$$
	-\frac{1}{e^{ r }} \left[ re^{ r } + \sum_{k=0}^{\infty} \frac{r^{k}}{k!}\log k! -r \log r e^{ r } \right]
$$
$$
	r\log r -r - \frac{1}{e^{ r }} \sum_{k=0}^{\infty} \frac{r^{k}}{k!}\log k!
$$
- I have no idea how to complete this computation
# Question 7
Pigeon A picks from 1, 2, 3, 5, 7. Pigeon B picks from 1, 2, 4, 8.

Pigeon A has the higher surprise, because there is 1 more choice.