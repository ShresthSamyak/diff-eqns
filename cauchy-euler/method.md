# Cauchy-Euler Method: Complete Guide

## What Is the Cauchy-Euler Equation?

A **Cauchy-Euler equation** (also called an *equidimensional equation*) is a second-order (or higher-order) linear ODE where **the power of `x` in each term matches the order of the derivative** in that term.

**Standard Form (2nd order):**

$$x^2 \frac{d^2y}{dx^2} + ax \frac{dy}{dx} + by = f(x)$$

> In general, an *n*-th order Cauchy-Euler equation looks like:
> $$a_n x^n y^{(n)} + a_{n-1} x^{n-1} y^{(n-1)} + \cdots + a_1 x y' + a_0 y = f(x)$$

---

## Step-by-Step Solution Method

### Step 1 — Change of Variables (Transform to Constant Coefficients)

The key idea is to **eliminate the variable coefficients** by substituting:

$$x = e^z \quad \Longleftrightarrow \quad z = \ln(x)$$

This maps `x ∈ (0, ∞)` to `z ∈ (-∞, ∞)` and converts the equation into one with **constant coefficients**.

Define the differential operator:

$$D = \frac{d}{dz}$$

#### Derivative Replacement Rules

| Original Term | Transformed Form |
| :--- | :--- |
| $x \dfrac{dy}{dx}$ | $Dy$ |
| $x^2 \dfrac{d^2y}{dx^2}$ | $D(D-1)\,y$ |
| $x^3 \dfrac{d^3y}{dx^3}$ | $D(D-1)(D-2)\,y$ |
| $x^n \dfrac{d^ny}{dx^n}$ | $D(D-1)(D-2)\cdots(D-n+1)\,y$ |

> **Why does this work?**  
> Since $x = e^z$, we have $\frac{dy}{dx} = \frac{1}{x}\frac{dy}{dz}$, so $x\frac{dy}{dx} = \frac{dy}{dz} = Dy$. Each successive derivative follows the same pattern by the chain rule.

---

### Step 2 — Solve the Homogeneous Part (Find $y_c$)

After substitution, the left-hand side becomes a constant-coefficient ODE. For the **homogeneous equation** ($f(x) = 0$), substitute $y = x^m$ (equivalently $y = e^{mz}$) to get the **characteristic equation**:

$$m^2 + (a - 1)m + b = 0$$

Analyze the roots $m_1, m_2$:

| Root Type | Condition | Complementary Solution $y_c$ |
| :--- | :--- | :--- |
| **Distinct Real** | $m_1 \neq m_2$, both real | $y_c = C_1\, x^{m_1} + C_2\, x^{m_2}$ |
| **Repeated Real** | $m_1 = m_2 = m$ | $y_c = x^m\bigl(C_1 + C_2 \ln x\bigr)$ |
| **Complex Conjugate** | $m = \alpha \pm i\beta$ | $y_c = x^\alpha\bigl[C_1 \cos(\beta \ln x) + C_2 \sin(\beta \ln x)\bigr]$ |

> **Tip:** Complex roots arise when the discriminant $(a-1)^2 - 4b < 0$.

---

### Step 3 — Find the Particular Integral $y_p$ (Operator Method)

Once the equation is in the $z$-domain with constant coefficients, find $y_p$ using inverse operators:

$$y_p = \frac{1}{f(D)}\,g(z)$$

where $g(z)$ is the right-hand side after substituting $x = e^z$.

#### Common Inverse Operator Shortcuts

| Right-hand side $g(z)$ | Method | Rule |
| :--- | :--- | :--- |
| $e^{az}$ | Exponential shift | Replace $D$ with $a$: $\;\frac{1}{f(D)}e^{az} = \frac{e^{az}}{f(a)}$, provided $f(a) \neq 0$ |
| $	ext{sin}(az)$ or $	ext{cos}(az)$ | Trig shortcut | Replace $D^2$ with $-a^2$ |
| $z^n$ (polynomial) | Binomial expansion | Expand $(1 + g(D))^{-1}$ using the series $1 - g(D) + [g(D)]^2 - \cdots$ |
| $e^{az} \cdot v(z)$ | Exponential shift theorem | $\frac{1}{f(D)}e^{az}v(z) = e^{az}\frac{1}{f(D+a)}v(z)$ |

> **Note:** If $f(a) = 0$ for the exponential case, multiply by $z$ and differentiate the denominator (analogous to the repeated-root case).

---

### Step 4 — Combine the General Solution

$$y = y_c + y_p$$

---

### Step 5 — Back-Substitution (Return to the $x$-domain)

After finding the complete solution in terms of $z$, convert back using:

$$z = \ln(x) \qquad \text{and} \qquad e^z = x$$

Replace every occurrence of $z$ with $\ln(x)$ and every $e^z$ with $x$ to express the final answer in terms of the original variable $x$.

---

## Quick Summary Flowchart

```
Cauchy-Euler ODE in x
        |
        v
Substitute x = e^z  (z = ln x),  D = d/dz
        |
        v
Constant-coefficient ODE in z
        |
   _____|_____
  |           |
  v           v
Find y_c    Find y_p
(char. eq.) (inv. operator)
  |           |
  |___________|
        |
        v
   y = y_c + y_p
        |
        v
Back-substitute z = ln(x)
        |
        v
Final answer in x
```

---

## Key Reminders

- The substitution $x = e^z$ only works for $x > 0$. For $x < 0$, use $|x|$ instead of $x$ throughout.
- The repeated-root solution $C_2\, x^m \ln(x)$ comes from the $z$-domain solution $C_2\, z\, e^{mz}$, since $z = \ln(x)$.
- Always verify your particular integral by substituting back into the original ODE.