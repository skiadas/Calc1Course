# The Substitution Method

## Reading

- Section 5.6

## Practice problems

- Section 5.6: 7, 9, 13, 15, 19, 37, 41, 55, 69, 71
- To turn in: 5.6 14, 16, 38, 60, 72

## Notes

### The Substitution Method

The substitution method is a powerful tool in our efforts to compute integrals and antiderivatives. It is essentially the inverse to the chain rule.

#### Indefinite Integrals

> **Substitution Method: Indefinite Integrals**
>
> If $F'(x)=f(x)$, i.e. if $F$ is an antiderivative for $f$, then:
> $$\int f(u(x))u'(x)dx = F(u(x)) + C$$
> Note that the RHS can also be thought of as $\int f(u)du$ with an understanding the at the end we would substitute $u=u(x)$. With that in mind, the substitution method is also written:
> $$\int f(u(x))u'(x)dx = \int f(u)du$$

This follows from direct observation: The derivative of $F(u(x))$ would equal $F'(u(x))u'(x) = f(u(x))u'(x)$.

Example: Suppose we had to compute $\int x\sin(x^2)dx$. We can then consider $u(x) = x^2$, and we would have:
$$\int x\sin(x^2)dx = \frac{1}{2}\int \sin(x^2)(2x)dx = \frac{1}{2}\int\sin u du = -\frac{1}{2}\cos u = -\frac{1}{2}\cos(x^2) + C$$

In general to carry out the substitution:

1. Identify a $u=u(x)$ transformation.
2. Replace $u'(x)dx$ with $du$.
3. Replace all other occurences of $x$ via a suitable form with $u$. If that is not possible then a $u$-substitution is not possible.
4. Compute the resulting indefinite integral.
5. Substitute back for $x$.

As another example, consider the following:
$$\int \frac{x^3}{(1+x^2)^3}dx$$
Here the denominator is problematic, and so it is a good candidate for a substitution:
$$u = 1+x^2$$
We then need to compute:
$$du = (1+x^2)'dx = 2xdx$$
This leaves an $x^2$ in the numerator, and we need to replace it with a suitable expression of $u$:
$$x^2 = u-1$$
Finally, our integral becomes:
$$\int \frac{u-1}{u^3}\frac{du}{2}$$
We can then compute this integral by braking it up in two pieces:
$$\int \frac{u-1}{u^3}\frac{du}{2} = \frac{1}{2}\int \frac{u}{u^3}du - \frac{1}{2}\int \frac{1}{u^3}du = \frac{1}{2}\int \frac{1}{u^2}du - \frac{1}{2}\int \frac{1}{u^3}du = - \frac{1}{2u} + \frac{1}{4u^2} = \frac{-2u + 1}{4u^2} + C$$
Finally, we put back in $u=1+x^2$:
$$\int \frac{x^3}{(1+x^2)^3}dx = \frac{-2(1+x^2) + 1}{4(1+x^2)^2}$$

#### Definite Integrals

There if a version of the substitution method for definite integrals. The main difference is that the *endpoints change*:

> **Substitution Method: Definite Integrals**
>
> $$\int_a^b f(u(x))u'(x)dx = \int_{u(a)}^{u(b)}f(u)du$$

In other words:

1. Identify $u=u(x)$
2. Replace $u'(x)dx$ with $du$.
3. Replace all other occurences of $x$ via a suitable form with $u$. If that is not possible then a $u$-substitution is not possible.
4. Change the endpoints from $x$ values to corresponding $u$ values.
5. Compute the resulting definite integral

As an example, let us compute the integral:
$$\int_0^{\frac{\pi}{2}}\cos x\sin xdx$$
We can do here a substitution $u=\sin x$. Then $du=\cos x dx$. The endpoints will change: When $x=0$ we have $u=\sin 0 = 0$ and when $x=\frac{pi}{2}$ we have $u=\sin \frac{pi}{2} = 1$. So we get the integral:
$$\int_0^{\frac{\pi}{2}}\cos x\sin xdx = \int_0^1 udu = \left.\frac{u^2}{2}\right|_0^1 = \frac{1}{2}$$
