# Laplace Transform — Laplace of Integrals

## 1. Property

If

$$L\{f(t)\} = F(s)$$

then

$$L\left(\int_0^t f(u)\,du\right) = \frac{F(s)}{s}$$

Meaning:

Taking an **integral in the time domain** corresponds to **division by $s$ in the Laplace domain**.

---

## 2. Intuition

From the Laplace definition

$$L\{f(t)\} = \int_0^\infty e^{-st}f(t)dt$$

If

$$g(t)=\int_0^t f(u)du$$

then

$$L\{g(t)\} = \frac{1}{s}F(s)$$

So integration in time produces an extra **factor $\frac{1}{s}$**.

---

## 3. Example 1

Find

$$L\left(\int_0^t e^{-2u}u^3\,du\right)$$

Step 1: Identify the inner function

$$f(t)=e^{-2t}t^3$$

Step 2: Find Laplace of $f(t)$

First

$$L(t^3)=\frac{3!}{s^4}=\frac{6}{s^4}$$

Apply exponential shift

$$s \rightarrow s+2$$

$$F(s)=\frac{6}{(s+2)^4}$$

Step 3: Apply the integral property

$$L\left(\int_0^t e^{-2u}u^3du\right)=\frac{1}{s}\cdot\frac{6}{(s+2)^4}$$

Final result

$$=\frac{6}{s(s+2)^4}$$

---

## 4. Example 2

Find

$$L\left(\int_0^t \cosh(u)\,du\right)$$

Step 1: Base transform

$$L(\cosh t)=\frac{s}{s^2-1}$$

Step 2: Apply property

$$L\left(\int_0^t \cosh(u)\,du\right)=\frac{1}{s}\cdot\frac{s}{s^2-1}$$

Result

$$=\frac{1}{s^2-1}$$

---

## 5. Example 3

Find

$$L\left(\int_0^t e^{-4u}\sin 3u\,du\right)$$

Step 1: Base transform

$$L(\sin 3t)=\frac{3}{s^2+9}$$

Apply exponential shift

$$s \rightarrow s+4$$

$$F(s)=\frac{3}{(s+4)^2+9}$$

Step 2: Apply integral property

$$L\left(\int_0^t e^{-4u}\sin3u\,du\right)=\frac{1}{s}\cdot\frac{3}{(s+4)^2+9}$$

Final result

$$=\frac{3}{s\big((s+4)^2+9\big)}$$

---

## 6. Strategy for Problems

1. Identify the function inside the integral.
2. Compute its Laplace transform.
3. Divide the result by $s$.

---

### Key Idea

Integration in time-domain  

$$\int_0^t f(u)du$$

becomes

$$\frac{F(s)}{s}$$

in the Laplace domain.