# Limit Laws

## Reading

- Sections 2.3

## Practice problems

- Section 2.3 3, 5, 8, 9, 11, 13, 27, 31
- To turn in (together with 2.4): 2.3 12, 14

## Notes

### Limit Laws

A number of laws govern the computation of limits. These laws allow us to compute a limit of a more complex function based on the limits of its (simpler) components.

> **Basic Limit Laws:**
>
> If $\displaystyle\lim_{x\to c}f(x)$ and $\displaystyle\lim_{x\to c}g(x)$ exist, then:
>
> - **Constant and Linear Law**: $\displaystyle \lim_{x\to c}k = k$, $\displaystyle \lim_{x\to c} x = c$.
> - **Sum Law**: The limit $\displaystyle\lim_{x\to c}f(x) + g(x)$ also exists and:
>     $$\displaystyle\lim_{x\to c}f(x) + g(x) = \lim_{x\to c}f(x) + \lim_{x\to c}g(x)$$
> - **Constant Multiple Law**: The limit $\displaystyle\lim_{x\to c}k f(x)$ also exists and:
>     $$\displaystyle\lim_{x\to c}k f(x) = k\lim_{x\to c}f(x)$$
> - **Product Law**: The limit $\displaystyle\lim_{x\to c}f(x)g(x)$ also exists and:
>     $$\displaystyle\lim_{x\to c}f(x)g(x) = \lim_{x\to c}f(x)\lim_{x\to c}g(x)$$
> - **Quotient Law**: If further $\displaystyle\lim_{x\to c}g(x)\neq 0$, then the limit $\displaystyle\lim_{x\to c}\frac{f(x)}{g(x)}$ also exists and:
>     $$\displaystyle\lim_{x\to c}\frac{f(x)}{g(x)} = \frac{\displaystyle\lim_{x\to c}f(x)}{\displaystyle\lim_{x\to c}g(x)}$$
> - **Power Law**: The limit $\displaystyle\lim_{x\to c}f(x)^n$ also exists and:
>     $$\displaystyle\lim_{x\to c}f(x)^n = \left(\lim_{x\to c}f(x)\right)^n$$
> - **Root Law**: If further $\displaystyle\lim_{x\to c}g(x)\neq 0$, then the limit $\displaystyle\lim_{x\to c}\sqrt[n]{f(x)}$ also exists and:
>     $$\displaystyle\lim_{x\to c}\sqrt[n]{f(x)} = \sqrt[n]{\lim_{x\to c}f(x)}$$

For example, let's compute $\displaystyle\lim_{x\to 1} \sqrt{x^3 + 2x}$:

- $\displaystyle\lim_{x\to 1} \sqrt{x^3 + 2x} = \sqrt{\lim_{x\to 1} x^3 + 2x} = \sqrt{\lim_{x\to 1} x^3 + \lim_{x\to 1} 2x}$
- We now compute each part: $\displaystyle \lim_{x\to 1} x^3 = \left(\lim_{x\to 1} x\right)^3 = 1^3 = 1$
- And: $\displaystyle\lim_{x\to 1} 2x = 2\lim_{x\to 1} x = 2\times 1 = 2$
- Putting it all together we get: $\sqrt{1 + 2} = \sqrt{3}$
