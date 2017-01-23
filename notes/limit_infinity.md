# Limits at Infinity

## Reading

- Sections 2.7

## Practice problems

- Section 2.7: 1, 3, 7, 9, 13, 17, 19, 37
- In class: 2.7 35
- To turn in (due Wednesday, together with 2.8): 2.7 8, 20

## Notes

### Limits at Infinity

- We can consider limits when $x\to\infty$ or $x\to \infty$.
- If $\displaystyle\lim_{x\to\infty}f(x) = L$, we say that the line $y=L$ is a **horizontal asymptote** for $f$.
- Key limits:

    > For all $n > 0$: $$\lim_{x\to\infty}x^n = \infty,\qquad \lim_{x\to \infty}x^{-n}=0$$
    > For odd whole numbers $n$: $$\lim_{x\to -\infty}x^n = -\infty$$
    > For even whole numbers $n$: $$\lim_{x\to -\infty}x^n = \infty$$
    > For all whole numbers $n$: $$\lim_{x\to -\infty}x^{-n} = 0$$
- Limits of rational functions behave in the same way as their leading terms:

    > $$\lim_{x\to\pm\infty}\frac{a_n x^n + a_{n-1}x^{n-1}+\cdots + a_0}{b_m x^m + b_{m-1}x^{m-1}+\cdots + b_0} =\frac{a_n}{b_n}\lim_{x\to\pm\infty} x^{n-m}$$
- Example: $\displaystyle\lim_{x\to\infty}\frac{x^3-2x+1}{2x^2+1}$
- One approach to this: Factor out greatest power at numerator and denominator separately. Leaves a lot of $\frac{1}{x^n}$ that go to $0$.
- Another approach to limits at infinity: Set $t=\frac{1}{x}$, look at $t\to 0^+$ or $t\to 0^-$.
