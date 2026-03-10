# Inverse Laplace Transform — Shifting Property

## 1. First Shifting Property

If

$$L\{f(t)\} = F(s)$$

then

$$L^{-1}\{F(s-a)\} = e^{at}f(t)$$

Meaning:

A shift in the Laplace domain produces an **exponential multiplier in time-domain**.

---

## 2. Interpretation

| Laplace Domain | Time Domain |
|---|---|
| $F(s-a)$ | $e^{at}f(t)$ |
| $F(s+a)$ | $e^{-at}f(t)$ |

So shifting the variable $s$ corresponds to multiplying by an exponential function.

---

## 3. Example 1

Find

$$L^{-1}\left(\frac{1}{s-3}\right)$$

Compare with formula

$$L^{-1}\left(\frac{1}{s-a}\right) = e^{at}$$

Result

$$= e^{3t}$$

---

## 4. Example 2

Find

$$L^{-1}\left(\frac{1}{s+4}\right)$$

Rewrite

$$\frac{1}{s+4} = \frac{1}{s-(-4)}$$

Result

$$= e^{-4t}$$

---

## 5. Example 3

Find

$$L^{-1}\left(\frac{s-2}{(s-2)^2+9}\right)$$

Compare with

$$L^{-1}\left(\frac{s}{s^2+a^2}\right) = \cos(at)$$

Here

$$a=3$$

Apply shifting property

Result

$$= e^{2t}\cos(3t)$$

---

## 6. Example 4

Find

$$L^{-1}\left(\frac{5}{(s+1)^2+25}\right)$$

Compare with

$$L^{-1}\left(\frac{a}{s^2+a^2}\right)=\sin(at)$$

Here

$$a=5$$

Apply shift

$$s \rightarrow s+1$$

Result

$$= e^{-t}\sin(5t)$$

---

## 7. Strategy for Problems

1. Identify the standard Laplace form.
2. Detect the shift in $s$.
3. Apply exponential multiplier $e^{at}$.

---

### Key Idea

A shift in $s$ corresponds to multiplying by an **exponential function in time**.