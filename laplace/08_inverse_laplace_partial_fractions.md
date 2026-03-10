# Inverse Laplace Transform — Partial Fractions Method

## 1. Why Partial Fractions Are Needed

Many Laplace expressions look like:

$$
\frac{P(s)}{Q(s)}
$$

where the denominator contains multiple factors.

Example

$$
\frac{2s-5}{s^2-9}
$$

We cannot directly take the inverse Laplace.

So we **decompose the fraction into simpler parts**.

---

## 2. Basic Idea

If the denominator factors as

$$
(s-a)(s-b)
$$

we write

$$
\frac{P(s)}{(s-a)(s-b)}
=
\frac{A}{s-a} + \frac{B}{s-b}
$$

Then we solve for constants $A$ and $B$.

---

## 3. Example 1

Find

$$
L^{-1}\left(\frac{2s-5}{s^2-9}\right)
$$

### Step 1: Factor denominator

$$
s^2-9 = (s-3)(s+3)
$$

---

### Step 2: Write partial fractions

$$
\frac{2s-5}{(s-3)(s+3)}
=
\frac{A}{s-3} + \frac{B}{s+3}
$$

---

### Step 3: Multiply by denominator

$$
2s-5 = A(s+3) + B(s-3)
$$

---

### Step 4: Expand

$$
2s-5 = (A+B)s + (3A-3B)
$$

---

### Step 5: Compare coefficients

For $s$:

$$
A+B=2
$$

For constants:

$$
3A-3B=-5
$$

Solving:

$$
A=\frac{1}{6}, \quad B=\frac{11}{6}
$$

---

### Step 6: Apply inverse Laplace

$$
L^{-1}\left(\frac{1}{s-a}\right)=e^{at}
$$

Result

$$
y(t)=\frac{1}{6}e^{3t}+\frac{11}{6}e^{-3t}
$$

---

## 4. Example 2

Find

$$
L^{-1}\left(\frac{1}{s^2(s+3)}\right)
$$

---

### Step 1: Write decomposition

$$
\frac{1}{s^2(s+3)}
=
\frac{A}{s} + \frac{B}{s^2} + \frac{C}{s+3}
$$

---

### Step 2: Multiply denominator

$$
1 = As(s+3) + B(s+3) + Cs^2
$$

---

### Step 3: Expand

$$
1 = (A+C)s^2 + (3A+B)s + 3B
$$

---

### Step 4: Compare coefficients

$$
A+C=0
$$

$$
3A+B=0
$$

$$
3B=1
$$

Solve

$$
B=\frac{1}{3},\quad A=-\frac{1}{9},\quad C=\frac{1}{9}
$$

---

### Step 5: Apply inverse Laplace

$$
L^{-1}\left(\frac{1}{s}\right)=1
$$

$$
L^{-1}\left(\frac{1}{s^2}\right)=t
$$

$$
L^{-1}\left(\frac{1}{s+3}\right)=e^{-3t}
$$

Final result

$$
y(t)=-\frac{1}{9}+\frac{t}{3}+\frac{1}{9}e^{-3t}
$$

---

## 5. Strategy

1. Factor the denominator.
2. Write the correct partial fraction form.
3. Solve constants.
4. Apply inverse Laplace formulas.

---

### Key Idea

Partial fractions convert complicated rational functions into **standard Laplace forms**.