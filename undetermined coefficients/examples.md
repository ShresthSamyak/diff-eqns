# Examples — Method of Undetermined Coefficients

This file contains worked examples of solving non-homogeneous linear differential equations using the **method of undetermined coefficients**.

---

## Example 1 — Polynomial RHS

Solve:
$$y'' - 3y' - 10y = 1 + x^2$$

### Step 1: Complementary Function
Homogeneous equation: $y'' - 3y' - 10y = 0$  
Auxiliary equation:
$$m^2 - 3m - 10 = 0$$
$$(m-5)(m+2)=0$$
$$m=5, -2$$

So:
$$y_c = C_1 e^{5x} + C_2 e^{-2x}$$

---

### Step 2: Guess Particular Integral
RHS is a polynomial of degree 2.
$$y_p = ax^2 + bx + c$$

---

### Step 3: Substitute and Solve
$$y_p' = 2ax + b$$
$$y_p'' = 2a$$

Substitute into the differential equation and match coefficients with $1 + x^2$:
$$a = -\frac{1}{10}, \quad b = \frac{3}{50}, \quad c = -\frac{69}{500}$$

Thus:
$$y_p = -\frac{50x^2 - 30x + 69}{500}$$

---

### Final Solution
$$y = C_1 e^{5x} + C_2 e^{-2x} - \frac{50x^2 - 30x + 69}{500}$$

---

## Example 2 — Exponential RHS

Solve:
$$y'' - 4y = e^{3x}$$

### Step 1: Complementary Function
$$m^2 - 4 = 0 \implies m = \pm 2$$
$$y_c = C_1 e^{2x} + C_2 e^{-2x}$$

---

### Step 2: Particular Integral
Guess:
$$y_p = Ae^{3x}$$

Substitute into the equation:
$$9Ae^{3x} - 4Ae^{3x} = e^{3x}$$
$$5A = 1 \implies A = \frac{1}{5}$$

---

### Final Solution
$$y = C_1 e^{2x} + C_2 e^{-2x} + \frac{1}{5} e^{3x}$$

---

## Example 3 — Trigonometric RHS

Solve:
$$y'' + 16y = 16\sin 4x$$

### Step 1: Complementary Function
$$m^2 + 16 = 0 \implies m = \pm 4i$$
$$y_c = C_1 \cos 4x + C_2 \sin 4x$$

---

### Step 2: Handle Duplication
RHS contains $\sin 4x$, which **already appears** in the complementary function. Multiply the trial solution by $x$:
$$y_p = x(A\cos 4x + B\sin 4x)$$

Substitute and solve:
$$A = -2, \quad B = 0$$

---

### Final Solution
$$y = C_1 \cos 4x + C_2 \sin 4x - 2x \cos 4x$$

---

## Example 4 — Exponential × Trigonometric RHS

Solve:
$$y'' + 2y' + 10y = e^{-x}\sin 3x$$

### Step 1: Complementary Function
$$m^2 + 2m + 10 = 0 \implies m = -1 \pm 3i$$
$$y_c = e^{-x}(C_1 \cos 3x + C_2 \sin 3x)$$

---

### Step 2: Particular Integral
Since the RHS duplicates the complementary function, multiply by $x$:
$$y_p = x e^{-x}(A \cos 3x + B \sin 3x)$$

Substitute and solve:
$$y_p = -\frac{x}{6} e^{-x} \cos 3x$$

---

### Final Solution
$$y = e^{-x}(C_1 \cos 3x + C_2 \sin 3x) - \frac{x}{6} e^{-x} \cos 3x$$

---

## Key Takeaways
* Always start with the **complementary function**.
* Choose a **trial form based on the RHS**.
* If the trial solution duplicates the CF $\rightarrow$ **multiply by $x$**.
* Substitute the trial function into the equation to determine coefficients.