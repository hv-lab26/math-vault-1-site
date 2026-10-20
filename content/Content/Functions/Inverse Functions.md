# Inverse Functions

A function takes an input and produces an output. The **inverse** of a function, written $f^{-1}(x)$, reverses this process: it takes an output of $f$ and returns the input that produced it. In symbols, if $f(a) = b$, then $f^{-1}(b) = a$.

Informally, $f^{-1}$ "undoes" whatever $f$ does, in the *reverse order*. This is exactly why finding an inverse algebraically amounts to peeling back the operations in $f$ one at a time, from the outside in — the same idea used later in this note to solve equations by "undoing" them.

**Important notational warning:** $f^{-1}(x)$ does **not** mean $\dfrac{1}{f(x)}$. The "$-1$" here is an inverse-function label, not an exponent. $\big(f(x)\big)^{-1} = \dfrac{1}{f(x)}$ is a completely different object.

Not every function has an inverse that is itself a function — this is discussed below.

## Key Facts and Formulas

| Concept | Statement |
|---|---|
| Notation | $f^{-1}(x)$ is the inverse of $f$. **$f^{-1}(x) \neq \dfrac{1}{f(x)}$.** |
| Defining property | $f^{-1}(b) = a \iff f(a) = b$ |
| Existence condition | $f^{-1}$ is a function $\iff$ $f$ is **one-to-one** (passes the Horizontal Line Test) |
| Domain/range swap | $\operatorname{domain}(f^{-1}) = \operatorname{range}(f)$ and $\operatorname{range}(f^{-1}) = \operatorname{domain}(f)$ |
| Graphical relationship | The graph of $f^{-1}$ is the graph of $f$ reflected in the line $y = x$ |
| Composition property | $f\big(f^{-1}(x)\big) = x$ and $f^{-1}\big(f(x)\big) = x$ |
| Algebraic method | (1) Let $y = f(x)$. (2) Swap $x$ and $y$. (3) Solve for $y$. (4) Replace $y$ with $f^{-1}(x)$. |
| Intersections of $f$ and $f^{-1}$ | If $f$ is increasing, solve $f(x) = x$ directly — quicker than finding $f^{-1}$ first. |

## One-to-One Functions and the Horizontal Line Test

A function $f$ is **one-to-one** if every output value corresponds to exactly one input value — no two different $x$-values ever give the same $y$-value.

This matters because of what an inverse has to *do*: reverse the mapping. If $f$ sent two different inputs $x_1 \neq x_2$ to the same output $y_0$, then $f^{-1}$ would have to send $y_0$ back to both $x_1$ and $x_2$ — but a function can only output one value for a given input. So $f^{-1}$ would fail to be a function. One-to-one-ness of $f$ is exactly what guarantees $f^{-1}$ is a genuine function.

Graphically this is the **Horizontal Line Test**: if any horizontal line $y=k$ crosses the graph of $f$ more than once, $f$ is not one-to-one. (Compare the Vertical Line Test, which checks that $f$ itself is a function. Reflecting a graph in $y=x$ swaps the roles of horizontal and vertical lines — which is exactly why the Horizontal Line Test on $f$ corresponds to the Vertical Line Test on $f^{-1}$.)

**Example (testing one-to-one-ness by factorising).** *Show that $f(x) = 2x^3+8x^2+2x-12$ is not one-to-one over the real numbers.* *(question text reconstructed from working — check original if this seems off)*

Test a simple value first: $f(1) = 2(1)^3+8(1)^2+2(1)-12 = 2+8+2-12 = 0$, so $x=1$ is a root, meaning $(x-1)$ is a factor. Divide $f(x)$ by $(x-1)$:

- $2x^3 \div x = 2x^2$. Multiply: $2x^2(x-1) = 2x^3-2x^2$. Subtract from $2x^3+8x^2$: remainder $10x^2$; bring down $+2x$: $10x^2+2x$.
- $10x^2 \div x = 10x$. Multiply: $10x(x-1) = 10x^2-10x$. Subtract: remainder $12x$; bring down $-12$: $12x-12$.
- $12x \div x = 12$. Multiply: $12(x-1) = 12x-12$. Subtract: remainder $0$.

Quotient: $2x^2+10x+12$, remainder $0$, so $f(x) = (x-1)(2x^2+10x+12)$. The quadratic factor simplifies: $2x^2+10x+12 = 2(x^2+5x+6) = 2(x+2)(x+3)$. Fully factorised:

$$f(x) = 2(x-1)(x+2)(x+3)$$

This has **three distinct real roots**: $x=1,-2,-3$. Since the graph of $f$ crosses the $x$-axis (the horizontal line $y=0$) three separate times, $f$ fails the Horizontal Line Test and is **not one-to-one** over all of $\mathbb{R}$. An inverse function for $f$ only exists once the domain is restricted to a piece on which $f$ is monotonic throughout — the same idea used to restrict a parabola's domain in [[Quadratic Functions]].

Compare this with $(x+3)^3-4$ (met again below): it is just $x^3$ shifted left and down, and $x^3$ is strictly increasing everywhere, so $(x+3)^3-4$ is too — no turning points, so it stays one-to-one on all of $\mathbb{R}$ with no restriction needed. Not every cubic is automatically one-to-one; it depends on whether the graph has turning points, which [[Differentiation Rules]] gives a systematic test for later.

## Finding an Inverse Algebraically

The standard method is built directly on the "swap $x$ and $y$" idea — reflecting a point $(a,b)$ in the line $y=x$ produces the point $(b,a)$, so swapping the variables in the equation mirrors that reflection:

1. Write the function as $y = f(x)$.
2. **Swap** $x$ and $y$.
3. **Solve** the resulting equation for $y$.
4. Replace $y$ with $f^{-1}(x)$.

### Power Functions

**Example 1 (Q21).** *Find the inverse function of $f(x) = (x-3)^3$.*

$$
\begin{aligned}
y &= (x-3)^3\\
x &= (y-3)^3 &&\text{(swap $x,y$)}\\
\sqrt[3]{x} &= y-3 &&\text{(cube root both sides)}\\
y &= \sqrt[3]{x}+3
\end{aligned}
$$

So $f^{-1}(x) = \sqrt[3]{x}+3$. *Check:* $f(3)=0$, and $f^{-1}(0)=\sqrt[3]{0}+3=3$. ✓

**Example 2 (Q19).** *Find the inverse function of $g(x) = -(x-1)^3$.*

$$
\begin{aligned}
y &= -(x-1)^3\\
x &= -(y-1)^3 &&\text{(swap)}
\end{aligned}
$$

It helps here to move the sign inside the bracket instead of leaving it outside. Because the power is **odd**, $-a^3 = (-a)^3$ for any $a$, so $-(y-1)^3 = \big(-(y-1)\big)^3 = (1-y)^3$:

$$
\begin{aligned}
x &= (1-y)^3\\
\sqrt[3]{x} &= 1-y\\
y &= 1-\sqrt[3]{x}
\end{aligned}
$$

So $g^{-1}(x) = 1-\sqrt[3]{x}$. *Check:* $g(0) = -(-1)^3 = 1$, and $g^{-1}(1) = 1-\sqrt[3]{1} = 0$. ✓

**Example 3 (Q11).** *Find the inverse function of $f(x) = (x-2)^5+3$.*

$$
\begin{aligned}
x &= (y-2)^5+3\\
x-3 &= (y-2)^5\\
\sqrt[5]{x-3} &= y-2\\
y &= \sqrt[5]{x-3}+2
\end{aligned}
$$

So $f^{-1}(x) = \sqrt[5]{x-3}+2$. *Check:* $f(2)=3$, and $f^{-1}(3)=\sqrt[5]{0}+2=2$. ✓

**Example 4 (Q31).** *Find the inverse function of $g(x) = x^3-1$.*

$$
\begin{aligned}
x &= y^3-1\\
x+1 &= y^3\\
y &= \sqrt[3]{x+1}
\end{aligned}
$$

So $g^{-1}(x) = \sqrt[3]{x+1}$. *Check:* $g(0)=-1$, and $g^{-1}(-1)=\sqrt[3]{0}=0$. ✓

### Radical (Root) Functions

All three examples below use an **odd**-index root ($\sqrt[3]{\ }$ or $\sqrt[5]{\ }$). Odd roots, unlike square roots, are defined for negative radicands too, so none of these functions need a domain restriction — each is one-to-one (in fact strictly monotonic) over all of $\mathbb{R}$.

**Example 5 (Q12).** *Find the inverse function of $g(x) = \sqrt[3]{x+1}+2$.*

$$
\begin{aligned}
x &= \sqrt[3]{y+1}+2\\
x-2 &= \sqrt[3]{y+1}\\
(x-2)^3 &= y+1\\
y &= (x-2)^3-1
\end{aligned}
$$

So $g^{-1}(x) = (x-2)^3-1$. *Check:* $g(0)=\sqrt[3]{1}+2=3$, and $g^{-1}(3)=1^3-1=0$. ✓

**Example 6 (Q22).** *Find the inverse function of $g(x) = \sqrt[5]{\dfrac{2-x}{2}}$.*

$$
\begin{aligned}
x &= \sqrt[5]{\dfrac{2-y}{2}}\\
x^5 &= \dfrac{2-y}{2} &&\text{(raise both sides to the 5th power)}\\
2x^5 &= 2-y\\
y &= 2-2x^5
\end{aligned}
$$

So $g^{-1}(x) = 2-2x^5$. *Check:* $g(0)=\sqrt[5]{1}=1$, and $g^{-1}(1)=2-2(1)=0$. ✓

**Example 7 (Q33).** *Find the inverse function of $h(x) = \dfrac{4-\sqrt[3]{4x}}{2}$.*

$$
\begin{aligned}
x &= \dfrac{4-\sqrt[3]{4y}}{2}\\
2x &= 4-\sqrt[3]{4y}\\
\sqrt[3]{4y} &= 4-2x\\
4y &= (4-2x)^3\\
y &= \dfrac{(4-2x)^3}{4}
\end{aligned}
$$

So $h^{-1}(x) = \dfrac{(4-2x)^3}{4}$. *Check:* $h(0)=\dfrac{4-0}{2}=2$, and $h^{-1}(2)=\dfrac{(4-4)^3}{4}=0$. ✓

### Linear Functions

**Example 8 (Q29).** *Find the inverse function of $g(x) = -5x+1$.*

$$
\begin{aligned}
y &= -5x+1\\
x &= -5y+1 &&\text{(swap)}\\
x-1 &= -5y\\
y &= \dfrac{1-x}{5}
\end{aligned}
$$

So $g^{-1}(x) = \dfrac{1-x}{5}$. *Check:* $g(2)=-10+1=-9$, and $g^{-1}(-9)=\dfrac{1-(-9)}{5}=\dfrac{10}{5}=2$. ✓

### Rational Functions

For a rational function $\dfrac{ax+b}{cx+d}$, the domain excludes the $x$-value that makes the denominator zero, and (because of the horizontal asymptote) the range excludes $y=\dfrac{a}{c}$. Finding the inverse swaps these two restrictions — a useful consistency check, used below.

**Example 9 (Q13).** *Find the inverse function of $g(x) = \dfrac{4}{x+2}$.*

$$
\begin{aligned}
x &= \dfrac{4}{y+2}\\
\dfrac{4}{x} &= y+2\\
y &= \dfrac{4}{x}-2
\end{aligned}
$$

So $g^{-1}(x) = \dfrac{4}{x}-2$. *Check:* $g(0)=\dfrac{4}{2}=2$, and $g^{-1}(2)=\dfrac{4}{2}-2=0$. ✓ Domain of $g$ is $x\neq-2$ with range $y\neq0$; domain of $g^{-1}$ is $x\neq0$ with range $y\neq-2$ — exactly swapped, as expected.

**Example 10 (Q27).** *Find the inverse function of $g(x) = \dfrac{8-5x}{4}$.*

$$
\begin{aligned}
x &= \dfrac{8-5y}{4}\\
4x &= 8-5y\\
y &= \dfrac{8-4x}{5}
\end{aligned}
$$

So $g^{-1}(x) = \dfrac{8-4x}{5}$. *Check:* $g(0)=\dfrac{8}{4}=2$, and $g^{-1}(2)=\dfrac{8-8}{5}=0$. ✓

**Example 11 (Q15).** *Find the inverse function of $f(x) = \dfrac{-2x-2}{x+2}$.*

$$
\begin{aligned}
x &= \dfrac{-2y-2}{y+2}\\
x(y+2) &= -2(y+1)\\
xy+2x &= -2y-2\\
xy+2y &= -2x-2\\
y(x+2) &= -2x-2\\
y &= \dfrac{-2x-2}{x+2}
\end{aligned}
$$

So $f^{-1}(x) = \dfrac{-2x-2}{x+2} = f(x)$ — this function is its own inverse (an *involution*). *Check:* $f(0)=\dfrac{-2}{2}=-1$, and $f^{-1}(-1)=\dfrac{2-2}{1}=0$. ✓ Graphically this means the graph of $f$ is symmetric about the line $y=x$; it also fits the asymptotes — vertical asymptote $x=-2$ and horizontal asymptote $y=-2$ sit symmetrically about $y=x$.

**Example 12 (Q37).** *Find the inverse function of $f(x) = \dfrac{7-3x}{x-2}$.*

$$
\begin{aligned}
x &= \dfrac{7-3y}{y-2}\\
x(y-2) &= 7-3y\\
xy-2x &= 7-3y\\
xy+3y &= 2x+7\\
y(x+3) &= 2x+7\\
y &= \dfrac{2x+7}{x+3}
\end{aligned}
$$

So $f^{-1}(x) = \dfrac{2x+7}{x+3}$. *Check:* $f(0)=\dfrac{7}{-2}=-3.5$, and $f^{-1}(-3.5)=\dfrac{-7+7}{-0.5}=0$. ✓ $f$ has vertical asymptote $x=2$ and horizontal asymptote $y=-3$; $f^{-1}$ has vertical asymptote $x=-3$ and horizontal asymptote $y=2$ — again exactly swapped.

## Solving Equations Using Inverse Operations

Finding an inverse function and solving an equation for $x$ use the same underlying skill: both "undo" a chain of operations in reverse order.

**Example 13.** *Solve $(x+3)^3-4=0$ for $x$.* *(question text reconstructed from working — check original if this seems off)*

$$
\begin{aligned}
(x+3)^3-4 &= 0\\
(x+3)^3 &= 4\\
x+3 &= \sqrt[3]{4}\\
x &= \sqrt[3]{4}-3 \approx 1.5874-3 \approx -1.4125
\end{aligned}
$$

Multiplied out, the same equation is a cubic in standard form: since $(x+3)^3=x^3+9x^2+27x+27$, $(x+3)^3-4=0$ becomes $x^3+9x^2+27x+23=0$. As noted above, $(x+3)^3-4$ is just $x^3$ shifted, so it's strictly increasing — this cubic has exactly the one real root found above, unlike the three-root example earlier in this note.

**Example 14.** *Determine whether $f(d)=0.25(d-4)^2+6$ can equal $0$ — that is, whether $0$ is in the range of $f$.* *(question text reconstructed from working — check original if this seems off)*

$$
\begin{aligned}
0.25(d-4)^2+6 &= 0\\
0.25(d-4)^2 &= -6\\
(d-4)^2 &= \dfrac{-6}{0.25} = -24
\end{aligned}
$$

This already signals a problem: a squared real number can never be negative — $(\text{anything})^2 \ge 0$ always (for instance $(d+4)^2\ge0$ for every real $d$, and the same holds for $(d-4)^2$). Writing it as a standard quadratic confirms this:

$$
\begin{aligned}
(d-4)^2 &= -24\\
d^2-8d+16 &= -24\\
d^2-8d+16+\dfrac{6}{0.25} &= 0\\
d^2-8d+40 &= 0
\end{aligned}
$$

Discriminant: $\Delta=(-8)^2-4(1)(40)=64-160=-96<0$. No real solutions. So $f(d)=0$ has **no real solution**: $0$ is not in the range of $f$. This connects directly to inverses — since $\operatorname{domain}(f^{-1})=\operatorname{range}(f)$, it means $f^{-1}(0)$ would not be defined.

## Verifying an Inverse by Composition

The defining property $f\big(f^{-1}(x)\big)=x$ and $f^{-1}\big(f(x)\big)=x$ gives a reliable way to check an inverse is correct. Using Example 1 ($f(x)=(x-3)^3$, $f^{-1}(x)=\sqrt[3]{x}+3$):

$$f\big(f^{-1}(x)\big) = \Big(\big(\sqrt[3]{x}+3\big)-3\Big)^3 = \big(\sqrt[3]{x}\big)^3 = x \quad\checkmark$$

$$f^{-1}\big(f(x)\big) = \sqrt[3]{(x-3)^3}+3 = (x-3)+3 = x \quad\checkmark$$

The second line works cleanly because **cube roots undo cubes exactly**, for every real number — no sign ambiguity to worry about, unlike an even root (e.g. $\sqrt{x^2}=|x|$, not simply $x$, unless $x\ge0$ is already known).

## The Graph of $f$ and $f^{-1}$: Reflection in $y=x$

The source includes a hand-drawn diagram rather than a typed example; it is described here instead of embedded.

- Axes drawn with the usual $x$–$y$ orientation.
- The curve $f$ (blue) is a square-root shape, matching the labelled function $f(x)=\sqrt{x-2}+3$. Its domain is $x\ge2$ (need $x-2\ge0$) and its range is $y\ge3$; it starts at a point and rises, flattening out, as $x$ grows.
- The point $A=(2,3)$ is marked on $f$ — the starting point ("corner") of the square-root curve.
- A dashed green line marked $y=x$ runs diagonally through the origin at $45°$.
- The curve $f^{-1}$ (red) is the mirror image of $f$ in this dashed line: it starts at the point $A'=(3,2)$ and opens the other way, matching a sideways-parabola shape (as expected when inverting a square-root function).
- Three boxed methods are listed for finding where $f$ and $f^{-1}$ intersect:
  - **Method 1:** solve $f(x) = f^{-1}(x)$
  - **Method 2:** solve $f^{-1}(x) = x$
  - **Method 3 (circled — the preferred method):** solve $f(x) = x$

**Why Method 3 works:** $f^{-1}$'s graph is $f$'s graph reflected in $y=x$. If $f$ is increasing (one-to-one), the only points where a curve and its own mirror image can meet are points that are their own reflection — that is, points sitting exactly on the line $y=x$. So solving $f(x)=x$ finds every intersection directly, without ever computing $f^{-1}$ (Methods 1 and 2 both need $f^{-1}$ found first — extra, avoidable work).

*Caveat:* this shortcut relies on $f$ being monotonic increasing. For a decreasing function, $f$ and $f^{-1}$ can meet at pairs of points that are reflections of each other but are not themselves on $y=x$, so Method 3 alone would miss those.

**Applying Method 3 to this exact function, as an illustration:**

$$
\begin{aligned}
\sqrt{x-2}+3 &= x\\
\sqrt{x-2} &= x-3
\end{aligned}
$$

This requires $x-3\ge0$, i.e. $x\ge3$ (consistent with the range of $f$, since any intersection point has $y=x\ge3$). Squaring both sides:

$$
\begin{aligned}
x-2 &= (x-3)^2 = x^2-6x+9\\
0 &= x^2-7x+11\\
x &= \dfrac{7\pm\sqrt{49-44}}{2} = \dfrac{7\pm\sqrt5}{2}
\end{aligned}
$$

This gives $x\approx4.618$ or $x\approx2.382$. Only $x\approx4.618$ satisfies $x\ge3$; the other is rejected as **extraneous** (introduced by the squaring step). *Check:* $f(4.618)=\sqrt{2.618}+3\approx1.618+3=4.618$. ✓ So $f$ and $f^{-1}$ meet at exactly one point, $x=\dfrac{7+\sqrt5}{2}$.

For reference, $f^{-1}$ itself (not worked on the source page, but found the same way as the earlier examples):

$$
\begin{aligned}
x &= \sqrt{y-2}+3\\
x-3 &= \sqrt{y-2}\\
(x-3)^2 &= y-2\\
y &= (x-3)^2+2, \qquad x\ge3
\end{aligned}
$$

*Check:* $f^{-1}(3)=(0)^2+2=2$, matching $A'=(3,2)$. ✓

---

For the exponential/logarithm pair of inverse functions — one of the most important inverse relationships in this course — see [[Logarithmic Functions]]. For more practice applying the swap-and-solve method, see [[Functions - Practice and Revision]].
