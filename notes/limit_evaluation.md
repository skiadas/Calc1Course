# Evaluating Limits

## Reading

- Sections 2.5

## Practice problems

- Section 2.5: 5, 7, 11, 13, 21, 24, 25
- To turn in (together with 2.6): 2.5 16, 30

## Notes

### Algebraic Evaluation of Limits

- Many limits cannot be evaluated by substitution.
- Most typical case is a "0 over 0".
- Example: $\displaystyle \lim_{x\to 2}\frac{x^2-4}{x-2}$
- Solution: Perform algebraic manipulation to the function, without changing the value but eliminating the problematic part.
- In this example: $\frac{x^2-4}{x-2} = \frac{(x-2)(x+2)}{x-2} = x+2$
- We were able to eliminate the term $x-2$, which was the one causing the zeros.
    > When dealing with limits that cannot be evaluated directly:
    >
    > - Perform algebraic transformations until the problematic terms go away.
    > - Evaluate limit of resulting expression by substitution/plugging in.
- Other examples:
    - $\displaystyle\lim_{x\to 4}\frac{\sqrt{x} - 2}{x-4}$. Use "conjugate".
    - $\displaystyle\lim_{x\to 1}\left(\frac{1}{x-1} - \frac{2}{x^2-1}\right)$ ($\infty - \infty$ form). Make common denominators.
    - $\displaystyle\lim_{x\to \frac{\pi}{2}}\frac{\tan x}{\sec x}$. Write in terms of $\sin$, $\cos$.
