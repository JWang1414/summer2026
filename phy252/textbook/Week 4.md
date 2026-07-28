# From one to many
Lets say we are now interested in seeing how the pigeons behaves returning to the pigeonholes a number of times. For just a single trip, we have the two possibilities: $p_{1}(L)$ and $p_{1}(R)$. However with two trips the sample space expands into $\Sigma_{2}=\{ L L, LR, RL, RR \}$. Our task is to define a new probability function $p_{2}$ for this sample space.

It is tempting to claim $p_{2}(LL)=p_{1}(L)p_{1}(L)$. However, this is not always true. Generally speaking, the probability is:
$$
	p_{2}(ba) = \tilde{p}(b|a)p_{1}(a)
$$
Where $\tilde{p}(b|a)$ is the conditional probability, the chance of $b$ occurring given that $a$ has already occurred.

Iff the conditional probability $\tilde{p}(b|a)=q(b)$ for some function $q$, the probability of measuring $b$ on the second trial doesn't depend on the outcome of the first trial. The two trials are said to be independent.

The probability of an outcome from $n$ repeated trials is:
$$
	p_{n}(a_{n}\dots a_{1}) = \tilde{p}(a_{n}|a_{n-1}\dots a_{1}) \dots \tilde{p}(a_{2}|a_{1}) p_{1}(a_{1})
$$
In the case of independent identically distributed trials, this simplifies to:
$$
	p_{n}(a_{n}\dots a_{1}) = p_{1}(a_{n}) p_{1}(a_{n-1}) \dots p_{1}(a_{2})p_{1}(a_{1})
$$
