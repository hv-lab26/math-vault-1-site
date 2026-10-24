# Functions - Practice and Revision

Mixed practice problems drawn from revision worksheets, organised by sub-topic. Each section links to the relevant concept note — see that note for the underlying theory. This note is problems and full worked solutions only.

## Quadratic Functions

See [[Quadratic Functions]].

### Example 1 — quadratic from two distinct x-intercepts

*(Question reconstructed from working: a parabola has two distinct x-intercepts, at $x=-3$ and $x=1$, and a y-intercept at $(0,-1)$. Find the equation of the parabola.)*

Since the parabola has two distinct ("2 diff") roots at $x=-3$ and $x=1$, write it in x-intercept form:

$$y = a(x-b)(x-c)$$

with $b=-3$, $c=1$, i.e. $y = a(x+3)(x-1)$.

Substitute the y-intercept $(0,-1)$:

$$-1 = a(0+3)(0-1) = a(3)(-1) = -3a$$

$$\implies a = \dfrac{1}{3}$$

$$\implies y = \dfrac{1}{3}(x+3)(x-1)$$

**Graph check:** this is an upward-opening parabola ($a=\dfrac13>0$). The vertex sits midway between the roots, at $x = \dfrac{-3+1}{2} = -1$, giving $y = \dfrac13(-1+3)(-1-1) = \dfrac13(2)(-2) = -\dfrac43$, so vertex $\left(-1,-\dfrac43\right)$. The curve comes down from the top-left, crosses the x-axis at $x=-3$, dips to the vertex at $\left(-1,-\dfrac43\right)$ (passing through the y-intercept $(0,-1)$ just after the vertex), then rises back up through $x=1$ and continues upward to the right.

### Example 2 — quadratic from a repeated root

*(Question reconstructed from working: a parabola touches the x-axis at $x=-2$ (a repeated root) and has a y-intercept at $(0,1)$. Find the equation.)*

A repeated ("2 same") root at $x=-2$ means the parabola touches but does not cross the x-axis there, so:

$$f(x) = a(x+2)(x+2) = a(x+2)^2$$

Substitute the y-intercept $(0,1)$:

$$1 = a(0+2)^2 = 4a \implies a = \dfrac{1}{4}$$

$$\implies f(x) = \dfrac{1}{4}(x+2)^2$$

**Graph check:** an upward-opening parabola with vertex (and only x-intercept) at $(-2,0)$, passing through $(0,1)$.

### Example 3 — factorising by grouping

Factorise $P(x) = x^2+9x+20$.

$$P(x) = x^2+9x+20 = x^2+4x+5x+20 = x(x+4)+5(x+4) = (x+5)(x+4)$$

So $(x+5)$ and $(x+4)$ are factors of $P(x)$.

## Cubic Functions

See [[Cubic Functions]].

### Quartic factorisation by common factor

Factorise $f(x) = 4x^4-64x^2$.

$$f(x) = 4x^2(x^2-16) = 4x^2(x+4)(x-4)$$

The x-intercepts are $x=-4$, $x=0$ (a repeated/touching root, since the $4x^2$ factor is squared), and $x=4$. (This example is degree 4, but uses exactly the same factorising-and-reading-off-intercepts approach as a cubic in factored form $y=a(x-b)(x-c)$.)

### Building a quartic from its roots

*(Question reconstructed from working: a quartic has x-intercepts at $x=-3$, $x=\dfrac{2}{5}$, and a repeated x-intercept at $x=4$, and passes through the point $(0,96)$. Find the equation.)*

Using the repeated root at $x=4$:

$$y = a(x+3)\left(x-\dfrac{2}{5}\right)(x-4)^2$$

Substitute $(0,96)$:

$$96 = a(0+3)\left(0-\dfrac25\right)(0-4)^2 = a(3)\left(-\dfrac25\right)(16)$$

$$= a \times 48 \times \left(-\dfrac25\right) = -\dfrac{96}{5}a$$

$$\implies a = 96 \div \left(-\dfrac{96}{5}\right) = -5$$

So $y = -5(x+3)\left(x-\dfrac25\right)(x-4)^2$. To clear the fraction, write $\left(x-\dfrac25\right) = \dfrac15(5x-2)$, so:

$$y = -5(x+3)\cdot\dfrac15(5x-2)\cdot(x-4)^2 = -1(x+3)(5x-2)(x-4)^2$$

$$\implies y = -(x+3)(5x-2)(x-4)^2$$

### Expanding a cubic from its roots, and sketching it

*(Question reconstructed from working: a cubic has x-intercepts at $x=-2,-1,4$. Write it in expanded form and sketch it.)*

In factored (intercept) form, with $a=1$:

$$y = (x+1)(x-4)(x+2)$$

Expand: first $(x+1)(x+2) = x^2+3x+2$. Then:

$$y = (x^2+3x+2)(x-4) = x^3-4x^2+3x^2-12x+2x-8 = x^3-x^2-10x-8$$

So $y = x^3-x^2-10x-8 = (x+1)(x-4)(x+2)$, with x-intercepts at $x=-2,-1,4$ and y-intercept at $x=0$: $y=(1)(-4)(2)=-8$, i.e. $(0,-8)$.

**Graph description:** leading coefficient is positive and degree is odd, so as $x\to-\infty$, $y\to-\infty$, and as $x\to+\infty$, $y\to+\infty$. Testing the sign of $y$ in each interval cut out by the roots ($x=-3$: negative; $x=-1.5$: positive; $x=0$: negative, matching the y-intercept $-8$; $x=5$: positive) gives the shape: the curve rises from the bottom-left, crosses the x-axis at $x=-2$, climbs to a small local maximum just after $x=-2$, turns and descends — crossing the x-axis again at $x=-1$ — continuing down through the y-intercept $(0,-8)$ to a local minimum somewhere between $x=-1$ and $x=4$, then rises steeply, crossing the x-axis at $x=4$ and continuing up to the top-right.

## Polynomial Division and the Factor Theorem

See [[Polynomial Division and the Factor Theorem]].

### Factorising a cubic using the Factor Theorem

Factorise $P(x) = 2x^3-x^2-13x-6$.

Test small integer values using the Factor Theorem:

$$P(1) \mathrel{\char"2260} 0, \qquad P(-1) \mathrel{\char"2260} 0, \qquad P(2) \mathrel{\char"2260} 0, \qquad P(-2) = 0 \ \text{(remainder } 0\text{)}$$

Check: $P(-2) = 2(-8)-(4)-13(-2)-6 = -16-4+26-6 = 0$. ✓ So $(x+2)$ is a factor.

Divide $2x^3-x^2-13x-6$ by $(x+2)$:

$$2x^3 \div x = 2x^2, \quad 2x^2(x+2) = 2x^3+4x^2, \quad \text{remainder: } -5x^2-13x$$

$$-5x^2\div x = -5x, \quad -5x(x+2) = -5x^2-10x, \quad \text{remainder: } -3x-6$$

$$-3x \div x = -3, \quad -3(x+2) = -3x-6, \quad \text{remainder: } 0$$

So the quotient is $2x^2-5x-3$. Factorising: looking for two numbers multiplying to $2\times(-3)=-6$ and summing to $-5$: these are $-6$ and $1$.

$$2x^2-5x-3 = 2x^2-6x+x-3 = 2x(x-3)+1(x-3) = (2x+1)(x-3)$$

$$\implies P(x) = (x+2)(2x+1)(x-3)$$

### Polynomial long division and full factorisation

Factorise $P(x) = 2x^3+x^2-13x+6$.

Divide by $(x-2)$:

$$2x^3 \div x = 2x^2, \quad 2x^2(x-2)=2x^3-4x^2, \quad \text{remainder: } 5x^2-13x$$

$$5x^2 \div x = 5x, \quad 5x(x-2) = 5x^2-10x, \quad \text{remainder: } -3x+6$$

$$-3x \div x = -3, \quad -3(x-2) = -3x+6, \quad \text{remainder: } 0$$

So $P(x) = (x-2)(2x^2+5x-3)$, confirming $P(2)=0$ (zero remainder). Factorise the quotient: need two numbers multiplying to $2\times(-3)=-6$, summing to $5$: these are $6$ and $-1$.

$$2x^2+5x-3 = 2x^2+6x-x-3 = 2x(x+3)-1(x+3) = (2x-1)(x+3)$$

$$\implies P(x) = (x-2)(2x-1)(x+3)$$

**Check** (expanding back): $(x-2)(2x^2+5x-3) = 2x^3+5x^2-3x-4x^2-10x+6 = 2x^3+x^2-13x+6$ ✓, matching the original polynomial.

## Reciprocal Functions

See [[Reciprocal Functions]].

### Rewriting improper rational functions in $y=\dfrac{a}{x-h}+k$ form

**(i)** Rewrite $f(x)=\dfrac{5x+1}{x}$ in the form $y=\dfrac{a}{x-h}+k$.

$$f(x) = \dfrac{5x+1}{x} = \dfrac{5x}{x}+\dfrac1x = \dfrac1x+5$$

So $(h,k) = (0,5)$: the graph is the basic hyperbola $y=\dfrac1x$ shifted up $5$ units, with asymptotes $x=0$ and $y=5$.

**(ii)** Rewrite $f(x) = \dfrac{3x+1}{x-1}$ in the same form.

Divide $3x+1$ by $x-1$: $3x+1 = 3(x-1)+3+1=3(x-1)+4$, so:

$$f(x) = \dfrac{3(x-1)+4}{x-1} = 3+\dfrac{4}{x-1} = \dfrac{4}{x-1}+3$$

So $(h,k)=(1,3)$: asymptotes $x=1$ and $y=3$, turning/centre point $(1,3)$.

### Finding asymptotes from a shifted hyperbola

Find the vertical and horizontal asymptotes of $y+5 = \dfrac{1}{2x+6}$.

$$y + 5 = \dfrac{1}{2x+6} = \dfrac{1}{2(x+3)}$$

$$\implies y = \dfrac{1}{2(x+3)} - 5$$

Comparing to $y=\dfrac{a}{x-h}+k$: $(h,k)=(-3,-5)$.

$$\implies \textbf{Asymptotes: } x=-3, \ \ y=-5$$

### Finding the equation from given features

*(Question reconstructed from working: a hyperbola $y=\dfrac{a}{x+5}+c$ has a vertical asymptote at $x=-5$, a horizontal asymptote at $y=10$, and a y-intercept at $(0,4)$. Find $a$, and hence find the x-intercept.)*

From the asymptotes: $b=5$ (vertical asymptote $x=-5$) and $c=10$ (horizontal asymptote $y=10$), so $y=\dfrac{a}{x+5}+10$.

Substitute the y-intercept $(0,4)$:

$$4 = \dfrac{a}{0+5}+10 \implies \dfrac{a}{5} = 4-10=-6 \implies a=-30$$

$$\implies y = \dfrac{-30}{x+5}+10$$

Find the x-intercept (set $y=0$):

$$0 = \dfrac{-30}{x+5}+10 \implies 10 = \dfrac{30}{x+5} \implies x+5 = 3 \implies x=-2$$

$$\implies \text{x-intercept: } (-2,0)$$

## Logarithmic Functions

See [[Logarithmic Functions]].

### Solving an exponential equation

Solve $2^{2x}-64=0$.

$$2^{2x} = 64 = 2^6$$

(equivalently, $64 = (2^3)^2 = 2^{2\times3}$, matching the $2x$ exponent form directly)

$$\implies 2x = 2\times 3 \implies x = 3$$

**Check:** $2^{2(3)} = 2^6 = 64$ ✓.

### Solving a logarithmic equation (log subtraction law)

Solve $\log_x(108) - \log_x(12) = 4$.

$$\log_x\left(\dfrac{108}{12}\right) = 4 \implies \log_x(9) = 4$$

$$\implies x^4 = 9 \implies (x^2)^2 = 3^2 \implies x^2 = \pm 3$$

Since $x^2\geq 0$ for all real $x$, $x^2=-3$ is impossible, so $x^2=3 \implies x=\pm\sqrt3$.

Since $x$ is the base of a logarithm, we need $x>0$ (and $x\mathrel{\char"2260}1$), so $x=-\sqrt3$ is rejected.

$$\implies x = \sqrt3$$

**Check:** $9^{(1/4)}$ should equal... more directly, $x^4=(\sqrt3)^4=(3)^2=9$ ✓.

### Solving a log equation by substitution

Solve $(\log_e(2x))^2+4\log_e(2x)-6=6$.

Let $a=\log_e(2x)$:

$$a^2+4a-6=6 \implies a^2+4a-12=0$$

Factorise (two numbers multiplying to $-12$, summing to $4$: these are $6$ and $-2$):

$$(a+6)(a-2)=0 \implies a=2 \ \text{ or } \ a=-6$$

**Case $a=2$:** $\log_e(2x)=2 \implies 2x=e^2 \implies x=\dfrac12e^2$

**Case $a=-6$:** $\log_e(2x)=-6 \implies 2x=e^{-6} \implies x=\dfrac12e^{-6}$

Both values give $2x>0$, so both are valid (no domain violation):

$$\implies x = \dfrac12e^2 \ \ \text{or} \ \ x=\dfrac12e^{-6}$$

### Domain, range, and inverse of a log function

A function is defined by $f(x)=\log_3(x-2)-1$.

**(a) Domain and range of $f$.**

Need $x-2>0 \implies x>2$, so:

$$D_f = (2,+\infty), \qquad R_f = \mathbb{R}$$

(the range is all of $\mathbb R$ since a log function takes every real value, and the $-1$ shift doesn't restrict this).

**(b) Find $f^{-1}(x)$.**

See [[Inverse Functions]] for the swap-$x$-and-$y$ method used here.

Let $y=\log_3(x-2)-1$. Swap $x$ and $y$:

$$x = \log_3(y-2)-1 \implies x+1 = \log_3(y-2)$$

$$\implies y-2 = 3^{x+1} \implies y = 3^{x+1}+2$$

$$\implies f^{-1}(x) = 3^{x+1}+2$$

Domain and range of $f^{-1}$ swap with those of $f$:

$$D_{f^{-1}} = \mathbb{R}, \qquad R_{f^{-1}} = (2,+\infty)$$

**(c) Sketch $f$ and $f^{-1}$ on the same axes.**

Both graphs are reflections of each other across the line $y=x$ (the defining symmetry of inverse functions):

- $f(x)=\log_3(x-2)-1$: a logarithmic curve with vertical asymptote $x=2$. Just to the right of $x=2$ the curve plunges steeply downward; moving right it rises, crossing through increasing $x$-values, increasing without bound but more and more slowly (concave down).
- $f^{-1}(x)=3^{x+1}+2$: an exponential curve with horizontal asymptote $y=2$. Far to the left, the curve sits just above $y=2$, nearly flat; moving right it curves upward, increasing steeply without bound.
- The two curves mirror each other in the diagonal line $y=x$: the vertical asymptote of $f$ ($x=2$) corresponds to the horizontal asymptote of $f^{-1}$ ($y=2$).

## Trigonometric Functions

See [[Trigonometric Functions]].

### Solving a trig equation by converting to tan

Solve $\cos\left(x+\dfrac{\pi}{6}\right) = \sin\left(x+\dfrac{\pi}{6}\right)$ for $x\in[0,2\pi]$.

Divide both sides by $\cos\left(x+\dfrac\pi6\right)$ (valid wherever this isn't zero):

$$\dfrac{\sin\left(x+\frac\pi6\right)}{\cos\left(x+\frac\pi6\right)} = 1 \implies \tan\left(x+\dfrac{\pi}{6}\right) = 1$$

The general solutions of $\tan\theta=1$ are $\theta=\dfrac\pi4+k\pi$ for integer $k$. So:

$$x+\dfrac{\pi}{6} = \dfrac{\pi}{4} \quad \text{or} \quad x+\dfrac{\pi}{6} = \pi+\dfrac{\pi}{4}$$

**First case:**

$$x = \dfrac{\pi}{4}-\dfrac{\pi}{6} = \dfrac{3\pi-2\pi}{12} = \dfrac{\pi}{12}$$

**Second case:**

$$x = \pi+\dfrac{\pi}{4}-\dfrac{\pi}{6} = \dfrac{12\pi+3\pi-2\pi}{12} = \dfrac{13\pi}{12}$$

Checking the next period ($k=2$: $x=\dfrac{25\pi}{12} > 2\pi$) falls outside $[0,2\pi]$, and $k=-1$ gives a negative $x$, so these are the only two solutions in range:

$$\implies x = \dfrac{\pi}{12} \ \ \text{or} \ \ x=\dfrac{13\pi}{12}$$

### Sinusoidal modelling: period, sign, and solving

*(Question reconstructed from working: the price of a commodity over an 8-month period is modelled by $P(t) = 5000+2000\sin\left(\dfrac{\pi t}{3}\right)$, $t\in[0,8]$, where $t$ is in months.)*

**(a) Find the period.**

For $y=a\sin(bx-c)+d$, Period $=\dfrac{2\pi}{|b|}$. Here $b=\dfrac\pi3$:

$$\text{Period} = \dfrac{2\pi}{\pi/3} = 6 \ \text{ months}$$

**(b) Show $P(t)\geq5000$ for $0\leq t\leq3$.**

For $t\geq0$, $\sin\left(\dfrac{\pi t}{3}\right)\geq0$ whenever $\dfrac{\pi t}{3}\in[0,\pi]$, i.e. $t\in[0,3]$ (within the given domain). For such $t$:

$$5000+2000\sin\left(\dfrac{\pi t}{3}\right) \geq 5000$$

so $P(t)\geq5000$ on $[0,3]$.

*(The source page also has a brief side-calculation checking the specific case $\sin\left(\frac{\pi t}{3}\right)=\dfrac{\sqrt3}{2}$, giving $P(t)=5000+2000\times\dfrac{\sqrt3}{2}=5000+1000\sqrt3\approx6732.05$ — shown here for completeness, though the main equation solved is part (c) below.)*

**(c) Find the values of $t$ for which $P(t)=6000$.**

$$5000+2000\sin\left(\dfrac{\pi t}{3}\right) = 6000$$

$$2000\sin\left(\dfrac{\pi t}{3}\right) = 1000 \implies \sin\left(\dfrac{\pi t}{3}\right) = \dfrac12$$

Let $\theta = \dfrac{\pi t}{3}$. Solve $\sin\theta=\dfrac12$ using the reference angle $\dfrac\pi6$ (since $\sin\dfrac\pi6=\dfrac12$) and the CAST diagram — a circle divided into four quadrants by a horizontal and vertical line through the centre, labelled (going anticlockwise from the top-right) **A** (all three ratios positive), **S** (sine positive), **T** (tangent positive), **C** (cosine positive). Since $\sin\theta$ is positive, only the **A** and **S** quadrants (1st and 2nd) are relevant:

$$\theta = \dfrac{\pi}{6} \ \text{(1st quadrant)} \quad \text{or} \quad \theta = \pi-\dfrac{\pi}{6}=\dfrac{5\pi}{6} \ \text{(2nd quadrant)}$$

Convert back to $t$ using $t=\dfrac{3\theta}{\pi}$:

$$t_1 = \dfrac{3(\pi/6)}{\pi} = \dfrac12, \qquad t_2 = \dfrac{3(5\pi/6)}{\pi} = \dfrac52$$

Since the period is $6$ (from part a), every subsequent solution repeats by adding multiples of $6$ to $t_1$ and $t_2$:

$$t_3 = t_1+6 = 6.5, \quad t_4 = t_2+6=8.5, \quad t_5=t_1+12=12.5, \quad t_6=t_2+12=14.5, \ \ldots$$

$$\implies t = \dfrac12, \dfrac52, 6.5, 8.5, 12.5, 14.5, \ldots \ \text{(months)}$$

within whatever extended domain the original question intended beyond $t\in[0,8]$ — only $t=\dfrac12$ and $t=\dfrac52$ fall inside $[0,8]$ itself ($t=6.5$ is the next one, also inside $[0,8]$; $t=8.5$ is just outside it).

## Function Notation, Domain and Range

See [[Function Notation, Domain and Range]].

### Hybrid (piecewise) function — linear and quadratic pieces

*(Question reconstructed from working: a hybrid function is defined by)*

$$
f(x) = \begin{cases} ax+b, & x>c \\ (x-d)^2+e, & x\leq c\end{cases}
$$

*(with $c=-2$ visible on the graph as the join point, and the graph passing through $A(-2,1)$ and $B(0,2)$. Find $a,b,c,d,e$.)*

Since $B(0,2)$ lies on the line piece ($x=0>c=-2$):

$$a(0)+b=2 \implies b=2$$

The two pieces meet continuously at the join point $A(-2,1)$. Using the line piece at $x=-2$:

$$a(-2)+b=1 \implies -2a+2=1 \implies -2a=-1 \implies a=\dfrac12$$

The quadratic piece's turning point is exactly the join point $A(-2,1)$ visible on the graph, so $(d,e)=(-2,1)$.

$$\implies a=\dfrac12,\ \ b=2,\ \ c=-2,\ \ d=-2,\ \ e=1$$

$$
f(x) = \begin{cases} \dfrac12x+2, & x>-2 \\ (x+2)^2+1, & x\leq-2\end{cases}
$$

**Graph description:** for $x\leq-2$, an upward parabola arm with vertex at $(-2,1)$ (included, filled dot), opening upward to the left as $x$ decreases. For $x>-2$, a straight line of gradient $\dfrac12$ starting (open dot) just above $(-2,1)$ and rising through the y-intercept $(0,2)$, continuing up and to the right.

### Hybrid (piecewise) function — cubic and quadratic pieces

*(Question reconstructed from working: a hybrid function is defined by)*

$$
f(x) = \begin{cases} (x-a)^3+b, & x\leq c \\ (x-c)^2-d, & x\geq c\end{cases}
$$

*(with the graph passing through the points $(0,2)$ and $(1,1)$ on the cubic piece, and $c=2$ marked as the join point on the graph.)*

**Method:** substitute the two known points on the cubic piece to form simultaneous equations in $a$ and $b$:

$$(0-a)^3+b=2 \implies -a^3+b=2 \qquad (\text{i})$$

$$(1-a)^3+b=1 \qquad (\text{ii})$$

Subtracting (i) from (ii) eliminates $b$ and gives a single equation in $a$ alone, which can then be solved (by inspection or numerically) and substituted back into (i) to find $b$. The second (quadratic) piece's vertex is $(c,-d)$; since the two pieces are required to meet continuously at $x=c$, equate the cubic piece's value at $x=c$ to $-d$ to find $d$ once $a,b,c$ are known.

*(The specific numbers on this source page were not legible/consistent enough to pin down a unique verified value for every one of $a,b,d$ with confidence — working the algebra through with the figures as read gave no real solution for $a$, suggesting at least one digit was misread on this particular page. The join point $c=2$ is clear from the diagram and is used above; check the original page for the exact coordinates if you need the fully numeric answer.)*

### Domain restrictions (combined example)

*(Question reconstructed from working: find the domain, given the restrictions $x>1$, $x\mathrel{\char"2260}2$ (from a term such as $\dfrac{1}{x-2}$ — see [[Reciprocal Functions]]), and $3-x>0$ (from a term such as $\sqrt{3-x}$ — see [[Square Root Function]]).)*

The reciprocal-type restriction:

$$x-2\mathrel{\char"2260}0 \iff x\mathrel{\char"2260}2$$

The square-root-type restriction:

$$3-x>0 \implies -x>-3 \implies x<3$$

Combining all three restrictions ($x>1$ and $x\mathrel{\char"2260}2$ and $x<3$):

$$\implies \text{Domain} = (1,2)\cup(2,3)$$

*(The same source page also shows the coordinate pairs $(-1,-5)$, $(0,2)$, $(5,-1)$ and the labels "$a(x-h)^2+k$" / "$a(x-h)^3+k$" — these appear to be scratch working for a separate problem and weren't recoverable with enough context to reconstruct safely, so they're omitted here.)*
