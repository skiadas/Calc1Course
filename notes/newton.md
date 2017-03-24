# Newton's method

## Reading

- Section 4.7

## Practice problems

- Section 4.7: 1, 3, 5, 7, 11, 15
- To turn in: 4.7 2, 16
- In class: 4.7 12, 34

## Notes

### Newton's Method

Newton's Method has a simple goal: To find a root for a function, i.e. a value $x$ for which $f(x) = 0$.

The method works as follows:

- Start with an initial "guess", $a_0$.
- From a guess (estimate) $a_n$, generate a next guess (estimate) $a_{n+1}$, which is hoped to be closer to the solution. This works better than it sounds.
- We repeat this process until we arrive at a number that is close enough to a solution. We can test that by putting the estimated value into the function.

The formula of going from the one guess to the next is:
$$a_{n+1} = a_n - \frac{f(a_n)}{f'(a_n)}$$

Note that if $a_n$ is a solution, then the numerator in the fraction is zero, and hence the above formula does not change $a_n$. The process therefore stops when each step doesn't really improve our estimate.

> **Geometric interpretation**
>
> If we follow the tangent line to the graph of $f(x)$ at the point $a_n$, and find where it meets the $x$ axis, then the next estimate $a_{n+1}$ is exactly that point.
>
> Intuitively this makes sense: If the function was fairly linear, then we want to follow that line until it hits the $x$ axis ($y=0$).

Let us do a standard example of this, to find the square root of $2$, $\sqrt{2}$. We can think of this as a solution to the equation:
$$x^2-2=0$$.
Therefore we have the function $f(x) = x^2-2$ and we are looking for its root.

First we find an initial guess: Since $f(1) < 0$ and $f(2) > 0$, we know there is a solution somewhere in the interval. It makes sense therefore to start somewhere in that interval, e.g. $a_0=1$ or $a_0=2$. We will start with the midpoint:
$$a_0 = 1.5$$

For our next estimate, we put this into the formula:
$$a_{n+1} = a_n - \frac{a_n^2-2}{2a_n}$$
If we plug $a_0=1.5$ in, we get:
$$a_1 = a_0 - \frac{a_0^2-2}{2a_0} = 1.5 - \frac{1.5^2 - 2}{2\times 1.5} = 1.416667$$

For our next estimate, we plug this $a_1 = 1.416667$ in to the same formula:
$$a_2 = a_1 - \frac{a_1^2-2}{2a_1} = 1.416667 - \frac{1.416667^2 - 2}{2\times 1.416667} = 1.414216$$

For our next estimate, we plug this $a_2 = 1.414216$ in to the same formula:
$$a_3 = a_2 - \frac{a_2^2-2}{2a_2} = 1.414216 - \frac{1.414216^2 - 2}{2\times 1.414216} = 1.414214$$

At this point we have arrived at a close approximation of our solution. If we plug it back in, we would get the same first six decimals. So we have an estimate for $\sqrt{2} = 1.414214$.

If we did our computation with more decimal points in our estimates, we could have kept going.

**Comparison with bisection method:**

Recall that earlier we saw a bisection method for finding a root: Keep cutting the interval in half and choosing the correct endpoint to continue. Newton's method is a lot faster: In just 3 steps it gave us six digits of accuracy. The bisection method would have taken roughly 15 steps.

The difference is that Newton's method does not always work well: If a function oscillates too much, it can make the sequence of numbers behave very erratically.
