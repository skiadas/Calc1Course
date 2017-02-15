# Implicit Differentiation

## Reading

- Sections 3.8

## Practice problems

- Section 3.8: 3, 5, 7, 9, 11, 31, 33, 39
- To turn in (together with 3.9): 3.8 6, 10, 38

## Notes

### Implicit Differentiation

Implicit differentiation is used when we have a relation between two variables $x$, $y$, which would in theory allow us to write $y$ as a function of $x$, but when actually doing so might be hard to do.

Example:

Let us look at a case that we can solve in two ways.

- Imagine we have the equation: $x^2 + y^2 = 1$.
- Then $y$ can be thought of as a function of $x$.
- We could in fact solve it, and get $y = \sqrt{1-x^2}$.
- Then we can compute the derivative by chain rule: $\frac{dy}{dx} = \frac{-x}{\sqrt{1-x^2}}$.
- Alternatively, we can differentiate the formula $x^2+y^2 = 1$ **treating $y=y(x)$ as a function of $x$**.
- This gives us: $2x + 2y \frac{dy}{dx} = 0$
- Solving for $\frac{dy}{dx}$ gives us: $\frac{dy}{dx} = - \frac{x}{y}$
- Since $y=\sqrt{1-x^2}$, these two formulas are the same.

> **Implicit Differentiation**
>
> Instead of a function $y=y(x)$, we are given a formula $F(x, y) = c$ that relates $x$ and $y$.
>
> We differentiate that formula with respect to $x$, treating $y$ as a function of $x$.
>
> Then we solve the resulting equation for $\frac{dy}{dx}$. The result will contain both $x$ and $y$.

Key property: The chain rule tells us that if $y$ is a function of $x$, then:
$$\frac{d}{dx}f(y) = f'(y) \frac{dy}{dx}$$

Example: Consider the relation $y^3+xy^2=x^2+1$. The point $(1, 1)$ belongs to this curve. We want to find the equation of the tangent line to this graph at that point.

The equation would be:
$$y-1 = \left.\frac{dy}{dx}\right|_{(x,y)=(1,1)}(x-1)$$
We use implicit differentiation to compute that derivative. We have:
$$3y^2\frac{dy}{dx} + y^2 + 2xy\frac{dy}{dx} = 2x$$
Solving for $\frac{dy}{dx}$:
$$\frac{dy}{dx} = \frac{2x-y^2}{3y^2+2xy}$$
Plugging in $(x, y) = (1, 1)$:
$$\frac{dy}{dx} = \frac{1}{5}$$
So tangent line equation becomes:
$$y-1 = \frac{1}{5}(x-1)$$

