# Quadratic Functions

A **quadratic function** has the general form

$$f(x) = ax^2 + bx + c, \qquad a, b, c \in \mathbb{R}, \ a \mathrel{\char"2260} 0$$

Its graph is a **parabola** — a symmetric, U-shaped curve. The sign of $a$ tells you which way it opens:

- If $a > 0$, the parabola opens **upward** and has a **minimum** turning point.
- If $a < 0$, the parabola opens **downward** and has a **maximum** turning point.

Everything else about the parabola — where its turning point sits, how many times it crosses the $x$-axis, how wide or narrow it is — is controlled by $a$, $b$ and $c$ (or by the equivalent constants in the other forms below). This note works through all three standard forms, the key formulas for locating a parabola's features, fully worked examples transcribed and re-solved from the original lecture notes, and the standard techniques for solving quadratic equations and inequalities, transforming parabolas, and solving a line-and-parabola system.

This note focuses purely on quadratics. Related function families taught in the same block of lectures — polynomial division, cubics, reciprocal (hyperbola) functions, and the square root function — each have their own note: [[Polynomial Division and the Factor Theorem]], [[Cubic Functions]], [[Reciprocal Functions]], [[Square Root Function]].

## Key Formulas

**The three forms of a quadratic:**

| Form | Equation | What it's good for |
|---|---|---|
| General (standard) form | $f(x) = ax^2+bx+c$ | Reading off the $y$-intercept ($c$) directly |
| Vertex (turning point) form | $f(x) = a(x-h)^2+k$ | Reading off the turning point $(h,k)$ directly |
| Factored ($x$-intercept) form | $f(x) = a(x-p)(x-q)$ | Reading off the $x$-intercepts $p, q$ directly |

**Key quantities:**

| Quantity | Formula |
|---|---|
| Axis of symmetry | $x = \dfrac{-b}{2a}$ |
| Turning point (vertex) | $\left(\dfrac{-b}{2a},\ c-\dfrac{b^2}{4a}\right)$ |
| Discriminant | $\Delta = b^2-4ac$ |
| Quadratic formula | $x = \dfrac{-b \pm \sqrt{\Delta}}{2a}$ |

**Nature of the roots:**

| Discriminant | Number of real roots | What the graph does |
|---|---|---|
| $\Delta > 0$ | 2 distinct real roots | Crosses the $x$-axis **twice** |
| $\Delta = 0$ | 1 repeated real root | **Touches** the $x$-axis once (turning point sits exactly on the axis) |
| $\Delta < 0$ | 0 real roots | **Never** touches the $x$-axis |

## 1. Forms of a Quadratic Function

### 1.1 General (Standard) Form

$$f(x) = ax^2+bx+c$$

Here $c$ is the $y$-intercept directly ($f(0)=c$), but the turning point and $x$-intercepts aren't obvious just by looking — you need the formulas above or one of the other two forms. Lecture notes often present a quadratic in a scrambled order and expect you to rearrange it first. For example, given

$$-x^2-3 = 3x$$

bring everything to one side:

$$-x^2-3x-3 = 0 \ \implies\ x^2+3x+3=0$$

(multiplying through by $-1$). Reading off the coefficients: $a=1$, $b=3$, $c=3$.

### 1.2 Vertex (Turning Point) Form

$$f(x) = a(x-h)^2+k$$

$(h,k)$ is the **turning point** (vertex) of the parabola, directly. This is the exact analogue of the vertex form used for cubics in [[Cubic Functions]], $y=a(x-h)^3+k$ — the same $h,k$ shift idea, just applied to a different base shape.

### 1.3 Factored (x-intercept) Form

$$f(x) = a(x-p)(x-q)$$

$p$ and $q$ are the $x$-intercepts (roots) directly, since the function is zero exactly when $x=p$ or $x=q$. This only exists when the quadratic actually has real roots (i.e. $\Delta \ge 0$) — compare with the factored form for cubics, $y=a(x-b)(x-c)(x-d)$, in [[Cubic Functions]].

### 1.4 Converting General Form to Vertex Form: Completing the Square

The vertex form doesn't have to be guessed — it comes directly out of **completing the square** on the general form, and this is also *why* the axis-of-symmetry formula $x=\dfrac{-b}{2a}$ works.

$$
\begin{aligned}
f(x) &= ax^2+bx+c \\
&= a\left(x^2+\frac{b}{a}x\right)+c \\
&= a\left(x^2+\frac{b}{a}x + \left(\frac{b}{2a}\right)^2 - \left(\frac{b}{2a}\right)^2\right)+c \\
&= a\left(x+\frac{b}{2a}\right)^2 - \frac{b^2}{4a}+c \\
&= a\left(x-\left(\frac{-b}{2a}\right)\right)^2 + \left(c-\frac{b^2}{4a}\right)
\end{aligned}
$$

Comparing with $f(x)=a(x-h)^2+k$ gives exactly

$$h = \frac{-b}{2a}, \qquad k = c-\frac{b^2}{4a} = -\frac{\Delta}{4a}$$

(the last equality holds because $\Delta = b^2-4ac \implies -\Delta = 4ac-b^2 \implies \dfrac{-\Delta}{4a}=c-\dfrac{b^2}{4a}$). This is a genuinely useful shortcut: **the turning point's $y$-value is always $-\dfrac{\Delta}{4a}$.**

**Worked example.** Convert $f(x)=x^2+2x-4$ to vertex form by completing the square directly:

$$f(x) = x^2+2x-4 = (x^2+2x+1)-1-4 = (x+1)^2-5$$

So the turning point is $(-1,-5)$. This matches $h=\dfrac{-b}{2a}=\dfrac{-2}{2}=-1$ and $k=c-\dfrac{b^2}{4a}=-4-\dfrac{4}{4}=-5$ computed from the formula — and it matches the fully worked example in [Section 4](#4-worked-example-2-a-complete-analysis-of-a-parabola) below, which analyses this exact function from every angle.

## 2. Axis of Symmetry

Every parabola is symmetric about a vertical line through its turning point — the **axis of symmetry**:

$$x = \frac{-b}{2a}$$

This drops straight out of the completing-the-square work above (it's the $h$ value). For example, if

$$f(x) = -4x+3+2x^2 = 2x^2-4x+3$$

then $a=2$, $b=-4$, so the axis of symmetry is

$$x = \frac{-b}{2a} = \frac{4}{2\times 2} = 1$$

Later on, [[Differentiation Rules]] gives you a second, completely different way to find the turning point — by solving $f'(x)=0$ — which will agree with $x=\dfrac{-b}{2a}$ every time.

## 3. Intercepts, the Discriminant, and the Quadratic Formula

### 3.1 The y-intercept

Set $x=0$: for $f(x)=ax^2+bx+c$, the $y$-intercept is always just $(0,c)$.

### 3.2 The x-intercepts and the Discriminant

The $x$-intercepts are the solutions of $ax^2+bx+c=0$. Rather than solve this by completing the square every single time, we solve it once in general and package the result as the **quadratic formula**:

$$
\begin{aligned}
ax^2+bx+c&=0\\
x^2+\frac{b}{a}x &= -\frac{c}{a}\\
x^2+\frac{b}{a}x+\left(\frac{b}{2a}\right)^2 &= \left(\frac{b}{2a}\right)^2-\frac{c}{a}\\
\left(x+\frac{b}{2a}\right)^2 &= \frac{b^2-4ac}{4a^2}\\
x+\frac{b}{2a} &= \pm\frac{\sqrt{b^2-4ac}}{2a}\\
x&=\frac{-b\pm\sqrt{b^2-4ac}}{2a}
\end{aligned}
$$

The expression under the square root, $\Delta = b^2-4ac$, is called the **discriminant**, giving the quadratic formula its usual compact form:

$$\Delta = b^2-4ac \qquad\Longrightarrow\qquad x=\frac{-b\pm\sqrt{\Delta}}{2a}$$

Because $\Delta$ sits under a square root, its *sign* alone — without actually solving for $x$ — tells you how many real $x$-intercepts the parabola has (see the table in Key Formulas above):

- **$\Delta > 0$:** two different (distinct) real roots — the square root is a real, nonzero number, so $+\sqrt{\Delta}$ and $-\sqrt{\Delta}$ give two different values of $x$.
- **$\Delta = 0$:** two *equal* roots (a repeated root) — $\sqrt{\Delta}=0$, so both signs give the same single value of $x$, the turning point itself.
- **$\Delta < 0$:** no real roots — you'd need the square root of a negative number, which isn't a real number, so the parabola never reaches $y=0$.

**Quick check example.** For $f(x) = x^2-4+2x = x^2+2x-4$, is $\Delta$ positive, zero, or negative, and how many $x$-intercepts does the graph have?

$$\Delta = b^2-4ac = 2^2-4(1)(-4) = 4+16=20 > 0$$

Since $\Delta>0$, the graph has **2 distinct $x$-intercepts**. (We come back to this exact function for a full analysis in [Section 4](#4-worked-example-2-a-complete-analysis-of-a-parabola).)

## 4. Worked Example 1: Roots, a Table of Values, and a Sketch

**Question.** Let $f(x) = -3+x^2-2x$. Find the $x$-intercepts of $f$, then sketch its graph using a table of values.

*(question text reconstructed from working — check original if this seems off)*

**Part (a): find the $x$-intercepts.**

First rewrite in standard order:

$$f(x) = -3+x^2-2x = x^2-2x-3$$

so $a=1,\ b=-2,\ c=-3$.

$$\Delta = b^2-4ac = (-2)^2-4(1)(-3) = 4+12=16$$

$$x_1 = \frac{-b+\sqrt{\Delta}}{2a}=\frac{2+4}{2}=3 \qquad\qquad x_2=\frac{-b-\sqrt{\Delta}}{2a}=\frac{2-4}{2}=-1$$

So the $x$-intercepts are $x=3$ and $x=-1$.

**Part (b): sketch the graph using a table of values.**

The turning point sits at $x=\dfrac{-b}{2a}=\dfrac{2}{2}=1$, so a sensible table samples $x=-1,0,1,3$:

| $x$ | $-1$ | $0$ | $1$ | $3$ |
|---|---|---|---|---|
| $y$ | $0$ | $-3$ | $-4$ | $0$ |

(Check: $f(0)=-3$ ✓, $f(1)=1-2-3=-4$ ✓, $f(3)=9-6-3=0$ ✓ — all consistent with the roots found above.)

**Graph description:** an upward-opening parabola ($a=1>0$, minimum). Key features:

- $x$-intercepts at $(-1,0)$ and $(3,0)$
- $y$-intercept at $(0,-3)$
- Turning point (minimum) at $(1,-4)$
- Axis of symmetry: the vertical line $x=1$
- Domain: $\mathbb{R}$ (all real numbers)
- Range: $[-4,\infty)$

## 5. Worked Example 2: A Complete Analysis of a Parabola

This example works through every technique above on one function, from an unsimplified starting equation all the way to domain and range — essentially a template for "fully analyse this parabola" questions.

**Question.** For the relation $-x^2+y=2x-4$:
(a) write it in standard presentation; (b) discuss the sign of $a$ and what it means for the graph; (c) find the discriminant and state how many roots the graph has; (d) find the roots ($x$-intercepts); (e) find the equation of the axis of symmetry; (f) sketch the graph using a table of values; (g) state the domain and range.

**(a) Standard form.**

$$-x^2+y=2x-4 \ \implies\ y = x^2+2x-4$$

So $a=1,\ b=2,\ c=-4$.

**(b) Sign of $a$.**

$a=1>0$, so the parabola is **concave up** and has a **minimum** turning point.

**(c) Discriminant.**

$$\Delta = b^2-4ac = 2^2-4(1)(-4) = 4+16=20 > 0$$

Since $\Delta>0$, there are **2 distinct real roots** (the graph crosses the $x$-axis twice).

**(d) The roots.**

$$x=\frac{-b\pm\sqrt{\Delta}}{2a}=\frac{-2\pm\sqrt{20}}{2}=\frac{-2\pm 2\sqrt5}{2}=-1\pm\sqrt5$$

Since $\sqrt5 \approx 2.236$:

$$x\approx -1+2.236 = 1.236 \qquad\text{or}\qquad x\approx -1-2.236=-3.236$$

**(e) Axis of symmetry.**

$$x=\frac{-b}{2a}=\frac{-2}{2}=-1$$

**(f) Sketch, via a table of values.**

Using $x=-1$ (the axis of symmetry / turning point) and the two roots and the $y$-intercept:

| $x$ | $-3.236$ | $-1$ | $0$ | $1.236$ |
|---|---|---|---|---|
| $y$ | $0$ | $-5$ | $-4$ | $0$ |

(Check: $f(-1)=1-2-4=-5$ ✓, $f(0)=0+0-4=-4$ ✓, and $f$ at both roots is $0$ by construction.)

**Graph description:** an upward-opening parabola with

- $x$-intercepts at approximately $(-3.24,0)$ and $(1.24,0)$
- $y$-intercept at $(0,-4)$
- Turning point (minimum) at $(-1,-5)$
- Axis of symmetry: $x=-1$

**(g) Domain and range.**

Every quadratic has domain $\mathbb{R}$. Since this parabola opens upward with minimum value $-5$ (at the turning point):

$$D = \mathbb{R}, \qquad R=[-5,+\infty)$$

## 6. More Practice with the Discriminant

**Exercise E3.** For $f(x)=2x^2+3x-10$, determine the number of $x$-intercepts (without finding them explicitly).

$$\Delta = b^2-4ac = 3^2-4(2)(-10)=9+80=89$$

Since $\Delta=89>0$, there are **2 distinct $x$-intercepts**. (Because $89$ is not a perfect square, the actual roots are irrational — but the question only asks for the *count*, which the discriminant gives you immediately without solving anything else.)

**Exercise: sketch $f(x) = 12-5x-2x^2$.** This was set as a homework question in the original notes with no worked solution recorded, so here is the full solution.

Rewrite in standard order: $f(x) = -2x^2-5x+12$, so $a=-2,\ b=-5,\ c=12$.

$$\Delta = (-5)^2-4(-2)(12)=25+96=121=11^2$$

Since $121$ is a perfect square, the roots are rational:

$$x=\frac{-b\pm\sqrt\Delta}{2a}=\frac{5\pm11}{-4}$$

$$x_1=\frac{5+11}{-4}=\frac{16}{-4}=-4 \qquad\qquad x_2=\frac{5-11}{-4}=\frac{-6}{-4}=\frac32$$

Turning point: $x=\dfrac{-b}{2a}=\dfrac{5}{-4}=-\dfrac54$, and

$$f\!\left(-\tfrac54\right)=-2\left(\tfrac{25}{16}\right)-5\left(-\tfrac54\right)+12=-\tfrac{25}{8}+\tfrac{25}{4}+12=\tfrac{121}{8}=15.125$$

So the turning point is $\left(-\dfrac54,\ \dfrac{121}{8}\right)=(-1.25,\ 15.125)$ — a **maximum**, since $a=-2<0$. The $y$-intercept is $f(0)=12$.

**Graph description:** a downward-opening parabola with $x$-intercepts $(-4,0)$ and $(1.5,0)$, $y$-intercept $(0,12)$, maximum turning point at $(-1.25,15.125)$, axis of symmetry $x=-1.25$. Domain $\mathbb{R}$, range $(-\infty,\ 15.125]$.

## 7. Solving Quadratic Equations

Every quadratic equation $ax^2+bx+c=0$ can be solved by either of two routes, and it's worth knowing both:

1. **Factoring** (fast, when the factors are "nice"): write $ax^2+bx+c$ as $a(x-p)(x-q)$ and use the fact that a product is zero only if one of its factors is zero.
2. **The quadratic formula** (always works): $x=\dfrac{-b\pm\sqrt\Delta}{2a}$, whether or not the roots are rational.

**Factoring by splitting the middle term.** To factorise $2x^2-5x-3$ (the same technique used to factorise the quadratic that falls out of a cubic in [[Cubic Functions]]): find two numbers that multiply to $a\times c = 2\times(-3)=-6$ and add to $b=-5$. Those numbers are $-6$ and $1$:

$$
\begin{aligned}
2x^2-5x-3&=0\\
2x^2+x-6x-3&=0\\
x(2x+1)-3(2x+1)&=0\\
(x-3)(2x+1)&=0\\
\end{aligned}
$$

$$\implies x=3 \quad\text{or}\quad x=-\frac12$$

The same idea in reverse lets you build the factored form directly from known roots. For example, Worked Example 1 above found the roots $x=3$ and $x=-1$ for $f(x)=x^2-2x-3$ — so its factored form must be

$$f(x) = (x-3)(x+1)$$

(Check: $(x-3)(x+1)=x^2+x-3x-3=x^2-2x-3$ ✓.)

## 8. Solving Quadratic Inequalities

The quadratic equations above tell you *where* a parabola crosses the $x$-axis. A quadratic **inequality** asks for the whole *range* of $x$-values where the parabola is above or below the axis — and once you know the roots and which way the parabola opens, you can read the answer straight off a sketch.

**Method:**
1. Rearrange so one side is $0$.
2. Find the roots (by factoring or the quadratic formula).
3. Use the sign of $a$ to decide the shape, then read off which intervals are positive/negative from the sketch.

**Worked example.** Solve $x^2-2x-3 \ge 0$.

This is exactly the function from Worked Example 1, with roots $x=-1,3$ and $a=1>0$ (opens upward, minimum at $(1,-4)$). An upward parabola is *below* the axis **between** its roots and *above* the axis **outside** them. So:

$$x^2-2x-3\ge 0 \iff x\le -1 \ \text{ or }\ x\ge 3$$

i.e. $x\in(-\infty,-1]\cup[3,\infty)$.

**Second example.** Solve $-2x^2-5x+12 < 0$.

This is the function from [Section 6](#6-more-practice-with-the-discriminant), with roots $x=-4,\ 1.5$ and $a=-2<0$ (opens downward, maximum at $(-1.25,15.125)$). A downward parabola is *above* the axis **between** its roots and *below* the axis **outside** them, so it is negative outside the roots:

$$-2x^2-5x+12<0 \iff x<-4 \ \text{ or }\ x>1.5$$

i.e. $x\in(-\infty,-4)\cup(1.5,\infty)$ (strict inequalities throughout, since the original inequality was strict).

## 9. Transformations of Parabolas

Writing a parabola in vertex form, $f(x)=a(x-h)^2+k$, makes every transformation of the basic graph $y=x^2$ visible directly in the constants:

| Parameter | Effect |
|---|---|
| $h$ | Horizontal shift: right by $h$ if $h>0$, left by $\lvert h\rvert$ if $h<0$ |
| $k$ | Vertical shift: up by $k$ if $k>0$, down by $\lvert k\rvert$ if $k<0$ |
| $\lvert a\rvert > 1$ | Vertical **stretch** — narrower parabola |
| $0<\lvert a\rvert<1$ | Vertical **compression** — wider parabola |
| $a<0$ | **Reflection** in the $x$-axis — flips a minimum into a maximum (and vice versa) |

This is exactly the same $a,h,k$ transformation language used for the [[Square Root Function]] and for [[Reciprocal Functions]] — once you understand how $a$, $h$ and $k$ act on $y=x^2$, the same logic carries straight across to $y=a\sqrt{x-h}+k$ and $y=\dfrac{a}{x-h}+k$.

## 10. Simultaneous Equations: A Line and a Parabola

Finding where a straight line meets a parabola means solving the two equations together. Since the line is linear, the standard method is to substitute it directly into the quadratic equation — this reduces the system to a single quadratic in one variable, which you then solve exactly as in [Section 7](#7-solving-quadratic-equations).

Geometrically, the discriminant of that resulting quadratic tells you how many times the line meets the parabola: $\Delta>0$ gives two intersection points, $\Delta=0$ means the line is a tangent (touches once), and $\Delta<0$ means the line misses the parabola entirely.

**Worked example.** Find where the line $y=x+2$ intersects the parabola $y=x^2$.

Set the two expressions for $y$ equal:

$$x^2 = x+2 \implies x^2-x-2=0$$

Factoring (numbers multiplying to $-2$, adding to $-1$: $-2$ and $1$):

$$(x-2)(x+1)=0 \implies x=2 \ \text{ or }\ x=-1$$

Substitute back into the line $y=x+2$ to get the matching $y$-values:

- $x=2$: $y=2+2=4$
- $x=-1$: $y=-1+2=1$

So the line and parabola intersect at $(2,4)$ and $(-1,1)$. (Check against the parabola: $2^2=4$ ✓, $(-1)^2=1$ ✓.) See [[Linear Functions]] for more on the line side of this.

## 11. Applications of Quadratic Functions

Quadratic models turn up whenever a quantity changes at a *constant rate of change of its rate of change* — the two most common examples at this level are:

- **Projectile motion:** height over time often follows $h(t)=-\frac12 g t^2+v_0t+h_0$, which is a quadratic in $t$. The turning point of this parabola gives the maximum height reached and the time at which it occurs, found exactly as in Sections 2–5 above.
- **Optimisation:** many "maximise the area" or "minimise the cost" problems reduce to a quadratic model, where the answer is simply the turning point of the parabola.

No problem of this type appeared in this particular set of lecture notes, so there's no specific worked example to transcribe here — but the method is identical to finding the turning point worked through above.

## 12. Homework Practice

**Question.** For $f(x)=x^2-3+3x$: (a) find the $x$-intercepts; (b) sketch the graph.

*(question text reconstructed from working — check original if this seems off)*

Rewrite in standard order: $f(x)=x^2+3x-3$, so $a=1,\ b=3,\ c=-3$.

**(a) x-intercepts.**

$$\Delta = 3^2-4(1)(-3)=9+12=21$$

Since $21$ is not a perfect square, the roots are irrational surds:

$$x=\frac{-3\pm\sqrt{21}}{2}$$

With $\sqrt{21}\approx4.583$: $x\approx0.79$ or $x\approx-3.79$.

**(b) Sketch.**

Turning point: $x=\dfrac{-b}{2a}=-\dfrac32=-1.5$,

$$f(-1.5)=(-1.5)^2+3(-1.5)-3=2.25-4.5-3=-5.25$$

So the turning point (minimum, since $a=1>0$) is $(-1.5,-5.25)$. The $y$-intercept is $f(0)=-3$.

**Graph description:** upward-opening parabola, $x$-intercepts at approximately $(-3.79,0)$ and $(0.79,0)$, $y$-intercept $(0,-3)$, minimum at $(-1.5,-5.25)$, axis of symmetry $x=-1.5$, domain $\mathbb{R}$, range $[-5.25,\infty)$.

For further mixed practice across all the Unit 1 function topics, see [[Functions - Practice and Revision]]. For the function families covered in the same source material, see [[Polynomial Division and the Factor Theorem]], [[Cubic Functions]], [[Reciprocal Functions]], and [[Square Root Function]].
