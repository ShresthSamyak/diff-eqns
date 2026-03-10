# Laplace Transform — Exponential Shifting Property

## 1. First Shifting Property

If

$$L\{f(t)\} = F(s)$$

then

$$L\{e^{at}f(t)\} = F(s-a)$$

This means multiplying a function by $e^{at}$ shifts the Laplace transform.

---

## 2. Negative Exponential Shift

If

$$L\{f(t)\} = F(s)$$

then

$$L\{e^{-at}f(t)\} = F(s+a)$$

So the rule becomes:

| Function | Replace $s$ with |
|------|------|
| $e^{at}f(t)$ | $s-a$ |
| $e^{-at}f(t)$ | $s+a$ |

---

## 3. Intuition Behind the Property

From the Laplace definition

$$L\{f(t)\} = \int_0^\infty e^{-st}f(t)\,dt$$

If the function is multiplied by $e^{at}$:

$$L\{e^{at}f(t)\} = \int_0^\infty e^{-st}e^{at}f(t)\,dt$$

Combine the exponentials:

$$e^{-st}e^{at} = e^{-(s-a)t}$$

So the transform becomes

$$F(s-a)$$

---

## 4. Example 1

Find

$$L(e^{3t}t)$$

We know

$$L(t)=\frac{1}{s^2}$$

Apply the shift:

$$s \rightarrow s-3$$

Result

$$L(e^{3t}t)=\frac{1}{(s-3)^2}$$

---

## 5. Example 2

Find

$$L(e^{-3t}t^4)$$

Step 1: Basic Laplace

$$L(t^4)=\frac{4!}{s^5}=\frac{24}{s^5}$$

Step 2: Apply shift

$$s \rightarrow s+3$$

Result

$$L(e^{-3t}t^4)=\frac{24}{(s+3)^5}$$

---

## 6. Example 3

Find

$$L(e^{-3t}\sin 5t)$$

First

$$L(\sin 5t)=\frac{5}{s^2+25}$$

Apply shift

$$s \rightarrow s+3$$

Result

$$L(e^{-3t}\sin5t)=\frac{5}{(s+3)^2+25}$$

---

## 7. Strategy for Problems

1. Ignore the exponential first.
2. Compute the Laplace transform of the remaining function.
3. Apply the shift:
   - $s-a$ for $e^{at}$
   - $s+a$ for $e^{-at}$.

---

### Key Idea

Multiplying by an exponential **shifts the Laplace transform horizontally in the $s$-domain**.