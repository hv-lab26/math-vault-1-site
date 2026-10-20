# Polynomial Division and the Factor Theorem

Dividing one polynomial $P(x)$ (the **dividend**) by another $D(x)$ (the **divisor**) gives a **quotient** $Q(x)$ and a **remainder** $R(x)$, related by

$$P(x) = Q(x)\cdot D(x) + R(x) \qquad\Longleftrightarrow\qquad \frac{P(x)}{D(x)} = Q(x)+\frac{R(x)}{D(x)}$$

(the degree of $R(x)$ is always less than the degree of $D(x)$ — when $D(x)$ is linear, $R(x)$ is just a constant). This note works through long division itself, then the Remainder and Factor Theorems, which let you find a remainder — or confirm a factor — without doing the division at all.

## Worked Example: Long Division

Divide $-3x^2+x-4$ by $-x+3$:

$$
\begin{array}{r}
3x+8 \phantom{00}\\
-x+3{\big)}\ -3x^2+x-4\phantom{00}\\
\underline{-3x^2+9x\phantom{-4}}\phantom{0}\\
-8x-4\phantom{0}\\
\underline{-8x+24}\\
-28
\end{array}
$$

So dividing $-3x^2+x-4$ by $-x+3$ gives quotient $3x+8$ and remainder $-28$.

**Exercise 11.** Divide $x^4-3x^3+2x^2-8$ by $x+2$.

$$
\begin{array}{r}
x^3-5x^2+12x-24\phantom{00}\\
x+2{\big)}\ x^4-3x^3+2x^2+0x-8\phantom{00}\\
\underline{x^4+2x^3\phantom{-5x^2+0x-8.}}\phantom{0}\\
-5x^3+2x^2+0x-8\phantom{0}\\
\underline{-5x^3-10x^2\phantom{+0x-8..}}\phantom{0}\\
12x^2+0x-8\phantom{0}\\
\underline{12x^2+24x\phantom{-8..}}\phantom{0}\\
-24x-8\phantom{0}\\
\underline{-24x-48}\\
40
\end{array}
$$

So the quotient is $x^3-5x^2+12x-24$ and the remainder is $40$.

(Check both results by expanding $Q(x)\cdot D(x)+R(x)$ and confirming it reproduces $P(x)$ — this is always worth doing after a long division, since a single sign slip early on throws off every term after it.)

## The Remainder Theorem

> When $P(x)$ is divided by $(x-a)$, the remainder is $P(a)$.
> More generally, when $P(x)$ is divided by $(ax+b)$, the remainder is $P\!\left(-\dfrac{b}{a}\right)$.

This is worth pausing on: it means you can find a division's remainder **without doing the division at all** — just substitute the right value into $P(x)$. (It follows directly from the relationship above: if $D(x)=x-a$, then at $x=a$, $D(a)=0$, so $P(a)=Q(a)\cdot 0+R=R$ — the remainder, whatever it is, is exactly $P(a)$.)

## The Factor Theorem

If the remainder above happens to be zero, then the divisor must be an exact factor of $P(x)$. This gives the **factor theorem**:

> If $P(a)=0$, then $(x-a)$ is a factor of $P(x)$.
> If $(ax+b)$ is a factor of $P(x)$, then $P\!\left(-\dfrac{b}{a}\right)=0$.

**Useful shortcut:** if $(x-a)$ is a factor of $P(x)$ and $a$ is an integer, then $a$ must divide the constant term of $P(x)$ exactly. For example, $(x-2)$ could be a factor of $x^3-2x^2-x+2$ (constant term $2$, divisible by $2$) — and checking confirms it: $P(2)=8-8-2+2=0$. But $(x+3)$ could *not* be a factor of this polynomial, since $3$ does not divide $2$. This narrows down which values are worth testing instead of guessing blindly, and is exactly the shortcut used to factorise a cubic in [[Cubic Functions]].

**Exercise 12.** Is $D(x)=(x-3)$ a factor of $P(x)=2x^3-4x^2-3x-8$?

By the factor theorem, test $P(3)$:

$$P(3)=2(3)^3-4(3)^2-3(3)-8=54-36-9-8=1$$

Since $P(3)=1\neq0$, $(x-3)$ is **not** a factor of $P(x)$.

## Homework Exercise: Division with a Negative Leading Divisor

**Exercise E2.** $P(x)=x^3+x^4-3+2x^2$ is divided by $D(x)=3-x$. Find $Q(x)$ and $R(x)$.

*(question text reconstructed from working — check original if this seems off)*

Rewrite $P(x)$ in descending order: $P(x)=x^4+x^3+2x^2+0x-3$. The divisor $3-x=-x+3$ has a *negative* leading coefficient, so divide exactly as in the opening worked example above:

$$
\begin{array}{r}
-x^3-4x^2-14x-42\phantom{00}\\
-x+3{\big)}\ x^4+x^3+2x^2+0x-3\phantom{00}\\
\underline{x^4-3x^3\phantom{+2x^2+0x-3..}}\phantom{0}\\
4x^3+2x^2+0x-3\phantom{0}\\
\underline{4x^3-12x^2\phantom{+0x-3..}}\phantom{0}\\
14x^2+0x-3\phantom{0}\\
\underline{14x^2-42x\phantom{-3..}}\phantom{0}\\
42x-3\phantom{0}\\
\underline{42x-126}\\
123
\end{array}
$$

So $Q(x)=-x^3-4x^2-14x-42$ and $R(x)=123$.

(Check: expand $Q(x)\cdot D(x)+R(x) = (-x^3-4x^2-14x-42)(3-x)+123$. Multiplying out gives $x^4+x^3+2x^2+0x-126$, and adding $123$ gives $x^4+x^3+2x^2-3$ — exactly $P(x)$ ✓.)

For more mixed practice across all the Unit 1 function topics, see [[Functions - Practice and Revision]]. For the factor theorem applied to fully factorise and solve a cubic equation, see [[Cubic Functions]].
