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
until heads appears. Prove the mean of this Geometric distribution is $\frac{1}{p}$ in two
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

(b.) On average, how many times must a $6$-sided be rolled until there are two rolls in a row 
that differ by $1$ (for example $2$ followed by a $1$ or a $3$, or a $5$ followed by a $6$, ect.)

<details>
<summary>Observation 1</summary>
In our last meeting we made the following notation and observations:

1. We let $E_i$ denote the expected number of rolls after rolling an $i$ (not following an $i-1$ or an $i+1$).
2. We let $E$ denote the expected number of rolls.
</details>

<details>
<summary>Observation 2</summary>
It helps to list the transition between rolls that we are interested in. Below we consider a given 
a roll $i$, and we consider what values $j$ can the next roll be so that $|i - j| = 1$. In otherwords the list below considers the optimial cases when we're considering $E_i$.

$$\dots 1 \rightarrow 2~~~~~~~$$

$$\dots 2 \rightarrow 1 ~\text{or}~ 3$$

$$\dots 3 \rightarrow 2 ~\text{or}~ 4$$

$$\dots 4 \rightarrow 3 ~\text{or}~ 5$$

$$\dots 5 \rightarrow 4 ~\text{or}~ 6$$

$$\dots 6 \rightarrow 1~~~~~~~$$

Note that $E_1$ and $E_6$ are unique in that they only have a single value that can lead to 
the process ending. By symmetry we see that $E_1 = E_6$. (after all $1$ and $6$ are just labels).

Moreso, notice that in the $E_2$ case, it you can potentially roll a $1$ which brings us to the $E_1$ case. So $E_2$ is not the same as $E_3$ or $E_4$. This is because those cases don't have the possiblility or rolling a $1$ or a $6$ leading to the special $E_1$ or $E_2$ cases. But $E_5$ does
have a way to lead to an $E_1$-type of case, namely $E_6$. Therefore $E_2 = E_5$ by symmetry. Lastly, the only two left cases that are symmetrically equivalent are $E_3$ and $E_4$. Thus, $E_3 = E_4$.

Since there is a $\frac{1}{6}$ probability that you can be in any particular state $E_i$ when we 
start the die-rolling process and we must always roll one-time when starting the process, thus 
we may express the general expectation as:

$$
E = 1 + \frac{1}{6}(E_1 + E_2 + E_3 + E_4 + E_5 + E_6)
$$

And by applying the symmetry we observed above, we have:

$$
E = 1 + \frac{2}{6}(E_1 + E_2 + E_3)
$$
</details>

<details>
<summary>Observation 3</summary>
Now we can break the problem down in determining $E_1, E_2, E_3$.

Notice that:

$$E_1 = 1 + \frac{1}{6}E_1 + \frac{1}{6}E_3 + \frac{1}{6}E_4 + \frac{1}{6}E_5 + \frac{1}{6}E_6$$

Now we apply the symmetries from before:

$$E_1 = 1 + \frac{2}{6}E_1 + \frac{1}{6}E_2 + \frac{2}{6}E_3$$

The same argument can be made for $E_2$ and $E_3$. Verify for yourself that:


$$E_2 = 1 + \frac{1}{6}E_1 + \frac{2}{6}E_2 + \frac{1}{6}E_3$$

$$E_3 = 1 + \frac{2}{6}E_1 + \frac{1}{6}E_2 + \frac{1}{6}E_3$$

Now we have a system of equations of $3$ variables and $3$ unknowns:

$$E_1 = 1 + \frac{2}{6}E_1 + \frac{1}{6}E_2 + \frac{2}{6}E_3$$

$$E_2 = 1 + \frac{1}{6}E_1 + \frac{2}{6}E_2 + \frac{1}{6}E_3$$

$$E_3 = 1 + \frac{2}{6}E_1 + \frac{1}{6}E_2 + \frac{1}{6}E_3$$
</details>

<details>
<summary>Solution</summary>
Solving the system of equations yields:

$E_1 = \frac{70}{17}, E_2 = \frac{58}{17}, E_3 = \frac{60}{17}$

Now recall that $E = 1 + \frac{2}{6}(E_1 + E_2 + E_3)$, therefore

$$
E
= 
1 + \frac{2}{6}(\frac{70}{17} + \frac{58}{17} + \frac{60}{17})
=
\frac{2039}{51}
\approx 4.6863
$$
</details>




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


