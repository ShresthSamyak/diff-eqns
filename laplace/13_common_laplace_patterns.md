# Common Laplace Transform Patterns (Exam Cheat Sheet)

These patterns appear frequently in Laplace transform problems.
Recognizing them quickly saves a lot of time in exams.

---

# 1. Power Functions

$$L(t^n) = \frac{n!}{s^{n+1}}$$

Examples

$$L(t) = \frac{1}{s^2}$$

$$L(t^2) = \frac{2}{s^3}$$

---

# 2. Exponential Functions

$$L(e^{at}) = \frac{1}{s-a}$$

Example

$$L(e^{3t}) = \frac{1}{s-3}$$

---

# 3. Trigonometric Functions

### Cosine

$$L(\cos at) = \frac{s}{s^2 + a^2}$$

Example

$$L(\cos 2t) = \frac{s}{s^2 + 4}$$

---

### Sine

$$L(\sin at) = \frac{a}{s^2 + a^2}$$

Example

$$L(\sin 3t) = \frac{3}{s^2 + 9}$$

---

# 4. Hyperbolic Functions

$$L(\sinh at) = \frac{a}{s^2 - a^2}$$

$$L(\cosh at) = \frac{s}{s^2 - a^2}$$

---

# 5. Exponential Shift

If

$$L\{f(t)\} = F(s)$$

then

$$L\{e^{at}f(t)\} = F(s-a)$$

Example

$$L(e^{-2t}\sin t) = \frac{1}{(s+2)^2+1}$$

---

# 6. Multiplication by $t$

$$L(tf(t)) = -\frac{d}{ds}F(s)$$

Example

$$L(t\sin t) = \frac{2s}{(s^2+1)^2}$$

---

# 7. Division by $t$

$$L\left(\frac{f(t)}{t}\right) = \int_s^\infty F(u)du$$

Example

$$L\left(\frac{\sin t}{t}\right) = \tan^{-1}\left(\frac{1}{s}\right)$$

---

# 8. Unit Step Function

$$L\{u(t-a)\} = \frac{e^{-as}}{s}$$

---

# 9. Inverse Laplace Patterns

| Expression | Inverse |
|---|---|
| $\frac{1}{s}$ | $1$ |
| $\frac{1}{s^2}$ | $t$ |
| $\frac{1}{s-a}$ | $e^{at}$ |
| $\frac{s}{s^2+a^2}$ | $\cos(at)$ |
| $\frac{a}{s^2+a^2}$ | $\sin(at)$ |

---

# Key Idea

Most Laplace problems reduce to **pattern recognition**.