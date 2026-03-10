# Examples — Cauchy–Euler via Operator Method

## Core Substitution
[cite_start]For all examples, let $x = e^z$ or $z = \ln x$[cite: 25].
The operators transform as:
- $x y' = Dy$
- $x^2 y'' = D(D-1)y$
[cite_start]where $D = \frac{d}{dz}$[cite: 26].

---

## Example 4 — Non-Homogeneous (Linear RHS)
**Problem:** $x^2y'' + xy' - y = 24x$

### Step 1 — Operator Transformation
$$[D(D-1) + D - 1]y = 24e^z$$
$$(D^2 - 1)y = 24e^z$$

### Step 2 — Homogeneous Solution ($y_c$)
$m^2 - 1 = 0 \implies m = \pm 1$
$$y_c = C_1e^z + C_2e^{-z} = C_1x + C_2x^{-1}$$

### Step 3 — Particular Integral ($y_p$) via Operator Method
$$y_p = \frac{1}{D^2 - 1} 24e^z$$
Since $D=1$ makes the denominator zero (Case of Failure), use the $xe^{ax}$ rule:
$$y_p = 24 \cdot \frac{z}{2D} e^z = 24 \cdot \frac{z e^z}{2} = 12z e^z$$
**Back-substituting:** $y_p = 12x \ln x$

---

## Example 5 — Non-Homogeneous (Logarithmic RHS)
**Problem:** $x^2y'' - xy' - y = \ln x$

### Step 1 — Operator Transformation
$$[D(D-1) - D - 1]y = z$$
$$(D^2 - 2D - 1)y = z$$

### Step 2 — Homogeneous Solution ($y_c$)
$m^2 - 2m - 1 = 0 \implies m = 1 \pm \sqrt{2}$
$$y_c = C_1 x^{1+\sqrt{2}} + C_2 x^{1-\sqrt{2}}$$

### Step 3 — Particular Integral ($y_p$) via Binomial Expansion
For polynomial $z$, factor out the constant $(-1)$:
$$y_p = \frac{1}{-1(1 + 2D - D^2)} z = -(1 + (2D - D^2))^{-1} z$$
Expand as $(1+X)^{-1} \approx 1 - X$:
$$y_p = -[1 - 2D]z = -(z - 2) = 2 - z$$
**Back-substituting:** $y_p = 2 - \ln x$

---

## [cite_start]Exam Practice — Question 3(a) [cite: 24, 25]
[cite_start]**Problem:** $x^2y'' + xy' + 4y = 2x \ln x$ [cite: 25]

### Step 1 — Operator Transformation
$$(D^2 + 4)y = 2ze^z$$

### Step 2 — Particular Integral ($y_p$) via Exponential Shift
Shift $e^z$ out by replacing $D$ with $D+1$:
$$y_p = 2e^z \left[ \frac{1}{(D+1)^2 + 4} \right] z = 2e^z \left[ \frac{1}{D^2 + 2D + 5} \right] z$$
Factor out $5$ for Binomial Expansion:
$$y_p = \frac{2e^z}{5} [1 - \frac{2D}{5}]z = \frac{2e^z}{5}(z - \frac{2}{5})$$
[cite_start]**Back-substituting:** $y_p = \frac{2x \ln x}{5} - \frac{4x}{25}$ [cite: 27]