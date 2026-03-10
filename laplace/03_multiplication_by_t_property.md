# Laplace Transform — Multiplication by $t$ Property

## 1. Property

If

$$L\{f(t)\} = F(s)$$

then multiplying the function by $t$ gives

$$L\{t f(t)\} = -\frac{d}{ds}F(s)$$

This means **multiplication by $t$ in time-domain becomes differentiation in the $s$-domain**.

---

## 2. Higher Powers of $t$

If the function is multiplied by higher powers of $t$:

### First power
$$L\{t f(t)\} = -\frac{d}{ds}F(s)$$

### Second power
$$L\{t^2 f(t)\} = \frac{d^2}{ds^2}F(s)$$

### General rule

$$L\{t^n f(t)\} = (-1)^n \frac{d^n}{ds^n}F(s)$$

---

## 3. Why This Works

From the Laplace definition

$$L\{f(t)\} = \int_0^\infty e^{-st}f(t)dt$$

Differentiating with respect to $s$:

$$\frac{d}{ds}F(s) = \frac{d}{ds}\left(\int_0^\infty e^{-st}f(t)dt\right)$$

Derivative of $e^{-st}$:

$$\frac{d}{ds}(e^{-st}) = -t e^{-st}$$

So

$$\frac{d}{ds}F(s) = -\int_0^\infty t e^{-st}f(t)dt$$

Therefore

$$L\{t f(t)\} = -\frac{d}{ds}F(s)$$

---

## 4. Example 1

Find

$$L(t\sin t)$$

Step 1: Basic transform

$$L(\sin t)=\frac{1}{s^2+1}$$

Step 2: Apply property

$$L(t\sin t) = -\frac{d}{ds}\left(\frac{1}{s^2+1}\right)$$

Differentiate

$$\frac{d}{ds}\left(\frac{1}{s^2+1}\right) = -\frac{2s}{(s^2+1)^2}$$

Final result

$$L(t\sin t)=\frac{2s}{(s^2+1)^2}$$

---

## 5. Example 2

Find

$$L(t\cos t)$$

Step 1: Basic transform

$$L(\cos t)=\frac{s}{s^2+1}$$

Step 2: Apply property

$$L(t\cos t)=-\frac{d}{ds}\left(\frac{s}{s^2+1}\right)$$

Differentiate

$$=\frac{s^2-1}{(s^2+1)^2}$$

---

## 6. Example 3

Find

$$L(t^2\cos t)$$

Step 1: Base transform

$$F(s)=\frac{s}{s^2+1}$$

Step 2: Apply second derivative

$$L(t^2\cos t)=\frac{d^2}{ds^2}\left(\frac{s}{s^2+1}\right)$$

Final result

$$L(t^2\cos t)=\frac{2s(s^2-3)}{(s^2+1)^3}$$

---

## 7. Strategy for Problems

1. Find the Laplace transform of the **base function**.
2. Apply derivatives with respect to $s$.
3. Simplify the result.

---

### Key Idea

Multiplying by $t$ in time-domain  
$\rightarrow$ Differentiation in $s$-domain.