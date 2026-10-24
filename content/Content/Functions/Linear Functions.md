# Linear Functions

A linear function is a function whose graph is a straight line in the $xy$-plane. It is called "linear" because its rate of change is constant: every time $x$ increases by $1$, $y$ changes by the same fixed amount, no matter where on the graph you look. That constant rate of change is the **gradient** (slope), and the point where the line crosses the $y$-axis is its **$y$-intercept**.

## Key Formulas

| Concept | Formula | Notes |
|---|---|---|
| Slope-intercept form | $y = ax + b$ | $a$ = gradient (slope), $b$ = $y$-intercept |
| Gradient between two points | $m = \dfrac{y_B - y_A}{x_B - x_A}$ | "rise over run" |
| Point–gradient form | $y - y_A = m(x - x_A)$ | line through $(x_A,y_A)$ with gradient $m$ |
| $x$-intercept | set $y=0$, solve for $x$ | where the line crosses the $x$-axis |
| $y$-intercept | set $x=0$, solve for $y$ | equals $b$ in $y=ax+b$ |
| Horizontal line | $y=k$ | gradient $0$ |
| Vertical line | $x=k$ | gradient undefined; **not a function** |

## The General Form $y = ax + b$

Every non-vertical straight line can be written as

$$y = ax + b$$

where $a$ is the **gradient** (how steep the line is, and whether it rises or falls left-to-right) and $b$ is the **$y$-intercept** (the value of $y$ when $x=0$). A straight line is completely pinned down by these two numbers, so finding "the equation of a line" always comes down to finding $a$ and $b$.

**Example 1.** If $a=2$ and $b=-1$, write the equation of the line.

$$y = ax+b = 2x+(-1)$$
$$y = 2x-1$$

Here both parameters are already known, so they're substituted directly into the general form.

## Finding a Linear Equation From Given Information

Usually you are *not* handed both $a$ and $b$ directly — instead you're given just enough other information (one parameter plus a point, or two points) to work them out. Since $y=ax+b$ has exactly two unknowns, every point you substitute into it produces one equation relating $a$ and $b$; two independent equations (from two distinct points, or one point plus a known gradient/intercept) can always be solved simultaneously for a unique pair $(a,b)$.

**Example 2.** The gradient of a line is $a=-\dfrac12$, and the line passes through $(1,3)$. Find its equation.

Substitute the point into $y=ax+b$:

$$3 = -\frac12(1)+b$$
$$3 = -\frac12+b \iff b = 3+\frac12 = \frac72$$

$$\Rightarrow\ y = -\frac12 x+\frac72$$

**Example 3.** The $y$-intercept of a line is $b=2$, and it passes through $(-1,0)$. Find its equation.

$$y = ax+2$$

Substitute $(-1,0)$:

$$0 = a(-1)+2 \iff a=2$$

$$\Rightarrow\ y = 2x+2$$

*Check:* at $x=-1$, $y=2(-1)+2=0$ ✓.

**Example 4.** A line passes through $A=(1,3)$ and $B=(-3,2)$. Find its equation.

Since neither $a$ nor $b$ is known here, substitute **both** points into $y=ax+b$ to get a pair of simultaneous equations:

$$
\begin{cases}3 = a+b\\ 2 = -3a+b\end{cases}
$$

Subtracting the second equation from the first eliminates $b$:

$$3-2 = (a+b)-(-3a+b) = 4a \implies 1=4a \implies a=\frac14$$

Then $b = 3-a = 3-\dfrac14=\dfrac{11}{4}$.

$$\Rightarrow\ y=\frac14x+\frac{11}{4}$$

*Check:* at $x=1$, $y=\frac14+\frac{11}{4}=\frac{12}{4}=3$ ✓ (matches $A$). At $x=-3$, $y=-\frac34+\frac{11}{4}=\frac84=2$ ✓ (matches $B$).

## Gradient Between Two Points

There's a second, often quicker route to Example 4: compute the gradient directly, then use the point–gradient form.

$$m = \frac{y_B-y_A}{x_B-x_A}, \qquad y-y_A = m(x-x_A)$$

The gradient formula is just "rise over run": $y_B-y_A$ is how much $y$ changes between the two points, and $x_B-x_A$ is how much $x$ changes between them; their ratio is the constant rate of change that defines the line — and that ratio comes out the same no matter *which* two points on the line you pick, which is exactly what makes a line "straight". Applying it to Example 4:

$$m = \frac{2-3}{-3-1} = \frac{-1}{-4} = \frac14$$

(matches $a=\tfrac14$ found above, as it must). Using point $A=(1,3)$:

$$y-3 = \frac14(x-1) \implies y = \frac14x-\frac14+3 = \frac14x+\frac{11}{4}$$

— the identical equation, confirming both methods agree.

## Sketching a Linear Graph Using Intercepts

To sketch $y=ax+b$, the two easiest points to plot are usually the **intercepts**, since each only needs substituting $0$ for one variable:

- **$y$-intercept:** set $x=0$ → $y=b$.
- **$x$-intercept:** set $y=0$ → $0=ax+b \Rightarrow x=-b/a$ (provided $a\mathrel{\char"2260}0$).

Because two points are enough to draw a unique straight line, plotting these two and joining them with a ruler gives the whole graph.

**Example.** Sketch $y=2x-3$.

| $x$ | $0$ | $1.5$ |
|---|---|---|
| $y$ | $-3$ | $0$ |
| point | $A$ | $B$ |

So $A(0,-3)$ (the $y$-intercept) and $B(1.5,0)$ (the $x$-intercept).

*Graph description:* a straight line of gradient $2$ (positive, so it rises left-to-right), crossing the $y$-axis at $(0,-3)$ and the $x$-axis at $(1.5,0)$. For $x<0$ the line sits below both axes (third quadrant); for $x>1.5$ it rises into the first quadrant. Being a straight line, it has no turning points, no asymptotes, and no symmetry — it is unbounded and strictly increasing.

## Horizontal and Vertical Lines

Two special cases don't fit neatly into "plot two intercepts":

- **$y=3$** (a horizontal line): every $x$-value gives the same output, $3$. Gradient $=0$ (no rise, for any run). It's a horizontal line through $(0,3)$ with no $x$-intercept at all (it never reaches $y=0$).
- **$x=-2$** (a vertical line): every point on it has $x=-2$, for *any* value of $y$. The gradient is undefined (the "run" $x_B-x_A$ is always $0$, and nothing can be divided by $0$). A vertical line is **not the graph of a function**: the single input $x=-2$ is paired with infinitely many outputs, which immediately fails the vertical line test — see [[Function Notation, Domain and Range]].

## Exercise 1D — Sketching From Intercepts

**Q1(a).** *(The original typed equation for this part isn't legible in the source — only the intercept table and sketch remain. Reconstructed from the working: based on the intercepts $A(6,0)$ and $B(0,4)$ shown, the equation is taken to be $2x+3y=12$ — check the original if this seems off.)*

$$2x+3y=12$$

| $x$ | $0$ | $6$ |
|---|---|---|
| $y$ | $4$ | $0$ |

$A(6,0)$, $B(0,4)$.

*Graph description:* rearranging gives $y=-\dfrac23x+4$, so the gradient is $-\dfrac23$ (negative — the line falls left-to-right). It crosses the $y$-axis at $(0,4)$ and the $x$-axis at $(6,0)$, running from the second quadrant down through the first quadrant and into the fourth quadrant as $x$ increases past $6$.

**Q1(b).** $x-4y=8$

| $x$ | $0$ | $8$ |
|---|---|---|
| $y$ | $-2$ | $0$ |

$A(0,-2)$, $B(8,0)$.

*Check:* $0-4(-2)=8$ ✓; $8-4(0)=8$ ✓.

*Graph description:* rearranging gives $y=\dfrac14x-2$, gradient $\dfrac14$ (positive — rises left-to-right, quite shallow). It crosses the $y$-axis at $(0,-2)$ and the $x$-axis at $(8,0)$, lying in the third quadrant for $x<0$ and rising into the first quadrant for $x>8$.

---

For further practice, see [[Functions - Practice and Revision]].
