# Integration Techniques - Formula Sheet
## Quick Reference Guide

---

## Basic Integration Formulas

### Power Rule
$$\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$$

### Special Cases
$$\int \frac{1}{x} \, dx = \ln|x| + C$$

$$\int e^x \, dx = e^x + C$$

$$\int a^x \, dx = \frac{a^x}{\ln a} + C \quad (a > 0, a \neq 1)$$

---

## Trigonometric Integrals

$$\int \sin(x) \, dx = -\cos(x) + C$$

$$\int \cos(x) \, dx = \sin(x) + C$$

$$\int \tan(x) \, dx = -\ln|\cos(x)| + C = \ln|\sec(x)| + C$$

$$\int \cot(x) \, dx = \ln|\sin(x)| + C$$

$$\int \sec(x) \, dx = \ln|\sec(x) + \tan(x)| + C$$

$$\int \csc(x) \, dx = -\ln|\csc(x) + \cot(x)| + C$$

$$\int \sec^2(x) \, dx = \tan(x) + C$$

$$\int \csc^2(x) \, dx = -\cot(x) + C$$

$$\int \sec(x)\tan(x) \, dx = \sec(x) + C$$

$$\int \csc(x)\cot(x) \, dx = -\csc(x) + C$$

---

## U-Substitution Formula

$$\int f(g(x)) \cdot g'(x) \, dx = \int f(u) \, du = F(u) + C = F(g(x)) + C$$

where $u = g(x)$ and $du = g'(x) dx$

---

## Integration by Parts Formula

$$\int u \, dv = uv - \int v \, du$$

**LIATE Priority for choosing u:**
1. **L** - Logarithmic (ln, log)
2. **I** - Inverse trig (arcsin, arccos, etc.)
3. **A** - Algebraic (polynomials)
4. **T** - Trigonometric (sin, cos)
5. **E** - Exponential (e^x)

---

## Trigonometric Identities

### Pythagorean Identities
$$\sin^2(x) + \cos^2(x) = 1$$
$$1 + \tan^2(x) = \sec^2(x)$$
$$1 + \cot^2(x) = \csc^2(x)$$

### Power Reduction Formulas
$$\sin^2(x) = \frac{1 - \cos(2x)}{2}$$
$$\cos^2(x) = \frac{1 + \cos(2x)}{2}$$
$$\tan^2(x) = \frac{1 - \cos(2x)}{1 + \cos(2x)}$$

### Product-to-Sum Formulas
$$\sin(A)\sin(B) = \frac{1}{2}[\cos(A-B) - \cos(A+B)]$$
$$\cos(A)\cos(B) = \frac{1}{2}[\cos(A-B) + \cos(A+B)]$$
$$\sin(A)\cos(B) = \frac{1}{2}[\sin(A+B) + \sin(A-B)]$$

---

## Partial Fractions Decomposition

### General Form
$$\frac{P(x)}{(x-a)^m(x^2+bx+c)^n} = \frac{A_1}{x-a} + \frac{A_2}{(x-a)^2} + \cdots + \frac{Bx+C}{x^2+bx+c} + \cdots$$

### Simple Cases
**Distinct Linear Factors:**
$$\frac{A}{(x-a)(x-b)} = \frac{A}{x-a} + \frac{B}{x-b}$$

**Repeated Linear Factors:**
$$\frac{P(x)}{(x-a)^n} = \frac{A_1}{x-a} + \frac{A_2}{(x-a)^2} + \cdots + \frac{A_n}{(x-a)^n}$$

**Irreducible Quadratic:**
$$\frac{Ax+B}{x^2+bx+c}$$

---

## Inverse Trigonometric Integrals

$$\int \frac{1}{\sqrt{1-u^2}} \, du = \arcsin(u) + C$$

$$\int \frac{1}{1+u^2} \, du = \arctan(u) + C$$

$$\int \frac{1}{|u|\sqrt{u^2-1}} \, du = \operatorname{arcsec}(|u|) + C$$

---

## Hyperbolic Function Integrals

$$\int \sinh(x) \, dx = \cosh(x) + C$$

$$\int \cosh(x) \, dx = \sinh(x) + C$$

$$\int \tanh(x) \, dx = \ln|\cosh(x)| + C$$

---

## Important Integral Types

### Type: $\int \frac{du}{\sqrt{a^2-u^2}}$ (a > 0)
**Result:** $\arcsin(u/a) + C$

**Trigonometric Substitution:** $u = a\sin(\theta)$

### Type: $\int \frac{du}{a^2+u^2}$ (a > 0)
**Result:** $\frac{1}{a}\arctan(u/a) + C$

**Trigonometric Substitution:** $u = a\tan(\theta)$

### Type: $\int \frac{du}{\sqrt{u^2-a^2}}$ (a > 0)
**Result:** $\operatorname{arcsec}(|u|/a) + C$ or $\cosh^{-1}(u/a) + C$

**Trigonometric Substitution:** $u = a\sec(\theta)$

---

## Trigonometric Substitution Table

| Expression | Substitution | Identity Used | Resulting Form |
|------------|--------------|---------------|----------------|
| $\sqrt{a^2-u^2}$ | $u = a\sin\theta$ | $1-\sin^2\theta = \cos^2\theta$ | $a\cos\theta$ |
| $\sqrt{a^2+u^2}$ | $u = a\tan\theta$ | $1+\tan^2\theta = \sec^2\theta$ | $a\sec\theta$ |
| $\sqrt{u^2-a^2}$ | $u = a\sec\theta$ | $\sec^2\theta-1 = \tan^2\theta$ | $a\tan\theta$ |

---

## Reduction Formulas

$$\int \sin^n(x) \, dx = -\frac{1}{n}\sin^{n-1}(x)\cos(x) + \frac{n-1}{n}\int \sin^{n-2}(x) \, dx$$

$$\int \cos^n(x) \, dx = \frac{1}{n}\cos^{n-1}(x)\sin(x) + \frac{n-1}{n}\int \cos^{n-2}(x) \, dx$$

---

## Common Integrals (By Type)

### Logarithmic
$$\int \ln(x) \, dx = x\ln(x) - x + C$$

$$\int x\ln(x) \, dx = \frac{x^2}{2}\ln(x) - \frac{x^2}{4} + C$$

### Exponential Times Polynomial
$$\int x e^{ax} \, dx = e^{ax}\left(\frac{x}{a} - \frac{1}{a^2}\right) + C$$

$$\int x^2 e^{ax} \, dx = e^{ax}\left(\frac{x^2}{a} - \frac{2x}{a^2} + \frac{2}{a^3}\right) + C$$

### Trigonometric Times Exponential
$$\int e^{ax}\sin(bx) \, dx = \frac{e^{ax}(a\sin(bx) - b\cos(bx))}{a^2+b^2} + C$$

$$\int e^{ax}\cos(bx) \, dx = \frac{e^{ax}(a\cos(bx) + b\sin(bx))}{a^2+b^2} + C$$

---

## Quick Decision Guide

**Does it look like a chain rule?**
→ Try **U-Substitution**

**Is it a product of two different functions?**
→ Try **Integration by Parts**

**Does it have powers of sin/cos or tan/sec?**
→ Try **Trig Integrals** or **Trig Substitution**

**Is it a rational function (polynomial/polynomial)?**
→ Try **Partial Fractions**

**Does it fit none of the above?**
→ Consider **Completing the Square** or **Special Techniques**

---

**Print this sheet and keep it handy while studying!**
