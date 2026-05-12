# Monty Hall
We begin this course by introducing the Monty Hall Dilemma.

Suppose we are playing a game show. There are 3 doors. Behind 1 is a car, and beyond 2 are goats.

The game is as follows:
1. Choose door 1
2. The host will open another door, always revealing a goat
3. You are given the opportunity to switch

Notably, the car is equally likely to be behind any of the doors, and the host knows where the car is, and so will always intentionally choose to reveal a goat.

Intuitively, because one door has been revealed, it may seem like there is a 50/50 chance to find a car, regardless of your choice. However, drawing out a table...
![[Pasted image 20260505120938.png]]
reveals that switching gives us a 2/3 chance to win the car, whereas staying gives us a 1/3 chance.
# Outcomes, Sample Space, and Events
Definitions:
> *(Random) experiment* refers to the general phenomena where the *outcomes* are unpredictable, or random.

> A *sample space* $\Omega$ is the collection of all possible outcomes from an experiment

> An *event* is a subset of the sample space

I don't feel like writing out the examples presented in lecture. It's not worth my time. Just refer to the slides.
# Basic Set Theory
An event that satisfies $A$ or $B$ is equivalent to the union $A\cup B$.

$A$ and $B$ is equivalent to the intersection $A\cap B$.

The event that does not satisfy $A$ is the complement $A^{c}$. The complement is a special case of the set minus operation $\Omega\setminus A$.

Two events are called disjoint or mutually exclusive if they have no outcomes in common. That is $A\cap B=\emptyset$.

If all outcomes of $A$ lie within $B$, then $A\subseteq B$, or $A\implies B$. The intersection between the two is $A\cap B=A$.
## De Morgan’s Law
States that the following are equivalent:
$$
(A\cup B)^{c} \equiv A^{c}\cap B^{c} \qquad (A\cap B)^{c} \equiv A^{c}\cup B^{c}
$$
# Probability Measure
> The *probability measure* $P$ defined on a sample space $\Omega$ is a function of any event $A\subseteq \Omega$ such that,
- $0\leq P(A)\leq 1$
- $P(\Omega)=1$
- $P(A\cup B)=P(A)+P(B)$ if $A$ and $B$ are disjoint
> The number $P(A)$ is called the *probability* that $A$ occurs.

Note that for all cases where $A$ implies $B$, $A$ must be less likely.
$$
	A\subseteq B \implies P(A)<P(B)
$$
If $A$ and $B$ are not disjoint, then the probability of a union is,
$$
	P(A\cup B) = P(A) + P(B) - P(A\cap B)
$$
And the probability of the complement is,
$$
	P(A^{c}) = 1-P(A)
$$
In general, within a finite sample space, it is usually easy enough to compute the probability by counting:
$$
	P(A) = \frac{\text{number of outcomes that belong to }A}{\text{total number of outcomes in }\Omega} = \frac{\lvert A \rvert }{\lvert \Omega \rvert }
$$
# Product of Sample Spaces
The sample space of multiple experiments is the Cartesian product of the sample spaces for the individual experiments.

For example, in the case of two experiments:
$$
	\omega = \Omega_{1} \times \Omega_{2} = \{ (\omega_{1},\omega_{2}) : \omega_{1}\in \Omega_{1}, \omega_{2}\in \Omega_{2} \}
$$
In the case of tossing a fair coin twice, we might have:
$$
	\Omega_{1}=\Omega_{2}=\{ H, T \}
$$
Therefore,
$$
	\Omega=\Omega_{1}\times \Omega_{2} = \{ H, T \} \times \{ H, T \} = \{ (H, H), (H, T), (T, H), (T, T) \}
$$
If the probability of lands on heads for each of the coins is $p$ and $q$, respectively, then $P((H, H))=pq$.
# Combinatorial Analysis
Let $S$ be a set of length-$k$ sequences. If there are $n_{1}$ possible first entries, $n_{2}$ possible second entries for each first entry... and so on, then there are a total of $n_{1}n_{2}\dots n_{k}$ possible outcomes.

For example, the number of permutations for 1234 is $4\times 3\times 2\times 1=4!$.

Permutation:
> A *permutation* is a rearrangement of objects into distinct sequences (order matters). There are:
$$
	\frac{n!}{n_{1}!n_{2}!\dots n_{r}!}
$$
> different permutations for $n=n_{1}+n_{2}+\dots+n_{r}$ objects, where $n_{1}$ are alike, $n_{2}$ are alike and so on.


Combination:
> A *combination* is an unordered collection of objects (order doesn't matter). There are:
$$
	\begin{pmatrix}
	n \\
	r
	\end{pmatrix} = \frac{n!}{(n-r)!r!}
$$
> different combinations of $n$ distinct objects taken $r$ at a time. That is, pick $r$ from $n$.

Furthermore, it is possible to prove that,
$$
	\begin{pmatrix}
	n \\
	r
	\end{pmatrix} = \begin{pmatrix}
	n \\
	n-r
	\end{pmatrix}
$$
Which reflects what we would physically expect.
# The Birthday Problem
Suppose each person is equally likely to be born on any of the 365 days of the year (excluding February 29). What is the probability that in a group of ten people, no two people share the same birthday?

The probability for each person can be roughly modelled as:
$$
	\frac{365}{365} \times \frac{365-1}{365} \times \frac{365-2}{365} \times \dots
$$
Which is equivalent to,
$$
	P = \frac{365\times 364 \times 363 \times \dots}{365^{10}} = \frac{365!}{(365-10)!(365^{10})} \approx 0.883
$$
Which also consequently implies that, in a room with 10 people, there is roughly a 11.7% chance that two people share a birthday.
# Poker Hands
There are 52 cards in a deck. Each card has a value and belongs to a suit. There are 13 values: {1,2,3,4,5,6,7,8,9,10,J,Q,K}, and 4 suits: {space, club, heart, diamond}. In each hand, there are 5 cards.

How many different hands of a five-card draw are there?
$$
	\begin{pmatrix}
	52 \\
	5
	\end{pmatrix} = 2598960
$$
How many different hands with a four-of-a-kind?
$$
	\begin{pmatrix}
	13 \\
	1
	\end{pmatrix} \begin{pmatrix}
	48 \\
	1
	\end{pmatrix} = 13 \times 48=624
$$
Recall that, in this case, order does not matter. This hand is composed of a 4-of-a-kind, and some other card. First, we pick 1 value from the 13 values, and then pick 1 card from the remaining 48 cards.

The possibility of drawing a four-of-a-kind is therefore:
$$
	\frac{624}{2598960} = \frac{1}{4165} \approx 0.00024
$$
What about a full house?
$$
	\begin{pmatrix}
	13 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	3
	\end{pmatrix} \begin{pmatrix}
	12 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix}
$$
So, reading off, we: Pick 1 suit, and then pick 3 from the 4 possibilities; then pick 1 suit from the remaining 12, and pick 2 cards from the 4 possibilities.

Two pairs?
$$
	\begin{pmatrix}
	13 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix} \begin{pmatrix}
	12 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix} \begin{pmatrix}
	11 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	1
	\end{pmatrix} = \begin{pmatrix}
	13 \\
	2
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix}^{2} \begin{pmatrix}
	11 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	1
	\end{pmatrix}
$$
Which follows the same line of logic as the above.
# Climbing Stairs
Suppose there are 10 stairs, you can climb either 1 stair or 2 stairs at a time. How many different ways can you reach the top of the stairs (without overextending)?

Let $n_{1}$ be the number of 1-stair steps and $n_{2}$ be the number of 2-stair steps. The possibilities are:
$$
	(n_{1},n_{2}) = (10,0), (8, 1), (6,2), (4,3), (2,4), (0,5)
$$
The number of permutations in each case is:
$$
	\frac{(n_{1}+n_{2})!}{n_{1}!n_{2}!}
$$
If you sum over all the possible cases, you will find that there are 89 ways to climb the stairs.
