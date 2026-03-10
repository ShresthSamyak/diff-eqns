# Variation of Parameters Method

The **variation of parameters** method is used to find a particular solution of a **non-homogeneous linear differential equation**.

Unlike the method of undetermined coefficients, it works for **any RHS function**.

Examples where this method is useful:
- $\sec x$
- $\tan x$
- $\ln x$
- arbitrary functions

---

# General Form

A second-order linear differential equation:
$$y'' + P(x)y' + Q(x)y = R(x)$$

The complete solution is:
$$y = y_c + y_p$$

| Term | Meaning |
| :--- | :--- |
| $y_c$ | complementary function |
| $y_p$ | particular solution |

---

# Step 1 — Solve the Homogeneous Equation

Solve:
$$y'' + P(x)y' + Q(x)y = 0$$

Suppose the complementary solution is:
$$y_c = C_1 y_1(x) + C_2 y_2(x)$$
where $y_1, y_2$ are independent solutions.

---

# Step 2 — Replace Constants with Functions

Instead of constants $C_1, C_2$, assume:
$$y_p = u_1(x)y_1(x) + u_2(x)y_2(x)$$

Here:
- $u_1(x)$
- $u_2(x)$
are functions to be determined.

---

# Step 3 — Apply Two Conditions

To simplify derivatives we impose:
$$u_1' y_1 + u_2' y_2 = 0$$
$$u_1' y_1' + u_2' y_2' = R(x)$$

---

# Step 4 — Wronskian

Compute the **Wronskian**:
$$W = \begin{vmatrix} y_1 & y_2 \\ y_1' & y_2' \end{vmatrix}$$


---

# Step 5 — Key Formulas

Using determinants we obtain:
$$u_1' = -\frac{y_2 R(x)}{W}$$
$$u_2' = \frac{y_1 R(x)}{W}$$

---

# Step 6 — Integrate

Find:
$$u_1 = \int u_1' dx$$
$$u_2 = \int u_2' dx$$

---

# Step 7 — Particular Solution

$$y_p = u_1 y_1 + u_2 y_2$$

---

# Final Solution

$$y = y_c + y_p$$

---

# Quick Formula Summary

| Quantity | Formula |
| :--- | :--- |
| Wronskian | $W = y_1y_2' - y_2y_1'$ |
| $u_1'$ | $-y_2R(x)/W$ |
| $u_2'$ | $y_1R(x)/W$ |
| particular solution | $y_p = u_1y_1 + u_2y_2$ |

---

# When to Use Variation of Parameters

Use this method when RHS contains functions like:
- $\sec x$
- $\tan x$
- $\ln x$
- complicated expressions
- functions not suitable for undetermined coefficients

---

# Common Tricks

### Trick 1 — Always simplify $u_1'$ and $u_2'$ before integrating.
Many integrals become easier after algebraic simplification.

Example:
$$\sin x \sec x = \tan x$$

---

### Trick 2 — Use substitutions
Many integrals require substitutions like:
$$u = e^x$$
or
$$u = \tan x$$

---

### Trick 3 — Expect complicated integrals
Unlike undetermined coefficients, the final answer may contain **logarithms or integrals**.

---

# Common Mistakes

1. Forgetting to compute the **Wronskian** correctly.
2. Not simplifying $u_1'$ or $u_2'$ before integrating.
3. Dropping negative signs in the formulas.

---

# When NOT to Use This Method

Avoid variation of parameters when RHS is simple like:
- $e^{ax}$
- $\sin ax$
- $\cos ax$
- polynomials

Those are faster with **undetermined coefficients**.