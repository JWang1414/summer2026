# Question 1
```r
dbinom(4, size = 12, prob = 0.3)
pbinom(4, size = 12, prob = 0.3)
pbinom(4, size = 12, prob = 0.3, lower.tail = FALSE)
```
# Question 2
```r
dpois(3, lambda = 5)
ppois(6, lambda = 5, lower.tail = FALSE)
```
- Be careful here, it is easy to choose 8 instead of 6
# Question 3
```r
pnorm(120, mean = 100, sd = 15)
pnorm(120, mean = 100, sd = 15, lower.tail = FALSE)
qnorm(0.95, mean = 100, sd = 15)
```
