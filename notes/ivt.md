# Intermediate Value Theorem

## Reading

- Sections 2.8

## Practice problems

- Section 2.8:  1, 5, 7, 19
- In class: 2.8 14: $\tan x = x$ has infinitely many solutions
- To turn in (due Wednesday, together with 2.7): 2.8 2, 6

## Notes

### Intermediate Value Theorem

> **Intermediate Value Theorem**
>
> If $f(x)$ is a continuous function on $[a,b]$ and $L$ is a number between $f(a)$ and $f(b)$, then there must be a $c\in[a,b]$ such that $f(c) = L$.
>
> Simply put: A continuous function takes all values between $f(a)$ and $f(b)$.
>
> **Important special case:** If $f(a)$ and $f(b)$ have opposite signs, then the function $f$ must have a zero somewhere between $a$ and $b$.

- Make sure to have a good graphical representation of this result.
- The importance of the theorem is that it allows us to guaranteed the existence of solutions to equations.
- Example: We will show that $\sqrt{2}$ exists:
    - The square root is a number $c$ such that $c^2 = 2$.
    - Consider the function $f(x) = x^2$ on the interval $[1,2]$.
    - Then $f(1) < 2 < f(2)$.
    - The IVT tells us there must be a $c\in[1,2]$ with $f(c) = 2$.
- Example 2: Show that there is a positive $x$ with $x = \sin x$.
    - Idea: Bring everything to one side: $f(x) = x - \sin x$.
    - Look for a zero.
- **Bisection method**: Allows us to zero in on a solution:
    - In the previous example, consider $f(1.5)$. Since it is bigger than $2$, the $c$ is actually in $[1,1.5]$.
    - Try $f(1.25)$ next.
    - Keep bisecting the interval and trying the middle value.
    - Practice: Find the first 3 decimals points of $\sqrt{2}$.
