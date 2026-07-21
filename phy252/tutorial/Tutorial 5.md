# Question 2
The amount of work done here is:
$$
	W = Nk_{B}T \log r \implies Q=-Nk_{B}T \log r
$$
$$
	\Delta S = \frac{\Delta Q}{T} = -Nk_{B}\log r \approx -24.73
$$
- The sign might by off here? $\Delta S$ is supposed to be always positive
- It's possible $r$ is supposed to be 1/6 as opposed to 6
# Question 3
---
a.
$$
	\frac{1}{T} = \left( \frac{ \partial S }{ \partial \left< E \right>  }  \right)_{\left< V \right> } = A \left< V \right> ^{1 /4} \left( \frac{3}{4} \left< E \right> ^{-1 /4} \right) = \frac{3}{4}A \left< V \right> ^{1/4} \left< E \right> ^{-1/4}
$$
$$
	\frac{1}{T^{4}} = \left( \frac{3}{4}A \right)^{4} \frac{\left< V \right> }{\left< E \right> } \implies \left< E \right> = \left( \frac{3}{4}A \right)^{4}\left< V \right> T^{4}
$$
Therefore $\left< E \right>\propto VT^{4}$ as needed.

---
b.
$$
	\frac{P}{T} = \left( \frac{ \partial S }{ \partial \left< V \right>  }  \right)_{\left< E \right> } = \frac{1}{4}A \left< V \right> ^{-3/4} \left< E \right> ^{3/4}
$$
$$
	P \left( \frac{3}{4}A \left< V \right> ^{1/4} \left< E \right> ^{-1/4} \right) = \frac{1}{4}A \left< V \right> ^{-3/4} \left< E \right> ^{3/4}
$$
$$
	\frac{3}{4}AP \left< V \right>  = \frac{1}{4}A \left< E \right> \implies P\left< V \right> = \frac{1}{3}\left< E \right>
$$
As needed.

---
c.
$$
	P = \frac{1}{3} \frac{\left< E \right> }{\left< V \right> } = \frac{1}{3} \frac{1}{10^{-6}} = \frac{10^{6}}{3}
$$
Convert to atmospheres to find the pressure is about 3.29 atm
# Question 1
---
a.
There is no work done when $\Delta V=0$.

The work done during step A is $P_{1}(V_{1}-V_{2})$. The work done during step C is $P_{3}(V_{2}-V_{1})$.

So the total work done during this cycle is:
$$
	P_{1}(V_{2}-V_{1}) + P_{3}(V_{1}-V_{2}) = (P_{1}-P_{3})(V_{2}-V_{1})
$$
Which is the area enclosed by the cycle.

Since $P_{3}=P_{1} /2$ and $V_{2}=2V_{1}$ this works out to be:
$$
	\left( \frac{P_{1}}{2} \right)(V_{1}) = \frac{P_{1}V_{1}}{2}
$$

---
b.
The initial temperature is:
$$
	T_{1} = \frac{P_{1}V_{1}}{Nk_{B}}
$$
The temperature after step A is:
$$
	T_{2} = 2T_{1}
$$
After step B:
$$
	T_{3}=T_{1}
$$
After step C:
$$
	T_{4}=\frac{T_{1}}{2}
$$
And then it goes back to $T_{1}$ again.

The heat transfer during step A is:
$$
	\Delta Q = C(\Delta T) = \frac{5}{2}Nk_{B}T_{1}
$$
During step B:
$$
	\Delta Q = -\frac{3}{2}Nk_{B}T_{1}
$$
During step C:
$$
	\Delta Q = \frac{5}{2} Nk_{B} \left( -\frac{T_{1}}{2} \right) = -\frac{5}{4} Nk_{B}T_{1}
$$
During step D:
$$
	\Delta Q = \frac{3}{2} Nk_{B}\left( \frac{T_{1}}{2} \right) = \frac{3}{4} Nk_{B}T_{1}
$$
The heat input is:
$$
	\left( \frac{5}{2} + \frac{3}{4} \right) Nk_{B}T_{1} = \frac{13}{4} P_{1}V_{1}
$$
The efficiency of the engine is:
$$
	\eta= \frac{\lvert W_\text{net} \rvert }{Q_\text{in}} = \frac{P_{1}V_{1}}{2} \left( \frac{4}{13P_{1}V_{1}} \right) = \frac{2}{13} \approx 0.154
$$
The heat output is:
$$
	\left( \frac{5}{4} + \frac{3}{2} \right)Nk_{B}T_{1} = \frac{11}{4} P_{1}V_{1}
$$
The COP of the refrigerator is:
$$
	\text{COP} = \frac{Q_\text{out}}{W_\text{net}} = \frac{11}{4} P_{1}V_{1} \left( \frac{2}{P_{1}V_{1}} \right) = \frac{11}{2}
$$
- I don't think this number is supposed to be greater than 1
---
c.
The work done during step C is:
$$
	P_{3}(V_{2}-V_{1}) = \frac{P_{1}}{2}(2V_{1}-V_{1}) = \frac{1}{2}(2-1)P_{1}V_{1} = \frac{P_{1}V_{1}}{2} = 10^{6}
$$
So 1 MJ of work done.
- I also feel like this answer is wrong, because I don't use the provided value for $T_{1}$
