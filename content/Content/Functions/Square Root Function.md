# The Square Root Function

$$y=\sqrt x$$

Unlike a parabola or hyperbola, this graph starts at a fixed point and only goes one way: domain $[0,\infty)$, range $[0,\infty)$, passing through $(0,0)$ and $(1,1)$. It is, in fact, the inverse of $y=x^2$ restricted to $x\ge0$ — see [[Inverse Functions]] for why restricting the domain first is necessary before a parabola can have an inverse function at all.

## Reflections of the Base Graph

- If $a<0$ in $y=a\sqrt x$, the graph is reflected in the $x$-axis (e.g. $y=-\sqrt x$ passes through $(0,0)$ and $(1,-1)$); the range becomes $(-\infty,0]$.
- If $x$ is replaced with $-x$ (i.e. $y=\sqrt{-x}$), the graph is reflected in the $y$-axis (passing through $(0,0)$ and $(-1,1)$); the domain becomes $(-\infty,0]$.

## General Form and the Endpoint

$$y=a\sqrt{x-h}+k$$

$(h,k)$ is the **endpoint** of the curve (not a turning point — the graph only exists on one side of it), exactly the same $a,h,k$ transformation idea used for the [[Quadratic Functions|parabola]] and the [[Reciprocal Functions|hyperbola]]. The easiest way to find the endpoint and domain for *any* square-root function, without worrying about which exact sign convention is being used, is:

1. Set the expression under the square root to $0$ and solve for $x$ — that gives the endpoint's $x$-coordinate.
2. Check the sign of the coefficient of $x$ *inside* the root: if it's positive, the domain extends to the **right** of the endpoint ($[\,\cdot\,,\infty)$); if it's negative, the domain extends to the **left** ($(-\infty,\,\cdot\,]$).

(For the reflected case, this corresponds to the general form $y=a\sqrt{h-x}+k$, so that $(h,k)$ is still the endpoint directly — a cleaner way to write it than $a\sqrt{-x-h}+k$, which shifts the endpoint to $-h$ instead.)

The reflection rules above still apply on top of this: if $a<0$ the curve is also flipped vertically (range becomes $(-\infty,k]$ instead of $[k,\infty)$).

**Worked example.** State the transformation that changes $y=\sqrt x$ into $y=-3\sqrt{x+5}+3$.

Matching against $y=a\sqrt{x-h}+k$: $a=-3$, $x-h=x+5 \implies h=-5$, $k=3$.

**Exercise 2.**

**(a)** $y=2\sqrt{x-3}+1$: here $h=3,\ k=1$, and the coefficient inside the root ($+1$ on $x$) is positive, so the domain extends right of the endpoint:

$$D=[3,\infty), \qquad R=[1,\infty)$$

**(b)** $y=-4\sqrt{3x+2}-4$. Factor the inside first: $3x+2=3\left(x+\tfrac23\right)$, so $y=-4\sqrt3\sqrt{x+\tfrac23}-4$, giving endpoint $x=-\tfrac23$. The coefficient on $x$ inside is positive ($+3$), so the domain extends right:

$$D=\left[-\frac23,\infty\right)$$

Here $k=-4$ and $a<0$, so the range is reflected downward from the endpoint:

$$R=(-\infty,-4]$$

**(c)** $y=\sqrt{4-x}+2 = \sqrt{-(x-4)}+2$: endpoint at $x=4$ (since $4-x=0 \implies x=4$), $k=2$. The coefficient on $x$ inside is negative ($-1$), so the domain extends **left** of the endpoint:

$$D=(-\infty,4], \qquad a=1>0 \implies R=[2,\infty)$$

**Worked example: sketch $y=-2\sqrt{x-3}+1$.**

Endpoint: $x-3=0\implies x=3$, so the endpoint is $(3,1)$. Since the coefficient inside is positive, the domain extends right: $D=[3,\infty)$. Since $a=-2<0$, the range is reflected downward from the endpoint: $R=(-\infty,1]$.

- $x$-intercept: set $y=0$: $-2\sqrt{x-3}+1=0 \implies \sqrt{x-3}=\dfrac12 \implies x-3=\dfrac14 \implies x=\dfrac{13}{4}$, i.e. $\left(\dfrac{13}{4},0\right)$
- $y$-intercept: set $x=0$: $-2\sqrt{0-3}+1=-2\sqrt{-3}+1$, which is **undefined** (square root of a negative number) — so there is **no** $y$-intercept, consistent with $D=[3,\infty)$ not including $x=0$ at all.

**Graph description:** a curve starting at the endpoint $(3,1)$ and sweeping down and to the right (since $a<0$), crossing the $x$-axis at $\left(\dfrac{13}4,0\right) = (3.25,0)$, with no $y$-intercept.

For more mixed practice across all the Unit 1 function topics, see [[Functions - Practice and Revision]].
