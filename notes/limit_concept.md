# The concept of a limit

## Reading

- Sections 2.1, 2.2

## Practice problems

- Section 2.1: 1, 5, 25, 31
- Section 2.2: 1, 3, 9, 17, 21
- To turn in: 2.1 6, 8, 2.2 2, 22

## Notes

### Average and instantaneous rates of change

- Imagine someone's position on the $x$ axis as as function of time $t$ is given by $x=2t^2$.
- We can find their average *velocity* between two times by taking the ratio of the difference in the $x$ positions over the difference in times.
- If we want to find out how fast the person is going at one specific time, their *instantaneous velocity*, that's harder.
- Think of the value you see in the speedometer of a car. How is it computed?
- Idea: Measure very small time intervals. In fact, make them smaller and smaller.

### Tangent lines

- Consider the graph of a function $f$, and look at a point $(a, f(a))$ on it.
- What is the line that best describes the curve, near $a$?
- Idea: Start with the secant lines: Lines joining the point $a$ and a nearby point.
- Look at the slopes of the secant lines as the nearby point gets closer and closer to $a$.
- Practice: Try this out for $f(x) = $\sqrt{x}$ near $x=1$.

### Limits

- Limits express the idea of what happens to a function $f(x)$ as we look at values of $x$ very close to a specific number $a$.
- Example: $\frac{\sin x}{x}$ when $x$ is near $0$.
- Numerically: Try numbers $x$ closer and closer to $0$. See that the resulting values get closer and closer to 1.
- Definition of limit:
    > We say that *the limit of $f(x)$ as $x$ approaches $a$ is $L$, and we write:
    > $$\lim_{x\to a}f(x) = L$$
    > if the difference $|f(x)-L|$ becomes arbitrarily small when $x$ is sufficiently close (but not equal) to $a$.
    >
    > In other words, the values of $f(x)$ must get arbitrarily close to $L$ when $x$ is sufficiently close but not equal to $a$.
- Simple examples: $\displaystyle\lim_{x\to a} k = k$, $\displaystyle\lim_{x\to a} x = a$
- More complex example: $\displaystyle\lim_{x\to 1} 2x+1 = 3$.
