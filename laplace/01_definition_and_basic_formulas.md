# Laplace Transform — Definition & Basic Formulas

## 1. Definition

The Laplace Transform of a function $f(t)$ is:

$$L\{f(t)\} = F(s) = \int_{0}^{\infty} e^{-st} f(t) dt$$



**Purpose:**
- Converts time-domain functions into algebraic expressions.
- Makes differential equations easier to solve.

---

## 2. Linearity Property

Laplace transform is linear:

$$L\{af(t) + bg(t)\} = aL\{f(t)\} + bL\{g(t)\}$$

**Example:**

$$L\{4t^2 + \sin 3t + e^{2t}\}$$

$$= 4L(t^2) + L(\sin 3t) + L(e^{2t})$$

---

## 3. Basic Laplace Transforms

### Constant
$$L(1) = \frac{1}{s}$$

---

### Power Functions
$$L(t) = \frac{1}{s^2}$$

$$L(t^2) = \frac{2}{s^3}$$

**General formula:**
$$L(t^n) = \frac{n!}{s^{n+1}}$$

---

### Exponential Functions
$$L(e^{at}) = \frac{1}{s-a}$$

**Example:**
$$L(e^{2t}) = \frac{1}{s-2}$$

---

### Trigonometric Functions

#### Sine
$$L(\sin at) = \frac{a}{s^2 + a^2}$$

**Example:**
$$L(\sin 3t) = \frac{3}{s^2 + 9}$$

#### Cosine
$$L(\cos at) = \frac{s}{s^2 + a^2}$$

**Example:**
$$L(\cos 2t) = \frac{s}{s^2 + 4}$$

---

### Hyperbolic Functions

#### Sinh
$$L(\sinh at) = \frac{a}{s^2 - a^2}$$

#### Cosh
$$L(\cosh at) = \frac{s}{s^2 - a^2}$$

---

## 4. Strategy for Basic Laplace Problems

1. **Split** the function using linearity.
2. **Apply** standard Laplace formulas.
3. **Simplify** the result.

**Example:**
$$L(4t^2 + \sin 3t + e^{2t})$$

**Step 1: Split**
$$= 4L(t^2) + L(\sin 3t) + L(e^{2t})$$

**Step 2: Apply formulas**
$$= 4\left(\frac{2}{s^3}\right) + \frac{3}{s^2 + 9} + \frac{1}{s - 2}$$

**Step 3: Final result**
$$= \frac{8}{s^3} + \frac{3}{s^2 + 9} + \frac{1}{s - 2}$$

---

### Key Idea
Laplace Transform converts:
**Differential equations $\rightarrow$ Algebraic equations**