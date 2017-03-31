*# The Definite Integral

## Reading

- Section 5.2

## Practice problems

- Section 5.2: 3, 5, 7, 13, 15, 17, 37, 41, 45, 55, 57
- To turn in: 5.2 4, 14, 18, 40

## Notes

### The definite integral

In the previous section we estimated areas by considering a partition of an interval into subintervals, then estimating the area on each interval as a rectangle, using the leftmost endpoint or rightmost endpoint each time, or a couple of other variations. These are all variations of what is known as a *Riemann Sum*

> Given a function $f$ on $[a, b]$ and a *partition* $P$ of $f$ consisting of $N$ intervals (and $N+1$ points): $a = x_0 < x_1 < \cdots < x_{N} = b$, we further pick a point $c_i$ on each interval $[x_{i-1}, x_i]. These are called *sample points*, and we denote the overall choice of one such point for each interval as $C$. We then define the **Riemann Sum** for the function for that partition and that choice of sample points as:
> $$R(f, P, C) = \sum_{i=1}^N f(c_i)\Delta x_i$$
> We define the **definite integral** of $f$ as the limit of these sums as the partitions have a smaller and smaller *norm*. The **norm** of a partition is defined as the largest interval length:
> $$\|P\| = \max\{\Delta x_i\}$$
> The integral is written as follows:
> $$\int_a^b f(x) dx = \lim_{\|P\|\to 0} R(f, P, C) = \lim_{\|P\|\to 0}\sum_{i=1}^N f(c_i)\Delta x_i$$
> If the integral exists, we say the function is **integrable**.
>
> Geometrically, we can think of the definite integral as the *signed area* between the function and the $x$-axis.

Directly computing the above limit is not very practical, and we will find ways around it shortly. For now, we can use the following theorem that guarantees for us that these integrals exist for many functions:
> If $f(x)$ is continuous on $[a, b]$, or continuous except for maybe finitely many points, then $f$ is integrable over $[a, b]$.

### Properties of the definite integral

The definite integrals enjoys some key properties that allow us to compute it in many concrete situations. Most of these properties follow from considering the corresponding Riemann sums.

> Integral of constant
>
> If $f(x)=k$ is a constant function, then:
> $$\int_a^b k dx = k (b-a)$$

> Linearity of integral
>
> If $f$, $g$ are integrable functions, then $f+g$ and $kf(x)$ are also integrable and:
> $$\int_a^b f(x) + g(x)dx = \int_a^b f(x)dx + \int_a^b g(x)dx$$
> $$\int_a^b k f(x)dx = k\int_a^b f(x)dx$$

**Practice problem 1**: Armed with these properties, along with the identities $\int_0^b xdx = \frac{b^2}{2}$ and $\in_0^b x^2dx = \frac{b^3}{3}$, compute the integral $\int_0^5 \left(2x^2-3x+1\right)$

Another set of properties has to do with changing the endpoints of integration:

> When the endpoints $a = b$ match, we define:
> $$\int_a^a f(x)dx = 0$$
> For $a< b$, we define:
> $$\int_b^a f(x)dx = -\int_a^b f(x)dx$$
>
> For any three numbers $a, b, c$ we have:
> $$\int_a^c f(x)dx = \int_a^bf(x)dx + \int_b^c f(x)dx$$
> or alternatively written:
> $$\int_b^c f(x)dx = \int_a^cf(x)dx - \int_a^b f(x)dx$$

**Practice problem 2**: Using these properties, compute $\int_a^b x^2 dx$.

Finally we have two theorems that have to do with a comparison of function:

> Comparison
>
> If $f$ and $g$ are integral functions, $a < b$ and $g(x) \leq f(x)$ for all $x\in[a, b]$, then the integrals have the same relationship:

> $$\int_a^b f(x)dx \leq \int_a^b g(x)dx$$

An important consequence of this is the following:

> If $m$ and $M$ are such that $m\leq f(x) \leq M$ for all $x\in[a, b]$, then:
> $$m(b-a)\leq \int_a^b f(x)dx\leq M(b-a)$$
