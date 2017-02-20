# Extreme Values

## Reading

- Section 4.2

## Practice problems

- Section 4.2 3, 7, 17, 19, 25, 29, 40, 41, 61
- In class: 4.2 63, 64
- To turn in (together with 4.1): 4.2 18, 30

## Notes

### Extreme Values

By far the most important application of derivatives is in optimization, namely the search for maximum and minimum values for functions.

> **Extreme Values**
>
> If $f(x)$ is a function defined on an interval $I$, and we consider a point $c$ in that interval $I$, then we say that $f(a)$ is:
> - An **absolute maximum** of $f(x)$ on the interval $I$ if $f(a)\leq f(x)$ for all $x\in I$.
> - An **absolute minimum** of $f(x)$ on the interval $I$ if $f(a)\geq f(x)$ for all $x\in I$.
> - An **local maximum** of $f(x)$ at $a$ if $f(a)\leq f(x)$ for all $x$ in a small interval around $a$.
> - An **local minimum** of $f(x)$ at $a$ if $f(a)\geq f(x)$ for all $x$ in a small interval around $a$.

The first main tool for finding extreme values is the following:

> **Extreme Value Theorem**
>
> If $f$ is a continuous function on a *closed* interval $[a, b]$, then $f$ takes both an absolute maximum value and an absolute minimum value on that interval.
>
> This theorem does *not* work if the function is not continuous, or if the interval is not closed. Figure 2 in the book contains graphical examples of what can go wrong.

This theorem guarantees for us that under certain conditions an absolute max/min exists. It does not tell us how to find it. But every absolute maximum/minimum will also be a local one, and we will now develop ways for finding local maxima/minima.

In this direction, the following definition will be key.

> **Critical Points**
>
> A point $c$ is called a **critical point** for $f$ if $f'(c) = 0$ or $f'(c)$ does not exist.

The following theorem helps us find local extrema:

> **Fermat's Theorem on local extrema**
>
> If $c$ is an interior point of domain of $f$, and $f(c)$ is a local minimum or maximum of $f$, then $c$ must be a critical point.

This all provides us with a method of finding absolute maxima/minima:

> **Finding Extreme Values**
>
> If $f(x)$ is a continuous function on a closed interval $[a, b]$, then:
> - The Extreme Value Theorem guarantees that there are absolute minima and maxima for the function.
> - To find them we must look at:
>     - The endpoints $a$, $b$
>     - The critical points, where $f'(c)$ is $0$ or does not exist.
> - Whichever of these points has the largest/smallest value is the absolute max/min.

Example: Consider $f(x) = x^3-6x^2+8$ on the interval $[1, 6]$. The function is continuous since it is a polynomial. So it must have a maximum and minimum. To find them, we look at the endpoints and the critical points:

- Endpoints: $f(1) = 1-6+8 = 1$, $f(6) = 6^3-6\cdot 6^2 + 8 = 8$.
- Critical points: $f'(x) = 3x^2-6x = 0$. So we have one solution $x=0$ and another $x=2$. Since $0$ is outside the interval, we ignore it. So we compute $f(2) = 2^3 - 6\cdot 2^2 + 8 = -24$.

From the three point we had to compute, we find the minimum at $c=2$, with value $-24$, and the maximum at $c=6$ with value $8$.

### Rolle's Theorem

An important consequence of the study of extreme is Rolle's Theorem. It states the following:

> **Rolle's Theorem**
>
> If $f(x)$ is continuous on $[a, b]$ and differentiable on $(a, b)$, and $f(a) = f(b)$, then there is a $c\in(a, b)$ such that $f'(c) = 0$.

Proof: By the extreme value theorem, there must be a minimum and a maximum for the function $f$. If one of these occurs at an interior point $c\in(a, b)$, then Fermat's Theorem guarantees that $f'(c) = 0$. If not, then one endpoint is the maximum value and one is the minimum value. Since the endpoints have the same value, this would mean that the function must be constant.

And important consequence of Rolle's Theorem is the following:

> If $a$, $b$ are two zeros of $f$, i.e. $f(a) = f(b) = 0$, and $f$ is differentiable on $[a, b]$, then $f'(x)$ must have a zero in $[a, b]$.
>
> In other words, *the derivative of a function must have a zero inbetween any two zeros of the function*.

