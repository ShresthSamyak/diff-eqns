# Solving Differential Equations Using Laplace Transform

Laplace transforms convert differential equations into algebraic equations,
which are much easier to solve.

---

# 1. Core Idea

Laplace transform converts

$$
\text{Differential Equations} \rightarrow \text{Algebraic Equations}
$$

This allows us to solve differential equations systematically.

---

# 2. Key Formulas for Derivatives

Let

$$
L\{y(t)\} = Y(s)
$$

Then

### First derivative

$$
L\{y'(t)\} = sY(s) - y(0)
$$

### Second derivative

$$
L\{y''(t)\} = s^2Y(s) - s\,y(0) - y'(0)
$$

### Third derivative

$$
L\{y'''(t)\} = s^3Y(s) - s^2y(0) - s y'(0) - y''(0)
$$

---

# 3. General Method

To solve a differential equation using Laplace transform:

### Step 1

Take Laplace transform of both sides.

---

### Step 2

Use derivative formulas to replace derivatives.

Example

$$
y' \rightarrow sY(s) - y(0)
$$

---

### Step 3

Substitute initial conditions.

Example

$$
y(0), \quad y'(0)
$$

---

### Step 4

Solve the resulting algebraic equation for $Y(s)$.

---

### Step 5

Take inverse Laplace transform to obtain $y(t)$.

---

# 4. Example

Solve

$$
y' + y = \cos(2t), \quad y(0) = 1
$$

---

## Step 1: Take Laplace transform

$$
L(y') + L(y) = L(\cos 2t)
$$

---

## Step 2: Apply formulas

$$
L(y') = sY(s) - y(0)
$$

$$
L(y) = Y(s)
$$

$$
L(\cos 2t) = \frac{s}{s^2+4}
$$

Substitute

$$
(sY(s)-1) + Y(s) = \frac{s}{s^2+4}
$$

---

## Step 3: Simplify

$$
(s+1)Y(s) - 1 = \frac{s}{s^2+4}
$$

---

## Step 4: Solve for $Y(s)$

$$
(s+1)Y(s) = \frac{s}{s^2+4} + 1
$$

Combine fractions

$$
Y(s)=\frac{s^2+s+4}{(s^2+4)(s+1)}
$$

---

## Step 5: Partial fractions

$$
Y(s)=\frac{4}{5}\frac{1}{s+1}
+
\frac{1}{5}\frac{s}{s^2+4}
+
\frac{4}{5}\frac{1}{s^2+4}
$$

---

## Step 6: Inverse Laplace

$$
L^{-1}\left(\frac{1}{s+1}\right)=e^{-t}
$$

$$
L^{-1}\left(\frac{s}{s^2+4}\right)=\cos 2t
$$

$$
L^{-1}\left(\frac{2}{s^2+4}\right)=\sin 2t
$$

Final solution

$$
y(t)=\frac{4}{5}e^{-t}+\frac{1}{5}\cos 2t+\frac{2}{5}\sin 2t
$$

---

# 5. Strategy for Laplace Differential Equations

1. Take Laplace transform of the equation.
2. Replace derivatives using formulas.
3. Insert initial conditions.
4. Solve algebraically for $Y(s)$.
5. Apply inverse Laplace transform.

---

### Key Idea

Laplace transforms allow solving differential equations **without direct integration**.