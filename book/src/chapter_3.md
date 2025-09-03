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