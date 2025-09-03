# Geometric Probability

## Puzzle Style Geometry Problems

1. We draw two chords at random on a unit circle.
What is the probability that the chords intersect?

2. We take three samples uniformly from the interval $[0,1]$
and denote them $A$, $B$, and $C$. What is the probability that 
$A < B < C$?

3. We draw three points uniformly at random on the circumerence of 
the unit circle, what's the probability that all three points belong 
to the same semi-circle?

4. You are given a unit disk. Three poles are then stabbed perpendicularly 
into the unit disk, forming a table. What's the probability if we turn the 
table over it will stand up right without falling over?

## Classical Geometric Probability Results

1. (Buffon's Needle): We have parallel lines that are separated $1$-unit away 
from each other and they span the entire plane. We toss a needle a length $1$ 
onto the plane, what is the probability that the needle crosses a line?

<details>
<summary>Observation 1</summary>
The key observation is determining a good representation of the needle.

With probability $1$, the center of the needle must land in some parallel strip.
So it's enought to focus on a single strip.
</details>

<details>
<summary>Observation 2</summary>
More so, within the strip that contains the center of the needle, we also know with probability $1$ that the needle must be on one-half of the strip.
</details>

<details>
<summary>Solution</summary>
We denote the distance from the center of the needle to the nearest parallel line by $x$, and 
denote the acute angle formed by the needle and the orthogonal projection of the center of the 
neddle and the parallel line by $\theta$.

So the position of the needle is completely captureed by $(x, \theta)$ where $x \sim U[0, \frac{1}{2}]$ and $\theta \sim U[0, \frac{\pi}{2}]$. So we may think of the sample space as $\Omega \equiv [0, \frac{1}{2}] \times [0, \frac{\pi}{2}]$. 

Now we must determine what region corresponds to the needle crossing the parallel line. Let's call this region $A$. Once we find this region, then we can determine the probability of a needle 
crossing a parallel line by computing $\frac{|A|}{|\Omega|}$.


Notice that we can relate $x$, $\theta$, and hypotenuse (half of the needle) via $\cos \theta = \frac{x}{1/2} = 2x$. Thus $x = \frac{\cos \theta}{2}$.

Additionally, if $\theta = 0$, then the needle is orthogonal to the parallel line on the plane, so any $x$ in the range from $0$ up to $\frac{1}{2}$ indicates the needle is intersecting the parallel line. Also since $\frac{\cos \theta}{2}$ is a concave function, we can conclude that $x \leq \frac{\cos \theta}{2}$ is the region corresponding to the needle crossing.

As mentioned early, the probability corresponds to computing $\frac{|A|}{|\Omega|}$. Since $\Omega \equiv [0, \frac{1}{2}] \times [0, \frac{\pi}{2}]$, thus
$|\Omega| = \frac{1}{2} \times \frac{\pi}{2} = \frac{\pi}{4}$. To compute $|A|$ corresponds computing the area under the curve $x = \frac{\cos \theta}{2}$ which is given by:

$$
|A| = \int_0^{\frac{\pi}{2}} \frac{\cos \theta}{2} d\theta = \frac{1}{2}
$$

Therefore the probability of a needle crossing is $\frac{|A|}{|\Omega|} = \frac{2}{\pi}$.
</details>


<details>
<summary>Alternative Solution</summary>
Let $p(l)$ denote the probability that a needle of length $l$ intersects a line. We aim to derive 
$p(1)$ for a needle of length $1$.

Suppose we divide the needle of length $l$ into two parts of lengths $l_1$ and $l_2$ s.t. $l = l_1 + l_2$. Then the needle intersects a line if either of the two parts intersects a line. 

Under the assumption that the two parts behave indepedently, we have: 

$$
p(l) = p(l_1) + p(l_2)
$$

This property implies that $p(l)$ is a linear function of $l$. Therefore, we can write:

$$
p(l) = Cl ~~~~ (\star)
$$

where $C$ is some constant independent of l.

To determine the constant $C$, consider a more general case: instead of a needle, we toss a
polygonal curve with a total perimeter $P$ onto the plane. The curve can be divided into $n$ 
rectilinear segments of lengths $l_1, l_2, \dots, l_n$, where each segment has length less than 
some constant $d$. 

Define the indicator random variable for each segment:

$$
    X_i = 
    \begin{cases} 
    1 & \text{if the $i$-th segment intersects a line}, \\
    0 & \text{otherwise}.
    \end{cases}
$$   

Let $S$ denote the total number of intersections, i.e. 

$$
S = X_1 + \dots + X_n
$$

Since $E(X_i) = p_i$ is the probability of intersection of the $i$th segment and note the property above informs us that $p_i = Cl_i$. Thus by linearity of expectation we have:

$$
E(S)
= 
C(l_1 + l_2 + \dots + l_n)
= 
CP
~~~~(\star \star)
$$

where $P = \sum_i=1^n l_i$ is the total perimeter of the curve.

Note that this argument holds for any polygonal (as well as rectifiable: **requires analysis**)
curve. So to find $C$ way consider WLOG teh circle of diamter $d=1$. A circle always intersects 
a line in exactly two points.

Thus the expected number of i8ntersections for a circle is $E(S) = 2$. From equations $(\star \star)$, 
the perimeter of a circle is $P = \pi d$, so we have:

$$
E(S) = C \pi
$$

Now by substituting $E(S) = 2$, we find:

$$
C = \frac{2}{\pi}
$$

Substituting this value into equation $(\star)$, the probability of a needle of length $l$ 
intersecting a line is:

$$
p(l)
= 
\frac{2l}{\pi}
$$

Thus for a needle of length $1$ we have $p(1) = \frac{2}{\pi}$.
</details>



