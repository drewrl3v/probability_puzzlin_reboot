# Order Statistics


### Problem 1 (Uniform pdf)

Let $X_1$ be a uniform random variable between $0$ and $1$, dentoed: $X_1 \sim U[0,1]$.
What is the probability density function (pdf) of $X_1$?

### Problem 2 (Min and Max)

Let $X_1, \dots, X_n \sim^{i.i.d} U[0,1]$. What is the pdf of $\max(X_1, \dots, X_n)$ and 
$\min(X_1, \dots, X_n)$?

### Problem 3 (Multiplication v.s. Square-Root)
Say $X_1, X_2 \sim^{i.i.d} U[0,1]$. Then consider the following
random variables: $Y = \max(X_1, X_2)$ and $Z = \sqrt{X_2}$. Show that 
they have the same distribution.

### Problem 4 (K-th Order statistic)

Let $X_1, \dots, X_n \sim^{i.i.d} U[0,1]$. Now let's order these random variables and label them:

$$
X_{(1)}, \dots, X_{(n)}
$$

Note: $X_{(1)} = \min(X_1, \dots, X_n)$ and $X_{(n)} = \max(X_1, \dots, X_n)$.

In general what's the cumulative density function (cdf) and the pdf of $X_{(k)}$. 

### Problem 5 (Strange Powers)

Sample $3$ numbers uniformly in $[0,1]$, (call them $X, Y, Z$) and compute $W = (XY)^Z$.
What is the distribution of the random variable $W$?

### Problem 6 (The Beta Function)

Let $n, m \in \mathbb{N}$. Interpret the following integral as a probability:

$$
B(m+1, n+1)
=
\int_0^1 u^m(1-u)^n du
$$

Evaluate the integral using a counting argument.