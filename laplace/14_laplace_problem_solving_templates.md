# Laplace Problem Solving Templates

This file provides standard step-by-step templates
for solving common Laplace transform problems.

---

# 1. Direct Laplace Transform

### Template

1. Split the function using linearity.
2. Apply standard Laplace formulas.
3. Simplify.

Example

$$L(4t^2 + \sin3t + e^{2t})$$

Step 1

$$=4L(t^2)+L(\sin3t)+L(e^{2t})$$

Step 2

$$=\frac{8}{s^3}+\frac{3}{s^2+9}+\frac{1}{s-2}$$

---

# 2. Exponential Shift Problems

### Template

1. Ignore the exponential first.
2. Find Laplace of the base function.
3. Replace $s$ with $(s-a)$ or $(s+a)$.

Example

$$L(e^{-3t}\sin t)$$

Step 1

$$L(\sin t)=\frac{1}{s^2+1}$$

Step 2

$$s \rightarrow s+3$$

Result

$$\frac{1}{(s+3)^2+1}$$

---

# 3. Inverse Laplace (Direct Pattern)

### Template

1. Compare with standard formulas.
2. Identify parameters.

Example

$$L^{-1}\left(\frac{s}{s^2+4}\right)$$

Compare

$$L^{-1}\left(\frac{s}{s^2+a^2}\right)=\cos(at)$$

Result

$$\cos(2t)$$

---

# 4. Inverse Laplace with Partial Fractions

### Template

1. Factor denominator.
2. Write partial fraction decomposition.
3. Solve constants.
4. Apply inverse Laplace formulas.

Example

$$\frac{2s-5}{s^2-9}$$

Factor

$$s^2-9=(s-3)(s+3)$$

Decompose

$$\frac{A}{s-3}+\frac{B}{s+3}$$

Solve for $A,B$.

Then apply inverse Laplace.

---

# 5. Differential Equation using Laplace

### Template

Step 1

Take Laplace transform of both sides.

Step 2

Replace derivatives

$$y' \rightarrow sY(s)-y(0)$$

$$y'' \rightarrow s^2Y(s)-sy(0)-y'(0)$$

Step 3

Substitute initial conditions.

Step 4

Solve algebraically for $Y(s)$.

Step 5

Take inverse Laplace.

---

# Example

$$y' + y = \cos2t,\quad y(0)=1$$

Result

$$y(t)=\frac{4}{5}e^{-t}+\frac{1}{5}\cos2t+\frac{2}{5}\sin2t$$

---

# Key Idea

Most Laplace problems follow **repeatable templates**.