# Reciprocal Functions

$$y=\frac{a}{x-h}+k$$

The base case $y=\dfrac1x$ has two branches, one in each of the first and third quadrants relative to the origin, approaching but never touching either axis. The general form above shifts this basic hyperbola horizontally by $h$ and vertically by $k$, and scales/reflects it by $a$ — exactly the same $a,h,k$ transformation language used for the [[Quadratic Functions|parabola]] and the [[Square Root Function]].

- **Vertical asymptote:** $x=h$ (the graph is undefined here, since you'd divide by zero)
- **Horizontal asymptote:** $y=k$ (since $\dfrac{a}{x-h}\to0$ as $x\to\pm\infty$ — see [[Limits]] for more on this kind of limit)

## Worked Examples

**Exercise 1.** Sketch $y=\dfrac{1}{x+3}$.

- Vertical asymptote: $x+3=0 \implies x=-3$
- Horizontal asymptote: $\displaystyle\lim_{x\to\infty}\frac{1}{x+3}=0 \implies y=0$
- $x$-intercept: set $y=0 \implies \dfrac{1}{x+3}=0$, which has **no solution** (a fraction is never zero) — so there is no $x$-intercept
- $y$-intercept: set $x=0 \implies y=\dfrac13$, i.e. $\left(0,\dfrac13\right)$

**Graph description:** two branches meeting the asymptotes $x=-3$ and $y=0$ — one branch in the region $x<-3$ (coming up from below $y=0$ as $x\to-\infty$, diving down toward $-\infty$ as $x\to-3^-$), and one branch for $x>-3$ (diving down from $+\infty$ as $x\to-3^+$, settling down toward $y=0$ from above as $x\to\infty$), passing through $\left(0,\tfrac13\right)$.

**Exercise 2.** Sketch $y=\dfrac1x+1$.

- Vertical asymptote: $x=0$
- Horizontal asymptote: $\displaystyle\lim_{x\to\infty}\left(\frac1x+1\right)=0+1=1 \implies y=1$
- $x$-intercept: $\dfrac1x+1=0 \implies \dfrac1x=-1 \implies x=-1$, i.e. $(-1,0)$
- $y$-intercept: undefined at $x=0$, so there is **no** $y$-intercept

For more mixed practice across all the Unit 1 function topics, see [[Functions - Practice and Revision]].
