# Applications of Differentiation

Once a derivative can be found (see [[Differentiation Rules]]), it can be put to work answering genuinely useful questions about a function: how fast is it changing right now, rather than on average? Where is it at its largest or smallest? What does its graph actually look like? This note works through the "rates of change" theory and both full optimisation problems from the source material, in full.

## Key Formulas

| Concept | Formula |
|---|---|
| Volume of a rectangular prism | $V = \text{width}\times\text{height}\times\text{length}$ |
| Total surface area | $A = $ sum of the areas of all faces |
| Average rate of change of $f$ over $[a,b]$ | $\dfrac{f(b)-f(a)}{b-a}$ |
| Instantaneous rate of change at $x=a$ | $f'(a)$ |
| Equation of the tangent at $(a, f(a))$ | $y - f(a) = f'(a)(x-a)$ |
| Stationary point condition | $f'(x) = 0$ |
| First derivative test | $f'(x)$ changes $+\to 0\to -$: local **maximum**. Changes $-\to 0\to +$: local **minimum**. No sign change: **not** a turning point (e.g. a stationary point of inflection). |
| Second derivative test | $f''(a) < 0$: local **maximum**. $f''(a) > 0$: local **minimum**. $f''(a)=0$: test is inconclusive — use the first derivative test instead. |

## Average Rate of Change vs Instantaneous Rate of Change

The **average rate of change** of $y=f(x)$ over an interval $x\in[a,b]$ is the gradient of the straight line (the **secant**) joining the two points $(a,f(a))$ and $(b,f(b))$ on the curve:

$$\text{average rate of change} = \frac{f(b)-f(a)}{b-a}$$

The **instantaneous rate of change** at a single point $x=a$ is found by drawing the **tangent** to the curve at $(a,f(a))$ and finding its gradient — which is exactly $f'(a)$, the derivative evaluated at $a$. This is the key link between "differentiation" as an algebraic technique ([[Differentiation Rules]]) and "gradient of a curve at a point" as a geometric idea, and it is built on the same limiting process used to define the derivative in [[Limits]] (the secant gradient *is* the difference quotient $\frac{f(b)-f(a)}{b-a}$; letting $b\to a$ turns the secant into the tangent).

#### Worked Example: $f(x) = (x-2)(x+2)$

Expanding, $f(x) = x^2-4$, an upward parabola with turning point (minimum) at $(0,-4)$ and $x$-intercepts at $(-2,0)$ and $(2,0)$. The two points used in this example, $(-1,f(-1))$ and $(3,f(3))$, are marked on the curve:

$$f(-1) = (-1)^2-4 = -3 \qquad\qquad f(3) = 3^2-4=5$$

giving the points $(-1,-3)$ and $(3,5)$.

**Average rate of change over $[-1,3]$** — the gradient of the secant line joining these two points:

$$\text{average rate of change} = \frac{f(3)-f(-1)}{3-(-1)} = \frac{5-(-3)}{4} = \frac{8}{4} = 2$$

**Instantaneous rate of change at $x=3$** — differentiate first: $f'(x) = 2x$ (power rule). Then the gradient of the tangent at $(3,5)$ is

$$f'(3) = 2(3) = 6$$

Notice the tangent (gradient $6$) is steeper than the secant (gradient $2$) at this point — reasonable, since the curve is getting steeper as $x$ increases past $0$, so the instantaneous gradient right at $x=3$ is larger than the average gradient over the whole interval leading up to it.

**Graph described:** an upward parabola $y=x^2-4$ with vertex $(0,-4)$, crossing the $x$-axis at $(-2,0)$ and $(2,0)$. The point $(-1,-3)$ lies on the left (falling) branch and $(3,5)$ lies on the right (rising) branch. A straight secant line joins $(-1,-3)$ to $(3,5)$ (gradient $2$). A separate, steeper straight line is drawn touching the curve only at $(3,5)$ — the tangent there (gradient $6$).

### Extension: the equation of the tangent line

The source stops at finding the gradient of the tangent, but once you have a point and a gradient, the tangent line's equation follows immediately from $y-y_1=m(x-x_1)$. Using the point $(3,5)$ and gradient $f'(3)=6$ found above:

$$y - 5 = 6(x-3) \;\Rightarrow\; y = 6x - 18 + 5 \;\Rightarrow\; y = 6x-13$$

## Stationary Points and the Sign of the Derivative

A **stationary point** of $f$ occurs where $f'(x) = 0$ — the tangent there is horizontal. To work out whether a stationary point is a local maximum, local minimum, or neither, check the sign of $f'(x)$ just before and just after it (the **first derivative test**):

| Sign pattern of $f'(x)$ | Shape of the graph | Nature of the stationary point |
|---|---|---|
| $+ \to 0 \to -$ | increasing, flat, decreasing | local **maximum** |
| $- \to 0 \to +$ | decreasing, flat, increasing | local **minimum** |

Both worked examples below use exactly this method, with a small table of values of $x$ either side of the critical value. As noted in [[Differentiation Rules]], the **second derivative test** is a quicker alternative when $f''(x)$ is easy to find: a negative second derivative at the stationary point means the gradient is decreasing through zero (curve turning downward, concave down) — a local maximum; a positive second derivative means a local minimum. Both worked examples below are checked against this alternative test too, and the two methods agree.

## Worked Example: Closed Box with Fixed Surface Area

**Reconstructed question** *(the source pages show only the working — question text reconstructed from it; check the original if this seems off)*:

> A closed rectangular box has a base measuring $x$ cm by $2x$ cm, and height $h$ cm. The total surface area of the box is $300\text{ cm}^2$.
> a) Show that $h = \dfrac{150-2x^2}{3x}$.
> b) Show that the volume of the box is $V = 100x - \dfrac{4}{3}x^3 \text{ cm}^3$.
> c) Find the values of $x$ for which $V=0$.
> d) Find the volume of the box when $x=6$.
> e) State the domain of $V$ as a function of $x$.
> f) Sketch the graph of $V$ against $x$, showing all intercepts and the turning point.
> g) Find the value of $x$ that produces the maximum volume, and find that maximum volume.
> h) Find the average rate of change of $V$ as $x$ increases from $0.5$ to $2$.
> i) Find the instantaneous rate of change of $V$ when $x=1$.
> j) Use a table of values of $V'(x)$ to confirm the nature of the stationary point found in part (g).
> k) If a manufacturing constraint means $x$ cannot exceed $4.5$ cm, find the maximum possible volume of the box under this restriction.

### a) Setting up $h$ in terms of $x$

With a base $x$ by $2x$ and height $h$, the three pairs of faces have areas $x\cdot 2x = 2x^2$ (top/bottom), $2x\cdot h = 2xh$ (front/back) and $x\cdot h = xh$ (sides). Total surface area (both faces of each pair):

$$A = 2(2xh + xh + 2x^2) = 2x(3h+2x) = 300$$

$$\Rightarrow 3h+2x = \frac{150}{x} \;\Rightarrow\; 3h = \frac{150}{x}-2x = \frac{150-2x^2}{x}$$

$$\Rightarrow h = \frac{150-2x^2}{3x}$$

### b) Volume in terms of $x$

The base area is $x\times 2x = 2x^2$, so:

$$V = 2x^2 \times h = 2x^2\times\frac{150-2x^2}{3x} = \frac{300x^2-4x^4}{3x}$$

Dividing every term by $x$:

$$V = \frac{300x-4x^3}{3} = 100x - \frac{4}{3}x^3$$

### c) Finding where $V=0$

$$100x-\frac43x^3 = 0 \;\Rightarrow\; x\left(100-\frac43x^2\right)=0$$

$$\Rightarrow x=0 \quad\text{or}\quad 100-\frac43x^2=0$$

$$\frac43x^2 = 100 \;\Rightarrow\; x^2 = 100\times\frac34 = 75 \;\Rightarrow\; x=\pm\sqrt{75}=\pm5\sqrt3$$

Since $x$ is a length, $x>0$, so $x=-5\sqrt3$ is rejected.

$$\Rightarrow x=0 \text{ and } x=5\sqrt3$$

### d) Volume when $x=6$

$$V(6) = 100(6)-\frac43(6)^3 = 600-\frac43(216) = 600-288=312\text{ cm}^3$$

### e) Domain of $V$

Physically, the height must be positive: $h>0 \;\Rightarrow\; \dfrac{150-2x^2}{3x}>0$. For $x>0$ (a length), this requires $150-2x^2>0$, i.e. $x^2<75$, i.e. $0<x<5\sqrt3$ (the alternative case, $3x<0$ with $150-2x^2<0$, needs $x<0$ *and* $x>5\sqrt3$ simultaneously, which is impossible). So:

$$D = [0,\,5\sqrt3]$$

(Strictly, $x=0$ and $x=5\sqrt3$ both give a degenerate box of zero volume, so a genuine box needs $0<x<5\sqrt3$; the closed interval above is simply the relevant domain for sketching and analysing the volume function.)

### f) Sketching $V$

| Feature | Value |
|---|---|
| $y$-intercept | $(0,0)$ |
| $x$-intercepts | $(0,0)$ and $(5\sqrt3,0)\approx(8.66,0)$ |
| Turning point (local max) | $(5,\ 333.3)$ |

The graph rises smoothly from the origin, curving upward then over (concave down throughout this stretch) to a single rounded peak at $(5,333.3)$, then falls away symmetrically-ish back down to touch the $x$-axis at $(5\sqrt3,0)$ — a single "hump" shape over $[0,5\sqrt3]$, consistent with the restricted domain found in (e).

### g) Maximum volume

$$V'(x) = 100-4x^2$$

Setting $V'(x)=0$: $100-4x^2=0 \;\Rightarrow\; 4x^2=100 \;\Rightarrow\; x=5$ (taking the positive root, consistent with the domain).

$$V(5) = 100(5)-\frac43(5)^3 = 500-\frac{500}{3} = \frac{1000}{3}\text{ cm}^3$$

$$\Rightarrow V_{\max} = \frac{1000}{3}\text{ cm}^3 \approx 333.3\text{ cm}^3 \text{ when } x=5$$

(This matches the turning point read off the sketch in part (f).) As a check with the **second derivative test**: $V''(x) = -8x$, so $V''(5) = -40 < 0$, confirming a local maximum.

### h) Average rate of change from $x=0.5$ to $x=2$

$$V(2) = 100(2)-\frac43(2)^3 = 200-\frac{32}{3}=\frac{568}{3}$$

$$V(0.5) = 100(0.5)-\frac43(0.5)^3 = 50-\frac{1}{6} = \frac{299}{6}$$

$$\text{average rate of change} = \frac{V(2)-V(0.5)}{2-0.5} = \dfrac{\dfrac{568}{3}-\dfrac{299}{6}}{1.5} = \frac{139.5}{1.5}=93$$

### i) Instantaneous rate of change at $x=1$

$$V'(1) = 100-4(1)^2 = 96 \text{ cm}^3\text{ per cm}$$

### j) Confirming the maximum with a table of values

| $x$ | $4$ | $5$ | $6$ |
|---|---|---|---|
| $V'(x)$ | $+$ | $0$ | $-$ |
| Shape | increasing ↗ | stationary — | decreasing ↘ |

$V'(x)$ changes from positive to negative through $x=5$, confirming (by the first derivative test) that the maximum volume occurs when $x=5$.

### k) Maximum volume if $x\le 4.5$ cm

Since the unrestricted maximum occurs at $x=5$, which is now outside the allowed range, and $V$ is still **increasing** on $(0,4.5)$ (because $4.5<5$, so $V'(x)>0$ there), the largest volume under this restriction occurs at the boundary $x=4.5$:

$$V(4.5) = 100(4.5)-\frac43(4.5)^3 = 450-121.5=328.5\text{ cm}^3$$

$$\Rightarrow V_{\max}=328.5\text{ cm}^3 \text{ when } x \text{ can be no more than } 4.5\text{ cm}$$

## Worked Example: Square-Based Box from a Fixed Length Budget

**Reconstructed question** *(question text reconstructed from the working — check the original if this seems off)*:

> An open box with a square base of side length $x$ cm and height $L$ cm is to be made so that the sum of its height and the perimeter of its base is $12$ cm.
> a) Show that $L=12-4x$.
> b) Show that the volume of the box is $V = 4x^2(3-x)\text{ cm}^3$.
> c) State the domain of $V$.
> d) Sketch the graph of $V$ against $x$, showing the turning point and all intercepts.
> e) Find the value of $x$ that maximises the volume, and find this maximum volume.
> f) Find the average rate of change of $V$ as $x$ increases from $0.5$ to $2$.
> g) Find the instantaneous rate of change of $V$ when $x=1$.
> h) Use a table of values of $V'(x)$ to confirm the value of $x$ that maximises $V$.

**Diagram described:** a rectangular prism (box) with a square base of side length $x$ and height $L$.

### a) Setting up $L$ in terms of $x$

The square base has perimeter $4x$, and the sum of this perimeter with the height is $12$:

$$L+4x=12 \;\Rightarrow\; L = 12-4x$$

### b) Volume in terms of $x$

$$V = x^2 \times L = x^2(12-4x) = 12x^2-4x^3 = 4x^2(3-x)$$

### c) Domain of $V$

The height must be positive: $L>0 \;\Rightarrow\; 12-4x>0 \;\Rightarrow\; 4x<12 \;\Rightarrow\; 0<x<3$.

### d) Sketching $V$

| Feature | Value |
|---|---|
| $y$-intercept | $(0,0)$ |
| $x$-intercepts | $(0,0)$ and $(3,0)$ |
| Turning point (local max) | $(2,16)$ |

Since $x=0$ is a **repeated** root of $V=4x^2(3-x)$, the graph just **touches** the $x$-axis at the origin (it doesn't cross — $V\ge0$ immediately either side of $x=0$) before rising to a rounded peak at $(2,16)$, then falling to **cross** the $x$-axis at $(3,0)$ (a simple root, so the curve continues down into negative values beyond $x=3$, outside the physical domain found in part (c)).

### e) Maximum volume (product rule)

Using the product rule on $V=4x^2(3-x)$ with $u=4x^2$ ($u'=8x$) and $v=3-x$ ($v'=-1$):

$$V'(x) = u'v+uv' = 8x(3-x) + 4x^2(-1) = 24x-8x^2-4x^2 = 24x-12x^2$$

Setting $V'(x)=0$:

$$-12x^2+24x=0 \;\Rightarrow\; x^2-2x=0 \;\Rightarrow\; x(x-2)=0 \;\Rightarrow\; x=0 \text{ or } x=2$$

Only $x=2$ lies inside the domain $0<x<3$.

$$V(2) = 4(2)^2(3-2) = 4\times4\times1=16\text{ cm}^3$$

$$\Rightarrow V_{\max}=16\text{ cm}^3 \text{ when } x=2$$

As a check with the **second derivative test**: $V''(x) = 24-24x$, so $V''(2)=24-48=-24<0$, confirming a local maximum.

### f) Average rate of change from $x=0.5$ to $x=2$

$$V(0.5) = 4(0.5)^2(3-0.5) = 1\times2.5=2.5 \qquad V(2)=16$$

$$\text{average rate of change} = \frac{16-2.5}{2-0.5} = \frac{13.5}{1.5}=9$$

### g) Instantaneous rate of change at $x=1$

$$V'(1) = -12(1)^2+24(1) = 12\text{ cm}^3\text{ per cm}$$

### h) Confirming the maximum with a table of values

| $x$ | $1$ | $2$ | $3$ |
|---|---|---|---|
| $V'(x)$ | $+$ | $0$ | $-$ |
| Shape | increasing ↗ | stationary — | decreasing ↘ |

$V'(x)$ changes from positive to negative through $x=2$, confirming that $V$ reaches its maximum when $x=2$.

## Summary

Both worked problems above follow the same four-step optimisation pattern: (1) use a geometric constraint to write one variable in terms of the other, (2) substitute into the quantity to be optimised (here, volume) to get a single-variable function, (3) differentiate and solve $V'(x)=0$ for stationary points, restricted to the domain where the model makes physical sense, and (4) use a sign table (or the second derivative test) to confirm whether that stationary point is actually a maximum. This pattern — and the rules used to differentiate $V(x)$ along the way — reappear throughout [[Introductory Calculus - Practice and Revision]]. For the differentiation techniques themselves, see [[Differentiation Rules]]; for the limiting process underlying "instantaneous" rate of change, see [[Limits]].
