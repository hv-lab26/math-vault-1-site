# Function Notation, Domain and Range

A function is a rule that assigns to every input ($x$-value) exactly one output ($y$-value). Not every relationship between $x$ and $y$ qualifies as a function — if even one $x$-value is paired with two (or more) different $y$-values, it is still a *relation*, but not a *function*. This note covers how to recognise a function, how to describe its set of valid inputs (**domain**) and resulting outputs (**range**), and the different notations used for a function, its equation, and its graph.

## Key Summary

| Term | Meaning |
|---|---|
| Function | a set of ordered pairs $(x,y)$ in which every $x$-value is paired with a unique $y$-value |
| Domain ($D$) | the set of all $x$-values used (all valid inputs) |
| Range ($R$) | the set of all $y$-values produced (all possible outputs) |
| Vertical line test | if any vertical line crosses the graph more than once, it is **not** a function |
| $f(x)$ | the function itself (an expression) |
| $f(x)=0$ | an **equation** — solving it gives the roots/zeros of $f$ |
| $y=f(x)$ | the **graph** of $f$ in the $xy$-plane |
| $A\cup B$ | union — all elements in $A$ or $B$ (or both) |
| $A\cap B$ | intersection — elements common to both $A$ and $B$ |
| $A\,/\,B$ | difference — elements of $A$ with any $B$-elements removed |

## What Is a Function? The Vertical Line Test

A function is a set of ordered pairs in which every $x$-value is paired to a unique $y$-value. Graphically, this means: draw a vertical line anywhere across the graph, and it must cross the graph **at most once** — a vertical line at a fixed $x$ that crossed twice would mean that one input has two different outputs, which is exactly what a function forbids.

**Example 1.**

**(a)** Is $\{(1,4),\ (2,0),\ (2,3),\ (5,-1)\}$ a function?

The $x$-value $2$ appears twice: once paired with $y=0$, once with $y=3$. Since this single input has two different outputs, **this is not a function**. (Its domain — the set of $x$-values that appear, whether or not it's a function — is still meaningful: $D=\{1,2,5\}$.)

**(b)** *Graph description:* a curve that dips to a minimum below the $x$-axis and rises on both sides, crossing the $x$-axis exactly once. Checking several vertical lines across its width, each one crosses the curve exactly **once**. $\Rightarrow$ **this is a function.** (Its minimum turning point sits at $y=-2$; since the curve is otherwise unbounded upward on both sides, its range is $R=[-2,+\infty)$.)

**(c)** *Graph description:* a circle centred on the origin. Any vertical line through the circle's interior crosses it **twice** — once on the top half, once on the bottom half. $\Rightarrow$ **not a function.**

This is why a circle's equation ($x^2+y^2=r^2$) is never written as a single "$y=f(x)$" — solved for $y$, it splits into two separate functions, $y=\sqrt{r^2-x^2}$ (the top half) and $y=-\sqrt{r^2-x^2}$ (the bottom half), each of which *does* pass the vertical line test on its own.

## Domain and Range

For a function given as a set of ordered pairs, the domain is simply the set of all first coordinates (every $x$-value used), and the range is the set of all second coordinates (every $y$-value produced): $x=$ domain, $y=$ range.

**Example.** Function $A=\{(1,2),\ (3,4),\ (5,3)\}$.

$$D=\{1,3,5\}, \qquad R=\{2,4,3\}$$

### Reading Domain and Range Off a Graph

When a function is given as a graph rather than a list of points, the domain is its full horizontal extent (the "shadow" it casts on the $x$-axis), and the range is its full vertical extent (the "shadow" it casts on the $y$-axis).

- *Graph description:* a line segment running from $(-1,-1)$ up to $(3,4)$. Its horizontal extent runs from $x=-1$ to $x=3$, so $D=[-1,3]$.
- *Graph description:* a curve shaped like a shallow basin bounded between two vertical guide lines at $x=-2$ and $x=3$. Its horizontal extent gives $D=[-2,3]$.

### Set Notation for Domain and Range

A domain or range is sometimes naturally built from more than one interval (for example, a graph with a gap or an excluded point), so it helps to have notation for combining and comparing sets:

- $A\cup B$ — **union**: all items from $A$ **and** $B$ together.
- $A\cap B$ — **intersection**: only the items that are in **both** $A$ and $B$.
- $A\,/\,B$ (also written $A\setminus B$) — **difference**: all items of $A$, with any items also in $B$ removed.

## Function Notation: $f(x)$, Equations, and Graphs

Three closely related but distinct objects use similar-looking notation, and it's worth being precise about which is which:

- $f(x)$ is **the function** — an expression that produces an output for each input $x$.
- $f(x)=0$ is **an equation** — asking "for which $x$ does the output equal zero?" Solving it gives the function's roots (zeros), i.e. the $x$-intercepts of its graph.
- $y=f(x)$ is **the graph** — the set of all points $(x,y)$ in the plane satisfying this relationship.

## Worked Example — Finding Domain and Range (Homework Q8)

Find the domain and range of each of the following.

**(a)** $y=3-2x$

This is a (non-constant) linear function. A line like this is defined for every real $x$, and as $x$ ranges over all reals, $y$ also takes every real value — a non-horizontal line is unbounded in both directions.

$$D:(-\infty,+\infty), \qquad R:(-\infty,+\infty)$$

**(b)** $y=x^2-4x+4$

Completing the square (recognising the perfect square trinomial):

$$y = x^2-4x+4 = (x-2)^2$$

A perfect square is never negative, so $(x-2)^2\geq0$ for every real $x$ — and it does reach $0$, at $x=2$. This is a parabola with vertex $(2,0)$ opening upward (see [[Quadratic Functions]] for more on vertex form). A parabola like this is defined for every real $x$, but only ever outputs values from its turning point upward.

$$R:[0,\infty), \qquad D:\mathbb{R}$$

**(c)** $y=\sqrt{5-2x}$

A square root is only defined (as a real number) when the expression underneath it is non-negative, so this function requires

$$5-2x\geq0 \iff -2x\geq-5 \iff x\leq\frac52$$

(dividing by the negative number $-2$ reverses the inequality direction). So the domain is every $x$ up to and including $2.5$. For the range: a square root always outputs a value $\geq0$, and as $x\to-\infty$ the expression inside the root, $5-2x$, grows without bound — so $\sqrt{5-2x}$ also grows without bound, meaning every non-negative output value is actually achieved.

$$D:(-\infty,2.5], \qquad R:[0,\infty)$$

A square-root function needing its radicand to stay non-negative is the same kind of restriction that shows up for other functions with "forbidden" inputs — see [[Logarithmic Functions]] for the analogous restriction on logarithms (the argument must be strictly positive).

---

For further practice, see [[Functions - Practice and Revision]].
