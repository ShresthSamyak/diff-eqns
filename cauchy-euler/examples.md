# Examples — Cauchy–Euler Differential Equations

A **Cauchy–Euler equation** has the form:
$$x^2y'' + axy' + by = f(x)$$

Key substitution used to convert it into a constant coefficient equation:
$$x = e^t \quad \text{or} \quad t = \ln x$$

Then derivatives transform as:
$$\frac{dy}{dx} = \frac{1}{x} \frac{dy}{dt}$$
$$\frac{d^2y}{dx^2} = \frac{1}{x^2} \left( \frac{d^2y}{dt^2} - \frac{dy}{dt} \right)$$

After substitution, the equation becomes a **linear constant coefficient equation in $t$**.

---

## Example 1 — Conceptual Example

Solve:
$$x^2y'' - 2y = 0$$

### Step 1 — Assume solution
For Cauchy–Euler equations, assume:
$$y = x^m$$

### Step 2 — Derivatives
$$y' = m x^{m-1}$$
$$y'' = m(m-1)x^{m-2}$$

### Step 3 — Substitute
$$x^2[m(m-1)x^{m-2}] - 2x^m = 0$$
$$m(m-1)x^m - 2x^m = 0$$
$$x^m[m(m-1) - 2] = 0$$

### Step 4 — Auxiliary equation
$$m(m-1) - 2 = 0$$
$$m^2 - m - 2 = 0$$
$$(m-2)(m+1) = 0 \implies m = 2, -1$$

### Final solution
$$y = C_1x^2 + C_2x^{-1}$$

---

## Example 2 — Moderate Example

Solve:
$$x^2y'' + xy' + 4y = 0$$

### Step 1 — Assume
$$y = x^m$$

### Step 2 — Substitute
$$m(m-1)x^m + m x^m + 4x^m = 0$$
$$x^m[m^2 + 4] = 0$$

### Step 3 — Roots
$$m^2 + 4 = 0 \implies m = \pm 2i$$

### Final solution
$$y = C_1 \cos(2 \ln x) + C_2 \sin(2 \ln x)$$

---

## Example 3 — Hard Example

Solve:
$$x^2y'' - 3xy' - 2y = 0$$

### Step 1 — Assume
$$y = x^m$$

### Step 2 — Substitute
$$m(m-1)x^m - 3m x^m - 2x^m = 0$$

### Step 3 — Simplify
$$m^2 - m - 3m - 2 = 0$$
$$m^2 - 4m - 2 = 0$$

### Step 4 — Roots
$$m = \frac{4 \pm \sqrt{16 - 4(1)(-2)}}{2} = 2 \pm \sqrt{6}$$

### Final solution
$$y = C_1 x^{2+\sqrt{6}} + C_2 x^{2-\sqrt{6}}$$

---

## Example 4 — Required Question

Solve:
$$x^2y'' + xy' - y = 24x$$

### Step 1 — Homogeneous equation
$$x^2y'' + xy' - y = 0$$
Assume $y = x^m \implies m(m-1) + m - 1 = 0 \implies m^2 - 1 = 0 \implies m = \pm 1$

**Complementary solution:**
$$y_c = C_1x + \frac{C_2}{x}$$

### Step 2 — Particular solution
RHS = $24x$. Since $x$ is already in $y_c$, try:
$$y_p = Ax \ln x$$

After simplification:
$$A = 12$$

### Final solution
$$y = C_1x + \frac{C_2}{x} + 12x \ln x$$

---

## Example 5 — Required Question

Solve:
$$x^2y'' - xy' - y = \ln x$$

### Step 1 — Homogeneous equation
Assume $y = x^m \implies m(m-1) - m - 1 = 0 \implies m^2 - 2m - 1 = 0$

**Roots:**
$$m = 1 \pm \sqrt{2}$$

**Complementary solution:**
$$y_c = C_1 x^{1+\sqrt{2}} + C_2 x^{1-\sqrt{2}}$$

### Step 2 — Particular solution
Use substitution $t = \ln x$. 
This converts the equation into a **constant coefficient differential equation in $t$**:
$$\frac{d^2y}{dt^2} - 2\frac{dy}{dt} - y = t$$

Solve the resulting equation and substitute back.

### Final solution
$$y = C_1 x^{1+\sqrt{2}} + C_2 x^{1-\sqrt{2}} + (\text{particular term involving } \ln x)$$