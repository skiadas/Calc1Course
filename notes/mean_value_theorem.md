# Mean Value Theorem

## Reading

- Section 4.3

## Practice problems

- Section 4.3 13, 15, 17, 21,  23, 27, 35, 39
- In class: 4.3 14, 22
- To turn in: 4.3 20, 26, 38, 46

## Notes

### The Mean Value Theorem

The mean value theorem relates the values of a function at two points to the value of the derivative somewhere between the two points.

> **Mean Value Theorem**
>
> If $f(x)$ is continous on $[a, b]$ and differentiable on $(a, b)$, then there is a point $c\in(a, b)$ such that:
> $$f'(c) = \frac{f(b)-f(a)}{b-a}$$

Rate-of-change interpretation: The average rate of change over an interval must equal the instantaneous rate of change somewhere along the interval.

A very important corollary of this theorem is the following:

> If $f(x)$ is differentiable and $f'(x) = 0$ for all $x\in(a, b)$, then $f(x)$ must be a constant function on $(a, b)$.

Proof:

- We can instead show that any two points in the interval $(a, b)$ must have the same value.
- If $c<d$ are two points in $(a, b)$, then the mean value theorem says that $f(d)-f(c) = f'(x)(d-c)$ for some $x\in(c, d)$. But then that $x$ must also be in $(a, b)$, so $f'(x) = 0$. But then $f(d)-f(c) = 0$, so $f(c) = f(d)$.

A second important consequence has to do with how the sign of the derivative dictates the behavior of the function:

> A function $f$ is **(strictly) increasing** on an interval $(a, b)$ if for any two points $c<d$ in $(a, b)$ we have $f(c) < f(d)$. In other words *later points have higher values*. Conversely the function is called **(strictly) decreasing** if for any two points $c<d$ we have $f(c) > f(d)$, so later points have lower values.
>
> - If $f(x)$ is differentiable on $(a, b)$ and $f'(x) > 0$ for all $x\in(a, b)$,  then $f$ must be strictly increasing on $(a, b)$
> - If $f(x)$ is differentiable on $(a, b)$ and $f'(x) < 0$ for all $x\in(a, b)$,  then $f$ must be strictly decreasing on $(a, b)$

This again follows from the mean value theorem.

This result can help us examine what happens at critical points. The question basically is the following: Can we determine if a critical point is a local max or min (or neither) by considering the derivative?

The answer is simple: If the derivative is positive before the critical point and negative after the critical point, then the function must have been increasing before the point and decreasing after it, making the point a local maximum. And conversely for a minimum.

> **First Derivative Test for Critical Points**
>
> If $f(x)$ is differentiable and $c$ is a critical point of $f(x)$. Then:
>
> - If $f(x)$ changes from positive to negative at $c$, then $f(c)$ is a local maximum.
> - If $f(x)$ changes from negative to positive at $c$, then $f(c)$ is a local minimum.
> - If $f(x)$ preserves its sign, then the point is neither local maximum nor local minimum.

### Proof of the Mean Value Theorem

The insight of the proof is to consider the distance between the function and the straight line connecting the endpoints. So we define a new function:
$$g(x) = f(x) - f(a) - \frac{f(b)-f(a)}{b-a}(x-a)$$
Then we can observe that $g(x)$ is differentiable, and that $g(a) = g(b) = 0$. So by Rolle's theorem, we can see that the derivative $g'(x)$ must have a zero at some point $c$, so $g'(c)=0$. But:
$$g'(x) = f'(x) - \frac{f(b)-f(a)}{b-a}$$
So if this equals zero, we get that $f'(c) = \frac{f(b)-f(a)}{b-a}$.
