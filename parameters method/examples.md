# Examples — Variation of Parameters

This file contains worked examples using the **variation of parameters** method.

---

## Example 1 — Conceptual Example

Solve:
$$y'' + y = \sin x$$

### Step 1 — Complementary Function
Solve the homogeneous equation: $y'' + y = 0$.
Auxiliary equation:
$$m^2 + 1 = 0 \implies m = \pm i$$

Thus:
* $y_1 = \cos x$
* $y_2 = \sin x$
* $y_c = C_1 \cos x + C_2 \sin x$

---

### Step 2 — Wronskian
$$W = \begin{vmatrix} y_1 & y_2 \\ y_1' & y_2' \end{vmatrix} = \begin{vmatrix} \cos x & \sin x \\ -\sin x & \cos x \end{vmatrix}$$
$$W = \cos^2 x + \sin^2 x = 1$$

---

### Step 3 — Compute $u_1'$ and $u_2'$
Using $R(x) = \sin x$:
* $u_1' = \frac{-y_2 R(x)}{W} = -\sin^2 x$
* $u_2' = \frac{y_1 R(x)}{W} = \sin x \cos x$

---

### Step 4 — Integrate
Using trig identities: $\sin^2 x = \frac{1 - \cos 2x}{2}$
$$u_1 = -\int \sin^2 x \, dx = -\frac{x}{2} + \frac{\sin 2x}{4}$$

Using trig identities: $\sin x \cos x = \frac{1}{2}\sin 2x$
$$u_2 = \int \sin x \cos x \, dx = -\frac{\cos 2x}{4}$$

---

### Step 5 — Particular Solution
$$y_p = u_1 y_1 + u_2 y_2$$
$$y_p = \left(-\frac{x}{2} + \frac{\sin 2x}{4}\right)\cos x - \left(\frac{\cos 2x}{4}\right)\sin x$$

---

## Example 2 — Moderate Example

Solve:
$$y'' + y = \sec x$$

### Complementary Function & Wronskian
* $y_c = C_1 \cos x + C_2 \sin x$
* $W = 1$

### Compute $u_1'$ and $u_2'$
Using $R(x) = \sec x$:
* $u_1' = -\sin x \sec x = -\tan x$
* $u_2' = \cos x \sec x = 1$

### Integrate
* $u_1 = -\int \tan x \, dx = \ln|\cos x|$
* $u_2 = \int 1 \, dx = x$

### Particular Solution
$$y_p = \cos x \ln|\cos x| + x \sin x$$

---

## Example 3 — Exponential RHS

Solve:
$$y'' + 3y' + 2y = \frac{1}{1 + e^x}$$

### Complementary Function
Auxiliary equation: $m^2 + 3m + 2 = 0 \implies m = -1, -2$.
$$y_c = C_1 e^{-x} + C_2 e^{-2x}$$

### Wronskian
$$W = \begin{vmatrix} e^{-x} & e^{-2x} \\ -e^{-x} & -2e^{-2x} \end{vmatrix} = -e^{-3x}$$

### Compute $u_1'$ and $u_2'$
Using $R(x) = \frac{1}{1+e^x}$:
* $u_1' = \frac{e^x}{1+e^x}$
* $u_2' = -\frac{e^{2x}}{1+e^x}$

### Integrate
* $u_1 = \ln(1 + e^x)$
* $u_2 = -(e^x - \ln(1 + e^x))$

### Particular Solution
$$y_p = e^{-x} \ln(1 + e^x) + e^{-2x} (\ln(1 + e^x) - e^x)$$

---

## Example 4 — Tricky Example

Solve:
$$y'' + 3y' + 2y = \sin(e^x)$$

### Complementary Function & Wronskian
* $y_c = C_1 e^{-x} + C_2 e^{-2x}$
* $W = -e^{-3x}$

### Compute and Integrate
Using substitution $u = e^x, du = e^x dx$:
* $u_1' = e^x \sin(e^x) \implies u_1 = -\cos(e^x)$
* $u_2' = -e^{2x} \sin(e^x) \implies u_2 = e^x \cos(e^x) - \sin(e^x)$

### Final Solution
$$y = C_1 e^{-x} + C_2 e^{-2x} - e^{-2x} \sin(e^x)$$

---

## Key Takeaways
* Always compute the **Wronskian** first.
* Simplify $u_1'$ and $u_2'$ before integrating.
* Variation of parameters is powerful for RHS functions like $\sec x$ or $\frac{1}{1+e^x}$ where undetermined coefficients fail.