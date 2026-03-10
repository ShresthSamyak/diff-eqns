# Reduction of Order Method

Reduction of order is used to find the **second linearly independent solution** of a second-order differential equation when **one solution is already known**.

It works for equations of the form:

$$
y'' + P(x)y' + Q(x)y = 0
$$

where one solution **y₁(x)** is given.

---

# Goal

Given:

- Differential equation
- One solution **y₁(x)**

Find the **second solution y₂(x)**.

---

# Reduction of Order Formula

The second solution is:

$$
y_2 = y_1 \int \frac{e^{-\int P(x)\,dx}}{y_1^2} \, dx
$$

---

# Step-by-Step Method

## Step 1 — Write equation in standard form

Convert the equation into:

$$
y'' + P(x)y' + Q(x)y = 0
$$

If the equation is not in this form, divide by the coefficient of **y''**.

---

## Step 2 — Identify components

From the equation determine:

- **P(x)**
- given solution **y₁(x)**

---

## Step 3 — Compute

First calculate:

$$
\int P(x)dx
$$

Then compute:

$$
e^{-\int P(x)dx}
$$

---

## Step 4 — Substitute into formula

Use the formula:

$$
y_2 = y_1 \int \frac{e^{-\int P(x)dx}}{y_1^2} dx
$$

Simplify the integrand before integrating.

---

## Step 5 — Obtain the second solution

After integration, **y₂(x)** will be the **second linearly independent solution**.

---

# General Solution

Once both solutions are known:

$$
y = C_1 y_1 + C_2 y_2
$$

---

# When Reduction of Order is Used

Use this method when:

- One solution **y₁** is already given
- Equation is second order
- The equation is homogeneous

Example situation:

> "If **y₁ = x** is a solution of the equation, find the general solution."

---

# Important Properties

Two solutions must be **linearly independent**.

This means:

$$
\frac{y_2}{y_1} \neq \text{constant}
$$

---

# Recognition Pattern (Exam Tip)

If the problem states:

- *One solution is known*
- *Find the other solution*

Then the method to use is:

**Reduction of Order**

---

# Quick Formula Box

$$
y_2 = y_1 \int \frac{e^{-\int P(x)dx}}{y_1^2} dx
$$

General solution:

$$
y = C_1 y_1 + C_2 y_2
$$
