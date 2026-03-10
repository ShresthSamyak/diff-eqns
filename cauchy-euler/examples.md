# Examples — Cauchy–Euler Equations via the Operator Method

---

## 🔑 Core Idea: The Substitution

Every Cauchy–Euler equation is converted into a **constant-coefficient ODE** using the substitution:

$$x = e^z \quad \Longleftrightarrow \quad z = \ln x$$

This transforms the variable-coefficient operators into polynomial operators in $D$, where $D = \dfrac{d}{dz}$.

### Operator Conversion Table

| Original Term | Operator Form |
|---|---|
| $x\,y'$ | $D\,y$ |
| $x^2 y''$ | $D(D-1)\,y$ |
| $x^3 y'''$ | $D(D-1)(D-2)\,y$ |

> **Why does this work?**
> If $x = e^z$, then $\frac{dy}{dx} = \frac{1}{x}\frac{dy}{dz}$, so $x\frac{dy}{dx} = \frac{dy}{dz} = Dy$.
> Differentiating again gives $x^2 y'' = D(D-1)y$. The pattern continues for higher derivatives.

---

## Example 4 — Non-Homogeneous Equation (Exponential / Linear RHS)

**Problem:**
$$x^2 y'' + x y' - y = 24x$$

---

### Step 1 — Operator Transformation

Substitute $x = e^z$ and replace each term using the conversion table:

$$[D(D-1) + D - 1]\,y = 24e^z$$

Expand $D(D-1) = D^2 - D$, then collect:

$$D^2 - D + D - 1 = D^2 - 1$$

So the equation becomes:

$$(D^2 - 1)\,y = 24e^z$$

> Note: $24x = 24e^z$ because $x = e^z$.

---

### Step 2 — Homogeneous Solution $y_c$

Solve the auxiliary (characteristic) equation by setting the right-hand side to zero:

$$m^2 - 1 = 0 \implies (m-1)(m+1) = 0 \implies m = +1,\, -1$$

Two real distinct roots give:

$$y_c = C_1 e^{z} + C_2 e^{-z}$$

Back-substituting $e^z = x$ and $e^{-z} = x^{-1}$:

$$\boxed{y_c = C_1 x + C_2 x^{-1}}$$

---

### Step 3 — Particular Integral $y_p$ (Case of Failure)

Apply the inverse operator directly:

$$y_p = \frac{1}{D^2 - 1}\, 24e^z$$

**Problem:** Substituting $D = 1$ makes the denominator $1^2 - 1 = 0$ — this is called the **Case of Failure**.

**Fix — the $z e^{az}$ rule:**
When $D = a$ causes failure, multiply by $z$ and differentiate the denominator with respect to $D$:

$$y_p = 24 \cdot \frac{z}{2D}\,e^z = 24 \cdot \frac{z}{2}\,e^z = 12z\,e^z$$

> Here $\frac{d}{dD}(D^2 - 1) = 2D$, evaluated at $D=1$ gives $2$, so we divide by $2D$.

Back-substituting $z = \ln x$ and $e^z = x$:

$$\boxed{y_p = 12x \ln x}$$

---

### ✅ General Solution

$$y = y_c + y_p = C_1 x + C_2 x^{-1} + 12x \ln x$$

---

## Example 5 — Non-Homogeneous Equation (Logarithmic / Polynomial RHS)

**Problem:**
$$x^2 y'' - x y' - y = \ln x$$

---

### Step 1 — Operator Transformation

Substitute $x = e^z$ (so $\ln x = z$) and convert each term:

$$[D(D-1) - D - 1]\,y = z$$

Expand and collect:

$$D^2 - D - D - 1 = D^2 - 2D - 1$$

So the equation becomes:

$$(D^2 - 2D - 1)\,y = z$$

---

### Step 2 — Homogeneous Solution $y_c$

Solve the auxiliary equation:

$$m^2 - 2m - 1 = 0 \implies m = \frac{2 \pm \sqrt{4 + 4}}{2} = 1 \pm \sqrt{2}$$

Two real distinct (irrational) roots give:

$$y_c = C_1 e^{(1+\sqrt{2})z} + C_2 e^{(1-\sqrt{2})z}$$

Back-substituting $e^{mz} = x^m$:

$$\boxed{y_c = C_1\, x^{1+\sqrt{2}} + C_2\, x^{1-\sqrt{2}}}$$

---

### Step 3 — Particular Integral $y_p$ (Binomial Expansion)

The RHS is $z$, a polynomial in $z$, so we use the **Binomial Expansion** method.

$$y_p = \frac{1}{D^2 - 2D - 1}\, z$$

Rewrite the denominator by factoring out $-1$:

$$y_p = \frac{-1}{1 + 2D - D^2}\, z = -(1 + (2D - D^2))^{-1} z$$

Expand using $(1 + X)^{-1} \approx 1 - X + \cdots$ (truncate after $D^1$ since $z$ is degree 1):

$$y_p = -\bigl[1 - (2D - D^2)\bigr] z = -\bigl[1 - 2D\bigr] z$$

> $D^2 z = 0$ since $z$ is linear, so the $D^2$ term vanishes.

Apply the operators ($Dz = 1$, $D^2 z = 0$):

$$y_p = -(z - 2\cdot 1) = -(z - 2) = 2 - z$$

Back-substituting $z = \ln x$:

$$\boxed{y_p = 2 - \ln x}$$

---

### ✅ General Solution

$$y = y_c + y_p = C_1\, x^{1+\sqrt{2}} + C_2\, x^{1-\sqrt{2}} + 2 - \ln x$$

---

## Example 6 — Non-Homogeneous Equation (Exponential Shift + Binomial, Complex Roots)

**Problem:**
$$x^2 y'' + x y' + 4y = 2x \ln x$$

---

### Step 1 — Operator Transformation

Substitute $x = e^z$ (so $\ln x = z$, $x = e^z$, meaning $2x\ln x = 2e^z \cdot z = 2ze^z$):

$$[D(D-1) + D + 4]\,y = 2ze^z$$

Expand and collect:

$$D^2 - D + D + 4 = D^2 + 4$$

So the equation becomes:

$$(D^2 + 4)\,y = 2ze^z$$

---

### Step 2 — Homogeneous Solution $y_c$

Solve the auxiliary equation:

$$m^2 + 4 = 0 \implies m = \pm 2i$$

Complex roots $\alpha \pm \beta i$ with $\alpha = 0$, $\beta = 2$ give:

$$y_c = e^{0 \cdot z}(C_1 \cos 2z + C_2 \sin 2z) = C_1 \cos 2z + C_2 \sin 2z$$

Back-substituting $z = \ln x$:

$$\boxed{y_c = C_1 \cos(2\ln x) + C_2 \sin(2\ln x)}$$

---

### Step 3 — Particular Integral $y_p$ (Exponential Shift + Binomial)

Apply the inverse operator:

$$y_p = \frac{1}{D^2 + 4}\,2ze^z$$

**Exponential Shift Rule:** For $\frac{1}{f(D)} e^{az} g(z)$, shift by replacing $D \to D + a$:

$$y_p = 2e^z \cdot \frac{1}{(D+1)^2 + 4}\,z = 2e^z \cdot \frac{1}{D^2 + 2D + 5}\,z$$

**Binomial Expansion:** Factor out $5$ from the denominator:

$$y_p = \frac{2e^z}{5} \cdot \frac{1}{1 + \frac{2D + D^2}{5}}\,z$$

Expand $(1 + X)^{-1} \approx 1 - X$ (truncate at $D^1$ since $z$ is degree 1):

$$y_p = \frac{2e^z}{5}\left[1 - \frac{2D}{5}\right] z$$

Apply the operators ($Dz = 1$):

$$y_p = \frac{2e^z}{5}\left(z - \frac{2}{5}\right)$$

Back-substituting $z = \ln x$ and $e^z = x$:

$$\boxed{y_p = \frac{2x\ln x}{5} - \frac{4x}{25}}$$

---

### ✅ General Solution

$$y = y_c + y_p = C_1\cos(2\ln x) + C_2\sin(2\ln x) + \frac{2x\ln x}{5} - \frac{4x}{25}$$

---

## 📋 Quick Reference — Method Summary

| Situation | Technique |
|---|---|
| RHS is $e^{az}$ and $f(a) \neq 0$ | Direct substitution: $y_p = \frac{e^{az}}{f(a)}$ |
| RHS is $e^{az}$ and $f(a) = 0$ (**Failure**) | Multiply by $z$, differentiate denominator |
| RHS is a polynomial in $z$ | Binomial expansion of $[f(D)]^{-1}$ |
| RHS is $e^{az} \cdot g(z)$ | Exponential shift: replace $D \to D+a$, then expand |