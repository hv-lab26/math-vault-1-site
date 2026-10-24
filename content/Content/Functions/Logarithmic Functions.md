# Logarithmic Functions

A logarithm answers the question "what power do I need?" Specifically, $\log_a y$ is the power that $a$ must be raised to in order to get $y$. Because of this, the logarithm function $\log_a x$ is defined as the **inverse** of the exponential function $a^x$ (see [[Inverse Functions]]): one undoes the other.

$$a^x = y \quad\Longleftrightarrow\quad \log_a(y) = x \qquad (a>0,\ a\mathrel{\char"2260}1,\ y>0)$$

Applying the swap-$x$-and-$y$ method from [[Inverse Functions]] to $y=a^x$ gives exactly this: swapping produces $x=a^y$, and solving for $y$ (by definition) gives $y=\log_a x$ — so $\log_a x$ and $a^x$ are genuinely inverse functions of one another, not just related by coincidence.

## Key Facts and Formulas

| Law | Statement |
|---|---|
| Definition | $a^x=y \iff \log_a y = x$ |
| Product law | $\log_a(mn) = \log_a m + \log_a n$ |
| Quotient law | $\log_a\!\left(\dfrac{m}{n}\right) = \log_a m - \log_a n$ |
| Power law | $\log_a(m^p) = p\log_a m$ |
| Change of base | $\log_b N = \dfrac{\log_a N}{\log_a b}$, most often used as $\log_b N = \dfrac{\log_{10} N}{\log_{10} b}$ |
| Special values | $\log_a 1 = 0$ (since $a^0=1$); $\log_a a = 1$ (since $a^1=a$) |
| Domain | $\log_a x$ is defined only for $x>0$ |
| Natural log | $\log_e x$ is written $\ln x$; $e \approx 2.71828$ |

## The Exponential–Logarithm Relationship

The source page sketches the graph of $y=e^x$: it rises from the lower left, passing through $(0,1)$, flattening as $x\to-\infty$ to a horizontal asymptote at $y=0$ (the curve gets arbitrarily close to the $x$-axis but never reaches or crosses it), and increasing steeply, without bound, as $x$ grows. It is defined for every real $x$ and is always positive.

Since $\log_a x$ is the inverse of $a^x$, its graph is the reflection of the exponential graph in the line $y=x$ (as in [[Inverse Functions]]), which swaps the domain/range and the intercept/asymptote:

| Feature | $y=a^x$ ($a>1$) | $y=\log_a x$ ($a>1$) |
|---|---|---|
| Domain | all real $x$ | $x>0$ |
| Range | $y>0$ | all real $y$ |
| Intercept | $(0,1)$ | $(1,0)$, since $\log_a 1=0$ |
| Asymptote | horizontal, $y=0$ | vertical, $x=0$ (the $y$-axis) |
| Shape | increasing, curving upward, growing faster and faster | increasing, curving downward, growing slower and slower |

This also explains the **domain restriction for logs**: because $a^x$ can only ever output a positive number, its inverse $\log_a x$ can only ever accept a positive number as input. $\log_a x$ is simply undefined for $x \le 0$ — this shows up repeatedly below, whenever a solution to a log equation has to be rejected.

## Why the Log Laws Work

Each law follows directly from the index laws, by writing logarithms as exponents. Let $p=\log_a m$ and $q=\log_a n$, so by definition $a^p=m$ and $a^q=n$.

- **Product law:** $mn = a^p a^q = a^{p+q}$, so $\log_a(mn) = p+q = \log_a m + \log_a n$.
- **Quotient law:** $\dfrac{m}{n} = \dfrac{a^p}{a^q} = a^{p-q}$, so $\log_a\!\left(\dfrac{m}{n}\right) = p-q = \log_a m - \log_a n$.
- **Power law:** $m^k = (a^p)^k = a^{pk}$, so $\log_a(m^k) = pk = k\log_a m$.
- **Change of base:** let $y=\log_b N$, so $b^y=N$. Taking $\log_a$ of both sides and applying the power law: $\log_a(b^y) = \log_a N \Rightarrow y\log_a b = \log_a N \Rightarrow y = \dfrac{\log_a N}{\log_a b}$.

## Worked Examples: Simplifying Logarithmic Expressions

**Example 1.** Simplify $\log_{10}5+\log_{10}2$ (without a calculator).

$$\log_{10}5+\log_{10}2 = \log_{10}(5\times2) = \log_{10}10 = 1$$

**Example 2.** Simplify $\log_4 20 - \log_4 5$.

$$\log_4 20-\log_4 5 = \log_4\!\left(\dfrac{20}{5}\right) = \log_4 4 = 1$$

**Example 3.** Simplify $\log_2 16$.

$$\log_2 16 = \log_2(2^4) = 4\log_2 2 = 4\times1 = 4$$

**Example 4.** Simplify $\log_5 \sqrt[5]{x}$.

$$\log_5\sqrt[5]{x} = \log_5 x^{1/5} = \dfrac15\log_5 x$$

**Example 5.** Simplify $\log_3 27+\log_3 9-\log_3 81$.

$$
\begin{aligned}
\log_3 27+\log_3 9-\log_3 81 &= \log_3 3^3+\log_3 3^2-\log_3 3^4\\
&= 3\log_3 3+2\log_3 3-4\log_3 3\\
&= 3+2-4 = 1
\end{aligned}
$$

**Example 6.** Simplify $2+\log_{10}3$.

$$
\begin{aligned}
2+\log_{10}3 &= 2\log_{10}10+\log_{10}3 &&\text{(since $\log_{10}10=1$)}\\
&= \log_{10}(10^2\times3)\\
&= \log_{10}300
\end{aligned}
$$

**Example 7.** Simplify $3\log_3 6-3\log_3 18$.

$$
\begin{aligned}
3\log_3 6-3\log_3 18 &= \log_3 6^3-\log_3 18^3 &&\text{(power law)}\\
&= \log_3\!\left(\dfrac{6^3}{18^3}\right) = \log_3\!\left(\dfrac{6}{18}\right)^{\!3} = \log_3\!\left(\dfrac{1}{3^3}\right)\\
&= \log_3 3^{-3}\\
&= -3\log_3 3 = -3
\end{aligned}
$$

**Example 8.** Simplify $\dfrac{\log_3 9}{\log_3 27}$.

$$\dfrac{\log_3 9}{\log_3 27} = \dfrac{\log_3 3^2}{\log_3 3^3} = \dfrac{2\log_3 3}{3\log_3 3} = \dfrac{2}{3}$$

**Example 9 — change of base in practice.** Find the value of $\log_2 18$.

Since $18$ is not a power of $2$, this can't be simplified by inspection — the change of base law converts it into a form a calculator can evaluate directly:

$$\log_2 18 = \dfrac{\log_{10}18}{\log_{10}2} \approx \dfrac{1.2553}{0.3010} \approx 4.170$$

## Solving Exponential Equations

To solve an equation with the unknown in the exponent, take $\log_e$ (or any convenient log) of both sides, then use the power law to bring the exponent down.

**Example 10.** Solve $e^{3x}=e$.

Since both sides already share the base $e$ (and $e=e^1$), the exponents can be compared directly:

$$e^{3x}=e^1 \iff 3x=1 \iff x=\dfrac13$$

**Example 11.** Solve $e^x=3$.

$$
\begin{aligned}
e^x &= 3\\
\log_e e^x &= \log_e 3\\
x\log_e e &= \log_e 3 &&\text{(power law)}\\
x &= \log_e 3 \approx 1.099 &&\text{(since $\log_e e=1$)}
\end{aligned}
$$

**Example 12 (Practice).** Solve $e^{2x+1}=3$.

$$
\begin{aligned}
e^{2x+1} &= 3\\
\log_e e^{2x+1} &= \log_e 3\\
(2x+1)\log_e e &= \log_e 3\\
2x+1 &= \log_e 3\\
x &= \dfrac{\log_e 3 - 1}{2} \approx \dfrac{1.0986-1}{2} \approx 0.049
\end{aligned}
$$

**Example 13.** Solve $e^{x(x-1)}=10^3$.

$$
\begin{aligned}
e^{x(x-1)} &= 10^3\\
x(x-1) &= \log_e 10^3 &&\text{(taking $\log_e$ of both sides)}\\
x^2-x &= 3\log_e 10 &&\text{(power law; $x(x-1)=x^2-x$)}\\
x^2-x-3\log_e 10 &= 0
\end{aligned}
$$

This is a quadratic in $x$ (see [[Quadratic Functions]] for the method). With $3\log_e10 \approx 6.9078$:

$$x = \dfrac{1\pm\sqrt{1+4(6.9078)}}{2} = \dfrac{1\pm\sqrt{28.631}}{2} = \dfrac{1\pm5.3508}{2}$$

$$x_1 \approx -2.175 \qquad x_2 \approx 3.175$$

Both are valid here — unlike the logarithmic equations further below, there's no "$\log$ of a negative number" issue to check, since the *original* equation only ever takes $e$ to a power (always defined, for any real exponent).

## Exponential Equations That Reduce to a Quadratic

When an equation contains both $e^x$ and $e^{-x}$, rewriting $e^{-x}=\dfrac{1}{e^x}$ and substituting $a=e^x$ turns it into an ordinary quadratic in $a$ (see [[Quadratic Functions]]). Because $e^x>0$ for every real $x$, any root $a\le0$ must be **rejected** at the end — it doesn't correspond to a real value of $x$.

**Example 14 (Worked Example 26).** Solve $e^x-3e^{-x}=2$.

$$
\begin{aligned}
e^x-3e^{-x} &= 2\\
e^x - \dfrac{3}{e^x} &= 2 &&\text{(rewrite $e^{-x}$)}\\
(e^x)^2-3 &= 2e^x &&\text{(multiply every term by $e^x$)}\\
(e^x)^2-2e^x-3 &= 0
\end{aligned}
$$

Let $a=e^x$: $\quad a^2-2a-3=0 \iff (a-3)(a+1)=0 \iff a=3 \text{ or } a=-1$.

- $a=3 \Rightarrow e^x=3 \Rightarrow x=\log_e 3 \approx 1.099$
- $a=-1 \Rightarrow e^x=-1$ — **no solution**, since $e^x$ is never negative.

**Example 15.** Solve $2+e^x-4e^{-x}=0$.

$$
\begin{aligned}
2+e^x-\dfrac{4}{e^x} &= 0\\
2e^x+(e^x)^2-4 &= 0 &&\text{(multiply every term by $e^x$)}\\
(e^x)^2+2e^x-4 &= 0
\end{aligned}
$$

Let $a=e^x$: $\quad a^2+2a-4=0$. Discriminant: $\Delta = b^2-4ac = 2^2-4(1)(-4) = 4+16 = 20$.

$$a = \dfrac{-2\pm\sqrt{20}}{2}$$

- $a_1 = \dfrac{-2+\sqrt{20}}{2} \approx \dfrac{-2+4.4721}{2} \approx 1.236 = e^x \;\Rightarrow\; x = \log_e(1.236) \approx 0.212$
- $a_2 = \dfrac{-2-\sqrt{20}}{2} \approx -3.236 = e^x$ — **no solution**, since this is negative.

## Solving Logarithmic Equations

The strategy is the reverse: combine all logs into a single log term using the laws, then convert back to exponential form using the definition $\log_a b = x \iff a^x = b$ (noting $b$ must come out positive — any solution that fails this is **extraneous** and must be rejected).

**Example 16.** Solve $\log_2 4+\log_2 x-\log_2 8=3$.

$$
\begin{aligned}
\log_2 4+\log_2 x-\log_2 8 &= 3\\
\log_2\!\left(\dfrac{4x}{8}\right) &= 3\\
\log_2\!\left(\dfrac{x}{2}\right) &= 3\\
2^3 &= \dfrac{x}{2}\\
8 &= \dfrac{x}{2} \;\Rightarrow\; x=16
\end{aligned}
$$

*Check:* $\log_2 4+\log_2 16-\log_2 8 = 2+4-3 = 3$. ✓

**Example 17.** Solve $\log_{10}x+\log_{10}(x-3)=\log_{10}4$.

$$
\begin{aligned}
\log_{10}x+\log_{10}(x-3) &= \log_{10}4\\
\log_{10}\!\left(\dfrac{x(x-3)}{4}\right) &= 0\\
\log_{10}\!\left(\dfrac{x^2-3x}{4}\right) &= 0\\
10^0 = 1 &= \dfrac{x^2-3x}{4}\\
x^2-3x-4 &= 0\\
(x-4)(x+1) &= 0 \;\Rightarrow\; x=4 \text{ or } x=-1
\end{aligned}
$$

$x=-1$ is **rejected**: the original equation needs $\log_{10}x$ and $\log_{10}(x-3)$ both defined, which requires $x>0$ *and* $x>3$ simultaneously — $x=-1$ satisfies neither. So the only valid solution is $\boxed{x=4}$. *Check:* $\log_{10}4+\log_{10}1 = \log_{10}4+0=\log_{10}4$. ✓

**Example 18.** Solve $\log_e x=3$.

$$\log_e x = 3 \iff e^3 = x \iff x \approx 20.0855$$

**Example 19.** Solve $\log_e x+\log_e 3=\log_e 6$.

$$
\begin{aligned}
\log_e x+\log_e 3 &= \log_e 6\\
\log_e(3x) &= \log_e 6\\
3x &= 6 \;\Rightarrow\; x=2
\end{aligned}
$$

## Application: Exponential Decay

**Example 20.** *A quantity decays according to the model $D=10000e^{-0.223t}$, where $t$ is time in years. (d) After how many years has $D$ fallen to half its initial value? (e) After how many years has it fallen to $100$? (f) After how many years has it fallen to $350$? What is the initial quantity?* *(question text reconstructed from working — check original if this seems off; parts (a)–(c), which likely set up this model, are not in the scanned pages)*

**(d) Halving ($D=5000$):**

$$
\begin{aligned}
10000e^{-0.223t} &= 5000\\
e^{-0.223t} &= 0.5\\
\log_e e^{-0.223t} &= \log_e 0.5\\
-0.223t\log_e e &= \log_e 0.5\\
-0.223t &= \log_e 0.5\\
t &= \dfrac{\log_e 0.5}{-0.223} \approx \dfrac{-0.6931}{-0.223} \approx 3.108
\end{aligned}
$$

**About 3 years.**

**(e) $D=100$:**

$$
\begin{aligned}
10000e^{-0.223t} &= 100\\
e^{-0.223t} &= 0.01\\
\log_e 0.01 &= -0.223t\\
t &= \dfrac{\log_e 0.01}{-0.223} \approx \dfrac{-4.6052}{-0.223} \approx 20.651
\end{aligned}
$$

**About 21 years.**

**(f) $D=350$:**

$$
\begin{aligned}
10000e^{-0.223t} &= 350\\
e^{-0.223t} &= 0.035\\
\log_e 0.035 &= -0.223t\\
t &= \dfrac{\log_e 0.035}{-0.223} \approx 15.033
\end{aligned}
$$

**About 15 years.**

**Initial quantity:** setting $t=0$ gives $D=10000e^{0}=10000\times1=10000$ — confirming the $10000$ in the model *is* the initial quantity, consistent with every part above.

---

For solving the quadratics that show up when substituting $a=e^x$, see [[Quadratic Functions]]. For the general method of finding and working with inverse functions (of which $\log_a x$ and $a^x$ are the key example here), see [[Inverse Functions]]. For more practice, see [[Functions - Practice and Revision]].
