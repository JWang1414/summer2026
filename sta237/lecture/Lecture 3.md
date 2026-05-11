# Amoeba Population
In the beginning, there is just one amoeba. For each generation, it undergoes the following process: 1/6 chance of dying, 1/3 chance of doing nothing and 1/2 chance of dividing into two. Assume, every amoeba undergoes such process independently, what is the probability of extinction?

Call $P$ the probability of extinction
$$
	P=P(\text{extinction})
$$
The probability for extinction will depend on itself. It recurs.
$$
	p=\frac{1}{6} + \frac{p}{3} + \frac{p^{2}}{2}
$$
The 1/6 arises from the amoeba dying immediately. The 1/3 is when the amoeba does nothing, but once again rolls the possibility for extinction. The 1/2 is the chance of dividing into two. Notably, it is rolled twice, because the amoeba has divided into two.

Solve this equation to find $p=1 /3$.
# Coin Flip
Two people take turns to flip a fair coin. If whoever first lands a head wins, is it better to flip first? What is the winning probability for the person who flips first?

The probability to win on the first round is 1/2, and the probability to win on subsequent turns is $1 /2 \times 1 /2$. Which arises because the other player must flip tails before you get a chance to flip again.
$$
	p = \frac{1}{2} + \frac{1}{2} \frac{1}{2}p = \frac{1}{2} + \frac{p}{4}
$$
Which results in $p=2 /3$ if you are the first player to flip. A higher chance than the second player.
# Discrete Random Variables
Random variable:
> Let $\Omega$ be a sample space. A *random variable* $X$ is a function that maps the sample space $\Omega$ to real numbers $\mathbb{R}$. That is, $X:\Omega\to \mathbb{R}$.

Discrete random variable:
>Let $\Omega$ be a sample space. A *discrete random variable* is a function $X:\Omega\to \mathbb{R}$ that takes on a finite number of values $a_{1}, \dots, a_{n}$ or an infinite number of values $a_{1}, a_{2}, \dots$

For example, suppose we toss three coins. The sample space is,
$$
	\Omega = \{ HHH, HHT , HTH, THH, HTT , THT , TTH, TTT \}
$$
If $X$ is the number of heads in the three tosses, $X$ assigns a real number to each outcome $\omega$.
$$
	X(\omega=\text{HHT}) = 2
$$
The event when we get exactly two heads can be written as:
$$
	\{ X=2 \} = \{ \omega \in \Omega : X(\omega)=2 \}
$$
Which reads as: a subset of events $\omega$ in $\Omega$ such that the number of heads is 2.

In this example, it is easy enough to see,
$$
	P(X=2) = \frac{3}{8} \qquad P(X\leq 1) = \frac{4}{8} = \frac{1}{2}
$$
# Independent Random Variables
Intuition: Random variables $X$ and $Y$ are independent if knowing the value of one does not change the probabilities for the other.

Independence of Discrete Random Variables:
> Discrete random variables X and Y are independent, denoted by
$$
	X\perp Y
$$
> if for all possible values of $x$ and $y$
$$
	P(X=x, Y=y) = P(X=x)P(Y=y)
$$
> Or,
$$
	P(X=x | Y=y) = P(X=x) \qquad \text{when } P(Y=y)>0
$$

Independent Collection of Discrete Random Variables:
>A collection of discrete random variables, such as an infinite sequence, is independent if for all finite subgroups $X_{1}, \dots, X_{k}$ of the collection,
$$
	P(X_{1}=x_{1}, \dots, X_{k}=x_{k}) = P(X_{1}=x_{1})\dots P(X_{k}=x_{k})
$$
>for all possible values $x_{1}, \dots, x_{k}$

Independent Random Variables:
>Random variables $X$ and $Y$ are independent if for all $A,B\subseteq \mathbb{R}$
$$
	P(X\in A, Y\in B) = P(X\in A)P(Y\in B)
$$
## Distribution of Random Variables
Generally speaking, we are interested in the possible values of a random variable, and the probability associated with each value.

The collection of these values is the *distribution* of the random variable. For a discrete random variable, the distribution is determined by the *probability mass function* (PMF) or the *cumulative distribution function* (CDF).

- I stopped writing notes here because it were taking too long. Finish this later. I'll write down anything that can't be found in the slides