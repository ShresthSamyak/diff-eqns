# Method of Undetermined Coefficients

The **method of undetermined coefficients** is used to find a particular solution of a **linear non-homogeneous differential equation with constant coefficients**.

It works when the right-hand side is made of functions like:

- polynomials
- exponentials
- sine / cosine
- combinations of the above

---

# General Form

A second-order linear differential equation:

\[
ay'' + by' + cy = f(x)
\]

The complete solution is:

\[
y = y_c + y_p
\]

where

- \(y_c\) → complementary solution (homogeneous part)
- \(y_p\) → particular solution

---

# Step 1: Find the Complementary Function (CF)

Solve the **homogeneous equation**

\[
ay'' + by' + cy = 0
\]

Form the **auxiliary equation**

\[
am^2 + bm + c = 0
\]

Solve for the roots \(m\).

### Cases

**Distinct real roots**

\[
y_c = C_1 e^{m_1 x} + C_2 e^{m_2 x}
\]

**Repeated root**

\[
y_c = (C_1 + C_2 x)e^{mx}
\]

**Complex roots**

If

\[
m = \alpha \pm \beta i
\]

then

\[
y_c = e^{\alpha x}(C_1\cos \beta x + C_2\sin \beta x)
\]

---

# Step 2: Guess the Particular Integral (PI)

Choose a trial solution depending on \(f(x)\).

| RHS \(f(x)\) | Trial Solution |
|---------------|----------------|
| polynomial \(P_n(x)\) | polynomial of same degree |
| \(e^{ax}\) | \(Ae^{ax}\) |
| \(\sin ax\), \(\cos ax\) | \(A\cos ax + B\sin ax\) |
| \(x^n e^{ax}\) | \(e^{ax}(Ax^n + ...)\) |
| \(e^{ax}\sin bx\) or \(e^{ax}\cos bx\) | \(e^{ax}(A\cos bx + B\sin bx)\) |

---

# Step 3: Handle Duplication

If the guessed \(y_p\) **already appears in the complementary function**, multiply by \(x\).

Example:

If CF contains \(e^{2x}\) and RHS is \(e^{2x}\)

Then instead of

\[
Ae^{2x}
\]

use

\[
Ax e^{2x}
\]

If duplication still occurs → multiply by \(x^2\).

---

# Step 4: Determine Coefficients

1. Substitute the trial \(y_p\) into the differential equation.
2. Expand and collect like terms.
3. Match coefficients with the RHS.
4. Solve for the unknown constants.

---

# Final Solution

\[
y = y_c + y_p
\]

where

- \(y_c\) comes from the auxiliary equation
- \(y_p\) comes from the trial function

---

# When This Method Works

This method works when \(f(x)\) is made of:

- polynomials
- exponentials
- trigonometric functions
- finite sums or products of these

It **does not work well** for functions like:

- \(\tan x\)
- \(\sec x\)
- \(\ln x\)
- arbitrary functions

For those cases use **variation of parameters**.