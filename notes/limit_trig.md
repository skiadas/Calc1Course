# Trigonometric Limits

## Reading

- Sections 2.6

## Practice problems

- Section 2.6: 5, 7, 14, 17, 19, 21, 33, 37, 43
- To turn in (together with 2.5): 2.6 10, 24, 40

## Notes

### The Squeeze Theorem

- The squeeze theorem allows us to deal with functions that have some parts that are hard to deal with, but end up not to not matter in the long run.
- Example: $\displaystyle \lim_{x\to 0} x \sin\frac{1}{x}$
    - $\sin\frac{1}{x}$ behaves erratically. But it stays within $\pm 1$.
    - $x$ goes to $0$.
    - Their product would also go to $0$, because it never exceeds $\pm x$.

> **Squeeze Theorem**:
>
> Assume that for all $x\neq c$ in some interval containing $c$ we have:
> $$\ell(x) \leq f(x) \leq u(x)$$
> and also that we have that the limits of $\ell$ and $u$ agree:
> $$\lim_{x\to c}\ell(x) = \lim_{x\to c}u(x) = L$$
> Then we have that the limit of $f(x)$ also exists and:
> $$\lim_{x\to c}f(x) = L$$

- Example of using the squeeze theorem:
    - $f(x) = x\sin\frac{1}{x}$, $\ell(x) = -x$, $u(x) = x$
    - Then $\ell(x) \leq f(x) \leq u(x)$
    - And $\displaystyle\lim_{x\to 0}\ell(x) =  \lim_{x\to 0}-x = 0$, $\displaystyle\lim_{x\to 0}u(x) =  \lim_{x\to 0}x = 0$
    - Therefore by the squeeze theorem we also get that $\displaystyle\lim_{x\to 0}f(x) =\lim_{x\to 0}x\sin\frac{1}{x} = 0$.

### Trigonometric Limits

The squeeze theorem allows us to prove two important trigonometric limits:

> **Important Trigonometric Limits**
> $$\lim_{x\to 0}\frac{\sin x}{x} = 1$$
> $$\lim_{x\to 0}\frac{1 - \cos x}{x} = 0$$

The first of these limits follows from the following theorem:

> **Theorem**
> For all $x\neq 0$ with $-\frac{\pi}{2} < x < \frac{\pi}{2}$, we have:
> $$\cos x \leq \frac{\sin x}{x}\leq 1$$

- Proof of the theorem: Consider the unit circle, and compare the area of a sector and two triangles surrounding it.
- The first limit follows directly from this theorem.
- The second limit follows from the following:
    $$\frac{1-\cos x}{x} = \frac{1-\cos^2 x}{x(1+\cos x)} = \frac{\sin^2 x}{x(1+\cos x)} = \frac{\sin x}{1+\cos x}\cdot \frac{\sin x}{x}$$

### Other trigonometric limits

The above limits can give rise to other limits as well:

- $\displaystyle\lim_{x\to 0}\frac{\sin(3x)}{x}$
- $\displaystyle\lim_{x\to 0}\frac{\sin(3x)}{\sin(5x)}$
- $\displaystyle\lim_{x\to 0}\frac{\sin(3x)}{\tan(x)}$
