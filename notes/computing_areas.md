# Computing Areas

## Reading

- Section 5.1

## Practice problems

- Section 5.1: 7, 9, 17, 29, 37, 38, 53, 55
- To turn in: 5.1 8, 16, 18, 28

## Notes

### Computing Areas

A fundamental problem in many fields is the computation of the area contained between curves and axes. It all essentially boils down to the following:

> Given a function $f(x)$ on the interval $[a, b]$, can we compute/approximate the area that is between the graph of $f$, the $x$ axis, and the vertical lines $x=a$ and $x=b$?

Computing these areas has been a problem of interest since ancient times, when for instance people estimated the area of a circle. It still is a non-trivial problem.

The method we will employ is easy:

- The one area we can directly compute easily is that of a rectangle with a given base and height.
- We will try to approximate other areas by dividing them into rectangles. This may not be a perfect process and result in some errors due to the rectangles being either more or less than they should.
- We try to minimize those errors by dividing the area into smaller and finer rectangles, an ever increasing number of them. We attempt to get a precise answer by then taking a *limit* of this process.

As an example, suppose we want to find the area under the function $f(x) = \sqrt{1-x^2}$, the $x$ axis, and the lines $x=0$ and $x=1$. If you draw the picture for a second you will see that this area is one fourth of the unit circle, so we know that it should equal $\frac{\pi}{4}\approx 0.7854$. We will see how close to that our method will get us.

Start by drawing a graph of the functino from $0$ to $1$. This will help you follow along.

We can make a initial rough estimates as follows:

- Look at the largest value the function takes in the range. The rectangle with that height fully encompasses the desired area, so the area of the rectangle is an upper bound for our desired area.
- Look at the smallest value the function takes in the range. The rectangle with that height is fully contained within the desired area, so the area of the rectangle is a lower bound for our desired area.

In our example, the largest value is $1$ and the smallest is $0$, so the upper estimate would be $1\times(1-0) = 1$ and the lower estimate would be $0\times (1-0) = 0$. So our desired area must be somewhere between $0$ and $1$. It's a start, but we really should try and do better.

To do better, we divide the $x$ interval into segments, then each segment will be the base for a rectangle. So we will do the following:

interval        max of f             min of f
--------------  -------------------  ----------------------
$[0, 0.25]$     $f(0) = 1$           $f(0.25) = 0.9682$
$[0.25, 0.5]$   $f(0.25) = 0.9682$   $f(0.5) = 0.866$
$[0.5, 0.75]$   $f(0.5) = 0.866$     $f(0.75) = 0.6614$
$[0.75, 1]$     $f(0.75) = 0.6614$   $f(1) = 0$
--------------  -------------------  ----------------------

Also note that each interval has a base size of $0.25$. Therefore if we want to estimate the interval, we can do two things:
$$\textrm{upper sum}=0.25\times 1 + 0.25\times 0.9682 + 0.25 \times 0.866 + 0.25 \times 0.6614 = 0.8739$$
and
$$\textrm{lower sum}=0.25\times 0.9682 + 0.25 \times 0.866 + 0.25 \times 0.6614 + 0.25\times 0 =0.6239$$
So now we can say that the actual area is between $0.6239$ and $0.8739$.

Notice that instead of multiplying each term with $0.25$, we could have done one multiplication at the end:
$$.25\times \left(0.9682 + 0.866 + 0.6614 + 0\right) = 0.6239$$
This works whenever we divide into equal length intervals, and we will use it frequently in the following.

**Practice:** Try to use $8$ intervals instead.

We can now imagine dividing the interval into smaller and smaller pieces. In general we can set up some terminology:

> A **partition** of the interval $[a, b]$ is a subdivision of the interval into a number of subintervals, indicated by their endpoints:
> $$a = x_0 < x_1 < x_2 < \cdots < x_N = b$$
> This partition is said to have **size** $N$.
>
> A standard way to form such a partition is to divide the interval into $N$ pieces of equal length. In that case each piece has a length:
> $$\Delta x = \frac{b-a}{N}$$
> And the actual values $x_0$, $x_1$, etc become:
> $$x_0 = a,\quad x_1 = a +\Delta x,\quad x_2=a+2\Delta x,\quad cdots$$
> So in general the $i$-th point is:
> $$x_i = a + i\Delta x$$
>
> Given such a partition, we can form three sums:
>
> - The **right-endpoint sum**, $R_N=\Delta x\left(f(x_1) + f(x_2) + f(x_3)+\cdots+f(x_N)\right)$
> - The **left-endpoint sum**, $R_N=\Delta x\left(f(x_0) + f(x_1) + f(x_2)+\cdots+f(x_{N-1})\right)$
> - The **mid-point sum**, where we use the midpoints on each interval.
> - The **lower sum**, where we use smallest value of the function on each interval.
> - The **upper sum**, where we use largest value of the function on each interval.
>
> NOTE: In our example above the left-endpoint sum is what we called the "upper sum". That is because our function was decreasing, so the left endpoint on each interval is the maximum on that interval. And similarly for lower sum and right endpoints. In general this will not be the case.

**Practice:** Use the midpoint sum to estimate the previous area.

### The Summation notation

To make it easier to write these long sums, a convenient notation has been created, which use a greek "sigma" to denote the act of adding, and a parameter to indicate the range. In general the notation looks like this:
$$\sum_{j=m}^n a_j= a_m + a_{m+1} + \cdots + a_n$$
As an example:
$$\sum_{j=3}^6 j^2= 3^2+4^2+5^2+6^2$$

We can use this to write the left/right-endpoint sums from earlier in a more compact form:
$$R_N = \Delta x\sum_{j=1}^N f(a + j\Delta x)$$
$$L_N = \Delta x\sum_{j=0}^{N-1} f(a + j\Delta x)$$
$$M_N = \Delta x\sum_{j=0}^{N-1} f\left(a + j\Delta x +\frac{1}{2}\Delta x\right)$$

There are some important properties of the summation notation, as well as some standard sums we can do:

> $$\sum_{j=m}^n(a_j + b_j) = \sum_{j=m}^n a_j + \sum_{j=m}^n b_j$$
> $$\sum_{j=m}^n(k\times a_j) = k\times\sum_{j=m}^n a_j$$
> $$\sum_{j=m}^n a_j = \sum_{i=0}^{n-m} a_{i+m}\qquad(i = j-m,\,j=i+m)$$
> $$\sum_{j=m}^n k = k\times(n-m+1)$$
> $$\sum_{j=1}^n j = \frac{N(N+1)}{2}$$
> $$\sum_{j=1}^n j^2 = \frac{N(N+1)(2N+1)}{6}$$
> $$\sum_{j=1}^n j^3 = \left(\frac{N(N+1)}{2}\right)^2$$

We can use a combination of these to solve some interesting problems. For example let's use these to find the area under $f(x) = x^2$ and from $a$ to $b$. We will use the righ-endpoint sum:
$$R_N = \Delta x\sum_{j=1}^N f(a + j\Delta x) = \Delta x\sum_{j=1}^N (a + j\Delta x)^2$$
We will worry about the sum first, then multiply by $\Delta x$ at the end. For the sum we have:
$$\sum_{j=1}^N (a + j\Delta x)^2 = \sum_{j=1}^N \left(a^2 + 2a\Delta x j + (\Delta x)^2 j^2\right) = \sum_{j=1}^N a^2 + 2a\Delta x\sum_{j=1}^N j + (\Delta x)^2\sum_{j=1}^N j^2$$
This then becomes:
$$a^2\times N + 2a\Delta x\times\frac{N(N+1)}{2} + \frac{N(N+1)(2N+1)}{6}$$
We now multiply the whole thing with $\Delta x$, and replace all the $\Delta x$ with $\Delta x = \frac{b-a}{N}$:
$$\frac{b-a}{N}\times a^2 N + 2a\frac{(b-a)^2}{N^2}\times\frac{N(N+1)}{2} + \frac{(b-a)^3}{N^3}\times\frac{N(N+1)(2N+1)}{6}$$
Now we want to imagine that we let the number of intervals, $N$, go to infinity. In order to do that we will write the same factors as above in a more easy to process form:
$$(b-a)\times a^2 + 2a(b-a)^2\times\frac{N(N+1)}{2N^2} + (b-a)^3\times\frac{N(N+1)(2N+1)}{6N^3}$$
Each of the quotients is a quotient of polynomials of the same degree. As $N$ goes to infinity, these quotients approach the ratio of the leading coefficients. so we would get the answer:
$$(b-a)\times a^2 + 2a(b-a)^2\frac{1}{2} + (b-a)^3\frac{1}{3}$$
We make common denominators and simplify:
$$\frac{3(b-a) a^2 + 3a(b-a)^2 + (b-a)^3}{3} = \frac{b^3-a^3}{3}$$
