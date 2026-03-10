# Inverse Laplace Transform — Basics

## 1. Definition

The inverse Laplace transform converts a function from the **$s$-domain** back to the **time-domain**.

If

$$F(s) = L\{f(t)\}$$

then

$$f(t) = L^{-1}\{F(s)\}$$

Meaning:

Laplace transform and inverse Laplace transform are **inverse operations**.

---

## 2. Basic Inverse Laplace Formulas

### Constant

$$L^{-1}\left(\frac{1}{s}\right) = 1$$

---

### Powers of $s$

$$L^{-1}\left(\frac{1}{s^2}\right) = t$$

$$L^{-1}\left(\frac{1}{s^3}\right) = \frac{t^2}{2}$$

General formula:

$$L^{-1}\left(\frac{1}{s^{n+1}}\right) = \frac{t^n}{n!}$$

---

### Exponential Functions

$$L^{-1}\left(\frac{1}{s-a}\right) = e^{at}$$

Example

$$L^{-1}\left(\frac{1}{s-3}\right) = e^{3t}$$

---

### Trigonometric Functions

#### Cosine

$$L^{-1}\left(\frac{s}{s^2+a^2}\right) = \cos(at)$$

Example

$$L^{-1}\left(\frac{s}{s^2+4}\right) = \cos(2t)$$

---

#### Sine

$$L^{-1}\left(\frac{a}{s^2+a^2}\right) = \sin(at)$$

Example

$$L^{-1}\left(\frac{3}{s^2+9}\right) = \sin(3t)$$

---

### Hyperbolic Functions

$$L^{-1}\left(\frac{s}{s^2-a^2}\right) = \cosh(at)$$

$$L^{-1}\left(\frac{a}{s^2-a^2}\right) = \sinh(at)$$

---

## 3. Linearity Property

Inverse Laplace is also linear.

$$
L^{-1}\{aF(s) + bG(s)\}
=
aL^{-1}\{F(s)\}
+
bL^{-1}\{G(s)\}
$$

Example

$$L^{-1}\left(\frac{4}{s}+\frac{2}{s^2}\right)$$

Split

$$=4L^{-1}\left(\frac{1}{s}\right)+2L^{-1}\left(\frac{1}{s^2}\right)$$

Result

$$=4+2t$$

---

## 4. Example

Find

$$L^{-1}\left(\frac{2s}{s^2+9}\right)$$

Compare with formula

$$L^{-1}\left(\frac{s}{s^2+a^2}\right)=\cos(at)$$

Here

$$a=3$$

Result

$$=2\cos(3t)$$

---

## 5. Strategy for Inverse Laplace Problems

1. Identify the form of $F(s)$.
2. Match with standard Laplace formulas.
3. Use linearity if multiple terms appear.

---

### Key Idea

Inverse Laplace is mostly **pattern recognition**.