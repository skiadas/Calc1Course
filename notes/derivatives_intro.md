# Introduction to derivatives

## Reading

- Sections 3.1

## Practice problems

- Section 3.1: 3, 5, 11, 13, 15, 21, 33, 35, 37, 41
- To turn in: 3.1 4, 26, 34, 38

## Notes

### Definition of Derivative

- The derivative is a formal description of the concept of "instantaneous rate of change" that we looked at when we discussed limits.
- Geometrically can be thought of as the slope of the tangent line, which is a *limit* of the slopes of the secant lines.
- Definition:

    > The **derivative** of $f(x)$ at the point $x=a$ is defined as:
    > $$f'(a) = \lim_{x\to a}\frac{f(x)-f(a)}{x-a}$$
    > Alternative description:
    > $$f'(a) = \lim_{h\to 9}\frac{f(a+h)-f(a)}{h}$$
- Equation for tangent line:

    > **Tangent Line**:
    > $$y - f(a) = f'(a)(x-a)$$
- Example 1:
    - $f(x) = x^3$, $a=2$.
    - $\frac{f(a+h)-f(a)}{h} = \frac{(2+h)^3-8}{h} = \frac{2^3+6h^2+12h + h^3 - 8}{h} = 6h + 12 +h^2$.
    - Taking limit as $h\to 0$: $f'(2) = 0 + 12 + 0 = 12$
- Practice: Do same example using the other limit formulation.
- Example 2:
    - $f(x) = \frac{1}{x}$, $a=2$.
    - $\frac{f(x)-f(a)}{x-a} = \frac{\frac{1}{x}-\frac{1}{a}}{x-a} = \frac{\frac{a-x}{xa}}{x-a} = -\frac{1}{xa} = -\frac{1}{a^2} = -\frac{1}{4}$
- Derivatives of linear and constant equations:
    - $(mx+b)' = m$
    - $b' = 0$

