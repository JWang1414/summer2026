Much of the work at the beginning of lecture was introducing a number of quantities like random variables, the mean, variance, standard deviation etc.
- Adding up all the deviations from the mean will result in 0
- The standard deviation is also called the RMS (root mean squared)

The surprise factor is a value that we will use to define how "surprising" an outcome is. The larger this value, the more surprising.
$$
	\mathcal{S}(i) = \ln\left( \frac{1}{p(i)} \right)
$$
If you are calculating the average surprise for something, you may find that you might get something like:
$$
	\left< \mathcal{S} \right> = \sum p_{i} \ln\left( \frac{1}{p_{i}} \right) = - \sum p_{i} \ln p_{i} = \dots + 0 \times \ln(0) + \dots
$$
Well this $0\times \infty$. However, it is possible to show that this 0 is much stronger than the infinity. So, in this case, the quantity ultimately evaluates to 0.
- If something has just one outcome, $\left< \mathcal{S} \right> =0$. So there is no surprise
- On the other hand, the surprise is maximized for a uniform distribution
