# Inclusion-Exclusion Principle
The combined probability of a union of events is:
$$
	P(A_{1}\cup\dots \cup A_{n}) = \sum_{k=1}^{n} \sum_{i_{1}<\dots<i_{k}} (-1)^{k+1}P(A_{i_{1}} \cap\dots \cap A_{i_{k}})
$$
For two and three events, for example,
$$
	P(A_{1}\cup A_{2}) = P(A_{1}) + P(A_{2}) - P(A_{1}\cap A_{2})
$$
$$
	P(A_{1}\cup A_{2}\cup A_{3}) = P(A_{1}) + P(A_{2}) + P(A_{3}) - P(A_{1}\cap A_{2}) - P(A_{1}\cap A_{3}) - P(A_{2}\cap A_{3}) + P(A_{1}\cap A_{2}\cap A_{3})
$$
## Locks and Keys
If you have three unique pairs of locks and keys but you do not know which key opens which lock and each key can only be used once, you decide to test your luck, what is the probability that none of the locks can be opened?

You could try to compute the probability none of them open, or find the conjugate for opening one lock.

We are therefore interested the probability of opening lock 1, 2, or 3. Applying the inclusion-exclusion principle you find:
$$
	P(\text{One lock}) = \frac{1}{3} + \frac{1}{3} + \frac{1}{3} - \frac{1}{6} - \frac{1}{6} - \frac{1}{6} + \frac{1}{6} = \frac{2}{3}
$$
So the probability of opening none of the locks is 1/3
# Conditional Probability
The probability of an event $A$ occurring, given that another event $C$ occurred. This is called the probability of $A$ conditioned on $C$.

The conditional probability of $A$ given $C$ is,
$$
	P(A|C) = \frac{P(A\cap C)}{P(C)}
$$
With a little algebra, we also find,
$$
	P(A\cap C) = P(A|C)P(C)
$$
This is called the multiplication rule.
## Unfair Coin
Suppose you have a fair coin and an unfair coin such that the probability of getting a tail is $p\neq 0.5$. If you randomly picked a coin from the two and you get a tail, what is the probability that the coin is unfair?
$$
	\begin{align}
	P(\text{unfair} | \text{tail}) & = \frac{P(\text{unfair and tails})}{P(\text{tails})} \\
	 & = \frac{P(\text{unfair and tails})}{P(\text{unfair and tails}) + P(\text{fair and tails})} \\
	 & = \frac{0.5p}{0.5p + 0.5^{2}} \\
	 & = \frac{p}{p+0.5}
	\end{align}
$$
# The Law of Total Probability
Suppose $C_{1},\dots,C_{m}$ are disjoint events such that $C_{1}\cup\dots \cup C_{m}=\Omega$. For any arbitrary event $A$, the Law of Total Probability states that:
$$
	P(A) = \sum_{i=1}^{m} [P(A|C_{i})P(C_{i})]
$$
Which essentially states that it is possible to find the probability $A$ will occur by partitioning it according to a set of disjoint scenarios.
# Bayes’ Rule
A result derived from the law of total probability, and the multiplication rule.

Suppose $C_{1}, \dots, C_{m}$ are disjoint events such that $C_{1}\cup\dots \cup C_{m}=\Omega$. The conditional probability of $C_{i}$ given an arbitrary events $A$ is:
$$
	P(C_{i}|A) = \frac{P(A|C_{i})P(C_{i})}{\sum_{i=1}^{m} [P(A|C_{i})P(C_{i})]}
$$
## 2 Fair Coins and 1 Unfair Coin
Suppose you have two fair coins and one unfair coin with probability $p\neq 0.5$ of landing head. You randomly choose two coins and flip them. As a result, you have two heads. What is the probability that you have chosen an unfair coin?

According to the definition of conditional probability, we have:
$$
	P(\text{unfair} | H H) = \frac{P(\text{unfair} \cap H H)}{P(H H)}
$$
The probability of getting two heads is,
$$
	P(H H) = \begin{pmatrix}
	3 \\
	2
	\end{pmatrix}^{-1} \left[ \frac{1}{2^{2}} + 2\left( \frac{p}{2} \right) \right] = \frac{1+4p}{12}
$$
And the probability of getting two heads, assuming we have the unfair coin is:
$$
	\begin{pmatrix}
	3 \\
	2
	\end{pmatrix} \left[ 2\left( \frac{p}{2} \right) \right] = \frac{p}{3}
$$
Therefore,
$$
	\frac{p /3}{(1+4p)/12} = \frac{4p}{1+4p}
$$
- The answer to this question doesn't use Bayes' formula at all, but it's written in this section in the slides
# Independence
Event $A$ is *independent* of $B$ if $P(A|B)=P(A)$. That is, the occurrence of $B$ has no effect on the probability of $A$.

Equivalent definitions of independence:
$$
	P(A|B) = P(A) \iff P(A\cap B) = P(A)P(B) \iff P(B|A) = P(B)
$$
$A$ can be replaced with $A^{c}$, $B$ with $B^{c}$, or both.

Note that two disjoint events cannot be independent.

Definitions:
> A collection of events $A_{1}, \dots, A_{m}$ is called *mutually independent* if the multiplication rule holds for every finite subgroup of events in the collection.

> That is, for any distinct indices $i_{1}, \dots, i_{k}\in \{ 1, 2, \dots, m \}$,
$$
	P(A_{i_{1}}\cap\dots \cap A_{i_{k}}) = P(A_{i_{1}})\dots P(A_{i_{k}})
$$

> A collection of events is called *pairwise independent* if every pair of events is independent.
$$
	P(A_{i}\cap A_{j}) = P(A_{i})P(A_{j})
$$
> Where $i\neq j$.

Notably, mutual independence implies pairwise independent, but the converse is not always true.