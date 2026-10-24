# Limits

A limit describes the value that a function $f(x)$ gets closer and closer to as the input $x$ gets closer and closer to some fixed value $a$. Crucially, this says nothing about what happens *at* $x=a$ itself — $f$ might not even be defined there. A limit is purely about the *approach*, not the destination. This distinction seems pedantic at first, but it turns out to be exactly what's needed to make sense of two separate problems: evaluating expressions that look undefined (like $\frac{0}{0}$) by studying the function's behaviour *near* a point rather than *at* it, and defining the gradient of a curve at a single point — which is where the derivative, the central object of [[Differentiation Rules]] and [[Applications of Differentiation]], comes from.

## Key Formulas

| Concept | Formula / Statement |
|---|---|
| Limit notation | $\lim_{x \to a} f(x) = L$ — as $x$ approaches $a$, $f(x)$ approaches $L$ |
| One-sided limits | $\lim_{x \to a^-} f(x)$ (from the left), $\lim_{x \to a^+} f(x)$ (from the right) |
| Limit exists | $\lim_{x\to a} f(x)$ exists $\iff$ $\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)$ |
| Direct substitution | If $f$ is continuous at $x=a$, then $\lim_{x \to a} f(x) = f(a)$ |
| Sum/Difference Law | $\lim_{x \to a}[f(x) \pm g(x)] = \lim_{x \to a} f(x) \pm \lim_{x \to a} g(x)$ |
| Constant Multiple Law | $\lim_{x \to a}[k f(x)] = k \lim_{x \to a} f(x)$ |
| Product Law | $\lim_{x \to a}[f(x)g(x)] = \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x)$ |
| Quotient Law | $\lim_{x \to a}\dfrac{f(x)}{g(x)} = \dfrac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)}$, provided $\lim_{x \to a} g(x) \mathrel{\char"2260} 0$ |
| Indeterminate form $\frac{0}{0}$ | Factorise numerator/denominator, cancel the common factor, *then* substitute |
| Continuity at $x = a$ | $f(a)$ is defined, $\lim_{x \to a} f(x)$ exists, and $\lim_{x \to a} f(x) = f(a)$ |
| Limits at infinity | Divide every term by the highest power of $x$ present; use $\dfrac{1}{x^n} \to 0$ as $x \to \infty$ |
| Average rate of change over $[x, x+h]$ | $\dfrac{f(x+h)-f(x)}{h}$ — the gradient of the chord (secant) |
| Instantaneous rate of change at $x$ | $f'(x) = \displaystyle\lim_{h \to 0}\dfrac{f(x+h)-f(x)}{h}$ — the gradient of the tangent |
| Notation for the derivative | $f'(x)$, or $\dfrac{dy}{dx}$ when $y = f(x)$ |

## The Idea of a Limit

The limit of a function $f(x)$ is the value that $f(x)$ approaches as $x$ approaches a given value — whether or not $x$ actually reaches that value, and whether or not $f$ is even defined there. For example, the limit of $f(x) = 3x+1$ (a straight line, see [[Linear Functions]]) as $x$ approaches $1$ is written

$$\lim_{x \to 1} (3x+1)$$

and read as "the limit of $3x+1$ as $x$ tends to $1$."

*Diagram from the source notes: the line $f(x)=3x+1$ is sketched on a set of axes, with $y$-intercept marked at $1$ (matching $f(0)=1$). A pair of dashed guide-lines run up from $x=1$ on the horizontal axis and across from $f(x)=4$ on the vertical axis, meeting exactly on the line. An arrow labelled "continuous" points at the line at that meeting point.*

The point of the diagram is this: because the line has no breaks, jumps or holes anywhere, the graph passes smoothly through the point above $x=1$. So as $x$ gets closer and closer to $1$ from either side, $f(x)$ gets closer and closer to $f(1) = 3(1)+1 = 4$ — and in fact *reaches* exactly $4$, since $f$ is defined and well-behaved there. That is,

$$\lim_{x \to 1}(3x+1) = 4 = f(1).$$

This is the simplest possible case: whenever a function is "unbroken" at the point in question, the limit is just the function value, and finding it is a matter of direct substitution. The next section makes this idea — continuity — precise, because it is the condition that decides when direct substitution is actually allowed.

## Continuity and Discontinuity

A function $f$ is **continuous** at $x = a$ if all three of the following hold:

1. $f(a)$ is defined (the function actually has a value there),
2. $\lim_{x \to a} f(x)$ exists (the function approaches a single, settled value from both sides),
3. $\lim_{x \to a} f(x) = f(a)$ (the value it approaches is the same as the value it actually takes).

If a function is continuous at every point of its domain, it is simply called continuous — this is the case for every polynomial (like the line $f(x)=3x+1$ above), and for every rational function at any point where its denominator isn't zero. If any one of the three conditions fails, $f$ is **discontinuous** at $x=a$. There are a few standard ways this can happen:

**Jump discontinuity** — the function approaches *different* values from the left and from the right, so condition 2 fails. This is where one-sided limits matter: the left-hand limit $\lim_{x \to a^-} f(x)$ looks only at values of $x$ below $a$, and the right-hand limit $\lim_{x \to a^+} f(x)$ only at values above $a$. The two-sided limit $\lim_{x\to a} f(x)$ only exists when these two agree. For example, consider $f(x) = \dfrac{\lvert x \rvert}{x}$ near $x=0$:

| As $x \to$ | $0^-$ (from the left) | $0^+$ (from the right) |
|---|---|---|
| $\lvert x \rvert$ | $-x$ | $x$ |
| $f(x) = \dfrac{\lvert x \rvert}{x}$ | $\dfrac{-x}{x} = -1$ | $\dfrac{x}{x} = 1$ |

Since the left-hand limit ($-1$) and right-hand limit ($1$) disagree, $\lim_{x \to 0} \dfrac{\lvert x \rvert}{x}$ does not exist, even though the function is perfectly well-defined on either side of $0$.

**Infinite discontinuity** — the function grows without bound near $x=a$, so again the limit fails to exist as a real number. For example, $f(x) = \dfrac1x$ near $x = 0$:

| As $x \to$ | $0^-$ | $0^+$ |
|---|---|---|
| $f(x) = \dfrac1x$ | $\to -\infty$ | $\to +\infty$ |

This kind of behaviour — shooting off to $\pm\infty$ near a point — is exactly what produces a *vertical asymptote* on a graph, the same feature that shows up at the excluded value of $x$ in the graphs covered in [[Logarithmic Functions]].

**Removable discontinuity** — the limit *does* exist, but either $f(a)$ is undefined or doesn't match the limit, so only condition 1 or 3 fails. This is the most important type for this course, because it's exactly what shows up in the indeterminate-form examples below — see Worked Example 3.

## Limit Laws

Evaluating limits algebraically relies on a handful of laws, each saying that limits respect the basic operations of arithmetic, provided the individual limits involved actually exist:

$$\lim_{x \to a}[f(x) \pm g(x)] = \lim_{x \to a} f(x) \pm \lim_{x \to a} g(x) \qquad \text{(sum/difference law)}$$

$$\lim_{x \to a}[k\,f(x)] = k\lim_{x \to a} f(x) \qquad \text{(constant multiple law)}$$

$$\lim_{x \to a}[f(x)g(x)] = \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x) \qquad \text{(product law)}$$

$$\lim_{x \to a}\frac{f(x)}{g(x)} = \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)}, \quad \text{provided } \lim_{x \to a} g(x) \mathrel{\char"2260} 0 \qquad \text{(quotient law)}$$

Why does this justify just "plugging in" a value, as in the worked examples below? Every polynomial is built from the identity function $x$ and constants, combined only by addition and multiplication. Two facts are intuitively obvious on their own: $\lim_{x \to a} k = k$ for any constant $k$ (a constant function never changes, so it trivially "approaches" its own value everywhere), and $\lim_{x \to a} x = a$ (the identity function approaches exactly whatever value $x$ is heading towards). Applying the sum, constant-multiple and product laws repeatedly to these two building blocks shows that for *any* polynomial $p(x)$,

$$\lim_{x \to a} p(x) = p(a).$$

The quotient law then extends this result to rational functions $\dfrac{p(x)}{q(x)}$ — but only at values of $a$ where $q(a) \mathrel{\char"2260} 0$, since the law explicitly requires the denominator's limit to be nonzero. This is precisely why direct substitution works in Worked Examples 1 and 2 below, and precisely why it breaks down in Worked Example 3.

## Evaluating Limits by Direct Substitution

When $f$ is continuous at $x=a$ (true of every polynomial, and of every rational function wherever the denominator isn't zero), evaluating $\lim_{x \to a} f(x)$ is simply a matter of substituting $x=a$ into the expression and simplifying.

### Worked Example 1

**Question:** Evaluate $\displaystyle\lim_{x \to 5}(x^2 - 3x)$.

**Solution:** $f(x) = x^2-3x$ is a polynomial, so it's continuous for every real $x$ — its graph has no gaps, jumps or holes anywhere. This means the limit can be found by direct substitution of $x=5$:

$$\lim_{x \to 5}(x^2-3x) = (5)^2 - 3(5) = 25 - 15 = 10$$

So the limit is $\mathbf{10}$.

### Worked Example 2

**Question:** Evaluate $\displaystyle\lim_{x \to 0}\dfrac{x^2+5x+6}{x+3}$.

*(The exact approach value is faint in the original handwritten working, but it must be $x \to 0$: this is the only reading consistent with the displayed arithmetic $\frac{6}{3}=2$, since substituting $x=0$ gives $\frac{0^2+5(0)+6}{0+3}=\frac{6}{3}$.)*

**Solution:** $f(x) = \dfrac{x^2+5x+6}{x+3}$ is a rational function, continuous everywhere except where its denominator is zero, i.e. everywhere except $x=-3$. Since $0 \mathrel{\char"2260} -3$, $f$ is continuous at $x=0$, so direct substitution applies:

$$\lim_{x \to 0}\frac{x^2+5x+6}{x+3} = \frac{(0)^2+5(0)+6}{0+3} = \frac{6}{3} = 2$$

So the limit is $\mathbf{2}$. Notice that no factoring was needed — direct substitution is always the *first* thing to try, and the only reason it ever fails is if it produces an undefined expression (almost always $\frac{0}{0}$).

## Limits Involving Indeterminate Forms

Sometimes direct substitution produces the meaningless expression $\frac{0}{0}$. This is called an **indeterminate form**: it carries no information about the actual limit by itself (a fraction heading towards $\frac{0}{0}$ could settle on any value at all, depending on *how fast* the numerator and denominator each shrink to zero). Getting $\frac{0}{0}$ does **not** mean the limit is zero, undefined, or nonexistent — it means direct substitution has failed, and a different technique is required: factorise, cancel, then substitute again.

### Worked Example 3

**Question:** Evaluate $\displaystyle\lim_{x \to -3}\dfrac{x^2+5x+6}{x+3}$.

**Solution:** Try direct substitution first, exactly as in Example 2:

$$\frac{(-3)^2+5(-3)+6}{-3+3} = \frac{9-15+6}{0} = \frac{0}{0}$$

This is indeterminate, so substitution alone doesn't work. Since the numerator is *also* zero at $x=-3$, $(x+3)$ must be a common factor of both. Factorising the numerator (looking for two numbers that multiply to $6$ and add to $5$: namely $2$ and $3$):

$$x^2+5x+6 = (x+2)(x+3)$$

(Check: $(x+2)(x+3) = x^2+3x+2x+6 = x^2+5x+6$ ✓.) So

$$\lim_{x \to -3}\frac{x^2+5x+6}{x+3} = \lim_{x \to -3}\frac{(x+2)(x+3)}{x+3}$$

A limit as $x \to -3$ only ever considers values of $x$ *near* $-3$, never $x=-3$ itself — so throughout this whole process $x+3 \mathrel{\char"2260} 0$, and it is completely legitimate to cancel it:

$$= \lim_{x \to -3}(x+2)$$

This is now just a polynomial, so direct substitution finishes the job:

$$= -3+2 = -1$$

So the limit is $\mathbf{-1}$.

It's worth noticing what this says about the function $f(x) = \dfrac{x^2+5x+6}{x+3}$ itself, as distinct from its limit. $f(-3)$ is undefined — $x=-3$ is excluded from the domain of $f$ (see [[Function Notation, Domain and Range]]) precisely because it makes the denominator zero. Yet the *limit* as $x \to -3$ exists and equals $-1$. Graphically, $f$ is identical to the line $y=x+2$ everywhere *except* that it has a single point missing at $(-3,-1)$ — an open circle, or "hole", in an otherwise straight-line graph. This is the **removable discontinuity** introduced above: condition 1 of continuity (that $f(a)$ be defined) fails, even though condition 2 (the limit exists) holds perfectly well.

## Limits at Infinity

A different flavour of limit asks what happens to $f(x)$ as $x$ grows without bound, written $x \to \infty$ (or $x \to -\infty$). To evaluate this kind of limit for a rational function, divide every term in the numerator and denominator by the highest power of $x$ appearing in the denominator. This works because for any $n>0$, $\dfrac{1}{x^n} \to 0$ as $x \to \infty$ — a fixed number divided by an ever-growing quantity shrinks towards zero. Rewriting the expression this way turns every troublesome term into something tending to $0$, leaving behind just the ratio of leading coefficients.

**Example:** $\displaystyle\lim_{x \to \infty}\frac{3x+1}{x}$. Dividing every term by $x$:

$$\lim_{x \to \infty}\frac{3x+1}{x} = \lim_{x \to \infty}\left(3 + \frac1x\right) = 3+0 = 3$$

**Example:** $\displaystyle\lim_{x \to \infty}\frac{2x^2+1}{x^2-5}$. Dividing every term by $x^2$ (the highest power present):

$$\lim_{x \to \infty}\frac{2x^2+1}{x^2-5} = \lim_{x \to \infty}\frac{2+\dfrac{1}{x^2}}{1-\dfrac{5}{x^2}} = \frac{2+0}{1-0} = 2$$

When a limit like this settles on a finite value $L$ as $x \to \pm\infty$, it means the graph of the function flattens out towards the horizontal line $y=L$ far to the left or right — a **horizontal asymptote**.

## From Secant to Tangent: The Derivative as a Limit

This is the key idea that limits exist to support in this course: using a limit to define the gradient of a curve *at a single point*.

For a straight line, "the gradient" is unambiguous — it's the same everywhere along the line. For a curve, it isn't: the steepness visibly changes from point to point, so "the gradient of the curve" only makes sense once you fix a *particular* point and ask for the gradient of the curve *there*. The gradient of a curve at a point $P$ is defined to be the gradient of the **tangent** to the curve at $P$ — the straight line that just grazes the curve at that one point, matching its direction exactly.

The difficulty is that computing the gradient of a line needs *two* points (rise over run), and a tangent only touches the curve at *one*. The way around this is to start with two points, compute the gradient of the straight line (**chord**, or **secant**) through them, and then study what happens as the second point slides towards the first.

### Worked Example 4

**Question:** Find the gradient of the chord $PQ$ drawn to the curve $f(x) = x^2+2$ — a basic parabola (see [[Quadratic Functions]]), shifted up by $2$ units — where $P = [1, f(1)]$ and $Q = [1+h, f(1+h)]$.

*Diagram from the source notes: the parabola $f(x) = x^2+2$ is sketched. The point $P = [1, f(1)]$ is marked on the curve, and a second point $Q = [1+h, f(1+h)]$ is marked further along the curve, up and to the right of $P$. A straight chord is drawn connecting $P$ to $Q$, cutting across the curve between them.*

**Solution:** The gradient of a chord is rise over run, i.e. $\Delta y / \Delta x$:

$$\text{Gradient} = \frac{\text{rise}}{\text{run}} = \frac{\Delta y}{\Delta x} = \frac{f(x+h)-f(x)}{h} \quad (h \mathrel{\char"2260} 0)$$

Applying this between $P$ at $x=1$ and $Q$ at $x=1+h$:

$$\text{Gradient} = \frac{f(1+h)-f(1)}{h}$$

Now substitute $f(x) = x^2+2$:

$$= \frac{\left[(1+h)^2+2\right] - \left(1^2+2\right)}{h}$$

Expand $(1+h)^2 = 1+2h+h^2$:

$$= \frac{(1+2h+h^2+2)-(1+2)}{h} = \frac{(h^2+2h+3)-3}{h} = \frac{h^2+2h}{h}$$

Factorise the numerator and cancel $h$ (valid since $h \mathrel{\char"2260} 0$):

$$= \frac{h(h+2)}{h} = h+2$$

So the gradient of chord $PQ$ is $\mathbf{h+2}$.

This answer depends on $h$ — which makes sense, since different choices of $Q$ (different values of $h$) give a chord with a different steepness. As $Q$ slides along the curve towards $P$, $h$ gets smaller, and intuitively the chord should swing around to match the tangent at $P$ more and more closely. We can now actually find that tangent gradient, by letting $h \to 0$:

$$f'(1) = \lim_{h \to 0}(h+2) = 2$$

### The General Case

Repeating the exact same argument at a general point $x$ on a general curve $y=f(x)$, rather than the specific point $x=1$ on the specific curve $f(x)=x^2+2$, gives the general definition.

*Diagram from the source notes: a general increasing curve $y=f(x)$ is sketched. Two points are marked: $P$ at horizontal position $x$ (height $f(x)$), and $Q$ further right at horizontal position $x+h$ (height $f(x+h)$). The straight chord $PQ$ is drawn between them. Beneath the chord, a right-angled triangle shows the "run" — a horizontal segment of length $h$, from $x$ to $x+h$ — and the "rise" — a vertical segment of length $f(x+h)-f(x)$, from the height of $P$ up to the height of $Q$.*

$$\text{Gradient of } PQ = \frac{\text{rise}}{\text{run}} = \frac{\Delta y}{\Delta x} = \frac{f(x+h)-f(x)}{h} \quad (h \mathrel{\char"2260} 0)$$

As $Q$ moves along the curve towards $P$, $h$ gets smaller and smaller. As $Q$ gets as close as possible to $P$, $h \to 0$, and the chord $PQ$ becomes a **tangent** at $P$. The gradient of the curve at a point $P$ is, by definition, the gradient of the tangent at that point — that is,

$$f'(x) = \lim_{h \to 0}\frac{f(x+h)-f(x)}{h} \quad (h \mathrel{\char"2260} 0)$$

Finding the gradient this way is called **differentiation from first principles**. Differentiating $f(x)$ gives $f'(x)$ — $f'(x)$ is *the derivative* of $f(x)$. Differentiating $y$ gives $\dfrac{dy}{dx}$ — $\dfrac{dy}{dx}$ is the derivative of $y$ with respect to $x$. The gradient function $f'(x)$ is the rule for the **instantaneous rate of change** of $f$ at any point $x$, as distinct from $\dfrac{f(x+h)-f(x)}{h}$, which is only ever an **average rate of change** over the interval from $x$ to $x+h$.

**Checking the general formula against Worked Example 4:** applying the definition above to $f(x) = x^2+2$ at a general point $x$ (not just $x=1$):

$$f(x+h) = (x+h)^2+2 = x^2+2xh+h^2+2$$

$$f(x+h)-f(x) = (x^2+2xh+h^2+2)-(x^2+2) = 2xh+h^2 = h(2x+h)$$

$$\frac{f(x+h)-f(x)}{h} = \frac{h(2x+h)}{h} = 2x+h$$

$$f'(x) = \lim_{h \to 0}(2x+h) = 2x$$

So $f'(x) = 2x$ for this curve — and at $x=1$, this gives $f'(1) = 2(1) = 2$, exactly matching the value found directly above by taking $\lim_{h \to 0}(h+2)$. This agreement is the whole point of the definition: first-principles differentiation gives the same answer whether you fix the point of interest first and then take the limit, or find the general derivative formula first and substitute the point in afterwards. The second approach is far more efficient in general, and systematising it — so that derivatives can be found without grinding through a limit calculation like this every time — is exactly the job of [[Differentiation Rules]]. What those rules are actually *for* (gradients of tangent lines, rates of change, maximum and minimum values of a function, and more) is covered in [[Applications of Differentiation]].

## Summary

A practical strategy for evaluating any limit encountered in this course:

1. **Try direct substitution first.** If the function is continuous at the point in question (true of every polynomial everywhere, and every rational function wherever its denominator is nonzero), substituting gives the limit immediately.
2. **If direct substitution gives $\frac{0}{0}$,** the expression has a common factor that vanishes at $x=a$. Factorise the numerator and/or denominator, cancel the common factor (always valid, since the limit never actually sets $x=a$), and substitute again. The underlying function typically has a removable discontinuity (a "hole") at that point.
3. **If $x \to \infty$ or $x \to -\infty$,** divide every term by the highest power of $x$ present, then use the fact that $\dfrac{1}{x^n} \to 0$.
4. **If the goal is the gradient of a curve at a point** rather than the limit of a numerical expression, set up the chord gradient $\dfrac{f(x+h)-f(x)}{h}$, simplify algebraically until the troublesome $h$ in the denominator cancels out, and only then let $h \to 0$. This is differentiation from first principles, and it is the limit that defines every derivative used from here on.

For further practice applying all of the above, see [[Introductory Calculus - Practice and Revision]].
