# The Fundamental Theorem of Calculus

## Reading

- Sections 5.3, 5.4

## Practice problems

- Section 5.3: 5, 7, 9, 15, 35, 41, 45
- To turn in: 5.3 10, 20, 38, 46
- Section 5.4: TODO
- To turn in: 5.4 TODO

## Notes

### The Fundamental Theorem of Calculus, Part I

The Fundamental Theorem of Calculus (FTC) is one of the cornerstones of the course. It is a deep theorem that relates the processes of integration and differentiation, and shows that they are in a certain sense inverse processes.

The FTC has two parts. We will first discuss the first form of the theorem:

> **Fundamental Theorem of Calculus, Part I**
>
> If $F(x)$ is an antiderivative of $f(x)$ on $[a, b]$, i.e. $F'(x) = f(x)$ on $[a, b]$, then we have:
> $$\int_a^bf(x)dx = F(b) - F(a)$$
>
> In essence, we can directly compute an integral if we know of an antiderivative for the integrand.
>
> Shorthand notation: The difference $F(b)-F(a)$ is often written as:
> $$\bigl.F(x)\bigr|_a^b$$

Examples:

$$\int_1^4 x^2dx = \left.\frac{x^3}{3}\right|_1^4 = \frac{4^3}{3}-\frac{1^3}{3} = \frac{63}{3} = 21$$
$$\int_0^\pi \cos xdx = \bigl.\sin x\bigr|_0^\pi = \sin\pi - \sin 0 = 0$$

Make sure to understand that second integral graphically, and why it should indeed equal $0$.

#### Proof of the Fundamental Theorem of Calculus, Part I

The idea of the theorem is to relate the difference $F(b) - F(a)$ to the Riemann sums.

We start with a partition $P$ of the interval $[a, b]$:
$$\left\{ a = x_0 < x_1 < x_2 < x_3 < \cdots < x_N = b \right\}$$
On each interval, we want to estimate the difference in the endpoints, $F(x_i) - F(x_{i-1})$. To do that, we use the mean value theorem, which says that this difference should equal $F'(c_i)(x_i-x_{i-1})$ for some point $c_i\in[x_{i-1}, x_i]$L
$$F(x_i) - F(x_{i-1}) = F'(c_i)(x_i-x_{i-1})$$
Since $F'=f$, we have:
$$F(x_i) - F(x_{i-1}) = f(c_i)\Delta x_i$$
If we write this for every $i$, then add up all the equations, the left-hand-side has many terms cancelling out:
$$\left[F(x_1)-F(x_0)\right] + \left[F(x_2)-F(x_1)\right] + \left[F(x_3)-F(x_2)\right] + \cdots + \left[F(x_N)-F(x_{N-1})\right]$$
Note that every term except for $F(x_0)=F(a)$ and $F(x_N)=F(b)$ appears twice, once with a plus sign and once with a minus sign. So they all cancel out. We end up with the formula:
$$F(b) - F(a) = \sum_{i=1}^N f(c_i)\Delta x_i$$
The right-hand-side is exactly a Riemann sum with those specific sample points. In other words:

> For every partition $P$ there is a choice $C$ of sample points such that:
> $$R(f, P, C) = \sum_{i=1}^N f(c_i)\Delta x_i = F(b) - F(a)$$

Since this happens for every partition, and since the right-hand-side is a constant independent of the partition, it follows that the limit should have the same relation, so:
$$\int_a^b f(x)dx = F(b) - F(a)$$
as desired.

### The Fundamental Theorem of Calculus, Part II

TODO
