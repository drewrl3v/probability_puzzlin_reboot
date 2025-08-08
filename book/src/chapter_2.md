# Chapter 2

## More Expectations

The following can all be accomplished via clever applicaiton of recursive expectations. 
Some of them can be easily resolved by applying the corollary of Doob's optional Stopping 
Theorem we learned last week. I'll also throw in some conditional expectations.


### Problem 1:

Consider a fair coin. The waiting time is the number of flips required to 
see a pattern. For example, if the pattern of interest is $HT$, then 
the waiting time in the sequqenceo of flips $TTHHHT$ is $6$.

(a.) What is the average waiting time for $HT$?

(b.) What is the average waiting time for $HH$

### Problem 2:

(a.) Consider a random sequence beginning with $HT$. What is the average 
waiting time until we see the sequence again?

(b.) Consider a sequence beginning with the pattern $HH$ what is the average 
waiting time until we see the sequence again?

### Problem 3:

A coin having probability $p$ of coming up heads, is to be succesively flipped
until heads appears. Prove the mean of this Geometric distribution is $p$ in two
ways:

(a.) Using an infinite series.

(b.) Using conditional expectation.

### Problem 4:

Sam will read either one chapter of his probability book or one chapter of 
his history book. If the number of misprints in a chapter of his probability 
book is Poisson distributed with mean $2$ and if the number of misprints in 
his history book is Poisson distributed with mean $5$, then assuming Sam 
is equally likely to choose either book, what is the expected number of 
misprints that Sam will come across?


### Problem 5:

(a.) On average, how many times must a $6$-sided die be rolled until you see a $65$ pattern?

(b.) On average, how mnay times must a $6-sided$ be rolled until there are two rolls in a row 
that differ by $1$ (for example $2$ followed by a $1$ or a $3$, or a $5$ followed by a $6$, ect.)

### Problem 6:

The monkey's are typing away on the keyboard again. What is the expected number of key presses until 
we see the pattern $RUINBRUIN$?

### Problem 7:

(a.) You roll a die until you get a 6. What is the expected number of rolls conditioned on the event 
that no odd numbers show up?

$$
\mathbb{E}[N_6 ~|~ \text{No odds.}] 
=
\text{?}
$$

(b.) You roll a $1$-million sided die until you get a 6. What is the expected number of rolls conditioned on the event 
that no odd numbers show up?

$$
\mathbb{E}[N_{1,000,000} ~|~ \text{No odds.}] 
=
\text{?}
$$


