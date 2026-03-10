# Laplace Transform — Common Exam Tricks & Mistakes

This file contains useful tricks, shortcuts, and common mistakes
students make while solving Laplace transform problems.

These tips help solve problems **faster during exams**.

---

# 1. Recognize Standard Patterns Quickly

Most Laplace problems reduce to pattern recognition.

### Common patterns

| Expression | Result |
|---|---|
| $\frac{1}{s}$ | $1$ |
| $\frac{1}{s^2}$ | $t$ |
| $\frac{1}{s-a}$ | $e^{at}$ |
| $\frac{s}{s^2+a^2}$ | $\cos(at)$ |
| $\frac{a}{s^2+a^2}$ | $\sin(at)$ |

---

# 2. Watch for Exponential Shifts

If you see

$$
(s-a)
$$

in the denominator, expect an exponential term.

Example

$$
L^{-1}\left(\frac{1}{s-4}\right)=e^{4t}
$$

Example

$$
L^{-1}\left(\frac{1}{s+3}\right)=e^{-3t}
$$

---

# 3. Complete the Square Quickly

Expressions like

$$
s^2 + 6s + 13
$$

should immediately become

$$
(s+3)^2 + 4
$$

This helps match sine/cosine formulas.

Example

$$
L^{-1}\left(\frac{1}{s^2+6s+13}\right)
=
\frac{1}{2}e^{-3t}\sin2t
$$

---

# 4. Always Try Partial Fractions

If the denominator contains multiple factors:

Example

$$
\frac{2s-5}{(s-3)(s+3)}
$$

Use

$$
\frac{A}{s-3}+\frac{B}{s+3}
$$

This converts the expression into standard Laplace forms.

---

# 5. Look for $t$ Multiplication

If a function is multiplied by $t$:

$$
L(tf(t))=-\frac{d}{ds}F(s)
$$

This appears often in exam questions.

Example

$$
L(t\sin t)
$$

---

# 6. Use the Laplace Integral Trick

To evaluate

$$
\int_0^\infty f(t)dt
$$

use

$$
\int_0^\infty f(t)dt = L\{f(t)\}\Big|_{s=0}
$$

Example

$$
\int_0^\infty t e^{-3t}\sin t dt
$$

Compute Laplace transform first, then substitute $s=0$.

---

# 7. Differential Equation Shortcut

When solving DEs using Laplace:

1. Replace derivatives immediately

$$
y' \rightarrow sY(s)-y(0)
$$

$$
y'' \rightarrow s^2Y(s)-sy(0)-y'(0)
$$

2. Solve algebraically for $Y(s)$.
3. Apply inverse Laplace.

---

# 8. Common Mistakes

### Forgetting initial conditions

Students often forget to substitute

$$
y(0),\; y'(0)
$$

when transforming derivatives.

---

### Incorrect partial fractions

Always match the decomposition with the denominator.

Example

$$
\frac{1}{s^2(s+3)}
$$

should be

$$
\frac{A}{s} + \frac{B}{s^2} + \frac{C}{s+3}
$$

---

### Not recognizing shifts

Expressions like

$$
(s+2)^2 + 9
$$

should immediately signal

$$
e^{-2t}\sin(3t) \text{ or } e^{-2t}\cos(3t)
$$

---

# Key Exam Advice

1. Memorize the **standard Laplace table**.
2. Practice **partial fractions quickly**.
3. Recognize **shifts and patterns immediately**.

Laplace transform problems are mostly **pattern recognition + algebra**.