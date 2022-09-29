name : hypergeometric distribution
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A discrete [[probability distribution]] that describes the probability of $k$ successes (random draws for which the object has a specified feature) in $n$ draws, without replacement, from a finite population of size $N$ that contains exactly $N_A$ objects of that feature, wherein each draw is either a success or a failure. This is in contrast with a [[binomial distribution]] which describes the probability of $k$ successes in $n$ draws **with replacement**.

Let $0 \leq N_A \leq N$ and $1 \leq n \leq N$ be integers. A [[random variable]] $X$ has the hypergeometric distribution with parameters $(N,N_A,n)$ if $X$ takes values in the set $\{0,1,...,n\}$ and has [[probability mass function]]:
$$P(X=k)=\frac{{N_a \choose k}{N-N_A \choose n-k}}{{N \choose n}}$$ for $k = 0,1,...,n$. This is abbreviated by $X \sim Hypergeom(N,N_A,n)$.

**Example:**
A basket contains a litter of 6 kittens, 2 males and 4 females. A neighbor comes and picks 3 kittens randomly to take home with him. Let $X$ be the number of male kittens in the group the neighbor chose. Thus $X \sim Hypergeom(6,2,3)$ and the probability 2 males were chosen:
$$P(X=2) = \frac{{2 \choose 2}{4 \choose 1}}{{6 \choose 3}} = \frac{4}{20}$$

**Parameters:** $$N \geq 1 \text{ Total population size}$$ $$N_A \geq 0 \text{ success group size}$$ $$n \geq 1 \text{ sample size}$$
**[[probability mass function]]:** $$p_X(k) = \frac{{N_A \choose k}{N-N_A \choose n-k}}{{N \choose n}}$$ $$0 \leq k \leq n$$
**[[cumulative distribution function]]:** *kind of a mess, look on Wikipedia*
**[[expectation]]:** $$\frac{nN_A}{N}$$
**[[variance]]:** $$\frac{N-n}{N-1}n\frac{N_A(N-N_A)}{N^2}$$

###### Properties:


###### Additional Thoughts:
