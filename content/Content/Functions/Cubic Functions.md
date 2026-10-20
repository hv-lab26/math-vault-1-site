# Cubic Functions

A cubic function has general form

$$y=ax^3+bx^2+cx+d, \qquad a\neq0$$

- If $a>0$, the cubic is "positive": as $x\to-\infty$, $y\to-\infty$, and as $x\to+\infty$, $y\to+\infty$ (the graph trends upward overall, left to right).
- If $a<0$, the cubic is "negative": the trend is reversed (downward overall, left to right).

A general cubic can have a local maximum and a local minimum in the middle of the curve (a "wiggle"), depending on $b,c,d$ — finding those exactly requires calculus (see [[Differentiation Rules]]), and wasn't covered in this set of notes.

## Vertex (Inflection) Form

$$y=a(x-h)^3+k$$

$(h,k)$ is the **inflection point** of the cubic. Unlike a parabola's vertex form (see [[Quadratic Functions]]), this shape has *no* turning points at all when it's this simple — it's a single S-shaped curve that momentarily flattens at $(h,k)$ but keeps moving in the same direction through it (always increasing if $a>0$, always decreasing if $a<0$).

## Worked Example: Factorising and Solving a Cubic

**Question.** (a) Factorise $P(x)=2x^3-x^2-13x-6$. (b) Solve $2x^3-x^2-13x-6=0$.

**(a) Factorise, using the factor theorem.** (See [[Polynomial Division and the Factor Theorem]] for the theorem itself.) Test integer divisors of the constant term ($6$: try $\pm1,\pm2,\pm3,\pm6$) until one gives $P(a)=0$:

$$P(1)=2(1)-1-13-6=-18 \neq 0$$
$$P(-1)=2(-1)-1+13-6=4\neq0$$
$$P(2)=2(8)-4-26-6=-20\neq0$$
$$P(-2)=2(-8)-4+26-6=-16-4+26-6=0 \ \checkmark$$

So $P(-2)=0$, meaning $(x+2)$ is a factor. Dividing $P(x)$ by $(x+2)$ (by long division) gives

$$P(x) = (x+2)(2x^2-5x-3)$$

(Check by expanding: $(x+2)(2x^2-5x-3)=2x^3-5x^2-3x+4x^2-10x-6=2x^3-x^2-13x-6$ ✓, matching $P(x)$ exactly.)

**(b) Solve $P(x)=0$.**

$$(x+2)(2x^2-5x-3)=0$$

so either $x=-2$, or $2x^2-5x-3=0$. Factor the quadratic by splitting the middle term (numbers multiplying to $-6$, adding to $-5$: $-6$ and $1$):

$$2x^2+x-6x-3=0 \implies x(2x+1)-3(2x+1)=0 \implies (x-3)(2x+1)=0$$

$$\implies x=3 \ \text{ or } \ x=-\frac12$$

**Full solution:** $x=-2$, $x=3$, or $x=-\dfrac12$.

## Factored Form and Repeated Factors

$$y=a(x-b)(x-c)(x-d), \qquad a\neq0$$

Here $b,c,d$ are the three $x$-intercepts, and the graph crosses the axis at each one.

If two of the roots coincide, you get a **repeated factor**, e.g.

$$y=(x-a)^2(x-b)$$

**Graph description** (for $a<b$): the curve rises from the bottom-left, **touches** the $x$-axis at $x=a$ without crossing it (a repeated/double root — the curve touches zero momentarily, then heads back down the way it came), dips to a local minimum between $a$ and $b$, then rises again and **crosses** the $x$-axis at $x=b$ (a simple root), continuing upward to the right.

## Homework Exercise

**Exercise E3.** Factorise $P(x)=2x^3-10x^2-3x-18$ and solve $P(x)=0$.

*(question text reconstructed from a faint photographed whiteboard — check original if this seems off; one or more coefficients may not be transcribed correctly)*

Following the same method as the worked example above: test the rational-root candidates (divisors of the constant term $18$ over divisors of the leading coefficient $2$: $\pm1,\pm2,\pm3,\pm6,\pm9,\pm18,\pm\tfrac12,\pm\tfrac32,\pm\tfrac92$):

$$P(1)=2-10-3-18=-29 \qquad P(-1)=-2-10+3-18=-27$$
$$P(2)=16-40-6-18=-48 \qquad P(-2)=-16-40+6-18=-68$$
$$P(3)=54-90-9-18=-63 \qquad P(6)=432-360-18-18=36$$

None of the standard rational-root candidates give exactly zero (there's a sign change between $x=2$ and $x=6$, so a real root does exist somewhere in between, but not at a "nice" value) — which strongly suggests a coefficient in the photographed question was misread here rather than this being an intentionally awkward homework problem. The method above (factor theorem trial-and-error, then long division, then splitting the middle term on the resulting quadratic) is exactly how to finish this once the correct coefficients are confirmed against the original.

For more mixed practice across all the Unit 1 function topics, see [[Functions - Practice and Revision]].
