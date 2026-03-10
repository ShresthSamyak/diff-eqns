# Laplace Transform — Unit Step Function

## 1. Definition

The **unit step function** (also called the Heaviside function) is defined as:

$$
u(t-a) =
\begin{cases}
0, & t < a \\
1, & t \ge a
\end{cases}
$$

It represents a function that **turns on at time $t=a$**.

---

## 2. Basic Laplace Transform

$$
L\{u(t-a)\} = \frac{e^{-as}}{s}
$$

This means the Laplace transform of a delayed step produces an **exponential factor**.

---

## 3. Shifting Property with Unit Step

If

$$
L\{f(t)\} = F(s)
$$

then

$$
L\{f(t-a)u(t-a)\} = e^{-as}F(s)
$$

This property is used to transform **delayed signals**.

---

## 4. Example 1

Find

$$
L\{u(t-3)\}
$$

Using the formula:

$$
L\{u(t-a)\} = \frac{e^{-as}}{s}
$$

Result:

$$
\frac{e^{-3s}}{s}
$$

---

## 5. Example 2

Find

$$
L\{(t-2)u(t-2)\}
$$

First identify the base function:

$$
f(t) = t
$$

Laplace transform:

$$
L\{t\} = \frac{1}{s^2}
$$

Apply shifting:

$$
L\{(t-2)u(t-2)\} = e^{-2s}\frac{1}{s^2}
$$

---

## 6. Example 3

Find

$$
L\{\sin(t-4)u(t-4)\}
$$

Base transform:

$$
L\{\sin t\} = \frac{1}{s^2+1}
$$

Apply shift:

$$
L\{\sin(t-4)u(t-4)\} = e^{-4s}\frac{1}{s^2+1}
$$

---

## 7. Converting Piecewise Functions

Example:

$$
f(t) =
\begin{cases}
0, & t < 2 \\
t-2, & t \ge 2
\end{cases}
$$

Rewrite using step function:

$$
f(t) = (t-2)u(t-2)
$$

Then apply Laplace transform.

---

## 8. Strategy for Problems

1. Convert piecewise functions into unit step form.
2. Identify the base function $f(t-a)$.
3. Apply the shifting property.

---

### Key Idea

Unit step functions allow us to represent **piecewise functions using Laplace transforms**.