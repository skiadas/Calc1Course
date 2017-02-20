# Linear Approximation

## Reading

- Section 4.1

## Practice problems

- Section 4.1 13, 15, 17, 19, 23, 25, 33, 38, 45
- To turn in (together with 4.2): 4.1 14, 46, 52

## Notes

### Linear Approximation

Derivatives allow us to approximate changes to a function over a small interval.

Some notation:

- $\Delta x$ represents a small change in $x$. So we consider our $x$ changing from $a$ to $a+\Delta x$.
- Denote by $\Delta f = f(a+\Delta x) - f(a)$. Namely how much $f$ has changed as $x$ changes from $a$ to $a+\Delta x$.

> **Linear Approximation of $\Delta f$**: If $f$ is differentiable at $a$, and $\Delta x$ is small, then:
> $$\Delta f \approx f'(a) \Delta x$$
> In other words, we can approximate the *actual change* $\Delta f$ with the quantity $f'(a)\Delta x$.
>
> In graphical terms, the linear approximation says that the tangent line is a good approximation to the function as long as we keep close to the point of tangency.

Example: Suppose $f(x) = \frac{1}{x}$, $a=5$ and $\Delta x = 0.1$. Then:
$$\Delta f = f(5.1) - f(5) = \frac{1}{5.1} - \frac{1}{5} = -0.003921569$$
Instead we could estimate this quantity via:
$$f'(5)\cdot 0.1 = \frac{-1}{5^2} \cdot 0.1 = -0.004$$
The error we have made is only $-0.004-(-0.003921569) = -0.000078431$, which is about a $2\%$ error relative to the actual value.

> **Differential Notation**
>
> In this notation we write $dx=\Delta x$ and $dy = f'(a)dx$. Then:
> $$\Delta y \approx dy$$

We can write the same approximation in terms of $f(x)$. For that we write $x = a + \Delta x$, so $\Delta f = f(x) - f(a)$, and $dy = f'(a)(x-a)$. We then have the following approximation:

> **Approximation of $f(x)$ by its linearization**
>
> If f(x) is differentiable at $x=a$, and $x$ is a number is close to $a$, then:
> $$f(x) \approx L(x) = f(a) + f'(a)(x-a)$$

Example: If $f(x) = \sqrt{x}$ and $a=4$. Then $f'(x) = \frac{1}{2\sqrt{x}}$, and we can compute the linearization:
$$L(x) = f(4) + f'(4)(x-4) = 2 + \frac{1}{4}(x-4)$$
As an example, let us estimate the value of $\sqrt{4.1}$, which is in reality very close to $2.024846$. Our linearization would instead give us:
$$L(x)  = 2 + \frac{1}{4}(4.1-4) = 2.025$$

Linearizations have numerous applications in other sciences.
