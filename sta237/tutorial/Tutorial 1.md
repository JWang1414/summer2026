# Poker Hands
## Question 1
How many different five-card hands are there?
$$
	\begin{pmatrix}
	52 \\
	5
	\end{pmatrix} = \frac{52!}{47!5!}
$$
It's a very big number
## Question 2
How many different hands contain a four-of-a-kind?

Pick one value from the 13 values. And then anything from the remaining 52-4 cards
$$
	\begin{pmatrix}
	13 \\
	1
	\end{pmatrix} \times \begin{pmatrix}
	48 \\
	1
	\end{pmatrix} = 13(48)
$$
## Question 3
What is the probability of drawing a hand with a four-of-a-kind?

Divide the two results.
$$
	13(48) \left( \frac{52!}{47!5!} \right)^{-1}
$$
## Question 4
How many different hands are full houses?

Pick out a triple, and then pick out a pair.
$$
	\begin{pmatrix}
	13 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	3
	\end{pmatrix} \times \begin{pmatrix}
	12 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix}
$$
## Question 5
How many different hands contain exactly two pairs?

Complete the same process as the above.
$$
	\begin{pmatrix}
	13 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix} \times \begin{pmatrix}
	12 \\
	1
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix} \times \begin{pmatrix}
	52-8 \\
	1
	\end{pmatrix} = \begin{pmatrix}
	13 \\
	2
	\end{pmatrix} \begin{pmatrix}
	4 \\
	2
	\end{pmatrix} ^{2} \begin{pmatrix}
	44 \\
	1
	\end{pmatrix}
$$
# Another Dice Problem
If you roll a fair six-sided die three times, what is the probability that the largest roll is exactly 4?

Note that the probability that the largest roll will be $k$ after $n$ rolls is:
$$
	P(\text{largest roll} \leq  k) = \left( \frac{k}{6} \right)^{n}
$$
Therefore, the probability that the largest roll will be exactly 4 is:
$$
	P(\text{exactly }4) = P(\text{largest roll}\leq 4) - P(\text{largest roll}\leq 3) = \left( \frac{4}{6} \right)^{3} - \left( \frac{3}{6} \right)^{3} = \frac{37}{216}
$$
# Free Throws
Suppose you are doing free throws. For the $k$-th throw, your chance of success is $m /k$ , where $m$ is the number of successful throws you have had before the $k$-th throw. If you throw $n$ times and you have already successfully landed the first throw, what is the probability of landing every throw?

Define the event that the $i$-th throw is successful as $A_{i}$. This question is asking,
$$
	P(A_{1}\cap\dots \cap A_{n}|A_{1})
$$
Given that you have landed the first free throw, what is the probability that you will land every single one?

According to the definition of conditional probability,
$$
	P(A_{1}\cap\dots \cap A_{n}|A_{1}) = \frac{P(A_{1}\cap\dots \cap A_{n})}{P(A_{1})}
$$
To determine the probability of hitting every free throw, notice that the probability of hitting just the first 2 is,
$$
	P(A_{1}\cap A_{2}) = P(A_{2}|A_{1}) P(A_{1})
$$
Now, imagine that $A_{1}\cap A_{2}$ is a single event. Then the probability of hitting the first 3 is,
$$
	P(A_{3} | A_{2}\cap A_{1})P(A_{1}\cap A_{2})  = P(A_{3} | A_{2}\cap A_{1})P(A_{2}|A_{1}) P(A_{1})
$$
Continuing the break down the probability in this manner, we have,
$$
	P(A_{1}\cap\dots \cap A_{n}) = P(A_{n}|A_{1}\cap\dots \cap A_{n-1}) \dots P(A_{2}|A_{1})P(A_{1})
$$
So the probability we are interested in is therefore,
$$
	P(A_{1}\cap\dots \cap A_{n}|A_{1}) = P(A_{n}|A_{1}\cap\dots \cap A_{n-1}) \dots P(A_{2}|A_{1})
$$
Now, from the question, the probability of hitting free throw $k$ after hitting $m$ free throws is $m /k$. So the probability of hitting a free throw assuming you have hit every single one prior is $(k-1) /k$.
$$
	P(A_{1}\cap\dots \cap A_{n}|A_{1}) = \frac{n-1}{n} \frac{n-2}{n-1} \times\dots \times \frac{2}{3} \frac{1}{2} = \frac{1}{n}
$$
# Candy Jar
Assume there is a jar with an infinite number of red candies, green candies and blue candies. Suppose you randomly choose any random number $N\geq 4$ and you pick $N$ candies from the jar. Is the event of drawing at least two candies of the same color independent of the random number $N$?

We are selecting at least 4 candies from the jar, but there are only 3 colours inside the jar. Therefore, the possibility of picking 2 candies of the same colour is always 100%