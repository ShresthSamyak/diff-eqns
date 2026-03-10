# Operator Method (D-Operator Method)

The **operator method** is used to solve linear differential equations with constant coefficients.

We define the differential operator:
$$D = \frac{d}{dx}$$

So derivatives become:

| Derivative | Operator form |
| :--- | :--- |
| $y'$ | $Dy$ |
| $y''$ | $D^2y$ |
| $y^{(n)}$ | $D^n y$ |

---

# General Form

A differential equation:
$$a_n y^{(n)} + a_{n-1} y^{(n-1)} + ... + a_1 y' + a_0 y = f(x)$$

can be written as:
$$F(D)y = f(x)$$

where:
$$F(D) = a_n D^n + a_{n-1}D^{n-1} + ... + a_1D + a_0$$

---

# Solution Structure

$$y = y_c + y_p$$

| Term | Meaning |
| :--- | :--- |
| $y_c$ | Complementary Function |
| $y_p$ | Particular Integral |

---

# Step 1 — Complementary Function

Solve:
$$F(D)y = 0$$

Replace $D$ with $m$ to form the **auxiliary equation**:
$$F(m) = 0$$

Solve for $m$.

### Root cases

**Distinct roots:**
$$y_c = C_1 e^{m_1 x} + C_2 e^{m_2 x}$$

**Repeated roots:**
$$y_c = (C_1 + C_2 x)e^{mx}$$

**Complex roots:**
If $m = \alpha \pm \beta i$, then:
$$y_c = e^{\alpha x}(C_1 \cos \beta x + C_2 \sin \beta x)$$

---

# Step 2 — Particular Integral

$$y_p = \frac{1}{F(D)} f(x)$$

The computation depends on the **type of RHS**.

---

# RHS Type Rules (Most Important Table)

| RHS $f(x)$ | Replace |
| :--- | :--- |
| $e^{ax}$ | $D = a$ |
| $\sin(ax), \cos(ax)$ | $D^2 = -a^2$ |
| polynomial $x^n$ | assume polynomial |
| $x^n e^{ax}$ | shift $D \rightarrow D+a$ |
| $e^{ax} \sin bx$, $e^{ax} \cos bx$ | combine exponential + trig rules |

---

# Rule 1 — Exponential RHS

If $f(x) = e^{ax}$, then:
$$y_p = \frac{1}{F(a)} e^{ax}$$

**Example:**
$$(D^2 - 5D + 6)y = e^{2x}$$
$$F(2) = 4 - 10 + 6 = 0$$

---

# Rule 2 — Trigonometric RHS

If $f(x) = \sin(ax)$ or $\cos(ax)$, then substitute $D^2 = -a^2$:
$$y_p = \frac{1}{F(-a^2)} f(x)$$

**Example:**
$$(D^2 + 4)y = \cos(3x)$$
$$F(-9) = -9 + 4 = -5$$
$$y_p = -\frac{1}{5}\cos(3x)$$

---

# Rule 3 — Polynomial RHS

If RHS is $x^n$, assume:
$$y_p = ax^n + bx^{n-1} + ...$$

Then substitute into the equation and solve coefficients.

---

# Rule 4 — Exponential × Polynomial

If RHS is $x^n e^{ax}$, use the **shift rule**:
$$\frac{1}{F(D)}(e^{ax}V(x)) = e^{ax}\frac{1}{F(D+a)}V(x)$$

---

# Special Case — Denominator Becomes Zero

If $F(a) = 0$ or $F(-a^2) = 0$, then multiply by $x$:
$$y_p = x \frac{1}{F'(a)} e^{ax}$$

If still zero $\rightarrow$ multiply by $x^2$.

**Example:**
$$(D^2 - 4)y = e^{2x}$$
$$F(2) = 4 - 4 = 0$$

So multiply by $x$:
$$F'(D) = 2D \implies F'(2) = 4$$
$$y_p = \frac{x}{4} e^{2x}$$

---

# Operator Tricks for Exams

### Trick 1
Always check **$F(a)$** before solving. If non-zero $\rightarrow$ direct answer.

### Trick 2
For trig RHS remember:
* $D^2(\sin ax) = -a^2\sin ax$
* $D^2(\cos ax) = -a^2\cos ax$

### Trick 3
For $e^{ax}V(x)$, always **shift the operator**: $D \rightarrow D+a$.

---

# When Operator Method Works Best

Works well for:
- exponentials
- trigonometric functions
- polynomials
- combinations of these

Not suitable for:
- $\tan x$
- $\sec x$
- $\ln x$

For those use **variation of parameters**.