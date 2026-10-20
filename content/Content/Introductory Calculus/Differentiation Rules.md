# Differentiation Rules

Differentiation is the process of finding the **derivative** of a function — a new function, $f'(x)$, that gives the gradient of the original function at every value of $x$. Working out a derivative directly from the limit definition (covered in [[Limits]]) every single time would be slow, so instead we use a toolkit of **rules** that let us differentiate almost any function built from powers, exponentials, logarithms and trigonometric functions, combined by addition, multiplication, division or composition. This note collects every one of those rules at Unit 1 level, explains briefly *why* each one works, and works through every example and exercise from the source lecture notes in full.

Once you can find $f'(x)$, [[Applications of Differentiation]] shows what it is actually used for — stationary points, optimisation, and rates of change.

## Notation

For a function $y = f(x)$, the derivative can be written in several equivalent ways:

$$f'(x) \quad \text{or} \quad y' \quad \text{or} \quad \dfrac{dy}{dx} \quad \text{or} \quad \dfrac{d}{dx}\big[f(x)\big]$$

All of these mean exactly the same thing: "the rate of change of $y$ with respect to $x$", i.e. the gradient function. $\dfrac{dy}{dx}$ is **not** a fraction in the ordinary sense (it comes from the limit $\lim_{h\to 0}\dfrac{\Delta y}{\Delta x}$), but it is useful to *treat* it like a fraction when applying the chain rule below — that is exactly what makes the "substitute $u$" method work.

## Key Formulas

Every rule used in this note, gathered in one place.

| Rule | If... | ...then |
|---|---|---|
| Constant rule | $f(x) = c$ | $f'(x) = 0$ |
| Power rule | $f(x) = x^n$ | $f'(x) = nx^{n-1}$ |
| Sum/difference rule | $f(x) = u(x) \pm v(x)$ | $f'(x) = u'(x) \pm v'(x)$ |
| Chain rule (Leibniz form) | $y$ is a function of $u$, and $u$ is a function of $x$ | $\dfrac{dy}{dx} = \dfrac{dy}{du} \times \dfrac{du}{dx}$ |
| Product rule | $f(x) = u(x)v(x)$ | $f'(x) = u(x)v'(x) + v(x)u'(x)$ |
| Quotient rule | $f(x) = \dfrac{u(x)}{v(x)}$ | $f'(x) = \dfrac{v(x)u'(x) - u(x)v'(x)}{[v(x)]^2}$ |
| Exponential | $f(x) = e^x$ | $f'(x) = e^x$ |
| Exponential (scaled) | $f(x) = e^{kx}$ | $f'(x) = ke^{kx}$ |
| Exponential (composite) | $f(x) = e^{g(x)}$ | $f'(x) = g'(x)e^{g(x)}$ |
| Natural log | $f(x) = \log_e x$ | $f'(x) = \dfrac{1}{x}$ |
| Natural log (scaled) | $f(x) = \log_e(kx)$ | $f'(x) = \dfrac{1}{x}$ |
| Natural log (composite) | $f(x) = \log_e[g(x)]$ | $f'(x) = \dfrac{g'(x)}{g(x)}$ |
| Sine | $f(x) = \sin x$ | $f'(x) = \cos x$ |
| Cosine | $f(x) = \cos x$ | $f'(x) = -\sin x$ |
| Tangent | $f(x) = \tan x$ | $f'(x) = \dfrac{1}{\cos^2 x}$ |
| Sine (scaled) | $f(x) = \sin(ax)$ | $f'(x) = a\cos(ax)$ |
| Cosine (scaled) | $f(x) = \cos(ax)$ | $f'(x) = -a\sin(ax)$ |
| Tangent (scaled) | $f(x) = \tan(ax)$ | $f'(x) = \dfrac{a}{\cos^2(ax)}$ |
| Sine (composite) | $f(x) = \sin[g(x)]$ | $f'(x) = g'(x)\cos[g(x)]$ |
| Cosine (composite) | $f(x) = \cos[g(x)]$ | $f'(x) = -g'(x)\sin[g(x)]$ |
| Tangent (composite) | $f(x) = \tan[g(x)]$ | $f'(x) = \dfrac{g'(x)}{\cos^2[g(x)]}$ |

(The composite-function rows are just the chain rule applied once and for all to each standard function — see each section below for why they take this form.)

## Power Rule and Sum/Difference Rule

The power rule, $\dfrac{d}{dx}(x^n) = nx^{n-1}$, is normally established from first principles before this stage of the course (see [[Limits]]); briefly, expanding $(x+h)^n$ with the [[Binomial Theorem]] gives $(x+h)^n = x^n + nx^{n-1}h + \binom{n}{2}x^{n-2}h^2 + \dots$, so $\dfrac{(x+h)^n - x^n}{h} = nx^{n-1} + \binom{n}{2}x^{n-2}h + \dots \to nx^{n-1}$ as $h\to 0$ — every term after the first one vanishes in the limit. A constant term differentiates to $0$ (it is "$x^0$ times a number", and its graph has zero gradient everywhere).

The **sum/difference rule** says you can differentiate a sum of terms one term at a time: $\dfrac{d}{dx}[u(x) \pm v(x)] = u'(x) \pm v'(x)$. This is really just saying that gradients add — the rate of change of a sum is the sum of the rates of change.

#### Practice Q1: Differentiate $f(x) = 3x^2 - 6x + 2$

Differentiating term by term with the power rule ($3x^2 \to 6x$, $-6x \to -6$, $2 \to 0$):

$$f'(x) = 6x - 6$$

#### Practice Q2: Differentiate $f(x) = \sin x + \log_e x - 2e^x - \cos x$

This question previews the exponential, logarithmic and trigonometric derivatives covered in detail later in this note — using the summary table above, each term differentiates independently:

$$f'(x) = \cos x + \frac{1}{x} - 2e^x - (-\sin x) = \cos x + \frac{1}{x} - 2e^x + \sin x$$

### Negative and Fractional Indices

The power rule works for **any** real index $n$ — including negative and fractional ones — once the function is rewritten as a power of $x$, using the index laws

$$\frac{a}{x^b} = ax^{-b} \qquad\qquad \sqrt[b]{x^a} = x^{a/b}$$

#### Example: Differentiate $h(x) = -\sqrt3\,x^{1/2}$

$$h'(x) = -\sqrt3\times\frac12\times x^{-1/2} = -\frac{\sqrt3}{2}x^{-1/2}$$

#### Worked Example: Differentiate (a) $f(x)=\dfrac1x+\dfrac{1}{\sqrt x}$

Rewriting as powers of $x$: $f(x) = x^{-1}+x^{-1/2}$.

$$f'(x) = -1x^{-2} - \frac12 x^{-3/2} = -\frac{1}{x^2} - \frac{1}{2\sqrt{x^3}}$$

#### Worked Example: Differentiate (b) $f(x) = \dfrac2x - 3\sqrt x$

Rewriting: $f(x) = 2x^{-1}-3x^{1/2}$.

$$f'(x) = -2x^{-2} - \frac32x^{-1/2} = -\frac{2}{x^2} - \frac{3}{2\sqrt x}$$

#### Example: Differentiate $g(x) = \dfrac{1}{\sqrt2}x^{-2} + \dfrac{x^5}{3}$

$$g'(x) = \frac{-2}{\sqrt2}x^{-3} + \frac53x^4 = -\sqrt2\,x^{-3}+\frac53x^4$$

since $\dfrac{-2}{\sqrt2}=-\sqrt2$.

#### Example: Differentiate $g(x) = \dfrac{x^{-3}+x^{-2/5}}{x}$

Divide each term of the numerator by $x$ (i.e. multiply by $x^{-1}$) before differentiating:

$$g(x) = x^{-3}\cdot x^{-1} + x^{-2/5}\cdot x^{-1} = x^{-4}+x^{-7/5}$$

$$g'(x) = -4x^{-5} - \frac75x^{-12/5}$$

#### Example: Differentiate $g(x) = x^{-3}+\dfrac1x+\sqrt x$, and evaluate $g'(1)$

Rewriting: $g(x) = x^{-3}+x^{-1}+x^{1/2}$.

$$g'(x) = -3x^{-4}-x^{-2}+\frac12x^{-1/2}$$

$$g'(1) = -3(1)^{-4}-(1)^{-2}+\frac12(1)^{-1/2} = -3-1+\frac12 = -\frac72$$

## The Chain Rule

### Why it works

The chain rule applies whenever one function is "nested inside" another — for example $y=(5x-4)^3$ is really "cube the result of $5x-4$". If $y$ depends on an intermediate variable $u$, and $u$ in turn depends on $x$, then a small change in $x$ produces a change in $u$ scaled by $\dfrac{du}{dx}$, and that change in $u$ produces a change in $y$ scaled by $\dfrac{dy}{du}$. The two scaling factors multiply:

$$\boxed{\dfrac{dy}{dx} = \dfrac{dy}{du} \times \dfrac{du}{dx}}$$

### Method

1. Choose the "inner" function and call it $u$.
2. Rewrite $y$ as a simple function of $u$.
3. Differentiate to find $\dfrac{du}{dx}$ and $\dfrac{dy}{du}$ separately.
4. Multiply them together, then substitute $u$ back in terms of $x$.

#### Example: Differentiate $f(x) = (x^2-2x)^3$

Let $g(x) = x^2-2x$, so $f(x) = [g(x)]^3$ and $g'(x) = 2x-2$. By the chain rule, $f'(x) = 3[g(x)]^2 \times g'(x)$:

$$f'(x) = 3(x^2-2x)^2(2x-2)$$

Factorising $x^2-2x = x(x-2)$ and $2x-2=2(x-1)$:

$$f'(x) = 3 \cdot x^2(x-2)^2 \cdot 2(x-1) = 6x^2(x-1)(x-2)^2$$

#### Exercise 7D(a): Differentiate $y = (5x-4)^3$

Let $u = 5x-4$, so $y = u^3$.

$$\frac{du}{dx} = 5$$

$$\frac{dy}{du} = 3u^2$$

$$\frac{dy}{dx} = \frac{dy}{du}\times\frac{du}{dx} = 3u^2 \times 5 = 15u^2 = 15(5x-4)^2$$

Expanding if required: $15(25x^2-40x+16) = 375x^2 - 600x + 240$.

> [!warning] Correction
> The original working wrote $\dfrac{dy}{du} = 3u$ (missing the square), carrying through to a final answer of $y' = 75x-60$ — should be $\dfrac{dy}{du} = 3u^2$ (the power rule on $u^3$ reduces the power by 1 and multiplies by the original power, i.e. $3u^{3-1}=3u^2$, not $3u^1$), giving the correct result $y' = 15(5x-4)^2 = 375x^2-600x+240$.

#### Worked Example 16: Differentiate $f(x) = \dfrac{1}{\sqrt{2x^2-3x}}$

Rewrite as a power first: $f(x) = (2x^2-3x)^{-1/2}$. Let $u = 2x^2-3x$, so $y = u^{-1/2}$.

$$\frac{du}{dx} = 4x-3$$

$$\frac{dy}{du} = -\frac{1}{2}u^{-3/2}$$

$$\frac{dy}{dx} = \frac{dy}{du}\times\frac{du}{dx} = -\frac{1}{2}u^{-3/2}\times(4x-3) = -\frac{1}{2}(2x^2-3x)^{-3/2}(4x-3)$$

$$f'(x) = -\frac{4x-3}{2(2x^2-3x)^{3/2}}$$

#### Practice (Sheet 2) Q5: Differentiate $f(x) = \sqrt{3x^2+1}$

Rewrite as $f(x) = (3x^2+1)^{1/2}$. Let $u=3x^2+1$, so $y=u^{1/2}$.

$$\frac{du}{dx} = 6x \qquad \frac{dy}{du} = \frac{1}{2}u^{-1/2}$$

$$f'(x) = 6x \times \frac{1}{2}(3x^2+1)^{-1/2} = 3x(3x^2+1)^{-1/2} = \frac{3x}{\sqrt{3x^2+1}}$$

### Further Chain Rule Practice

More practice applying the same substitution method to compositions involving negative and fractional powers.

#### Example: Differentiate $y=(x+3)^2$ (the simplest case)

Let $u=x+3$, so $y=u^2$.

$$\frac{du}{dx}=1 \qquad \frac{dy}{du}=2u$$

$$\frac{dy}{dx} = 2u\times1 = 2(x+3)$$

#### Example: Differentiate $y=(3-x)^4$

Let $u=3-x$, so $y=u^4$.

$$\frac{du}{dx}=-1 \qquad \frac{dy}{du}=4u^3$$

$$\frac{dy}{dx} = 4u^3\times(-1) = -4(3-x)^3$$

#### Example: Differentiate $y=\left(\dfrac12-2x\right)^{-3}$

Let $u=\frac12-2x$, so $y=u^{-3}$.

$$\frac{du}{dx}=-2 \qquad \frac{dy}{du}=-3u^{-4}$$

$$\frac{dy}{dx} = -3u^{-4}\times(-2) = 6u^{-4} = 6\left(\frac12-2x\right)^{-4}$$

#### Example: Differentiate $y=(-3x+1)^{-1/2}$

Let $u=-3x+1$, so $y=u^{-1/2}$.

$$\frac{du}{dx}=-3 \qquad \frac{dy}{du}=-\frac12u^{-3/2}$$

$$\frac{dy}{dx} = -\frac12u^{-3/2}\times(-3) = \frac32u^{-3/2} = \frac32(-3x+1)^{-3/2}$$

#### Example: Differentiate $y=(\sqrt x-2x)^3$

Let $u=\sqrt x-2x=x^{1/2}-2x$, so $y=u^3$.

$$\frac{du}{dx}=\frac12x^{-1/2}-2 \qquad \frac{dy}{du}=3u^2$$

$$\frac{dy}{dx} = 3u^2\times\left(\frac12x^{-1/2}-2\right) = 3(x^{1/2}-2x)^2\left(\frac12x^{-1/2}-2\right)$$

#### Example: Differentiate $y=\dfrac{-2}{\sqrt[3]{(x^2-3x)^2}}$

Rewrite the root as a power first: $y = -2(x^2-3x)^{-2/3}$. Let $u=x^2-3x$, so $y=-2u^{-2/3}$.

$$\frac{du}{dx}=2x-3 \qquad \frac{dy}{du}=\frac43u^{-5/3}$$

$$\frac{dy}{dx} = \frac43u^{-5/3}\times(2x-3) = \frac43(x^2-3x)^{-5/3}(2x-3)$$

#### Example: Differentiate $f(x)=\sqrt{x^4+9}$

Rewrite as $f(x)=(x^4+9)^{1/2}$. Let $u=x^4+9$, so $y=u^{1/2}$.

$$\frac{du}{dx}=4x^3 \qquad \frac{dy}{du}=\frac12u^{-1/2}$$

$$f'(x) = 4x^3\times\frac12(x^4+9)^{-1/2} = \frac{4x^3}{2\sqrt{x^4+9}} = \frac{2x^3}{\sqrt{x^4+9}}$$

#### Example: Differentiate $f(x) = 2(x-3)^{-1}+5$

Let $u=x-3$, so $y=2u^{-1}+5$ (the constant $+5$ differentiates to $0$).

$$\frac{du}{dx}=1 \qquad \frac{dy}{du}=-2u^{-2}$$

$$f'(x) = -2u^{-2}\times1 = -2(x-3)^{-2}$$

## Derivatives of Exponential Functions

### Why $\dfrac{d}{dx}(e^x) = e^x$

Using the limit definition of the derivative (see [[Limits]]):

$$f(x) = e^x \;\Rightarrow\; f'(x) = \lim_{h\to 0}\frac{e^{x+h}-e^x}{h} = e^x\lim_{h\to 0}\frac{e^h-1}{h}$$

The constant $e$ is defined precisely so that $\lim_{h\to 0}\dfrac{e^h-1}{h} = 1$ — it is "the base whose exponential graph has gradient exactly $1$ at $x=0$." Substituting this in:

$$f'(x) = e^x \times 1 = e^x$$

This is the defining property of $e^x$: it is its own derivative.

### Scaled and composite versions

> [!note] Shortcuts
> If $f(x) = e^{kx}$ ($k$ a constant), then $f'(x) = ke^{kx}$.
> If $f(x) = e^{g(x)}$, then $f'(x) = g'(x)e^{g(x)}$.

Both follow immediately from the chain rule with $u$ equal to the exponent.

#### Worked Example 18: Differentiate $y = e^{-5x}$

Let $u=-5x$, so $y=e^u$.

$$\frac{du}{dx} = -5 \qquad \frac{dy}{du} = e^u$$

$$\frac{dy}{dx} = e^u \times(-5) = -5e^{-5x}$$

(This matches the shortcut directly: $k=-5 \Rightarrow f'(x) = -5e^{-5x}$.)

#### Worked Example 21: Differentiate $y = e^{x^3-x}$

Let $u = x^3-x$, so $y=e^u$.

$$\frac{du}{dx} = 3x^2-1 \qquad \frac{dy}{du} = e^u$$

$$\frac{dy}{dx} = e^u\times(3x^2-1) = e^{x^3-x}(3x^2-1)$$

#### Exercise 7E, Q20(f): Differentiate $f(x) = \dfrac{4e^{7x}-2e^{-x}}{e^{-2x}}$

*(Only this sub-part of the exercise appears in the source.)*

The original working differentiated the numerator and denominator separately and divided:

$$f'(x) \overset{?}{=} \frac{28e^{7x}+2e^{-x}}{-2e^{-2x}}$$

> [!warning] Correction
> This is **not a valid differentiation rule** — there is no rule that lets you differentiate the top and bottom of a fraction separately and divide the results (that is confusing it with l'Hôpital's rule for *limits*, which does not apply here since this is not a limit of an indeterminate form). The correct approach is below; a quick check at $x=0$ confirms the original answer is wrong: it gives $\frac{28+2}{-2}=-15$, but the correct derivative (below) gives $36-2=34$ at $x=0$.

**Correct method 1 — simplify first using index laws.** Divide each term of the numerator by $e^{-2x}$:

$$f(x) = \frac{4e^{7x}}{e^{-2x}} - \frac{2e^{-x}}{e^{-2x}} = 4e^{7x-(-2x)} - 2e^{-x-(-2x)} = 4e^{9x}-2e^{x}$$

$$f'(x) = 36e^{9x} - 2e^{x}$$

**Correct method 2 — the quotient rule** (introduced properly later in this note, used here to confirm the answer). With $u = 4e^{7x}-2e^{-x}$ and $v=e^{-2x}$: $u' = 28e^{7x}+2e^{-x}$, $v'=-2e^{-2x}$.

$$f'(x) = \frac{vu'-uv'}{v^2} = \frac{e^{-2x}(28e^{7x}+2e^{-x}) - (4e^{7x}-2e^{-x})(-2e^{-2x})}{e^{-4x}}$$

$$= \frac{e^{-2x}\big[(28e^{7x}+2e^{-x}) + 2(4e^{7x}-2e^{-x})\big]}{e^{-4x}} = \frac{36e^{7x}-2e^{-x}}{e^{-2x}} = 36e^{9x}-2e^{x}$$

Both methods agree: $f'(x) = 36e^{9x}-2e^{x}$.

#### Practice (Sheet 1) Q5: Differentiate $f(x) = e^{\sin x}$

Let $u = \sin x$, so $y = e^u$.

$$\frac{du}{dx} = \cos x \qquad \frac{dy}{du}=e^u$$

$$f'(x) = \cos x \times e^{\sin x}$$

*(The source practises this exact result twice — once on its own, and again inside the "chain rule only" practice sheet — confirming the same answer both times.)*

## Derivatives of Logarithmic Functions

### Why $\dfrac{d}{dx}(\log_e x) = \dfrac{1}{x}$

The natural logarithm $\log_e x$ (also written $\ln x$) is the **inverse function** of $e^x$: if $f(x) = e^x$, then $f^{-1}(x) = \log_e x$. Writing $y = \log_e x$ means $x = e^y$. Differentiating both sides with respect to $x$ (using the chain rule on the right, since $y$ is itself a function of $x$):

$$1 = e^y \cdot \frac{dy}{dx} \;\Rightarrow\; \frac{dy}{dx} = \frac{1}{e^y} = \frac{1}{x}$$

### Scaled and composite versions

> [!note] Shortcuts
> If $f(x) = \log_e(kx)$ ($k$ a constant), then $f'(x) = \dfrac{1}{x}$ — the derivative does **not** depend on $k$. This makes sense from log laws: $\log_e(kx) = \log_e k + \log_e x$, and $\log_e k$ is just a constant (derivative $0$), leaving only $\dfrac{d}{dx}[\log_e x] = \dfrac1x$.
> If $f(x) = \log_e[g(x)]$, then $f'(x) = \dfrac{g'(x)}{g(x)}$ (valid wherever $g(x)>0$).

#### Worked Example 22: Differentiate $y = \log_e(7x)$

Let $u=7x$, so $y=\log_e u$.

$$\frac{du}{dx}=7 \qquad \frac{dy}{du}=\frac1u$$

$$\frac{dy}{dx} = \frac{1}{u}\times 7 = \frac{7}{7x} = \frac1x$$

#### Worked Example 23: Differentiate $y = 2\log_e(3x-4)$

Let $u = 3x-4$, so $y = 2\log_e u$.

$$\frac{du}{dx}=3 \qquad \frac{dy}{du}=\frac{2}{u}$$

$$\frac{dy}{dx} = \frac2u \times 3 = \frac{6}{3x-4}$$

#### Worked Example 24: Differentiate $y = \log_e(x^2+4x-1)$

Let $u = x^2+4x-1$, so $y=\log_e u$.

$$\frac{du}{dx}=2x+4 \qquad \frac{dy}{du}=\frac1u$$

$$\frac{dy}{dx} = \frac1u(2x+4) = \frac{2x+4}{x^2+4x-1}$$

#### Practice (Sheet 1) Q6: Differentiate $f(x) = \log_e(x^3)$, and evaluate $f'(5)$

Let $u=x^3$, so $y=\log_e u$.

$$\frac{du}{dx}=3x^2 \qquad \frac{dy}{du}=\frac1u$$

$$f'(x) = \frac{3x^2}{x^3} = \frac3x$$

(Neatly, $\log_e(x^3) = 3\log_e x$ by log laws, so $f'(x) = 3\times\dfrac1x = \dfrac3x$ directly — a good check on the chain-rule result.)

$$f'(5) = \frac{3}{5} = 0.6$$

#### Practice (Sheet 2) Q3: Differentiate $f(x) = \ln(x^2-5)$

Let $u = x^2-5$, so $y=\log_e u$.

$$\frac{du}{dx}=2x \qquad \frac{dy}{du}=\frac1u = \frac{1}{x^2-5}$$

$$f'(x) = \frac{2x}{x^2-5}$$

## Derivatives of Trigonometric Functions

### Why the signs work: reading them off the graph of $\sin x$

Consider $f(x) = \sin x$ on the domain $D=[0,2\pi]$. It has a maximum at $\left(\frac{\pi}{2},1\right)$ and a minimum at $\left(\frac{3\pi}{2},-1\right)$, rising from $(0,0)$ to the maximum, falling all the way to the minimum, then rising again to $(2\pi,0)$.

| Interval | Shape of $\sin x$ | Sign of $f'(x)$ |
|---|---|---|
| $0 \le x < \frac{\pi}{2}$ | increasing | $f'(x) > 0$ |
| $x = \frac{\pi}{2}$ | turning point (max) | $f'(x) = 0$ |
| $\frac{\pi}{2} < x < \frac{3\pi}{2}$ | decreasing | $f'(x) < 0$ |
| $x = \frac{3\pi}{2}$ | turning point (min) | $f'(x) = 0$ |
| $\frac{3\pi}{2} < x \le 2\pi$ | increasing | $f'(x) > 0$ |

This is exactly the behaviour of $\cos x$ over the same domain — positive on $\left(0,\frac\pi2\right)$ and $\left(\frac{3\pi}2,2\pi\right)$, negative on $\left(\frac\pi2,\frac{3\pi}2\right)$, zero at $\frac\pi2$ and $\frac{3\pi}2$ — which is the geometric reason $\cos x$ is the derivative of $\sin x$ (this same sign-matching idea — reading the nature of stationary points off the sign of the derivative — is used throughout [[Applications of Differentiation]]).

### Standard rules

$$f(x)=\sin x \;\Rightarrow\; f'(x)=\cos x \qquad f(x)=\cos x \;\Rightarrow\; f'(x)=-\sin x \qquad f(x)=\tan x \;\Rightarrow\; f'(x)=\frac{1}{\cos^2 x}$$

> [!note] Shortcuts (scaled argument, $a$ a constant)
> $f(x)=\sin(ax) \Rightarrow f'(x) = a\cos(ax)$
> $f(x)=\cos(ax) \Rightarrow f'(x) = -a\sin(ax)$
> $f(x)=\tan(ax) \Rightarrow f'(x) = \dfrac{a}{\cos^2(ax)}$

> [!note] Shortcuts (general composite function $g(x)$)
> $f(x)=\sin[g(x)] \Rightarrow f'(x) = g'(x)\cos[g(x)]$
> $f(x)=\cos[g(x)] \Rightarrow f'(x) = -g'(x)\sin[g(x)]$
> $f(x)=\tan[g(x)] \Rightarrow f'(x) = \dfrac{g'(x)}{\cos^2[g(x)]}$

All six of the boxed results are just the chain rule applied with $u = ax$ or $u=g(x)$.

#### Worked Example 26: Differentiate $y = \sin(5x)$

Let $u=5x$, so $y=\sin u$.

$$\frac{du}{dx}=5 \qquad \frac{dy}{du}=\cos u$$

$$\frac{dy}{dx} = \cos u \times 5 = 5\cos(5x)$$

#### Worked Example 28: Differentiate $y = \cos(x^2+2x-3)$

Let $u = x^2+2x-3$, so $y=\cos u$.

$$\frac{du}{dx}=2x+2 \qquad \frac{dy}{du}=-\sin u$$

$$\frac{dy}{dx} = -\sin u \times(2x+2) = -(2x+2)\sin(x^2+2x-3)$$

#### Practice (Sheet 2) Q1: Differentiate $f(x) = \sin(x^2+3x)$

Let $u=x^2+3x$, so $y=\sin u$.

$$\frac{du}{dx}=2x+3 \qquad \frac{dy}{du}=\cos u$$

$$f'(x) = (2x+3)\cos(x^2+3x)$$

#### Practice (Sheet 2) Q4: Differentiate $f(x) = \cos(e^{2x})$

Let $u=e^{2x}$, so $y=\cos u$.

$$\frac{du}{dx}=2e^{2x} \qquad \frac{dy}{du}=-\sin u$$

$$f'(x) = -2e^{2x}\sin(e^{2x})$$

(See [[Trigonometric Functions]] for the standard trig identities these rules build on.)

## The Product Rule

### Why it works

If $y = u(x)v(x)$, a small change $h$ in $x$ changes $u$ by roughly $u'(x)h$ and $v$ by roughly $v'(x)h$. The resulting change in the product is approximately

$$\big(u+u'h\big)\big(v+v'h\big) - uv = u v'h + v u'h + u'v'h^2$$

Dividing by $h$ and letting $h\to 0$, the $u'v'h^2$ term vanishes (it is second-order small), leaving $uv' + vu'$ — exactly the product rule.

$$y = uv \;\Rightarrow\; \frac{dy}{dx} = u\frac{dv}{dx} + v\frac{du}{dx}$$

or equivalently, for $f(x) = u(x)v(x)$:

$$f'(x) = u(x)v'(x) + v(x)u'(x)$$

#### Practice (Sheet 1) Q3: Differentiate $y = 3x\sin x$

Here $u = 3x$ and $v = \sin x$, so $u' = 3$ and $v' = \cos x$.

$$y' = u v' + v u' = 3x\cos x + 3\sin x = 3(\sin x + x\cos x)$$

## The Quotient Rule

### Why it works

The quotient rule is not a separate idea — it follows from the product rule and the chain rule. Writing $h(x) = \dfrac{f(x)}{g(x)} = f(x)\cdot[g(x)]^{-1}$ and applying the product rule:

$$h'(x) = f'(x)[g(x)]^{-1} + f(x)\cdot\frac{d}{dx}\Big[(g(x))^{-1}\Big]$$

By the chain rule (power rule with $n=-1$ on the inner function $g(x)$), $\dfrac{d}{dx}\big[(g(x))^{-1}\big] = -[g(x)]^{-2}g'(x)$, so

$$h'(x) = \frac{f'(x)}{g(x)} - \frac{f(x)g'(x)}{[g(x)]^2} = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}$$

$$\boxed{\left(\frac{f(x)}{g(x)}\right)' = \frac{g(x)f'(x) - g'(x)f(x)}{[g(x)]^2}}$$

In practice, if the denominator is a **single power of $x$** (as below), it is usually quicker to split the fraction and use the power rule term-by-term rather than apply the full quotient rule — both give the same answer.

#### Practice (Sheet 1) Q4: Differentiate $f(x) = \dfrac{x^2+2}{x}$, and evaluate $f'(3)$

**Method — split the fraction:**

$$f(x) = \frac{x^2+2}{x} = (x^2+2)\cdot x^{-1} = x + 2x^{-1}$$

$$f'(x) = 1 - 2x^{-2} = 1-\frac{2}{x^2}$$

$$f'(3) = 1 - \frac29 = \frac79 \approx 0.78$$

This agrees with applying the full quotient rule directly (with $f(x)=x^2+2$, $g(x)=x$, $f'(x)=2x$, $g'(x)=1$):

$$\left(\frac{x^2+2}{x}\right)' = \frac{x(2x) - (x^2+2)(1)}{x^2} = \frac{2x^2-x^2-2}{x^2} = \frac{x^2-2}{x^2} = 1-\frac{2}{x^2} \checkmark$$

(See the worked Exercise 7E, Q20(f) above for a second, fully-worked quotient rule example, including a common mistake to avoid.)

#### Example: Differentiate $h(x) = \dfrac{\cos x}{e^x}$

With $f(x)=\cos x$ and $g(x)=e^x$: $f'(x)=-\sin x$, $g'(x)=e^x$.

$$h'(x) = \frac{f'(x)g(x)-f(x)g'(x)}{[g(x)]^2} = \frac{(-\sin x)(e^x) - (\cos x)(e^x)}{e^{2x}} = \frac{-e^x(\sin x+\cos x)}{e^{2x}}$$

The original working then cancelled a factor of $e^x$ top and bottom and reached a final answer of $\dfrac{\sin x+\cos x}{e^x}$.

> [!warning] Correction
> The negative sign was dropped in that last cancellation step. $\dfrac{-e^x(\sin x+\cos x)}{e^{2x}} = \dfrac{-(\sin x+\cos x)}{e^x}$ — the final answer should stay negative: $h'(x) = -\dfrac{\sin x+\cos x}{e^x}$. This also follows from the product rule, writing $h(x)=\cos x\cdot e^{-x}$: $h'(x) = -\sin x\cdot e^{-x} + \cos x\cdot(-e^{-x}) = -e^{-x}(\sin x+\cos x)$, confirming the corrected result.

## More Mixed Chain Rule Examples

These combine logarithms, exponentials and trig functions inside one another — good practice for recognising *which* function is "outer" and which is "inner."

#### Q10(j): Differentiate $f(x) = \sin\big[\log_e(2x-1)\big]$

Let $u = \log_e(2x-1)$, so $y = \sin u$.

$$\frac{du}{dx} = \frac{2}{2x-1} \qquad \frac{dy}{du}=\cos u$$

$$\frac{dy}{dx} = \cos u \times \frac{2}{2x-1} = \frac{2\cos\big[\log_e(2x-1)\big]}{2x-1}$$

#### Q10(k): Differentiate $y = \cos(2e^{3x})$

Let $u = 2e^{3x}$, so $y=\cos u$.

$$\frac{du}{dx} = 2\times 3e^{3x} = 6e^{3x} \qquad \frac{dy}{du}=-\sin u$$

$$y' = -6e^{3x}\sin(2e^{3x})$$

#### Q10(l): Differentiate $y = 3\cos(\log_e 10x)$

Let $u = \log_e(10x)$, so $y = 3\cos u$.

$$\frac{du}{dx} = \frac{10}{10x} = \frac1x \qquad \frac{dy}{du}=-3\sin u$$

$$y' = -3\sin(\log_e 10x)\times\frac1x = \frac{-3\sin(\log_e 10x)}{x}$$

## Second Derivatives

Differentiating $f'(x)$ a second time gives the **second derivative**, written $f''(x)$ or $\dfrac{d^2y}{dx^2}$. It measures the rate of change *of the gradient* — equivalently, the concavity of the graph. For example, if $y=x^3$:

$$y' = 3x^2 \qquad\Rightarrow\qquad y'' = 6x$$

Second derivatives are the basis of the **second derivative test** for classifying stationary points, used in [[Applications of Differentiation]].

## Differentiability

A function is **differentiable** at a point if its derivative exists there — graphically, if the curve has a single well-defined (non-vertical) tangent line at that point. Differentiation can fail at a point where a graph has:

- a **sharp corner or cusp** (e.g. $f(x)=\lvert x\rvert$ at $x=0$, where the gradient jumps from $-1$ to $1$),
- a **discontinuity** (a break or jump in the graph), or
- a **vertical tangent**.

Every function differentiated in this note is a polynomial, exponential, logarithmic or trigonometric function (or a combination of these), all of which are differentiable everywhere on their natural domain — except that $\log_e(kx)$ and $\log_e[g(x)]$ are only differentiable where $kx>0$ or $g(x)>0$ respectively, since the logarithm itself is undefined otherwise.

## Summary

This note has covered: the power, sum/difference, chain, product and quotient rules, and the standard derivatives of exponential, logarithmic and trigonometric functions (plain, scaled, and composed with another function $g(x)$). For the limit definition these rules are built on, see [[Limits]]; for where differentiation is heading next, see [[Applications of Differentiation]]; for further mixed practice, see [[Introductory Calculus - Practice and Revision]].
