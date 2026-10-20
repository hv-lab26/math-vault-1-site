# Trigonometric Functions

A trigonometric function assigns, to every angle, a ratio defined using the unit circle — extending sine, cosine and tangent beyond the "opposite/adjacent/hypotenuse" ratios of a right triangle (which only make sense for angles between $0°$ and $90°$) to *every* real angle, including negative angles and angles beyond $360°$. This note covers angle measurement in radians, the unit-circle definitions, using symmetry to evaluate a trig ratio at any angle from a "reference angle", solving trigonometric equations, and sketching sine/cosine graphs.

## Key Formulas and Summary

| Concept | Formula / Rule |
|---|---|
| Degree–radian conversion | $180° = \pi$ rad, so $1$ rad $= \dfrac{180°}{\pi}\approx57.3°$ |
| Unit circle point at angle $\theta$ | $(x,y) = (\cos\theta,\ \sin\theta)$ |
| Tangent | $\tan\theta = \dfrac{\sin\theta}{\cos\theta}$ |
| Quadrant signs (ASTC) | QI all $+$, QII sin $+$, QIII tan $+$, QIV cos $+$ |
| Negative angles | $\sin(-\alpha)=-\sin\alpha$, $\cos(-\alpha)=\cos\alpha$, $\tan(-\alpha)=-\tan\alpha$ |
| General solution, $\sin\theta=\sin\alpha$ | $\theta=\alpha+2k\pi$ or $\theta=(\pi-\alpha)+2k\pi$ |
| General solution, $\cos\theta=\cos\alpha$ | $\theta=\pm\alpha+2k\pi$ |
| General solution, $\tan\theta=\tan\alpha$ | $\theta=\alpha+k\pi$ |
| Sinusoidal graph | $y=a\sin(bx+c)+d$ (or $\cos$): amplitude $\lvert a\rvert$, period $\dfrac{2\pi}{\lvert b\rvert}$, vertical shift $d$ |

## 1. Radians and the Unit Circle

A **radian** is an alternative unit for measuring angles, defined so that one full revolution ($360°$) equals $2\pi$ radians. Halving this gives the standard conversion:

$$180° = \pi\ \text{rad} \qquad\Longrightarrow\qquad 1\ \text{rad} = \frac{180°}{\pi}\approx57.3°$$

(A small raised "$^{c}$", as in $1^{c}$, is sometimes used as shorthand for "$1$ radian" — short for *circular measure*.)

On the **unit circle** (radius $1$, centred at the origin), an angle $\theta$ is measured anticlockwise from the positive $x$-axis. The point where its terminal ray meets the circle has coordinates

$$(x,y) = (\cos\theta,\ \sin\theta)$$

— this *is* the definition of sine and cosine for every real angle $\theta$, not just acute ones. Tangent is then defined as the ratio

$$\tan\theta = \frac{\sin\theta}{\cos\theta} = \frac{y}{x}$$

**Example.** Find the coordinates of the point on the unit circle at $\theta=315°$.

Convert to radians first: $315° = \dfrac{315}{180}\pi = \dfrac{7\pi}{4}$.

Since $x=\cos\theta$ and $y=\sin\theta$:

$$(x,y) = (\cos315°,\ \sin315°)$$

$315° = 360°-45°$ lies in the fourth quadrant, just before completing a full turn, so $45°$ is the reference angle: $\cos315°=\cos45°=\dfrac{\sqrt2}{2}$ (cosine is positive in quadrant IV) and $\sin315°=-\sin45°=-\dfrac{\sqrt2}{2}$ (sine is negative in quadrant IV).

$$(x,y) = \left(\frac{\sqrt2}{2},\ -\frac{\sqrt2}{2}\right)$$

## 2. Quadrant Signs — the ASTC Rule

Since $x=\cos\theta$ and $y=\sin\theta$, the sign of each ratio simply follows the sign of the matching coordinate in that quadrant of the unit circle:

| Quadrant | Angle range | Positive ratio(s) | Why |
|---|---|---|---|
| I | $0\to\dfrac\pi2$ ($0°\to90°$) | **A**ll (sin, cos, tan) | $x>0,\ y>0$ |
| II | $\dfrac\pi2\to\pi$ ($90°\to180°$) | **S**ine only | $x<0,\ y>0$ |
| III | $\pi\to\dfrac{3\pi}2$ ($180°\to270°$) | **T**angent only | $x<0,\ y<0$ (so $y/x>0$) |
| IV | $\dfrac{3\pi}2\to2\pi$ ($270°\to360°$) | **C**osine only | $x>0,\ y<0$ |

This is the standard "**A**ll **S**tudents **T**ake **C**alculus" (ASTC/CAST) memory aid, read anticlockwise starting from quadrant I.

## 3. Reference Angles and Reduction Formulas

Every angle outside the first quadrant has a **reference angle** $\theta$ — the acute angle between its terminal ray and the nearest $x$-axis — and its sine, cosine and tangent are just $\pm$ the sine, cosine and tangent of that reference angle, with the sign fixed by the ASTC rule:

| Quadrant | Angle (in terms of reference angle $\theta$) | $\sin$ | $\cos$ | $\tan$ |
|---|---|---|---|---|
| II | $\pi-\theta$ | $\sin\theta$ | $-\cos\theta$ | $-\tan\theta$ |
| III | $\pi+\theta$ | $-\sin\theta$ | $-\cos\theta$ | $\tan\theta$ |
| IV | $2\pi-\theta$ | $-\sin\theta$ | $\cos\theta$ | $-\tan\theta$ |

**Example — $\sin150°$.** $150°$ sits in quadrant II, with reference angle $180°-150°=30°$:

$$\sin(150°) = \sin(180°-150°) = \sin30° = \frac12$$

**Example — $\cos\dfrac{5\pi}{4}$.** $\dfrac{5\pi}{4}$ sits in quadrant III (between $\pi$ and $\dfrac{3\pi}2$), with reference angle $\dfrac{5\pi}4-\pi=\dfrac\pi4$. Cosine is negative in quadrant III:

$$\cos\frac{5\pi}{4} = -\cos\frac\pi4 = -\frac{\sqrt2}{2}$$

**Example — $\sin\dfrac{7\pi}{6}$.** $\dfrac{7\pi}{6}=\pi+\dfrac\pi6$ sits in quadrant III, reference angle $\dfrac\pi6$:

$$\sin\frac{7\pi}{6} = \sin\left(\pi+\frac\pi6\right) = -\sin\frac\pi6 = -\frac12$$

## 4. Negative Angles

A negative angle means rotating *clockwise* from the positive $x$-axis instead of anticlockwise. Geometrically, the point for angle $-\alpha$ is the reflection of the point for $\alpha$ across the $x$-axis: the $x$-coordinate (cosine) stays the same, but the $y$-coordinate (sine) flips sign. This gives two symmetry rules:

$$\sin(-\alpha) = -\sin\alpha \qquad\text{(sine is an odd function)}$$
$$\cos(-\alpha) = \cos\alpha \qquad\text{(cosine is an even function)}$$

and since $\tan\alpha=\dfrac{\sin\alpha}{\cos\alpha}$:

$$\tan(-\alpha) = \frac{\sin(-\alpha)}{\cos(-\alpha)} = \frac{-\sin\alpha}{\cos\alpha} = -\tan\alpha \qquad\text{(tangent is also odd)}$$

These let any negative-angle problem be converted straight back into a positive-angle one, solved exactly as above using the same reference-angle method.

**Example — $\cos(240°)$.** (A reference-angle example in its own right, reused below.) $240°=180°+60°$ lies in quadrant III, reference angle $60°$:

$$\cos(240°) = \cos(180°+60°) = -\cos(60°) = -\frac12$$

**Example — $\sin(-135°)$.**

$$\sin(-135°) = -\sin(135°)\qquad\text{(odd property)}$$

$135°=180°-45°$ lies in quadrant II, reference angle $45°$:

$$\sin(135°) = \sin(180°-45°) = \sin(45°) = \frac{\sqrt2}{2} \qquad\Rightarrow\qquad \sin(-135°) = -\frac{\sqrt2}{2}$$

**Example — $\cos(-225°)$.**

$$\cos(-225°) = \cos(225°)\qquad\text{(even property)}$$

$225°=180°+45°$ lies in quadrant III, reference angle $45°$:

$$\cos(225°) = \cos(180°+45°) = -\cos(45°) = -\frac{\sqrt2}{2} \qquad\Rightarrow\qquad \cos(-225°) = -\frac{\sqrt2}{2}$$

**Example — $\cos(-240°)$.** By the same even property, this reduces straight to the $\cos(240°)$ example above:

$$\cos(-240°) = \cos(240°) = -\frac12$$

**Example — $\tan(-330°)$.**

$$\tan(-330°) = -\tan(330°)\qquad\text{(odd property)}$$

$330°=360°-30°$ lies in quadrant IV, reference angle $30°$:

$$\tan(330°) = \tan(360°-30°) = -\tan(30°) = -\frac{\sqrt3}{3}$$

$$\Rightarrow\qquad \tan(-330°) = -\left(-\frac{\sqrt3}{3}\right) = \frac{\sqrt3}{3}$$

## 5. Periodicity

Sine and cosine repeat every $2\pi$ (a full revolution brings you back to the same point on the unit circle), while tangent repeats every $\pi$:

$$\sin(\theta+2k\pi)=\sin\theta,\qquad\cos(\theta+2k\pi)=\cos\theta,\qquad\tan(\theta+k\pi)=\tan\theta\qquad(k\in\mathbb Z)$$

**Worked Example.** Given $\sin x=0.6$, $\cos x=0.8$, with $x$ in the first quadrant (so every ratio of $x$ itself is positive), find:

**(a)** $\sin(3\pi-x)$

$$\sin(3\pi-x) = \sin\big(2\pi+(\pi-x)\big) = \sin(\pi-x)\quad\text{(periodicity removes the extra }2\pi\text{)}$$
$$=\sin x\quad\text{(quadrant II reduction formula)}$$
$$=0.6$$

**(b)** $\cos(4\pi+x)$

Since $4\pi$ is exactly two full periods of cosine:

$$\cos(4\pi+x) = \cos(0+x) = \cos x = 0.8$$

## 6. Solving Trigonometric Equations

The general method:

1. **Isolate** the trig ratio — get the equation into the form $\sin x=\ldots$, $\cos x=\ldots$, or $\tan x=\ldots$.
2. Find the **reference angle**: the positive, acute angle given by the inverse trig function applied to the *size* of the ratio (ignoring its sign).
3. Use the **ASTC rule** to decide *which quadrants* the actual solutions lie in, based on whether the ratio is positive or negative.
4. Build each quadrant's solution from the reference angle, using the reduction formulas above.
5. If the given domain covers more than one revolution, add whole multiples of the period ($2\pi$ for sin/cos, $\pi$ for tan) to generate the remaining solutions.

**Example — $\sin x=\dfrac{\sqrt3}{2}$, for $x\in[0,2\pi)$.**

Reference angle: $\sin^{-1}\left(\dfrac{\sqrt3}{2}\right)=\dfrac\pi3$. The ratio is **positive**, so $x$ lies in quadrants I or II:

$$x=\frac\pi3 \quad\text{or}\quad x=\pi-\frac\pi3=\frac{2\pi}{3}$$

**Worked Example — $\cos x=-\dfrac{\sqrt2}{2}$, for $x\in[0,2\pi]$.**

- *Step 1:* find the reference angle using the **positive** version of the ratio: $\cos^{-1}\left(\dfrac{\sqrt2}{2}\right)$.
- *Step 2:* this equals $\dfrac\pi4$.
- *Step 3:* the ratio is **negative**, so $x$ lies in quadrants II or III (where cosine is negative): $x=\pi\pm\dfrac\pi4$.

$$x=\pi-\frac\pi4=\frac{3\pi}{4} \qquad\text{or}\qquad x=\pi+\frac\pi4=\frac{5\pi}{4}$$

The same equation can turn up in disguise after a little algebra:

**Worked Example — $\sqrt2\cos x+1=0$, for $x\in[0,2\pi]$.**

$$\sqrt2\cos x=-1 \implies \cos x=-\frac{1}{\sqrt2}=-\frac{\sqrt2}{2}$$

— exactly the equation just solved above, so

$$x_{\text{ref}}=\frac\pi4,\qquad x=\pi-\frac\pi4=\frac{3\pi}{4}\quad\text{or}\quad x=\pi+\frac\pi4=\frac{5\pi}{4}$$

### Extending Past One Revolution

**Worked Example — $\sin\alpha=0.7$, for $\alpha\in[0,4\pi]$.**

This domain covers *two* full revolutions, so solve on the first circle $[0,2\pi]$ and then shift by $2\pi$ for the second.

**First circle, $[0,2\pi]$:** reference angle $\alpha_1=\sin^{-1}(0.7)\approx0.7754$. Since $\sin\alpha>0$, $\alpha$ is in quadrants I and II:

$$\alpha_1\approx0.7754,\qquad \alpha_2=\pi-\alpha_1\approx2.3662$$

**Second circle, $[2\pi,4\pi]$:** add $2\pi\approx6.2832$ to each value found above:

$$\alpha_3=2\pi+\alpha_1\approx7.0586,\qquad \alpha_4=2\pi+\alpha_2\approx8.6494$$

So the full solution set is $\alpha\approx\{0.7754,\ 2.3662,\ 7.0586,\ 8.6494\}$.

### Equations With a Multiple Angle

When the equation involves $\sin(kx)$, $\cos(kx)$ etc. rather than a plain $x$, it helps to **substitute** $u=kx$, solve for $u$ over the correspondingly *widened* domain, and only divide by $k$ right at the end.

**Worked Example — $2\sin(2x)=-\sqrt3$, for $x\in[0°,360°]$.**

$$\sin(2x)=-\frac{\sqrt3}{2}$$

Let $u=2x$. Since $x\in[0°,360°]$, the new variable ranges over **two full revolutions**: $u\in[0°,720°]$.

Reference angle: $u_{\text{ref}}=\sin^{-1}\left(\dfrac{\sqrt3}2\right)=60°$. Since $\sin u<0$, $u$ must lie in quadrants III or IV, in *each* of the two revolutions covered:

**First revolution ($u\in[0°,360°]$):**

$$u_1=180°+60°=240° \qquad u_2=360°-60°=300°$$

**Second revolution ($u\in[360°,720°]$),** adding $360°$ to each:

$$u_3=240°+360°=600° \qquad u_4=300°+360°=660°$$

Converting back to $x=u/2$:

$$x_1=120°,\quad x_2=150°,\quad x_3=300°,\quad x_4=330°$$

**Worked Example — $\sin3x=\cos3x$, for $x\in[0,2\pi]$.**

Divide both sides by $\cos3x$. This step is valid here because $\sin\theta$ and $\cos\theta$ can never both be zero at the same angle — since $\sin^2\theta+\cos^2\theta=1$, that would force $0=1$ — so no solution is ever lost by dividing:

$$\frac{\sin3x}{\cos3x}=1 \implies \tan(3x)=1$$

Let $u=3x$. Since $x\in[0,2\pi]$, $u\in[0,6\pi]$ — **three** full periods of tangent (period $\pi$). The reference angle is $u_{\text{ref}}=\tan^{-1}(1)=\dfrac\pi4$, and since $\tan u>0$, solutions occur in quadrants I and III, repeating every $\pi$:

$$u=\frac\pi4+k\pi,\quad k=0,1,2,3,4,5\quad\text{(six values fit inside }[0,6\pi]\text{)}$$

$$u_1=\frac\pi4,\ u_2=\frac{5\pi}4,\ u_3=\frac{9\pi}4,\ u_4=\frac{13\pi}4,\ u_5=\frac{17\pi}4,\ u_6=\frac{21\pi}4$$

Dividing every value by $3$ to recover $x=u/3$:

$$x_1=\frac{\pi}{12},\quad x_2=\frac{5\pi}{12},\quad x_3=\frac{3\pi}{4},\quad x_4=\frac{13\pi}{12},\quad x_5=\frac{17\pi}{12},\quad x_6=\frac{7\pi}{4}$$

(Notice the six solutions are evenly spaced exactly $\dfrac\pi3$ apart. The period of $\tan(3x)$ as a function of $x$ is $\dfrac\pi3$ — one-third of tangent's usual period $\pi$ — because tripling the angle inside makes the function complete a cycle three times as fast.)

## 7. Graphs of Sine and Cosine

For the general sinusoidal function

$$y=a\sin(bx+c)+d \qquad(\text{or }y=a\cos(bx+c)+d)$$

- $\lvert a\rvert$ is the **amplitude** — the distance from the midline up to the peak (equivalently, half the vertical distance between the highest point $d+a$ and the lowest point $d-a$).
- the **period** is $P=\dfrac{2\pi}{\lvert b\rvert}$ — how much of the $x$-axis one complete cycle takes up.
- $d$ is the **vertical shift** (the height of the midline).
- $c$ controls the horizontal (phase) shift.

### $y=\sin x$

| Feature | Value |
|---|---|
| Domain | $\mathbb R$ |
| Range | $[-1,1]$ |
| Period | $2\pi$ |
| Amplitude | $1$ |
| Zeros | $x=0,\ \pi,\ 2\pi,\ \ldots$ |
| Maximum | $y=1$ at $x=\dfrac\pi2$ |
| Minimum | $y=-1$ at $x=\dfrac{3\pi}2$ |
| Symmetry | odd function, symmetric about the origin |

*Graph description:* starting at the origin, the curve rises to a peak of height $1$ at $x=\dfrac\pi2$, falls back through zero at $x=\pi$, continues down to a trough of $-1$ around $x=\dfrac{3\pi}2$, and returns to zero at $x=2\pi$ — one complete wave per $2\pi$.

### $y=\cos x$

| Feature | Value |
|---|---|
| Domain | $\mathbb R$ |
| Range | $[-1,1]$ |
| Period | $2\pi$ |
| Amplitude | $1$ |
| Zeros | $x=\dfrac\pi2,\ \dfrac{3\pi}2,\ \ldots$ |
| Maximum | $y=1$ at $x=0$ and $x=2\pi$ |
| Minimum | $y=-1$ at $x=\pi$ |
| Symmetry | even function, symmetric about the $y$-axis |

*Graph description:* the same wave shape as $\sin x$, shifted — it starts at its **maximum** $(0,1)$, falls through zero at $x=\dfrac\pi2$, reaches a minimum of $-1$ at $x=\pi$, rises back through zero at $x=\dfrac{3\pi}2$, and returns to its maximum at $x=2\pi$.

### Changing the Period: $y=\sin(2x)$

Doubling the angle inside halves the period:

$$P=\frac{2\pi}{2}=\pi$$

*Graph description:* one full wave now fits inside $[0,\pi]$ instead of $[0,2\pi]$ — rising to a peak just before $x=\dfrac\pi4$, crossing zero at $x=\dfrac\pi2$, dipping to a trough just before $x=\dfrac{3\pi}4$, and returning to zero exactly at $x=\pi$.

**Example — $y=2\sin\!\left(\dfrac14x\right)$.**

$$P=\frac{2\pi}{1/4}=8\pi,\qquad\text{Amplitude}=2$$

The small coefficient $b=\tfrac14$ stretches the graph horizontally (a much slower-repeating wave, one cycle every $8\pi$), while $a=2$ stretches it vertically (peaks reach $y=2$, troughs reach $y=-2$).

## 8. Finding the Roots of a Trigonometric Function

**Worked Example.** Find the roots of $y=\sin\!\left(x+\dfrac\pi4\right)$.

The roots are the $x$-values where $y=0$:

$$\sin\!\left(x+\frac\pi4\right)=0$$

Since $\sin\theta=0$ exactly when $\theta$ is a whole multiple of $\pi$:

$$x+\frac\pi4=k\pi\qquad(k\in\mathbb Z)$$
$$\Rightarrow\ x=k\pi-\frac\pi4$$

Restricting to one cycle, $x\in[0,2\pi)$: $k=1$ gives $x=\pi-\dfrac\pi4=\dfrac{3\pi}4$, and $k=2$ gives $x=2\pi-\dfrac\pi4=\dfrac{7\pi}4$ (while $k=0$ gives $x=-\dfrac\pi4$, just outside this interval).

$$x=\frac{3\pi}{4},\ \frac{7\pi}{4}\qquad\text{(within }[0,2\pi)\text{)}$$

---

Domain and range for trigonometric functions follow the same general ideas set out in [[Function Notation, Domain and Range]] — $\sin$ and $\cos$ are defined for every real input, with range $[-1,1]$, which is exactly what bounds the amplitude of any sinusoidal graph. For further practice, see [[Functions - Practice and Revision]].
