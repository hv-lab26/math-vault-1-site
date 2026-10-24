# Introductory Calculus

Calc I topics: limits as the foundation for the derivative, the rules for differentiating, and what differentiation is actually used for.

## Notes

1. [[Limits]] — the limit concept, limit laws, continuity and discontinuity, limits at infinity, the first-principles definition of the derivative
2. [[Differentiation Rules]] — power rule, product rule, quotient rule, chain rule, derivatives of trig/exponential/log functions
3. [[Applications of Differentiation]] — stationary points and the first/second derivative test, curve sketching, optimisation, rates of change and kinematics
4. [[Introductory Calculus - Practice and Revision]] — mixed worked problems spanning every topic above

## Formula Sheet

**Limits and the derivative from first principles**

| Concept | Formula |
|---|---|
| Derivative from first principles | $f'(x) = \displaystyle\lim_{h\to0}\dfrac{f(x+h)-f(x)}{h}$ |
| Limit laws | $\displaystyle\lim_{x\to a}[f(x)\pm g(x)] = \lim_{x\to a}f(x)\pm\lim_{x\to a}g(x)$, and similarly for products/quotients (quotient needs $\lim g(x)\mathrel{\char"2260}0$) |
| Continuity at $x=a$ | $f(a)$ is defined, $\displaystyle\lim_{x\to a}f(x)$ exists, and the two are equal |

**Differentiation rules**

| Rule | Formula |
|---|---|
| Power rule | $\dfrac{d}{dx}(x^n) = nx^{n-1}$ |
| Sum/difference rule | $\dfrac{d}{dx}[f(x)\pm g(x)] = f'(x)\pm g'(x)$ |
| Product rule | $\dfrac{d}{dx}[f(x)g(x)] = f'(x)g(x)+f(x)g'(x)$ |
| Quotient rule | $\dfrac{d}{dx}\!\left[\dfrac{f(x)}{g(x)}\right] = \dfrac{f'(x)g(x)-f(x)g'(x)}{[g(x)]^2}$ |
| Chain rule | $\dfrac{d}{dx}f(g(x)) = f'(g(x))\cdot g'(x)$ |
| Exponential | $\dfrac{d}{dx}(e^{x}) = e^{x}$ |
| Natural log | $\dfrac{d}{dx}(\ln x) = \dfrac1x$ |
| Sine / cosine | $\dfrac{d}{dx}(\sin x)=\cos x, \qquad \dfrac{d}{dx}(\cos x)=-\sin x$ |

**Applications**

| Concept | Rule |
|---|---|
| Stationary point | Solve $f'(x)=0$ |
| First derivative test | $f'$ changes $+\to-$: local max; $-\to+$: local min; no sign change: neither |
| Second derivative test | $f''(x)<0$: local max; $f''(x)>0$: local min; $f''(x)=0$: test is inconclusive, fall back to the first derivative test |
| Increasing / decreasing | $f'(x)>0$ on an interval $\implies$ increasing there; $f'(x)<0 \implies$ decreasing |
| Tangent line at $x=a$ | $y-f(a) = f'(a)(x-a)$ |
| Average vs instantaneous rate of change | Average: $\dfrac{f(b)-f(a)}{b-a}$ (gradient of a chord). Instantaneous: $f'(a)$ (gradient of the tangent) |
