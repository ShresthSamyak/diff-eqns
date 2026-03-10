# Laplace Transform — Laplace of Derivatives

## 1. First Derivative

Let

$$L\{y(t)\} = Y(s)$$

Then

$$L\{y'(t)\} = sY(s) - y(0)$$

Meaning:

Taking a derivative in time becomes **multiplication by $s$ in the Laplace domain**, with subtraction of the initial value.

---

## 2. Second Derivative

For the second derivative:

$$L\{y''(t)\} = s^2Y(s) - s\,y(0) - y'(0)$$

---

## 3. Third Derivative

$$L\{y'''(t)\} = s^3Y(s) - s^2y(0) - s y'(0) - y''(0)$$

---

## 4. General Pattern

For the $n^{th}$ derivative:

$$
L\{y^{(n)}(t)\}
=
s^n Y(s)
-
s^{n-1}y(0)
-
s^{n-2}y'(0)
-
\cdots
-
y^{(n-1)}(0)
$$

So every derivative introduces:

- Higher powers of $s$
- Initial conditions

---

## 5. Example 1

Find

$$L\{y'(t)\}$$

if

$$L\{y(t)\}=Y(s)$$

Using the formula:

$$L\{y'\}=sY(s)-y(0)$$

---

## 6. Example 2

Find

$$L\{y''(t)\}$$

Given

$$y(0)=2,\quad y'(0)=3$$

Using the formula

$$L\{y''\}=s^2Y(s)-s y(0)-y'(0)$$

Substitute values

$$=s^2Y(s)-2s-3$$

---

## 7. Example 3

Find

$$L\{y''+3y'+2y\}$$

Step 1: Transform each term

$$L(y'')=s^2Y(s)-s y(0)-y'(0)$$

$$L(y')=sY(s)-y(0)$$

$$L(y)=Y(s)$$

Step 2: Combine

$$
s^2Y(s)-s y(0)-y'(0)
+
3(sY(s)-y(0))
+
2Y(s)
$$

---

## 8. Why This Is Important

This property allows us to convert

**Differential equations**

into

**Algebraic equations in $s$**.

Example:

$$y'+y=\cos 2t$$

becomes

$$sY(s)-y(0)+Y(s)=\frac{s}{s^2+4}$$

which can then be solved for $Y(s)$.

---

## 9. Strategy for Laplace Differential Equations

1. Take Laplace transform of both sides.
2. Replace derivatives using formulas.
3. Substitute initial conditions.
4. Solve algebraically for $Y(s)$.
5. Take inverse Laplace to get $y(t)$.

---

### Key Idea

Laplace transform converts

$$\text{Differential Equations} \rightarrow \text{Algebraic Equations}$$