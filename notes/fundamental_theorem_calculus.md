# The Fundamental Theorem of Calculus

## Reading

- Sections 5.3, 5.4

## Practice problems

- Section 5.3: 5, 7, 9, 15, 35, 41, 45
- To turn in: 5.3 10, 20, 38, 46
- Section 5.4: 17, 21, 29, 37, 39
- In class: 5.4 17, 33, 35, 44, 45
- To turn in: 5.4 24, 28, 34, 36

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

The Fundamental Theorem of Calculus has a second formulation, that is in a way the "other direction" than that described in the first part. In that part we started with a function $F(x)$, looked at its derivative $f(x) = F'(x)$, then took an integral of that, and landed back to $F$. This version goes the other way.

> **Fundamental Theorem of Calculus, Part II**
>
> Let $f(t)$ be a continuous function on $[a, b]$. Then for each $x\in[a,b]$ we can define:
> $$G(x) = \int_a^xf(t)dt$$
> This defines a function $G$ on $[a, b]$. The theorem is that this function is *differentiable*, and its derivative is:
> $$G'(x) = f(x)$$
> So in a single formula we would write:
> $$\frac{d}{dx}\left(\int_a^x f(t)dt\right) = f(x)$$

As an example, consider the function:
$$g(x) = \int_1^x \frac{1}{t}dt$$
Here's some things we can say about it:

- $g(x)$ is defined for all $x>0$.
- $g(1) = \int_1^1\frac{1}{t}dt = 0$.
- $g(x)$ is differentiable, with derivative $g'(x) = \frac{1}{x}$.
- As its derivative is always positive for $x>0$, $g$ is an increasing function.
- $g''(x) = \left(\frac{1}{x}\right)' = -\frac{1}{x^2}$.
- Since the second derivative is always negative for $x>0$, $g$ is a concave down function.
- Since for $t\geq 1$ we have $\frac{1}{t}\leq 1$, we can also say that for $t\geq 1$ we would have: $$g(x) = \int_1^x\frac{1}{t}dt\leq \int_1^x 1dt = x-1$$

All this information can give us a good handle on the function, and we can for instance do a decent job graphing the function.

Let us look at some variations of the theorem, where the endpoints are more complicated. Suppose we have the following integral function:
$$h(x)=\int_1^{x^2}\frac{1}{t}dt$$
We have no theorem that deals with this function directly. Instead we will think of the function:
$$g(u) = \int_1^u \frac{1}{t}dt$$
For that function we know that $g'(u) = \frac{1}{u}$.

Now $g$ and $h$ are related:
$$h(x) = g(x^2)$$
Therefore we can use the chain rule to find the derivative of $h$. We would have:
$$h'(x) = g'(x^2)(2x) = \frac{1}{x^2}(2x) = \frac{2}{x}$$
So "compute the integrand function at the upper endpoint, then multiply by the derivative of the upper endpoint".

Similarly we can work with cases where the lower endpoint has $x$ in it:
$$h_2(x) = \int_x^1\frac{1}{t}dt$$
We can then write the integral as:
$$h_2(x) = -\int_1^x\frac{1}{t}dt$$
so the derivative would be:
$$h_2'(x) = -\frac{1}{x}$$

If we have both endpoints containing $x$, we can break the problem up in two:
$$h_3(x) = \int_{x^2}^{x^3}\frac{1}{t}dt = \int_1^{x^3}\frac{1}{t}dt - \int_1^{x^2}\frac{1}{t}dt$$
The derivative would then be, as before:
$$h_3'(x) = \frac{1}{x^3}(3x^2) - \frac{1}{x^2}(2x) = \frac{3}{x} - \frac{2}{x} = \frac{1}{x}$$
This is rather interesting, the derivative of this function turned out to be the same as the derivative of our original $\int_1^x \frac{1}{t}dt$. This won't happen in general of course, but it does happen for this particular integrand.

**Practice**: Compute the derivatives of $\int_0^{x^2}\sin(t^2)dt$ and $\int_x^{2x}\frac{\sin t}{t}dt$.

#### Proof of the Fundamental Theorem of Calculus, Part II

We start with the function $f(t)$ and its integral function $G(x) = \int_a^x f(t) dt$. In order to determine if $G(x)$ is differentiable at a point $x$, we need to consider the expression:
$$\lim_{h\to 0}\frac{G(x+h) - G(x)}{h}$$
Throughout the rest of this section, we will treat this point $x$ as a constant.

In order to compute this limit, we start by considering the difference:
$$G(x+h) - G(x) = \int_a^{x+h}f(t)dt - \int_a^x f(t)dt = \int_x^{x+h}f(t)dt$$
We therefore need to get a hold on this integral $\int_x^{x+h}f(t)dt$. In order to do that, we will make a simpifying assumption that $f$ is an increasing function on the interval from $x$ to $x+h$. With that in mind, we can say that for every $t\in[x, x+h]$ we have the inequalities:
$$f(x)\leq f(t)\leq f(x+h)$$
These inequalities are presented when we integrate:
$$\int_x^{x+h}f(x)dt\leq \int_x^{x+h}f(t)dt\leq \int_x^{x+h}f(x+h)dt$$
The first and third integral are the integrals of constants, as our variable is $t$. Therefore they become (since $(x+h)-x=h$:
$$hf(x) \leq \int_x^{x+h}f(t)dt \leq f(x+h)$$
And dividing by $h$ we get:
$$f(x) \leq \frac{\int_x^{x+h}f(t)dt}{h} \leq f(x+h)$$
Going back to $G$, we have:
$$f(x) \leq \frac{G(x+h) - G(x)}{h} \leq f(x+h)$$
We next need to take the limit as $h\to 0$. Since $f$ is a continuous function, then:
$$\lim_{h\to 0}f(x+h) = f(x)$$
So by the squeeze theorem we get that:
$$\lim_{h\to 0}\frac{G(x+h) - G(x)}{h} = f(x)$$
This proves that $G(x)$ is differentiable and its derivative if $G'(x) = f(x)$.
