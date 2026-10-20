# Binomial Theorem

Expanding a bracket like $(x+a)^n$ by multiplying it out by hand becomes impractical once $n$ gets large. The **binomial theorem** gives a direct formula for every term of the expansion without multiplying anything out: the coefficients follow a simple triangular number pattern (**Pascal's triangle**), and the powers of $x$ and $a$ in each term follow a predictable pattern too.

## Key Formulas

| Concept | Formula |
|---|---|
| Binomial theorem | $(x+a)^n = \displaystyle\sum_{k=0}^{n}\dbinom{n}{k}x^{n-k}a^k$ |
| General term (the $(k{+}1)$-th term) | $T_{k+1} = \dbinom{n}{k}x^{n-k}a^k$ |
| Binomial coefficient | $\dbinom{n}{k} = \dfrac{n!}{k!\,(n-k)!}$ |
| Pascal's triangle recurrence | $\dbinom{n}{k} = \dbinom{n-1}{k-1}+\dbinom{n-1}{k}$ |
| Number of terms in the expansion | $n+1$ |

## Building the Pattern: Expanding $(x+a)^n$ for Small $n$

Multiplying out directly for the first few powers:

$$(x+a)^0 = 1$$
$$(x+a)^1 = x+a$$
$$(x+a)^2 = x^2+2xa+a^2$$
$$(x+a)^3 = x^3+3x^2a+3xa^2+a^3$$
$$(x+a)^4 = x^4+4x^3a+6x^2a^2+4xa^3+a^4$$

Looking only at the **coefficients** of each expansion:

$$1 \qquad 1\ 1 \qquad 1\ 2\ 1 \qquad 1\ 3\ 3\ 1 \qquad 1\ 4\ 6\ 4\ 1$$

these are exactly the rows of **Pascal's triangle**. Writing $(x+a)^4$ with its coefficients made explicit:

$$(x+a)^4 = 1(x)^4(a)^0+4(x)^3(a)^1+6(x)^2(a)^2+4(x)^1(a)^3+1(x)^0(a)^4$$

shows the pattern that holds for *any* power $n$: the power of $x$ starts at $n$ and drops by $1$ each term down to $0$, the power of $a$ starts at $0$ and rises by $1$ each term up to $n$ (so the two powers always add to $n$), and the coefficient of each term is the matching entry in row $n$ of Pascal's triangle.

## Pascal's Triangle

$$
\begin{array}{c}
1\\
1\quad 1\\
1\quad 2\quad 1\\
1\quad 3\quad 3\quad 1\\
1\quad 4\quad 6\quad 4\quad 1\\
1\quad 5\quad 10\quad 10\quad 5\quad 1
\end{array}
$$

(rows $n=0$ to $n=5$.) Every row starts and ends in $1$ — there's only one way to choose "all $x$'s" (every bracket contributes $x$) or "all $a$'s". Every interior entry is the sum of the two entries diagonally above it, because choosing $k$ copies of $a$ (and $n-k$ copies of $x$) out of $n$ brackets splits into two cases: either the *last* bracket contributes an $x$ (leaving $k$ to be chosen from the remaining $n-1$ brackets) or it contributes an $a$ (leaving only $k-1$ to be chosen from the remaining $n-1$). That is exactly the recurrence $\dbinom{n}{k}=\dbinom{n-1}{k-1}+\dbinom{n-1}{k}$.

**Example — expand $(x+a)^5$.** Using row $5$ of Pascal's triangle ($1,5,10,10,5,1$):

$$(x+a)^5 = 1(x^5)(a^0)+5(x^4)(a^1)+10(x^3)(a^2)+10(x^2)(a^3)+5(x^1)(a^4)+1(x^0)(a^5)$$

$$= x^5+5x^4a+10x^3a^2+10x^2a^3+5xa^4+a^5$$

## Worked Example 1 — Expand $(2x-3)^4$

Apply the binomial theorem with "$x$" replaced by $2x$ and "$a$" replaced by $-3$, using row $4$ of Pascal's triangle ($1,4,6,4,1$):

$$(2x-3)^4 = 1(2x)^4(-3)^0+4(2x)^3(-3)^1+6(2x)^2(-3)^2+4(2x)^1(-3)^3+1(2x)^0(-3)^4$$

Evaluating each term separately:

$$
\begin{aligned}
1(2x)^4(-3)^0 &= 1\cdot16x^4\cdot1 = 16x^4\\
4(2x)^3(-3)^1 &= 4\cdot8x^3\cdot(-3) = -96x^3\\
6(2x)^2(-3)^2 &= 6\cdot4x^2\cdot9 = 216x^2\\
4(2x)^1(-3)^3 &= 4\cdot2x\cdot(-27) = -216x\\
1(2x)^0(-3)^4 &= 1\cdot1\cdot81 = 81
\end{aligned}
$$

Adding these together:

$$(2x-3)^4 = 16x^4-96x^3+216x^2-216x+81$$

## Worked Example 2 — Expand $\left(\dfrac{2}{x^2}+x\right)^5$

Using row $5$ of Pascal's triangle ($1,5,10,10,5,1$), with "$x$" replaced by $\dfrac{2}{x^2}$ and "$a$" replaced by $x$ — so the power of $\dfrac{2}{x^2}$ decreases from $5$ to $0$ while the power of $x$ increases from $0$ to $5$:

$$\left(\frac{2}{x^2}+x\right)^5 = 1\left(\frac{2}{x^2}\right)^5(x)^0+5\left(\frac{2}{x^2}\right)^4(x)^1+10\left(\frac{2}{x^2}\right)^3(x)^2+10\left(\frac{2}{x^2}\right)^2(x)^3+5\left(\frac{2}{x^2}\right)^1(x)^4+1\left(\frac{2}{x^2}\right)^0(x)^5$$

Evaluating each term:

$$
\begin{aligned}
1\left(\frac{2}{x^2}\right)^5(x)^0 &= \frac{32}{x^{10}}\\[4pt]
5\left(\frac{2}{x^2}\right)^4(x)^1 &= 5\cdot\frac{16}{x^8}\cdot x = \frac{80}{x^7}\\[4pt]
10\left(\frac{2}{x^2}\right)^3(x)^2 &= 10\cdot\frac{8}{x^6}\cdot x^2 = \frac{80}{x^4}\\[4pt]
10\left(\frac{2}{x^2}\right)^2(x)^3 &= 10\cdot\frac{4}{x^4}\cdot x^3 = \frac{40}{x}\\[4pt]
5\left(\frac{2}{x^2}\right)^1(x)^4 &= 5\cdot\frac{2}{x^2}\cdot x^4 = 10x^2\\[4pt]
1\left(\frac{2}{x^2}\right)^0(x)^5 &= x^5
\end{aligned}
$$

So, fully simplified:

$$\left(\frac{2}{x^2}+x\right)^5 = x^5+10x^2+\frac{40}{x}+\frac{80}{x^4}+\frac{80}{x^7}+\frac{32}{x^{10}}$$

Each line above is also an instance of the **general term** formula, $T_{k+1}=\dbinom{5}{k}\left(\dfrac{2}{x^2}\right)^{5-k}x^k$ — useful when only *one particular term* of an expansion is wanted (for example "find the term in $x^2$") without expanding the whole bracket: you just need the value of $k$ that makes the powers work out, then evaluate that single term.

---

For further practice, see [[Functions - Practice and Revision]].
