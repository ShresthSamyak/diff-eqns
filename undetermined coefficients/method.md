# Method of Undetermined Coefficients

The **method of undetermined coefficients** is used to find a particular solution of a **linear non-homogeneous differential equation with constant coefficients**.

It works when the right-hand side is made of functions like:
* Polynomials
* Exponentials
* Sine / Cosine
* Combinations of the above

---

## General Form

A second-order linear differential equation:
$$ay'' + by' + cy = f(x)$$

The complete solution is:
$$y = y_c + y_p$$

where:
* $y_c$ $\rightarrow$ complementary solution (homogeneous part)
* $y_p$ $\rightarrow$ particular solution

---

## Step 1: Find the Complementary Function (CF)

Solve the **homogeneous equation**:
$$ay'' + by' + cy = 0$$

Form the **auxiliary equation**:
$$am^2 + bm + c = 0$$

### Cases for Roots ($m$)

**1. Distinct real roots:**
$$y_c = C_1 e^{m_1 x} + C_2 e^{m_2 x}$$

**2. Repeated root:**
$$y_c = (C_1 + C_2 x)e^{mx}$$

**3. Complex roots ($m = \alpha \pm \beta i$):**
$$y_c = e^{\alpha x}(C_1 \cos \beta x + C_2 \sin \beta x)$$

---

## Step 2: Guess the Particular Integral (PI)

| RHS $f(x)$ | Trial Solution ($y_p$) |
| :--- | :--- |
| Polynomial $P_n(x)$ | $A_n x^n + A_{n-1} x^{n-1} + \dots + A_0$ |
| $e^{ax}$ | $Ae^{ax}$ |
| $\sin ax$ or $\cos ax$ | $A \cos ax + B \sin ax$ |
| $x^n e^{ax}$ | $e^{ax}(A_n x^n + \dots + A_0)$ |
| $e^{ax} \sin bx$ or $e^{ax} \cos bx$ | $e^{ax}(A \cos bx + B \sin bx)$ |

---

## Step 3: Handle Duplication

If the guessed $y_p$ **already appears in the complementary function**, multiply by $x$.

* **Example:** If $y_c$ contains $e^{2x}$ and $f(x) = e^{2x}$, use $y_p = Axe^{2x}$.
* If duplication still occurs, multiply by $x^2$.

---

## Step 4: Determine Coefficients

1. **Substitute** the trial $y_p$ and its derivatives ($y_p', y_p''$) into the differential equation.
2. **Expand** and collect like terms.
3. **Match** coefficients with the RHS $f(x)$.
4. **Solve** for the unknown constants ($A, B, \dots$).

---

## Final Solution
$$y = y_c + y_p$$

---

## When This Method Works
This method works for polynomials, exponentials, and trigonometric functions. It **does not work** for:
* $\tan x$
* $\sec x$
* $\ln x$

For these cases, use **Variation of Parameters**.