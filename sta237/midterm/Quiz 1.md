# Question 1
![[Pasted image 20260531153840.png]]

The probability of rolling 3 increasing rolls is the same as rolling 3 different and increasing rolls.
$$
	\begin{align}
	 & = P(\text{increasing rolls}) \\
	 & = P(\text{different and increasing rolls}) \\
	 & = P(\text{different rolls})P(\text{increasing rolls} | \text{different rolls})
	\end{align}
$$
The chance of getting 3 different rolls is:
$$
	\frac{6\times 5\times 4}{6^{3}}
$$
The chance of them being in increasing order is $1 /3!$ since there are $3!$ possible permutations, and just one is in increasing order.

Final answer:
$$
	= \frac{6\times 5 \times 4}{6^{3}} \times \frac{1}{3!} = \frac{5}{54}
$$
![[Pasted image 20260531154555.png]]

After three rolls, the probability of rolling at least 3 is,
$$
	\left( \frac{4}{6} \right)^{3}
$$
Similarly, the probability of rolling at least 4 after 3 rolls is $(3 /6)^{3}$. Therefore, the probability of the smallest roll being exactly 3 is:
$$
	\left( \frac{4}{6} \right)^{3} - \left( \frac{3}{6} \right)^{3} = \frac{37}{216}
$$
