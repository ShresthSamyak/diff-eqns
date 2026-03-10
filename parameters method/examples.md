# Examples — Variation of Parameters

This file contains worked examples using the **variation of parameters** method.

Refer to `method.md` for formulas such as

- Wronskian
- \(u_1', u_2'\)
- solution construction

---

# Example 1 — Conceptual Example

Solve

y'' + y = sin x

---

## Step 1 — Complementary Function

Solve the homogeneous equation

y'' + y = 0

Auxiliary equation

m² + 1 = 0

m = ± i

Thus

y₁ = cos x  
y₂ = sin x

So

y_c = C₁ cos x + C₂ sin x

---

## Step 2 — Wronskian

W = | y₁  y₂ |
    | y₁' y₂' |

y₁ = cos x  
y₂ = sin x

y₁' = −sin x  
y₂' = cos x

W = cos²x + sin²x = 1

---

## Step 3 — Compute u₁' and u₂'

From the formulas (see `method.md`)

u₁' = −y₂R(x) / W  
u₂' = y₁R(x) / W

Here

R(x) = sin x

So

u₁' = −sin²x  
u₂' = sin x cos x

---

## Step 4 — Integrate

Use trig identities.

sin²x = (1 − cos2x)/2

u₁ = −∫ sin²x dx

u₁ = −x/2 + sin2x/4

---

u₂ = ∫ sin x cos x dx

sin x cos x = (1/2)sin2x

u₂ = −cos2x / 4

---

## Step 5 — Particular Solution

y_p = u₁y₁ + u₂y₂

y_p =
(−x/2 + sin2x/4)cos x
− (cos2x/4)sin x

---

## Final Solution

y = y_c + y_p

---

# Example 2 — Moderate Example

Solve

y'' + y = sec x

---

## Complementary Function

y_c = C₁ cos x + C₂ sin x

---

## Wronskian

W = 1

---

## Compute u₁' and u₂'

R(x) = sec x

u₁' = −sin x sec x

u₁' = −tan x

u₂' = cos x sec x

u₂' = 1

---

## Integrate

u₁ = −∫ tan x dx

u₁ = −ln|sec x|

u₂ = ∫ 1 dx

u₂ = x

---

## Particular Solution

y_p = −cos x ln|sec x| + x sin x

---

# Example 3 — Exponential RHS

Solve

y'' + 3y' + 2y = 1 / (1 + e^x)

---

## Complementary Function

Auxiliary equation

m² + 3m + 2 = 0

m = −1, −2

y_c = C₁ e⁻ˣ + C₂ e⁻²ˣ

---

## Wronskian

W = −e⁻³ˣ

---

## Compute u₁' and u₂'

R(x) = 1/(1+e^x)

u₁' = e^x/(1+e^x)

u₂' = −e²ˣ/(1+e^x)

---

## Integrate

u₁ = ln(1 + e^x)

u₂ = −(e^x − ln(1 + e^x))

---

## Particular Solution

y_p =
e⁻ˣ ln(1 + e^x)
+
e⁻²ˣ (ln(1 + e^x) − e^x)

---

# Example 4 — Tricky Example

Solve

y'' + 3y' + 2y = sin(e^x)

---

## Complementary Function

y_c = C₁ e⁻ˣ + C₂ e⁻²ˣ

---

## Wronskian

W = −e⁻³ˣ

---

## Compute u₁' and u₂'

u₁' = e^x sin(e^x)

u₂' = −e²ˣ sin(e^x)

---

## Integrate

Use substitution

u = e^x

du = e^x dx

u₁ = −cos(e^x)

---

u₂ = e^x cos(e^x) − sin(e^x)

---

## Particular Solution

y_p = −e⁻²ˣ sin(e^x)

---

## Final Solution

y =
C₁ e⁻ˣ + C₂ e⁻²ˣ − e⁻²ˣ sin(e^x)

---

# Key Takeaways

- Always compute the **Wronskian** first.
- Simplify \(u₁'\) and \(u₂'\) before integrating.
- Many integrals require substitutions.
- Unlike undetermined coefficients, the final answer may contain **logarithms or non-elementary expressions**.