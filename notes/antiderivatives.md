# Newton's method

## Reading

- Section 4.8

## Practice problems

- Section 4.8: 11, 13, 15, 23, 25, 45, 49, 64, 65
- To turn in: 4.8 14, 22, 50
- In class: 4.8 40, 41, 63

## Notes

### Antiderivatives

> An **antiderivative** for a function $f(x)$ is a function $F(x)$ such that $F'(x) = f(x)$. In this sense the antiderivative is an inverse process to the derivative.

An example: Since $(\sin(3x))' = 3\cos(3x)$, we can say that the function $\sin(3x)$ is *an antiderivative* for the function $3\cos(3x)$.

Note that also $\sin(3x) + 5$ would be an antiderivative, as an added constant goes away when we differentiate. In that sense we can have many antiderivatives for a function. They are however all related to each other via adding a constant, as the following theorem describes:

> **Theorem**
>
> If $F(x)$ is an antiderivative of $f(x)$ on an interval $(a, b)$, then all the antiderivatives of $f(x)$ have the form $F(x) + C$ for some constant $C$.
>
> We use the symbol $\int f(x)dx$ to denote these antiderivatives, and we call it the **indefinite integral**. Equalities involving indefinite integrals only make sense up to an additive constant.

One standard example where we can compute the antiderivative is polynomials. This essentially reverses the power rule that $\left(x^{n+1}\right)' = (n+1)x^n$:

> **Power Rule for Antiderivatives**
>
> $$\int x^n dx = \frac{x^{n+1}}{n+1} + C$$
> as long as $n\neq 1$.

The antiderivative of $\frac{1}{x}$ cannot be obtained via the above rule. It turns out to be a very interesting function, called the *natural logarithm*, and it will be defined and discussed more in Calculus 2.

The above theorem also shows us a general process for figuring out some of these antiderivatives: If we can guess a function that has the desired derivative, then we have found our antiderivative. For instance this way of thinking can produce the following antiderivatives:

> **Basic Trigonometric Antiderivatives**
>
> $$\int\sin x dx = -\cos x + C$$
> $$\int\cos x dx = \sin x + C$$
> $$\int\sec^2 x dx = \tan x + C$$
> $$\int\sec x\tan xdx = \sec x + C$$

### Initial Value Problems

A first application of these ideas is the solution of simple differential equations. A differential equation is an equation where the unknown is a function $y=y(x)$, and the equation involves the derivatives of the function. For example the antiderivative of a function $f(x)$ solves the differential equation:
$$\frac{dy}{dx} = f(x)$$

In these situations the solution is only determined up to a constant $C$. The constant can often be determined if they also provide us the value that the function must take at a particular point. This is often called an **initial value**.

**Example:** Find the function $y$ such that $\frac{dy}{dx} = x^3$ and with the initial value $y(0) = 3$.

We would start by computing $\int x^3dx = \frac{1}{4}x^4 + C$. So this tells us that our function $y$ must have the form $y(x) = \frac{1}{4} x^4 + C$. We just need to find the $C$.

But they also told us that $y(0) = 3$. This must mean that $3=\frac{1}{4}\times 0^4 + C = C$, so the constant must be $C=3$. So we have our final answer:
$$y(x) = \frac{1}{4}x^4 + 3$$
