# Laplace Transform — Division by $t$ Property

## 1. Property

If

$$L\{f(t)\} = F(s)$$

then

$$L\left(\frac{f(t)}{t}\right) = \int_s^{\infty} F(u)\,du$$

Meaning:

Division by $t$ in the time domain becomes **integration in the $s$-domain**.

---

## 2. Key Idea

| Time Domain | $s$ Domain |
|------|------|
| $tf(t)$ | Differentiation |
| $\frac{f(t)}{t}$ | Integration |

So this property is the **reverse of the multiplication by $t$ rule**.

---

## 3. Example 1

Find

$$L\left(\frac{\sin t}{t}\right)$$

Step 1: Basic transform

$$L(\sin t)=\frac{1}{s^2+1}$$

Step 2: Apply property

$$L\left(\frac{\sin t}{t}\right) = \int_s^\infty \frac{1}{u^2+1}\,du$$

Step 3: Integrate

$$\int \frac{1}{u^2+1}du = \tan^{-1}(u)$$

Apply limits

$$=\frac{\pi}{2}-\tan^{-1}(s)$$

Using identity

$$\frac{\pi}{2}-\tan^{-1}(s)=\tan^{-1}\left(\frac{1}{s}\right)$$

Final result

$$L\left(\frac{\sin t}{t}\right)=\tan^{-1}\left(\frac{1}{s}\right)$$

---

## 4. Example 2

Find

$$L\left(\frac{1-\cos t}{t}\right)$$

Step 1: Laplace of numerator

$$L(1)=\frac{1}{s}$$

$$L(\cos t)=\frac{s}{s^2+1}$$

So

$$F(s)=\frac{1}{s}-\frac{s}{s^2+1}$$

Step 2: Apply property

$$L\left(\frac{1-\cos t}{t}\right)=\int_s^\infty \left(\frac{1}{u}-\frac{u}{u^2+1}\right)du$$

Step 3: Integrate

$$=\frac12 \ln\left(\frac{s^2+1}{s^2}\right)$$

---

## 5. Example 3

Find

$$L\left(\frac{e^{-t}\sin t}{t}\right)$$

Step 1: Base transform

$$L(\sin t)=\frac{1}{s^2+1}$$

Apply exponential shift

$$s \rightarrow s+1$$

$$F(s)=\frac{1}{(s+1)^2+1}$$

Step 2: Apply property

$$L\left(\frac{e^{-t}\sin t}{t}\right)=\int_s^\infty \frac{1}{(u+1)^2+1}\,du$$

Step 3: Integrate

$$=\frac{\pi}{2}-\tan^{-1}(s+1)$$

---

## 6. Strategy for Problems

1. Compute Laplace transform of $f(t)$.
2. Integrate $F(s)$ from $s$ to $\infty$.
3. Simplify using log or arctan formulas.

---

### Key Idea

Dividing by $t$ introduces **logarithmic or inverse-trigonometric functions** in the Laplace transform.