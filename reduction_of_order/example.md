# Reduction of Order — Examples

These examples demonstrate how to apply the **Reduction of Order formula** when one solution of a second-order differential equation is already known.

Formula:

$$
y_2 = y_1 \int \frac{e^{-\int P(x)dx}}{y_1^2}dx
$$

General solution:

$$
y = C_1 y_1 + C_2 y_2
$$

---

# Example 1

Solve:

$$
x^2y'' - xy' + y = 0
$$

given that

$$
y_1 = x
$$

---

## Step 1 — Standard Form

Divide by \(x^2\):

$$
y'' - \frac{1}{x}y' + \frac{1}{x^2}y = 0
$$

Thus

$$
P(x) = -\frac{1}{x}
$$

---

## Step 2 — Compute the exponential term

$$
\int P(x)dx = \int -\frac{1}{x}dx = -\ln x
$$

$$
e^{-\int P(x)dx} = e^{\ln x} = x
$$

---

## Step 3 — Apply Reduction of Order formula

$$
y_2 = x \int \frac{x}{x^2}dx
$$

$$
y_2 = x \int \frac{1}{x}dx
$$

$$
y_2 = x \ln x
$$

---

## Step 4 — General Solution

$$
y = C_1 x + C_2 x\ln x
$$

---

# Example 2

Solve:

$$
x^2y'' - x(x+2)y' + (x+2)y = 0
$$

given that

$$
y_1 = x
$$

---

## Step 1 — Convert to standard form

Divide by \(x^2\):

$$
y'' - \frac{x+2}{x}y' + \frac{x+2}{x^2}y = 0
$$

Thus

$$
P(x) = -\frac{x+2}{x}
$$

---

## Step 2 — Compute the integral

$$
\int P(x)dx
=
\int -\frac{x+2}{x}dx
$$

Rewrite:

$$
-\left(1+\frac{2}{x}\right)
$$

So

$$
\int P(x)dx = -x -2\ln x
$$

---

## Step 3 — Compute exponential factor

$$
e^{-\int P(x)dx}
=
e^{x+2\ln x}
$$

Using log rule:

$$
e^{x+2\ln x} = e^x x^2
$$

---

## Step 4 — Substitute into formula

$$
y_2 = x \int \frac{e^x x^2}{x^2}dx
$$

$$
y_2 = x \int e^x dx
$$

---

## Step 5 — Integrate

$$
y_2 = x e^x
$$

---

## Step 6 — General Solution

$$
y = C_1 x + C_2 x e^x
$$

---

# Example 3 (Typical Exam Pattern)

Find the second solution if

$$
y_1 = e^x
$$

for the equation

$$
y'' - y = 0
$$

---

## Step 1

Standard form already:

$$
P(x) = 0
$$

---

## Step 2

$$
\int P(x)dx = 0
$$

$$
e^{-\int P(x)dx} = 1
$$

---

## Step 3

Apply formula

$$
y_2 = e^x \int \frac{1}{e^{2x}}dx
$$

$$
y_2 = e^x \int e^{-2x}dx
$$

---

## Step 4

$$
y_2 = e^x \left(-\frac12 e^{-2x}\right)
$$

Simplify:

$$
y_2 = e^{-x}
$$

---

## Step 5 — General Solution

$$
y = C_1 e^x + C_2 e^{-x}
$$

---

# Key Exam Strategy

Use **Reduction of Order** when:

• One solution is given  
• Second-order linear homogeneous equation  
• Need the second independent solution

Recognize pattern:

> "If \(y_1(x)\) is a solution, find the general solution."

That immediately signals **Reduction of Order**.