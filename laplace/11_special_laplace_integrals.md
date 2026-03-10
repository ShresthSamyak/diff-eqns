# Special Integrals Using Laplace Transform

Some definite integrals that are difficult to evaluate using standard calculus
can be solved using Laplace transform identities.

These results frequently appear in Laplace transform problems.

---

# 1. Key Identity

$$
\int_0^\infty f(t)\,dt = L\{f(t)\}\Big|_{s=0}
$$

Meaning:

To evaluate

$$
\int_0^\infty f(t)dt
$$

1. Find the Laplace transform $F(s)$
2. Substitute $s = 0$

---

# 2. Logarithmic Identity

One important result is

$$
\int_0^\infty \frac{\cos(at)-\cos(bt)}{t}dt
=
\ln\left(\frac{b}{a}\right)
$$

This identity appears when applying the property

$$
L\left(\frac{1-\cos(at)}{t}\right)
$$

---

## Example

Evaluate

$$
\int_0^\infty \frac{\cos 6t - \cos 4t}{t}dt
$$

Compare with

$$
\int_0^\infty \frac{\cos(at)-\cos(bt)}{t}dt
=
\ln\left(\frac{b}{a}\right)
$$

Here

$$
a = 6,\quad b = 4
$$

Result

$$
= \ln\left(\frac{4}{6}\right)
$$

$$
= \ln\left(\frac{2}{3}\right)
$$

---

# 3. Sine Integral Identity

Another useful identity is

$$
\int_0^\infty \frac{\sin(at)}{t}dt
=
\frac{\pi}{2}
$$

for $a>0$.

---

# 4. Example

Evaluate

$$
\int_0^\infty \frac{\sin 3t}{t}dt
$$

Using the identity

$$
\int_0^\infty \frac{\sin(at)}{t}dt = \frac{\pi}{2}
$$

Result

$$
= \frac{\pi}{2}
$$

---

# 5. Laplace-Based Evaluation

Consider

$$
\int_0^\infty t e^{-3t}\sin t\,dt
$$

Step 1: Identify function

$$
f(t)=t e^{-3t}\sin t
$$

Step 2: Use Laplace transform

$$
L\{f(t)\}
=
\frac{2(s+3)}{((s+3)^2+1)^2}
$$

Step 3: Substitute $s=0$

$$
=
\frac{2(3)}{(9+1)^2}
=
\frac{6}{100}
=
\frac{3}{50}
$$

---

# Key Idea

Laplace transforms allow evaluation of otherwise difficult integrals by
converting them into algebraic expressions in the $s$-domain.