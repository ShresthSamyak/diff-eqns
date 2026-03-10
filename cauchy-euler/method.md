# Cauchy–Euler Differential Equations

## 1. Definition

A **Cauchy–Euler equation** (also called **Equidimensional equation**) is a differential equation of the form:

$$x^2 y'' + a x y' + b y = f(x)$$

or in homogeneous form:

$$x^2 y'' + a x y' + b y = 0$$

where $a$ and $b$ are constants.

**Key characteristic:**
- Coefficient of $y''$ $\rightarrow$ $x^2$
- Coefficient of $y'$ $\rightarrow$ $x$

---

## 2. Standard Form

General Cauchy–Euler equation:
$$x^2 y'' + a x y' + b y = 0$$

Divide by $x^2$:
$$y'' + \frac{a}{x}y' + \frac{b}{x^2}y = 0$$

---

## 3. Trial Solution

Assume a solution of the form:
$$y = x^m$$

Then:
$$y' = m x^{m-1}$$
$$y'' = m(m-1)x^{m-2}$$

---

## 4. Substitution

Substitute into the equation:
$$x^2[m(m-1)x^{m-2}] + ax[mx^{m-1}] + b x^m = 0$$

Simplify:
$$x^m[m(m-1) + am + b] = 0$$

---

## 5. Auxiliary (Indicial) Equation

$$m(m-1) + am + b = 0$$

or

$$m^2 + (a-1)m + b = 0$$

Solve for $m$.

---

## 6. Cases of Roots

### Case 1: Distinct Real Roots
If $m_1 \neq m_2$, then:
$$y = C_1 x^{m_1} + C_2 x^{m_2}$$

---

### Case 2: Repeated Root
If $m_1 = m_2 = m$, then:
$$y = C_1 x^m + C_2 x^m \ln x$$

---

### Case 3: Complex Roots
If $m = \alpha \pm i\beta$, then:
$$y = x^\alpha [C_1 \cos(\beta \ln x) + C_2 \sin(\beta \ln x)]$$

---

## 7. Alternative Method (Change of Variable)

Sometimes we use the substitution:
$$x = e^t \quad \text{or} \quad t = \ln x$$

This converts the Cauchy–Euler equation into a **constant-coefficient differential equation**.

**Steps:**
1. Let $x = e^t$
2. Convert derivatives using chain rule
3. Solve resulting linear equation

---

## 8. Quick Recognition Trick

An equation is Cauchy–Euler if:

| Term | Pattern |
| :--- | :--- |
| $y''$ coefficient | $x^2$ |
| $y'$ coefficient | $x$ |
| $y$ coefficient | constant |

**Example:**
$$x^2y'' - 3xy' + 4y = 0$$

---

## 9. Summary

**Steps to solve:**
1. Identify equation as Cauchy–Euler.
2. Assume solution $y = x^m$.
3. Compute $y'$ and $y''$.
4. Substitute into equation.
5. Solve auxiliary equation.
6. Write general solution based on root type.