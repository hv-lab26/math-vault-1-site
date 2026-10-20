# Introductory Calculus - Practice and Revision

Mixed practice drawn from the Study Area 3 practice sheets, revision sets, revision quiz, and take-home test. Organised by sub-topic; each section links to the relevant concept note. Worked exactly, with every computation re-checked for accuracy.

## Differentiation Rules

See [[Differentiation Rules]].

### Chain rule

**Question.** Let $f(x) = \sqrt{x^4+9}$. Find $f'(x)$.

Write $f(x) = (x^4+9)^{1/2}$. Let $u = x^4+9$, so $y = u^{1/2}$.

$$\frac{du}{dx} = 4x^3, \qquad \frac{dy}{du} = \frac{1}{2}u^{-1/2}$$

By the chain rule,
$$\frac{dy}{dx} = \frac{dy}{du}\times\frac{du}{dx} = \frac{1}{2}(x^4+9)^{-1/2}\times 4x^3 = \frac{4x^3}{2\sqrt{x^4+9}} = \frac{2x^3}{\sqrt{x^4+9}}$$

---

**Question.** Let $f(x) = \dfrac{2}{x-3}+5$. Find $f'(x)$, and hence find the gradient of the curve at $x=4$.

Write $f(x) = 2(x-3)^{-1}+5$. Let $u = x-3$, so $y = 2u^{-1}+5$.

$$\frac{du}{dx}=1, \qquad \frac{dy}{du} = -2u^{-2}$$

$$\frac{dy}{dx} = \frac{dy}{du}\times\frac{du}{dx} = -2u^{-2}\times 1 = -2(x-3)^{-2}$$

So $f'(x) = -\dfrac{2}{(x-3)^2}$. At $x=4$:
$$f'(4) = -\frac{2}{(4-3)^2} = -\frac{2}{1} = -2$$

---

**Question.** For $y = 3\sqrt{x} - \dfrac{81}{x}+13$, find the value of $\dfrac{dy}{dx}$ when $x=9$.

Write $y = 3x^{1/2} - 81x^{-1}+13$.

$$\frac{dy}{dx} = \frac{3}{2}x^{-1/2} + 81x^{-2} = \frac{3}{2\sqrt{x}} + \frac{81}{x^2}$$

At $x=9$:
$$\frac{dy}{dx} = \frac{3}{2\sqrt{9}} + \frac{81}{9^2} = \frac{3}{2(3)} + \frac{81}{81} = \frac{1}{2}+1 = 1.5$$

### Product and quotient rule

**Question.** If $f(x) = \dfrac{x-2}{3-x^2}$, find $f'(x)$.

By the quotient rule with $u = x-2$, $v=3-x^2$ (so $u'=1$, $v'=-2x$):

$$f'(x) = \frac{u'v-uv'}{v^2} = \frac{(1)(3-x^2) - (x-2)(-2x)}{(3-x^2)^2} = \frac{3-x^2+2x(x-2)}{(3-x^2)^2}$$

$$= \frac{3-x^2+2x^2-4x}{(3-x^2)^2} = \frac{x^2-4x+3}{(3-x^2)^2}$$

---

**Question.** Find the derivative of $y = 2x^3\cos(x^2)$ with respect to $x$.

By the product rule, with $u=2x^3$ ($u'=6x^2$) and $v=\cos(x^2)$ ($v' = -2x\sin(x^2)$ by the chain rule):

$$\frac{dy}{dx} = 6x^2\cos(x^2) + 2x^3\times\big(-2x\sin(x^2)\big) = 6x^2\cos(x^2) - 4x^4\sin(x^2)$$

Factoring out $2x^2$:
$$\frac{dy}{dx} = 2x^2\big(3\cos(x^2) - 2x^2\sin(x^2)\big)$$

---

**Question.** Let $f(x) = \dfrac{\cos(x)}{e^x}$. Find $f'(x)$.

Write $f(x) = \cos(x)\,e^{-x}$ and use the product rule, with $u=\cos x$ ($u'=-\sin x$) and $v=e^{-x}$ ($v'=-e^{-x}$):

$$f'(x) = -\sin(x)e^{-x} + \cos(x)\big(-e^{-x}\big) = -e^{-x}\sin(x) - e^{-x}\cos(x)$$

$$= -e^{-x}\big(\sin(x)+\cos(x)\big) = -\frac{\sin(x)+\cos(x)}{e^x}$$

### Combined rules — answer as a single algebraic fraction

**Question.** Find the derivative of $h(x) = x^3\sqrt{1-x}$, expressing your answer as a single algebraic fraction.

Write $h(x) = x^3(1-x)^{1/2}$. By the product rule:

$$h'(x) = 3x^2(1-x)^{1/2} + x^3\times\frac{1}{2}(1-x)^{-1/2}\times(-1) = 3x^2\sqrt{1-x} - \frac{x^3}{2\sqrt{1-x}}$$

Combine over the common denominator $2\sqrt{1-x}$:

$$h'(x) = \frac{6x^2(1-x) - x^3}{2\sqrt{1-x}} = \frac{6x^2-6x^3-x^3}{2\sqrt{1-x}} = \frac{6x^2-7x^3}{2\sqrt{1-x}} = \frac{x^2(6-7x)}{2\sqrt{1-x}}$$

---

**Question.** Let $g(x) = \dfrac{\sin(x^2)}{e^{-x}}$. Find $g'(x)$, expressing your answer as a single algebraic fraction.

Write $g(x) = \sin(x^2)\,e^{x}$ (since $1/e^{-x}=e^x$). By the product rule, with $u=\sin(x^2)$ ($u'=2x\cos(x^2)$ by the chain rule) and $v=e^x$ ($v'=e^x$):

$$g'(x) = 2x\cos(x^2)\times e^x + \sin(x^2)\times e^x = e^x\big(2x\cos(x^2)+\sin(x^2)\big)$$

---

**Question.** For $x\ge 0$, let $m(x) = \sqrt{1+\sqrt{x}}$. Find $m'(x)$, expressing your answer as a single algebraic fraction.

Write $m(x) = (1+x^{1/2})^{1/2}$. Let $u = 1+x^{1/2}$, so $y=u^{1/2}$.

$$\frac{du}{dx} = \frac{1}{2}x^{-1/2}, \qquad \frac{dy}{du} = \frac{1}{2}u^{-1/2}$$

$$m'(x) = \frac{dy}{du}\times\frac{du}{dx} = \frac{1}{2}(1+\sqrt{x})^{-1/2}\times\frac{1}{2}x^{-1/2} = \frac{1}{4}x^{-1/2}(1+\sqrt{x})^{-1/2}$$

$$= \frac{1}{4\sqrt{x}}\times\frac{1}{\sqrt{1+\sqrt{x}}} = \frac{1}{4\sqrt{x}\,\sqrt{1+\sqrt{x}}}$$

## Applications of Differentiation

See [[Applications of Differentiation]].

### Recap: classifying a stationary point

A stationary point occurs where $y'=0$. Reading the sign of $y'$ just either side of it (a *sign test*) classifies it:

| Case | $y'$ before | $y'=0$ | $y'$ after | Nature |
|---|---|---|---|---|
| 1 | $+$ | 0 | $-$ | Local **maximum** |
| 2 | $-$ | 0 | $+$ | Local **minimum** |
| 3 | $+$ | 0 | $+$ | Positive (rising) point of **inflection** |
| 4 | $-$ | 0 | $-$ | Negative (falling) point of **inflection** |

### Classifying stationary points — worked questions

**Question.** Let $f(x) = 3x^4-8x^3+6x^2+5$.
**(a)** Find the stationary point(s) of $f$.
**(b)** Use a sign test to determine the nature of each.

**(a)** $f'(x) = 12x^3-24x^2+12x$. Set $f'(x)=0$:

$$12x(x^2-2x+1) = 0 \iff 12x(x-1)^2=0$$

So $12x=0 \Rightarrow x=0$, or $(x-1)^2=0\Rightarrow x=1$ (a repeated root).

- At $x=0$: $f(0) = 3(0)^4-8(0)^3+6(0)^2+5 = 5$, so the stationary point is $(0,5)$.
- At $x=1$: $f(1) = 3-8+6+5 = 6$, so the stationary point is $(1,6)$.

**(b)** Sign test around $x=0$:

| $x$ | $-1$ | $0$ | $0.5$ |
|---|---|---|---|
| $f'(x)$ | $-$ | $0$ | $+$ |
| gradient | ↘ | — | ↗ |

$f'(-1)=12(-1)(-2)^2=-48<0$; $f'(0.5)=12(0.5)(-0.5)^2=1.5>0$. Sign changes $-\to+$, so $(0,5)$ is a **local minimum**.

Sign test around $x=1$:

| $x$ | $0.5$ | $1$ | $2$ |
|---|---|---|---|
| $f'(x)$ | $+$ | $0$ | $+$ |
| gradient | ↗ | — | ↗ |

$f'(2)=12(2)(1)^2=24>0$. The sign stays positive on both sides, so $(1,6)$ is a **positive (rising) point of inflection**, not a turning point.

---

**Question.** Let $f(x) = xe^{-x}$.
**(a)** Show that $f'(x)$ can be written in the form $(a-x)e^{-x}$, and state the value of $a$.
**(b)** Hence find the stationary point of $f$, which occurs at $x=b$. State $b$ and the coordinates of the stationary point correct to three decimal places.
**(c)** Use a sign test to classify this stationary point.

**(a)** By the product rule:
$$f'(x) = (1)e^{-x} + x(-e^{-x}) = e^{-x}-xe^{-x} = (1-x)e^{-x}$$
So $a=1$.

**(b)** Set $f'(x)=0$: $(1-x)e^{-x}=0$. Since $e^{-x}>0$ for every real $x$, the only solution comes from $1-x=0$, i.e. $x=1=b$.

$$f(1) = 1\times e^{-1} = \frac{1}{e} \approx 0.368$$

Stationary point: $(1, 0.368)$.

**(c)**

| $x$ | $0.5$ | $1$ | $2$ |
|---|---|---|---|
| $f'(x)$ | $+$ | $0$ | $-$ |
| gradient | ↗ | — | ↘ |

$f'(0.5)=(0.5)e^{-0.5}\approx 0.303>0$; $f'(2)=(-1)e^{-2}\approx-0.135<0$. Sign changes $+\to-$, so $f(x)$ has a **maximum** at $x=1$, with maximum value $f(1)=\dfrac{1}{e}$.

---

**Question.** The graph of $f(x) = \dfrac{3x-2}{x^2}$ is a curve with a vertical asymptote at $x=0$, approaching $y=0$ as $x\to\pm\infty$, falling steeply to $-\infty$ as $x\to 0^-$, and falling from $+\infty$ down towards a flat hump for $x>0$ (consistent with the local behaviour found below).

**(a)** Find the exact value(s) of $x$ for which $f'(x)=0$.
**(b)** Determine the values of $x$ for which $f'(x)>0$.
**(c)** Determine the values of $x$ for which $f'(x)<0$.

**(a)** By the quotient rule, with $u=3x-2$ ($u'=3$) and $v=x^2$ ($v'=2x$):

$$f'(x) = \frac{3x^2-(3x-2)(2x)}{x^4} = \frac{3x^2-6x^2+4x}{x^4} = \frac{-3x^2+4x}{x^4} = \frac{x(4-3x)}{x^4} = \frac{4-3x}{x^3}$$

Set $f'(x)=0$ (noting $x\ne 0$, since $x=0$ is outside the domain): $4-3x=0 \Rightarrow x=\dfrac{4}{3}$.

**(b)** Need $\dfrac{4-3x}{x^3}>0$, i.e. numerator and denominator share the same sign.

- Both positive: $4-3x>0$ and $x^3>0$ $\Rightarrow x<\tfrac43$ and $x>0$ $\Rightarrow 0<x<\tfrac43$.
- Both negative: $4-3x<0$ and $x^3<0$ $\Rightarrow x>\tfrac43$ and $x<0$ — impossible.

So $f'(x)>0$ for $x\in\left(0,\dfrac43\right)$.

**(c)** Need $\dfrac{4-3x}{x^3}<0$, i.e. numerator and denominator have opposite signs.

- $4-3x>0$, $x^3<0$: $x<\tfrac43$ and $x<0$ $\Rightarrow x<0$.
- $4-3x<0$, $x^3>0$: $x>\tfrac43$ and $x>0$ $\Rightarrow x>\tfrac43$.

So $f'(x)<0$ for $x\in(-\infty,0)\cup\left(\dfrac43,\infty\right)$.

---

**Question.** Let $f(x) = 2e^{x^2}-2$ and $g(x)=\log_e(x^2+1)$.
**(a)** Find $g'(3)$.
**(b)** Find the value(s) of $x$ for which the gradient of the graph of $f$ equals 3 (correct to 3 d.p.).
**(c)** Find the value(s) of $x$ for which $f'(x) < g'(x)$.

**(a)** Let $u=x^2+1$, $y=\log_e u$. $\dfrac{du}{dx}=2x$, $\dfrac{dy}{du}=\dfrac1u$.

$$g'(x) = \frac{1}{x^2+1}\times 2x = \frac{2x}{x^2+1}$$

$$g'(3) = \frac{2(3)}{3^2+1} = \frac{6}{10} = \frac{3}{5} = 0.6$$

**(b)** $f'(x) = 2\times 2x\, e^{x^2} = 4xe^{x^2}$ (chain rule, since $\frac{d}{dx}e^{x^2}=2xe^{x^2}$). Set $f'(x)=3$:

$$4xe^{x^2}=3 \iff xe^{x^2} = \frac34$$

This is transcendental (not solvable by algebra), so solve numerically/graphically: $x\approx 0.553$. *(Check: $0.553\times e^{0.553^2}=0.553\times e^{0.306}\approx0.553\times1.358\approx0.751\approx\tfrac34$. ✓)*

**(c)** We need $4xe^{x^2} < \dfrac{2x}{x^2+1}$, i.e.
$$4xe^{x^2} - \frac{2x}{x^2+1} < 0 \iff 2x\left(2e^{x^2}-\frac{1}{x^2+1}\right) < 0$$

For **every** real $x$, $e^{x^2}\ge 1$ and $\dfrac{1}{x^2+1}\le 1$, so $2e^{x^2}-\dfrac{1}{x^2+1} \ge 2-1 = 1 > 0$ always. The second factor is therefore always strictly positive, so the sign of the whole expression is decided entirely by $2x$:

- $x>0 \Rightarrow$ expression $>0 \Rightarrow f'(x)>g'(x)$.
- $x<0 \Rightarrow$ expression $<0 \Rightarrow f'(x)<g'(x)$.
- $x=0 \Rightarrow f'(x)=g'(x)=0$.

So $f'(x)<g'(x)$ exactly when $x<0$.

---

**Question.** Let $y = 3x^3-4x-9$. Find the coordinates of the turning points, and the $y$-intercept.

*(question text reconstructed from working — check original if this seems off: the source gives $\frac{dy}{dx}=9x^2-4$ and the point $(0,-9)$, both of which match $y=3x^3-4x-9$ exactly, so this is almost certainly the original function)*

$$\frac{dy}{dx} = 9x^2-4$$

Turning points occur where $\dfrac{dy}{dx}=0$:
$$9x^2-4=0 \iff x^2=\frac49 \iff x=\pm\frac23$$

So there are two turning points, at $x=-\dfrac23$ and $x=\dfrac23$. Finding the corresponding $y$-values from $y=3x^3-4x-9$:

$$y\!\left(-\frac23\right) = 3\left(-\frac23\right)^3-4\left(-\frac23\right)-9 = -\frac{8}{9}+\frac{8}{3}-9 = \frac{-8+24-81}{9} = -\frac{65}{9}$$

$$y\!\left(\frac23\right) = 3\left(\frac23\right)^3-4\left(\frac23\right)-9 = \frac{8}{9}-\frac{8}{3}-9 = \frac{8-24-81}{9} = -\frac{97}{9}$$

Classifying each using the second derivative, $\dfrac{d^2y}{dx^2}=18x$:

- At $x=-\dfrac23$: $18\left(-\dfrac23\right)=-12<0$, so this is a **local maximum**: $\left(-\dfrac23,\,-\dfrac{65}{9}\right)$.
- At $x=\dfrac23$: $18\left(\dfrac23\right)=12>0$, so this is a **local minimum**: $\left(\dfrac23,\,-\dfrac{97}{9}\right)$.

(This agrees with a sign test on $\dfrac{dy}{dx}=9x^2-4$: it is $+,0,-,0,+$ moving through $x=-1,-\tfrac23,0,\tfrac23,1$ — e.g. at $x=0$, $\dfrac{dy}{dx}=-4<0$ — confirming maximum then minimum.)

**$y$-intercept:** at $x=0$,
$$y = 3(0)^3-4(0)-9 = -9 \implies (0,-9)$$

### Optimisation problems

**Method.** To optimise a quantity described by a function $f$:
1. Write $f$ as a function of **one** variable, using any given constraint to eliminate the other(s).
2. Solve $f'(x)=0$ for the critical point(s).
3. Use a sign test (or second derivative) to confirm whether each is a maximum or minimum.

---

**Question.** Two numbers $x$ and $y$ have a sum of 10. Find the two numbers such that the sum of their squares, $S$, is a minimum, and find this minimum value.

Since $x+y=10$, $y=10-x$.

$$S(x) = x^2+y^2 = x^2+(10-x)^2 = x^2+100-20x+x^2 = 2x^2-20x+100$$

$$S'(x) = 4x-20$$

Set $S'(x)=0$: $4x=20 \Rightarrow x=5$, so $y=5$.

| $x$ | $4$ | $5$ | $6$ |
|---|---|---|---|
| $S'(x)$ | $-$ | $0$ | $+$ |
| slope | ↘ | — | ↗ |

$S'(4)=16-20=-4<0$; $S'(6)=24-20=4>0$. Sign changes $-\to+$, confirming a **minimum** at $x=5$.

$$S(5) = 2(5)^2-20(5)+100 = 50-100+100 = 50$$

The two numbers are both $5$, and the minimum sum of squares is $50$.

---

**Question.** Two numbers $a$ and $b$ have a sum of 12. Find $a$ and $b$ such that their product is a maximum.

Since $a+b=12$, $b=12-a$. Let $f(a)=ab=a(12-a)=12a-a^2$.

$$f'(a) = 12-2a$$

Set $f'(a)=0$: $2a=12 \Rightarrow a=6 \Rightarrow b=6$.

Since $f(a)=12a-a^2$ is a downward parabola in $a$, this stationary point is automatically a maximum. Maximum product: $f(6)=6\times6=36$.

---

**Question.** A rectangular paddock has length $a$ and width $b$, and a perimeter of 900 m. Find the dimensions that maximise the enclosed area, and find this maximum area.

$$2(a+b)=900 \iff a+b=450 \iff b=450-a$$

Let $f(a) = ab = a(450-a) = 450a-a^2$.

$$f'(a) = 450-2a$$

Set $f'(a)=0$: $2a=450 \Rightarrow a=225 \Rightarrow b=225$.

Again $f(a)$ is a downward parabola, so this is a maximum. Maximum area: $A = 225\times225 = 50\,625\text{ m}^2$ (the paddock is in fact a square).

---

**Question.** Find the point on the line $y=x+2$ that is closest to the point $(8,1)$, and hence find the shortest distance between them.

*(question text reconstructed from working — check original if this seems off)*

The distance from a general point $(x,y)$ on the line to $(8,1)$ is

$$D = \sqrt{(x-8)^2+(y-1)^2}$$

Substituting $y=x+2$, so $y-1=x+1$:

$$D = \sqrt{(x-8)^2+(x+1)^2}$$

Let $u=(x-8)^2+(x+1)^2$, so $D=\sqrt{u}=u^{1/2}$, and $\dfrac{dD}{du}=\dfrac12u^{-1/2}$.

$$\frac{du}{dx} = 2(x-8)+2(x+1) = 4x-14$$

By the chain rule, $\dfrac{dD}{dx} = \dfrac{dD}{du}\times\dfrac{du}{dx} = \dfrac{1}{2\sqrt{u}}(4x-14)$. Since $\dfrac{1}{2\sqrt{u}}$ is never zero, $D'(x)=0$ exactly when $4x-14=0$:

$$x = \frac{14}{4} = 3.5$$

Then $y = 3.5+2 = 5.5$, so the closest point is $(3.5,\,5.5)$.

Minimum distance: $u(3.5) = (3.5-8)^2+(3.5+1)^2 = (-4.5)^2+(4.5)^2 = 20.25+20.25=40.5$

$$D_{\min} = \sqrt{40.5} = \sqrt{\frac{81}{2}} = \frac{9}{\sqrt2} = \frac{9\sqrt2}{2} \approx 6.364$$

---

**Question.** A cylinder of radius $r$ and height $h$ is inscribed in a sphere of radius 8. Find the radius $r$ (and height $h$) of the cylinder that maximises its volume.

*(question text reconstructed from working — check original if this seems off)*

If the cylinder's axis passes through the centre of the sphere, then half its height, its radius, and the sphere's radius form a right triangle: $r^2+\left(\dfrac h2\right)^2=8^2=64$, so

$$h = 2\sqrt{64-r^2}$$

Volume: $V=\pi r^2h = 2\pi r^2\sqrt{64-r^2}$.

By the product rule, with $u=r^2$ ($u'=2r$) and $v=(64-r^2)^{1/2}$ ($v'=-r(64-r^2)^{-1/2}$ by the chain rule):

$$V'(r) = 2\pi\left[2r\sqrt{64-r^2} + r^2\times\left(\frac{-r}{\sqrt{64-r^2}}\right)\right] = 4\pi r\sqrt{64-r^2} - \frac{2\pi r^3}{\sqrt{64-r^2}}$$

Set $V'(r)=0$ and multiply through by $\sqrt{64-r^2}$:

$$4\pi r(64-r^2) = 2\pi r^3 \;\overset{\div\,2\pi r}{\implies}\; 2(64-r^2)=r^2 \implies 128 = 3r^2 \implies r^2=\frac{128}{3}$$

$$r = \sqrt{\frac{128}{3}} = \frac{8\sqrt2}{\sqrt3} = \frac{8\sqrt6}{3} \approx 6.532$$

Then $h = 2\sqrt{64-\tfrac{128}{3}} = 2\sqrt{\tfrac{64}{3}} = \dfrac{16}{\sqrt3}=\dfrac{16\sqrt3}{3}\approx 9.238$.

Maximum volume: $V = 2\pi r^2\sqrt{64-r^2} = 2\pi\left(\dfrac{128}{3}\right)\left(\dfrac{8\sqrt3}{3}\right) = \dfrac{2048\sqrt3\,\pi}{9}\approx 1238.6$ (cubic units).

---

**Question.** A rectangular box has a base measuring $x$ by $2x$ and height $h$. Its total surface area is 48 square units. Express the volume $V$ as a function of $x$ alone, and hence find the value of $x$ (and $h$) that maximises the volume, and this maximum volume.

*(question text reconstructed from working — check original if this seems off)*

The box has three pairs of faces: two of size $x\times h$, two of size $2x\times h$, and two of size $2x\times x$ (top and bottom). Total surface area:

$$A = 2(xh) + 2(2xh) + 2(2x\cdot x) = 2\big(2x^2+xh+2xh\big) = 4x^2+6xh = 48$$

Solving for $h$:
$$h = \frac{48-4x^2}{6x} = \frac{8}{x}-\frac{2x}{3}$$

Volume: $V = x(2x)h = 2x^2h$, so
$$V(x) = 2x^2\left(\frac8x-\frac{2x}{3}\right) = 16x-\frac{4x^3}{3}$$

$$V'(x) = 16-4x^2$$

Set $V'(x)=0$: $x^2=4\Rightarrow x=2$ (taking the positive root, as $x$ is a length).

Since $V''(x)=-8x$, at $x=2$: $V''(2)=-16<0$, confirming a **maximum**.

$$h = \frac82 - \frac{2(2)}{3} = 4-\frac43 = \frac83$$

$$V_{\max} = 16(2)-\frac{4(2)^3}{3} = 32-\frac{32}{3} = \frac{96-32}{3} = \frac{64}{3}$$

---

**Question.** Tin boxes with a square base are to be made to contain 2 litres (2000 cm³) of olive oil. To keep the cost of metal to a minimum, the total surface area must be as small as possible. Let the side of the base be $x$ cm and the height be $h$ cm.

**(a)** Show that the total surface area $A$ is given by $A=2x^2+\dfrac{8000}{x}$.
**(b)** Sketch $A$ against $x$.
**(c)** Use calculus to find the exact value of $x$ that minimises $A$, and confirm it is a minimum.
**(d)** Find this minimum surface area, correct to the nearest cm².
**(e)** Sketch the box of smallest surface area, with dimensions correct to two decimal places.

**(a)** Volume: $V=x^2h = 2000 \Rightarrow h=\dfrac{2000}{x^2}$.

The box is closed (base, lid, and four sides), so
$$A = 2x^2 + 4xh = 2x^2+4x\left(\frac{2000}{x^2}\right) = 2x^2+\frac{8000}{x}$$

**(b)** The graph of $A$ against $x$ (for $x>0$) falls steeply from $+\infty$ as $x\to0^+$ (dominated by the $8000/x$ term), reaches a shallow minimum of about $950$ near $x\approx 13$, then rises again for larger $x$ (now dominated by $2x^2$) — e.g. at $x=10$, $A=200+800=1000$; at $x=20$, $A=800+400=1200$; at $x=40$, $A=3200+200=3400$ (off the top of a graph scaled to 2000).

**(c)** $A(x) = 2x^2+8000x^{-1}$, so
$$A'(x) = 4x - \frac{8000}{x^2}$$

Set $A'(x)=0$:
$$4x = \frac{8000}{x^2} \iff 4x^3 = 8000 \iff x^3=2000 \iff x=\sqrt[3]{2000}\approx 12.6$$

| $x$ | $12$ | $12.6$ | $13$ |
|---|---|---|---|
| $A'(x)$ | $-$ | $0$ | $+$ |
| slope | ↘ | — | ↗ |

$A'(12)=48-\dfrac{8000}{144}\approx-7.6<0$; $A'(13)=52-\dfrac{8000}{169}\approx4.7>0$. Sign changes $-\to+$, confirming $x=\sqrt[3]{2000}$ gives a **minimum**.

**(d)** With $x=\sqrt[3]{2000}=10\sqrt[3]{2}\approx12.599$:

$$A\big(\sqrt[3]{2000}\big) = 2\big(\sqrt[3]{2000}\big)^2 + \frac{8000}{\sqrt[3]{2000}} \approx 2(158.74)+635.0 \approx 317.5+635.0 \approx 952\text{ cm}^2$$

**(e)** $h = \dfrac{2000}{x^2} = \dfrac{2000}{158.74}\approx12.60$ cm. Since $x\approx h\approx12.60$ cm, the optimal box is (to two decimal places) a **cube** of side $12.60\text{ cm}\times12.60\text{ cm}\times12.60\text{ cm}$.

---

**Question.** For $0\le t\le 8$, let $V(t) = t\sqrt{8-t}$.
**(a)** Show that $V'(t)$ can be written in the form $\dfrac{a-bt}{2\sqrt{8-t}}$, and state $a$ and $b$.
**(b)(i)** At what time does $V$ reach its maximum?
**(ii)** Find this maximum value of $V$ (in surd form), and hence find the constant $k$ such that $V_{\max}=k\left(\dfrac83\right)^{3/2}$.

**(a)** Write $V(t) = t(8-t)^{1/2}$. By the product rule:

$$V'(t) = (8-t)^{1/2} + t\times\frac12(8-t)^{-1/2}\times(-1) = \sqrt{8-t} - \frac{t}{2\sqrt{8-t}}$$

Combine over a common denominator:

$$V'(t) = \frac{2(8-t)-t}{2\sqrt{8-t}} = \frac{16-2t-t}{2\sqrt{8-t}} = \frac{16-3t}{2\sqrt{8-t}}$$

So $a=16$, $b=3$.

**(b)(i)** $V$ is stationary where $V'(t)=0$:
$$\frac{16-3t}{2\sqrt{8-t}}=0 \iff 16-3t=0 \iff t=\frac{16}{3}$$

(The numerator and denominator have the sign pattern $+,0,-$ as $t$ passes through $16/3$ — e.g. checking $t<16/3$ gives $V'>0$ and $t>16/3$ gives $V'<0$ — so this is a maximum.)

**(ii)**
$$V\!\left(\frac{16}{3}\right) = \frac{16}{3}\sqrt{8-\frac{16}{3}} = \frac{16}{3}\sqrt{\frac{24-16}{3}} = \frac{16}{3}\sqrt{\frac83} = \frac{16}{3}\times\frac{2\sqrt2}{\sqrt3} = \frac{16}{3}\times\frac{2\sqrt6}{3} = \frac{32\sqrt6}{9}$$

To write this as $k\left(\dfrac83\right)^{3/2}$: note $\left(\dfrac83\right)^{3/2} = \dfrac83\sqrt{\dfrac83} = \dfrac83\times\dfrac{2\sqrt6}{3} = \dfrac{16\sqrt6}{9}$. Comparing with $V_{\max}=\dfrac{32\sqrt6}{9}$:

$$k\times\frac{16\sqrt6}{9} = \frac{32\sqrt6}{9} \implies k=2$$

---

### Composite figure: minimising a perimeter for fixed area

*(The figure — labelled $A,B,C,D$ in the original — could not be fully reconstructed: the perimeter breakdown below is clearly legible in the source, but the intermediate algebra linking the fixed area to $\theta$ was not legible enough to transcribe with confidence. The function $P(r)$ below, and every step of calculus built on it, is explicit in the source and has been independently verified here.)*

**Question.** A plane figure $ABCD$ is bounded by a semicircular arc $\widehat{ACD}$ of radius $r$, a circular arc $\widehat{AB}$ of radius $r$ subtending an angle $2\theta$ at the centre, and two straight edges each of length $r$. The area enclosed by the figure is fixed at 2 square units.

**(a)** Show that the perimeter is $P = r(\pi+2\theta+2)$.
**(b)** Using the fixed area to eliminate $\theta$, show that $P(r) = \left(2+\dfrac\pi2\right)r+\dfrac2r$.
**(c)(i)** Find $\dfrac{dP}{dr}$. **(ii)** Hence find the exact value of $r$ for which $P$ is stationary.
**(d)** Confirm this is a minimum, and find the minimum perimeter in exact (surd) form.

**(a)**
$$P_{\widehat{ACD}} = \pi r, \qquad P_{\widehat{AB}} = 2r\theta, \qquad P_{\text{straight}} = 2r$$

$$P = \pi r + 2r\theta + 2r = r(\pi+2\theta+2)$$

**(b)** Eliminating $\theta$ via the area constraint gives (as established in the source):
$$P(r) = \left(2+\frac\pi2\right)r + \frac2r = \left(2+\frac\pi2\right)r+2r^{-1}$$

**(c)(i)**
$$P'(r) = \left(2+\frac\pi2\right) - 2r^{-2} = \left(2+\frac\pi2\right)-\frac{2}{r^2}$$

**(ii)** Set $P'(r)=0$:
$$2+\frac\pi2 = \frac{2}{r^2} \iff r^2 = \frac{2}{2+\frac\pi2} = \frac{4}{4+\pi}$$

$$r = \frac{2}{\sqrt{4+\pi}}$$

**(d)**

| $r^2$ | $0.5$ | $\dfrac{4}{4+\pi}$ | $1$ |
|---|---|---|---|
| $P'$ | $-$ | $0$ | $+$ |
| gradient | ↘ | — | ↗ |

Sign changes $-\to+$, so $P$ is at a **minimum** when $r^2=\dfrac{4}{4+\pi}$, i.e. $r=\sqrt{\dfrac{4}{4+\pi}}=\dfrac{2}{\sqrt{4+\pi}}$.

$$P_{\min} = \left(2+\frac\pi2\right)\times\frac{2}{\sqrt{4+\pi}} + \frac{2}{\frac{2}{\sqrt{4+\pi}}} = \frac{2\left(2+\frac\pi2\right)}{\sqrt{4+\pi}} + \sqrt{4+\pi}$$

Since $2\left(2+\dfrac\pi2\right)=4+\pi$, the first term is $\dfrac{4+\pi}{\sqrt{4+\pi}}=\sqrt{4+\pi}$. So

$$P_{\min} = \sqrt{4+\pi}+\sqrt{4+\pi} = 2\sqrt{4+\pi}$$

### Rates of change and kinematics

**Question.** A particle moves along a straight line so that its displacement from the origin $O$ at time $t$ seconds is $x(t) = t^3-6t^2+5t$, for $t\ge0$.
**(a)** Find $x'(t)$, the velocity function.
**(b)(i)** After $t=0$, how many more times does the particle pass back through the origin?
**(ii)** How many times is the particle stationary (i.e. has zero velocity)?

**(a)**
$$x'(t) = 3t^2-12t+5$$

**(b)(i)** The particle is at $O$ when $x(t)=0$:
$$t^3-6t^2+5t=0 \iff t(t^2-6t+5)=0 \iff t(t-1)(t-5)=0$$

(Dividing $x(t)$ by $t$ gives $\dfrac{x(t)}{t}=t^2-6t+5=(t-1)(t-5)$, confirming the factorisation.) So $t=0,\,1,\,5$ — three solutions in total, including the start at $t=0$. **After** $t=0$, the particle returns to the origin $2$ times (at $t=1$ and $t=5$).

**(ii)** The particle is stationary when $x'(t)=0$: $3t^2-12t+5=0$. By the quadratic formula:
$$t = \frac{12\pm\sqrt{144-60}}{6} = \frac{12\pm\sqrt{84}}{6} = 2\pm\frac{\sqrt{21}}{3}$$

The discriminant $144-60=84>0$, so there are **2** real solutions (both positive, since $\sqrt{21}/3\approx1.53<2$): $t\approx0.472$ and $t\approx3.528$.

---

**Question.** The population (in thousands) of a colony of bacteria after $t$ hours is $P(t) = 300e^{0.2t}$.
**(a)** Find the average rate of change of $P$ between $t=3$ and $t=8$ hours.
**(b)** Find $P'(t)$, the instantaneous rate of change.
**(c)** Find the first time $t$ at which the instantaneous rate of change is 250.

*(question text reconstructed from working — check original if this seems off)*

**(a)**
$$\text{Avg rate of change} = \frac{P(8)-P(3)}{8-3} = \frac{300e^{0.2\times8}-300e^{0.2\times3}}{5} = \frac{300e^{1.6}-300e^{0.6}}{5}$$

$$\approx \frac{1485.91-546.64}{5} = \frac{939.27}{5} \approx 187.85 \text{ (thousand per hour)}$$

**(b)** By the chain rule:
$$P'(t) = 300\times0.2\times e^{0.2t} = 60e^{0.2t}$$

**(c)** Set $P'(t)=250$:
$$60e^{0.2t}=250 \iff e^{0.2t}=\frac{250}{60}=\frac{25}{6} \iff 0.2t = \ln\!\left(\frac{25}{6}\right)$$

$$t = \frac{\ln\!\left(\frac{25}{6}\right)}{0.2} \approx \frac{1.4271}{0.2} \approx 7.14 \text{ hours}$$

---

**Question.** A Ferris wheel at a carnival rotates at a constant rate anticlockwise. A point $P$ on the wheel is $h$ metres above the ground at time $t$ hours after 1 pm, where
$$h(t) = 62-60\cos\!\left(\frac{5\pi t}{2}\right)$$

**(a)** What was the height of $P$ above the ground at 1 pm?
**(b)** Find $h'(t)$, and hence find the instantaneous rate of change of height at 1:24 pm (i.e. $t=0.4$). What can you conclude about $P$ at this time?
**(c)** Find the average rate of change of height between 1 pm and 1:24 pm, in both m/h and m/min.
**(d)** What are the maximum and minimum heights of $P$ above the ground?
**(e)** At what time between 1 pm and 1:24 pm did the greatest rate of change of height occur?

**(a)** At $t=0$:
$$h(0) = 62-60\cos(0) = 62-60(1) = 2\text{ metres}$$

**(b)** By the chain rule:
$$h'(t) = -60\times\left(-\sin\!\left(\frac{5\pi t}{2}\right)\right)\times\frac{5\pi}{2} = 150\pi\sin\!\left(\frac{5\pi t}{2}\right)$$

At $t=0.4$: $\dfrac{5\pi(0.4)}{2}=\pi$, and $\sin(\pi)=0$, so
$$h'(0.4) = 150\pi\sin(\pi) = 0\text{ m/h}$$

Since the instantaneous rate of change is zero, $P$ is at a turning point of height at 1:24 pm — i.e. momentarily at its **highest or lowest** point on the wheel.

**(c)** At $t=0.4$: $h(0.4)=62-60\cos(\pi)=62-60(-1)=122$ metres.

$$\text{Avg rate of change} = \frac{122-2}{0.4-0} = \frac{120}{0.4} = 300\text{ m/h} = \frac{300}{60} = 5\text{ m/min}$$

**(d)** Since $\cos(\cdot)$ ranges over $[-1,1]$, $h(t)$ ranges over $[62-60(1),\,62-60(-1)] = [2,\,122]$.

$$\text{Maximum height} = 122\text{ m}, \qquad \text{Minimum height} = 2\text{ m}$$

**(e)** $h'(t)=150\pi\sin\!\left(\dfrac{5\pi t}{2}\right)$ is greatest when $\sin\!\left(\dfrac{5\pi t}{2}\right)=1$, i.e. (for the first time in range) when $\dfrac{5\pi t}{2}=\dfrac\pi2$:

$$t = \frac{\pi}{2}\times\frac{2}{5\pi} = \frac15 = 0.2\text{ hours} = 12\text{ minutes}$$

So the greatest rate of change of height occurred at **1:12 pm**.

## See also

[[Differentiation Rules]] · [[Applications of Differentiation]] · [[Limits]]
