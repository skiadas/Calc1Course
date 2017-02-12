# Chain Rule

## Reading

- Sections 3.7

## Practice problems

- Section 3.7: 7, 9, 13, 21, 27, 31, 69
- To turn in (together with 3.6): 3.7 12, 70

## Notes

### The Chain Rule

The chain rule tells us how to differentiate the composite of two functions:

> **Composite function**
> $$(f \circ g)(x) = f(g(x))$$

We evaluate the composite function on an $x$ by applying the *inner function* first, followed by the *outer function*.

> $$(f(g(x)))' = f'(g(x))g'(x)$$
> "Derivative of the outer, applied to the inner, times the derivative of the inner"

Examples:

- $\sin(x^3)$. Here $f(u) = \sin u$, $u=g(x) = x^3$. Derivative is $\cos(x^3)3x^2$.
- $\tan\left(\frac{1}{1+x}\right)$.
- $\cos(\cos x)$.

Alternative formulation:

> If $u=g(x)$, and $y=f(u)$, we can view $y=f(g(x))$ as a function of $x$. Then:
> $$\frac{dy}{dx} = \frac{dy}{du}\cdot\frac{du}{dx}$$

Special case of chain rule:

> **General Power Rule**
> $$\frac{d}{dx}g(x)^n = n g(x)^{n-1}g'(x)$$
