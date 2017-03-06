# Graph Sketching

## Reading

- Sections 4.4, 4.5

## Practice problems

- Section 4.4: 5, 11, 13, 21, 25; section 4.5: 13, 15, 21, 23, 31, 55, 57
- In class: 4.4 16, 4.5 17, 34, 52
- To turn in: 4.4 6, 24, 4.5 16, 32

## Notes

### Concavity

The change in the first first derivative dictates the curvature of the graph. The graph may be "curving upwards" or "curving downwards" depending on whether the slope (first derivative) increases or decreases.

> **Concavity**
>
> - A function $f(x)$ is said to be **concave up** on an interval $(a, b)$, if $f'(x)$ is increasing on $(a, b)$.
> - A function $f(x)$ is said to be **concave down** on an interval $(a, b)$, if $f'(x)$ is decreasing on $(a, b)$.

There is a geometric interpretation of concavity:

> **Geometric interpretation of Concavity**
>
> If a function is concave up, and we consider two points $a$, $b$, and we consider the line joining the two points, then the graph of the function between $a$ and $b$ lies *below* the line. Conversely for a concave down function.

Testing for concavity is easy using the second derivative, as the sign of the second derivative tells us whether the first derivative is increasing or decreasing:

> **Test for Concavity**
>
> - If $f''(x) > 0$ on an interval $(a, b)$, then $f$ is concave up on $(a, b)$.
> - If $f''(x) < 0$ on an interval $(a, b)$, then $f$ is concave down on $(a, b)$.

The points where the concavity behavior changes are of interest:

> **Inflection points**
>
> A point $c$ is called an **inflection point**, if the function changes concavity at $c$, either from up to down or from down to up.
>
> Test: If $f''(c) = 0$ and $f''$ changes sign from one side of $c$ to the other, then $c$ is an inflection point.

Example: Find the concavity and inflection points of $\sin(x)$.

### Second Derivative Test for critical points

We can use the second derivative to test a critical point. Briefly, a positive second derivative at the critical point means that the first derivative was increasing, and since it has to be zero at the critical point then it must have been negative before and positive afterwards. This means the point is a local maximum. Conversely for local minimum.

> **Second Derivative Test for Critical Points**
>
> If $c$ is a critical point with $f'(c) = 0$, and $f''(c)$ exists, then:
>
> - If $f''(c) > 0$ then $f(c)$ is a local minimum.
> - If $f''(c) < 0$ then $f(c)$ is a local maximum.
> - If $f''(c) = 0$ then the test is inconclusive and other methods must be used.

### Graph Sketching

In order to draw the graph of the function, we focus on the signs of the first and second derivative, as these tell us about the shape of the graph.

> **Graph Sketching**
>
> 1. Compute first and second derivatives, find when they equal $0$.
> 2. Create table with rows for $f'$, $f''$, and $f$, and vertical markers for the zeros of the derivatives and infinities.
> 3. Determine the signs of $f'$, $f''$ in the intervals inbetween the markers.
> 4. Determine asymptotic behavior as we approach infinity.
> 5. Find the values of $f$ at the marker points.
> 6. Use this information to do a rough graph of $f$.
