# Joint Distributions
> In the case of two random variables $X$ and $Y$, a *joint distribution* specifies the values and probabilities for all pairs of outcomes. The *joint PMF* of $X$ and $Y$ is a function of two variables $P(X=x, Y=y)$

If $X$ takes values in a set $S$ and $Y$ takes values in a set $T$ then:
$$
	\sum_{x \in S} \sum_{y \in T} P(X=x, Y=y)=1
$$
$$
	\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x, y) \, dx  \, dy =1
$$
The probabilities of events are obtained in the familiar manner:
$$
	P(X\in A, Y\in B) = \sum_{x_{i}\in A} \sum_{y_{j}\in B}P(X=x_{i}, Y=y_{j})
$$
$$
	P((X, Y)\in S) = \iint_{S} f(x, y) \, dx \, dy
$$
Expanded to the case of $n$ variables, the joint PMF might be:
$$
	P(X_{1}=x_{1}, \dots, X_{n}=x_{n})
$$
$$
	P((X_{1}, \dots, X_{n})\in S) = \int\dots \int_{S} f(x_{1}, \dots, x_{n}) \, dx_{1} \, \dots \, dx_{m}
$$
# Marginal Distributions
> The marginal distribution or marginal PMF of $X$ is obtained from the joint distribution of $X$ and $Y$ by summing over the values of $Y$
$$
	\{ X=x \} = \bigcup_{y\in T} \{ X=x, Y=y \}
$$
> That is,
$$
	P(X=x) = P\left( \bigcup_{y\in T} \{ X=x, Y=y \} \right) = \sum_{y\in T}P(X=x, Y=y)
$$
> And vice versa to find the PMF for $Y$.

More succinctly expressed, we have:
$$
	P(X=x) = \sum_{y\in T}P(X=x, Y=y) \qquad P(Y=y) = \sum_{x \in S} P(X=x, Y=y)
$$
# Joint Cumulative Distribution Function
> If $X$ and $Y$ have joint density function $f$, the joint *cumulative distribution function* is:
$$
	F(x, y) = P(X\leq x, Y\leq y) = \int_{-\infty}^{x} \int_{-\infty}^{y} f(s, t) \, dt  \, ds
$$

Differentiating with respect to both $x$ and $y$ gives,
$$
	\frac{ \partial^{2} }{ \partial x \partial y } F(x, y) = f(x, y)
$$
## Uniform Distribution in Two Dimensions
> Let $S$ be a bounded region in the plane. Then random variables $(X, Y)$ are uniformly distributed on $S$ if the joint density function of $X$ and $Y$ is:
$$
	f(x, y) = \frac{1}{\text{Area}(S)} \qquad \text{for }(x, y)\in S
$$
> Notated as $(X, Y)\sim\text{Unif}(S)$
# Expectation of Function of Jointly Distributed Random Variables
> If $X$ and $y$ are discrete random variables with joint PMF $p(x, y)$, and $g(x, y)$ is a function of two variables, then:
$$
	E[g(x, y)] = \sum_{x} \sum_{y} g(x, y) p(x, y) \equiv  \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x, y)f(x, y) \, dx  \, dy
$$
# Independent Random Variables
If $X$ and $Y$ are independent random variables, the joint PMF has a particularly simple form.
$$
	P(X=x, Y=y) = P(X=x)P(Y=y)
$$
That is, for any set $A$ and $B$
$$
	P(X \in A, Y\in B) = P(X\in A)P(Y\in B)
$$
In the continuous case this becomes:
$$
	f(x, y) = f_{X}(x)f_{Y}(y)
$$
And the cumulative distribution function is:
$$
	F(x, y) = P(X\leq x, Y\leq y) = P(X\leq x)P(Y\leq y) = F_{X}(x)F_{Y}(y)
$$

If $X_{1}, \dots, X_{n}$ are jointly distributed with joint density function $f$, then the random variables are mutually independent if and only if
$$
	f(x_{1}, \dots, x_{n}) = f_{X_{1}}(x_{1}) \dots f_{X_{n}}(x_{n}) \qquad \forall x_{1}, \dots, x_{n}
$$
# Conditional Distribution
> Let $X$ and $Y$ be two random variables with joint PMF $p(x, y)$ and marginal $X$ PMF $p_{X}(x)$. The conditional probability mass function of $Y$ given $X$ is,
$$
	p_{Y|X}(y|x) = \frac{p(x, y)}{p_{X}(x)}
$$
> The same formula holds in both the discrete and continuous cases.

If $X$ and $Y$ are independent, then:
$$
	p_{Y|X}(y|x) = \frac{p(x, y)}{p_{X}(x)} = \frac{p_{X}(x)p_{Y}(y)}{p_{X}(x)} = p_{Y}(y)
$$
# Conditional Expectation
> Let $X$ and $Y$ be two random variables with conditional probability mass function $p_{Y|X}(y|x)$. Then the *conditional expectation* or *conditional mean* of $Y$ given $X=x$ is:
$$
	\mu_{Y|X=x} = E(Y|X=x) = \sum_{y}yp_{Y|X}(y|x) \equiv  \int_{-\infty}^{\infty} yf_{Y|X}(y|x) \, dy
$$

More generally, we have:
$$
	E(h(Y) | X=x) = \sum_{y}h(y)p_{Y|X}(y|x) \equiv  \int_{-\infty}^{\infty} h(y)f_{Y|X}(y|x) \, dy
$$
Similarly, the conditional variance is:
$$
	\sigma^{2}_{Y|X=x} \text{Var}(Y|X=x)= E[(Y-\mu_{Y|X=x})^{2}|X=x] = E[Y^{2}|X=x] - \mu^{2}_{Y|X=x}
$$
## Law of Total Expectation
For any two random variables $X$ and $Y$
$$
	E[E(Y|X)] = E(Y)
$$
## Law of Total Variance
For any two random variables $X$ and $Y$
$$
	\text{Var}(E(X|Y)) + E(\text{Var}(X|Y)) = \text{Var}(X)
$$
