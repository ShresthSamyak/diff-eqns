# Examples — Operator Method

This file contains worked examples of solving differential equations using the **operator (D-operator) method**.

Refer to `method.md` for the rules and operator tricks.

---

## Example 1 — Exponential RHS

Solve:
$$y'' - 4y = e^{3x}$$

### Step 1: Operator form
$$(D^2 - 4)y = e^{3x}$$

---

### Step 2: Complementary Function
Auxiliary equation:
$$m^2 - 4 = 0 \implies m = \pm 2$$

So:
$$y_c = C_1 e^{2x} + C_2 e^{-2x}$$

---

### Step 3: Particular Integral
From the rule table (see `method.md`), for RHS $e^{ax}$:
$$y_p = \frac{1}{F(D)} e^{ax} \implies y_p = \frac{1}{F(a)} e^{ax}$$

Here, $F(D) = D^2 - 4$. Substitute $D = 3$:
$$F(3) = 9 - 4 = 5$$

Thus:
$$y_p = \frac{1}{5} e^{3x}$$

---

### Final Solution
$$y = C_1 e^{2x} + C_2 e^{-2x} + \frac{1}{5} e^{3x}$$

---

## Example 2 — Duplicate Exponential

Solve:
$$y'' - 4y = e^{2x}$$

### Operator form
$$(D^2 - 4)y = e^{2x}$$

### Complementary Function
$$y_c = C_1 e^{2x} + C_2 e^{-2x}$$

### Particular Integral
From the exponential rule:
$$y_p = \frac{1}{F(a)} e^{ax}$$

Here, $F(2) = 4 - 4 = 0$. The denominator becomes **zero**.
According to the **duplicate root rule**, multiply by $x$ and differentiate the denominator:
$$F'(D) = 2D \implies F'(2) = 4$$

Thus:
$$y_p = \frac{x}{F'(2)} e^{2x} = \frac{x}{4} e^{2x}$$

---

### Final Solution
$$y = C_1 e^{2x} + C_2 e^{-2x} + \frac{x}{4} e^{2x}$$

---

## Example 3 — Trigonometric RHS

Solve:
$$y'' + 4y = \cos 2x$$

### Operator form
$$(D^2 + 4)y = \cos 2x$$

### Complementary Function
$$m^2 + 4 = 0 \implies m = \pm 2i$$
$$y_c = C_1 \cos 2x + C_2 \sin 2x$$

### Particular Integral
For trig RHS, use the rule $D^2 = -a^2$. Here $a = 2$, so $D^2 = -4$.
$$F(-4) = -4 + 4 = 0$$

Again, the denominator becomes **zero**. Multiply by $x$ and solve:
Assume $y_p = x(A \cos 2x + B \sin 2x)$.
Substituting into the equation and solving gives:
$$y_p = \frac{x}{4} \sin 2x$$

---

### Final Solution
$$y = C_1 \cos 2x + C_2 \sin 2x + \frac{x}{4} \sin 2x$$

---

## Example 4 — Polynomial RHS

Solve:
$$y'' - y' + y = x^2$$

### Operator form
$$(D^2 - D + 1)y = x^2$$

### Complementary Function
$$m^2 - m + 1 = 0 \implies m = \frac{1}{2} \pm \frac{\sqrt{3}}{2}i$$
$$y_c = e^{x/2} \left( C_1 \cos \frac{\sqrt{3}}{2}x + C_2 \sin \frac{\sqrt{3}}{2}x \right)$$

### Particular Integral
RHS is a polynomial. Assume:
$$y_p = ax^2 + bx + c$$

Substitute into the differential equation. Matching coefficients gives:
$$a = 1, \quad b = -6, \quad c = -5$$

Thus:
$$y_p = x^2 - 6x - 5$$

---

### Final Solution
$$y = e^{x/2} \left( C_1 \cos \frac{\sqrt{3}}{2}x + C_2 \sin \frac{\sqrt{3}}{2}x \right) + x^2 - 6x - 5$$

---

## Key Takeaways
* Convert the equation to **operator form**.
* Identify RHS type using the **rule table in `method.md`**.
* Apply the correct substitution rule (e.g., $D=a$ for exponentials, $D^2=-a^2$ for trig).
* If the denominator becomes **zero**, multiply by $x$ and differentiate the operator $F(D)$.