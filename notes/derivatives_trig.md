# Derivatives of Trigonometric Functions

## Reading

- Section 3.6

## Practice problems

- Section 3.6: 5, 7, 17, 21, 27, 29, 41, 45
- To turn in (together with 3.7): 3.6 18, 28, 42

## Notes

### Derivatives of sine and cosine

> $$\frac{d}{dx}\sin x = \cos x,\qquad \frac{d}{dx} \cos x = -\sin x$$

Watch out for the minus sign!

Proof:

- Definition of derivative: $\frac{d}{dx}\sin x = \lim_{h\to 0}\frac{\sin(x+h) - \sin(x)}{h}$
- Use trig identity: $\sin(x+h) = \sin x \cos h + \cos x \sin h$
- Algebra

Second derivatives:

> $$\frac{d^x}{dx^2} \sin x = - \sin x, \qquad \frac{d^2}{dx^2} \cos x = - \cos x$$
> Both $\sin$ and $\cos$ satisfy the differential equation $f''(x) = f(x)$.

Practice problems: Derivatives of $\sin x  + \cos x$, $x\sin(2x)$, $\frac{x}{\cos x}$

### Derivatives of other trigonometric functions

Other trigonometric functions are written in terms of sine and cosine. We can compute their derivatives using the derivatives of $\sin$ and $\cos$.

> $$\frac{d}{dx}\tan x = \sec^2x = 1 + \tan^2x, \qquad \frac{d}{dx}\sec x = \sec x \tan x$$

Proof:

- $\tan x = \frac{\sin x}{\cos x}$
- Apply quotient rule: $\tan' x = \frac{\sin^2 x + \cos^2 x}{\cos^2 x}$
- Numerator equal 1, so this is $\sec^2x$.
- Alternatively, rewrite it as $1 + \frac{\sin^2x}{\cos^2x} = 1+\tan^2x$.

Practice: Do the same for $\sec x$.

Practice: Compute the tangent lines to $\tan x$ at $x=0$ and at $x=\frac{\pi}{4}$.
