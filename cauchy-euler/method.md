# Cauchy-Euler Method: Operational Guide

## 1. Identification
[cite_start]A differential equation is a Cauchy-Euler (equidimensional) equation if the power of $x$ matches the order of the derivative[cite: 25]:
$$x^2 \frac{d^2y}{dx^2} + a x \frac{dy}{dx} + b y = f(x)$$

## 2. Transformation (Change of Variables)
To convert the equation into one with constant coefficients, use the substitution:
- [cite_start]$x = e^z$ or $z = \ln(x)$ [cite: 25]
- Define the operator $D = \frac{d}{dz}$

### Derivative Replacements:
- $x \frac{dy}{dx} = Dy$
- $x^2 \frac{d^2y}{dx^2} = D(D-1)y$
- $x^3 \frac{d^3y}{dx^3} = D(D-1)(D-2)y$

## 3. The Characteristic Equation
For the homogeneous part, substitute $y = x^m$ or use the transformed operator equation:
$$m(m-1) + am + b = 0 \implies m^2 + (a-1)m + b = 0$$

### Case Analysis for Roots ($m$):
| Root Type | Homogeneous Solution ($y_c$) |
| :--- | :--- |
| **Distinct Real** ($m_1, m_2$) | $y_c = C_1 x^{m_1} + C_2 x^{m_2}$ |
| **Repeated Real** ($m_1 = m_2$) | $y_c = C_1 x^m + C_2 x^m \ln(x)$ |
| **Complex** ($\alpha \pm i\beta$) | $y_c = x^\alpha [C_1 \cos(\beta \ln x) + C_2 \sin(\beta \ln x)]$ |

## 4. Particular Integral ($y_p$) via Operator Method
Once transformed into the $z$-domain, find $y_p$ using inverse operators:
$$y_p = \frac{1}{f(D)} f(e^z)$$

**Common Shortcuts:**
- **Exponential:** If $f(z) = e^{az}$, replace $D$ with $a$.
- **Trig:** If $f(z) = \sin(az)$, replace $D^2$ with $-a^2$.
- **Polynomial:** If $f(z) = z^n$, use Binomial expansion $(1 + g(D))^{-1}$.

## 5. Back-Substitution
[cite_start]Always convert your final result from the $z$-domain back to the $x$-domain[cite: 25]:
- [cite_start]Replace $z$ with $\ln(x)$ [cite: 25]
- [cite_start]Replace $e^z$ with $x$ [cite: 25]