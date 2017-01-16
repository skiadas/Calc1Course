# Continuity

## Reading

- Sections 2.4

## Practice problems

- Section 2.4 3, 9, 11, 13, 18, 23, 37, 51, 60, 67, 69
- In class: 2.4 49, 57
- To turn in (due Monday, together with 2.3): 2.4 4, 12, 52

## Notes

### Continuity

- Continuity is meant to describe the concept that we can draw the graph of a function without lifting our pen: The function forms a continuous whole.
- The idea is to relate the limit of a function at a point $a$ to the value of the function at $a$. The limit tells us what happens *near* the point $a$. For continuity, this must agree with what happens exactly at $a$.
- Definition:
    > We say that a function $f(x)$ is **continuous** at a point $x=c$ if:
    >
    > - The limit $\displaystyle\lim_{x\to a}f(x)$ exists.
    > - The value $f(a)$ exists.
    > - They agree: $\displaystyle\lim_{x\to a}f(x) = f(a)$.
- Practical implication: Can compute a limit by "plugging in".
- If this is not the case, we say that the function is **discontinuous** at $x=c$.
- We say that $f$ is **continuous on an interval** $[a,b]$, if it is continuous at every point of the interval.
- Examples of continuous functions:
    - Constant function
    - $x^n$
    - Sum of continuous functions is continuous
    - Product of continuous functions is continuous
    - Quotient of continuous function is continuous, except where the denominator is $0$
    - Trigonometric functions are continuous
- Possible discontinuities:
    - Left-sided limit and right-sided limit exist but differ (**jump discontinuity**)
    - Limit exists, but value is different from it (**removable discontinuity**)
    - One-sided limits are infinity (**infinite discontinuity**) or don't exist
- Example of studying the continuity of a piecewise-defined function (example 2)
- **Function composition**: If $g(x)$ is continuous at $x=c$, and $f(u)$ is continuous at $u=g(c)$, then $f(g(x))$ is also continuous at $x=c$.
    - Example: $\sin(x^2)$ is continuous.
