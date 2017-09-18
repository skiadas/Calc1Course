# Trigonometric Limits

## Reading

- Sections 2.6

## Practice problems

- Section 2.6: 5, 7, 14, 17, 19, 21, 33, 37, 43
- To turn in (due Friday, together with 2.5): 2.6 10, 24, 40

## Notes

### The Squeeze Theorem

- The squeeze theorem allows us to deal with functions that have some parts that are hard to deal with, but end up to not matter in the long run.
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

###  Continuity of Trigonometric Functions

The squeeze theorem allows us to prove two important trigonometric limits. We first discuss how it can help us show that the trig functions are continuous. We first show that sine and cosine are continuous at $0$:

> $$\lim_{t\to 0}\sin t = 0,\quad \lim_{t\to 0}\cos t = 1$$

This follows from the following: Consider the unit circle, and a sector of angle $t$ radians on it, starting from the $x$ axis. Denote the point on the circle $A$, and the point on the $x$ axis where the circle starts as $B$.

Then the chord from $A$ to $B$ has length $\sqrt{(1-\cos t)^2 + \sin^2 t}$, while the part of the circle from $A$ to $B$ has length $|t|$. And the length of the chord is obviously less, so we have the inequality:
$$\sqrt{(1-\cos t)^2 + \sin^2 t}\leq |t|$$
Because the two sides of a right-angle triangle have length less than the hypotenuse, we also have the inequalities:
$$0\leq |1-\cos t|\leq\sqrt{(1-\cos t)^2 + \sin^2 t}\leq |t|$$
$$0\leq |\sin t|\leq\sqrt{(1-\cos t)^2 + \sin^2 t}\leq |t|$$
The squeeze theorem now gives us the desired results, along with the following important observation:

> $$\lim_{x\to a}f(x) = 0\textrm{ if and only if }\lim_{x\to a}|f(x)| = 0$$

We now show in general that the sine and cosine functions are continuous, namely:

> $$\lim_{x\to a}\sin x = \sin a,\quad \lim_{x\to a}\cos x = \cos a$$

We only show the case of sine here; the case of cosine is similar. The key is to rewrite the limit, using $t = x-a$, or $x=a+t$:
$$\lim_{x\to a}\sin x = \lim_{t\to 0} \sin(a+t)$$
We then use the trigonometric identity:
$$\lim_{t\to 0} \sin(a+t) = \lim_{t\to 0} \sin a \cos t + \cos a \sin t = \sin a \lim_{t\to 0}\cos t + \cos a\lim_{t\to 0} \sin t = \sin a\cdot 1 + \cos a \cdot 0 = \sin a$$

### Trigonometric Limits

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
