# Chapter 3: Trigonometric Integrals & Substitutions
## Using Identities and Special Substitutions

---

## 🎯 Learning Objectives

After completing this chapter, you will:

- ✅ Integrate powers of sine and cosine
- ✅ Integrate powers of tangent and secant
- ✅ Apply trigonometric identities to simplify integrals
- ✅ Use trigonometric substitution for algebraic expressions
- ✅ Match expressions to appropriate substitutions
- ✅ Apply trigonometric integrals to BSECE AC circuit problems

**Time Estimate:** 10-12 hours  
**Difficulty:** Intermediate ⭐⭐  
**Prerequisites:** Chapters 1-2, trigonometric identities, u-substitution  

---

## 💡 Intuitive Explanation: Why Trig Functions?

### The Power Reduction Insight

Trigonometric integrals look intimidating, but there's a hidden secret: **Most can be reduced to simpler forms using identities.**

For example:
- $\sin^2(x)$ looks hard to integrate
- But using the identity $\sin^2(x) = \frac{1 - \cos(2x)}{2}$, it becomes simple!

### Trigonometric Substitution

When you see expressions like:
- $\sqrt{a^2 - u^2}$ → Use $u = a\sin(\theta)$ (creates a right triangle!)
- $\sqrt{a^2 + u^2}$ → Use $u = a\tan(\theta)$
- $\sqrt{u^2 - a^2}$ → Use $u = a\sec(\theta)$

These "magic" substitutions leverage the Pythagorean identity to eliminate the square root!

---

## 📋 Trigonometric Identities (Quick Reference)

### Pythagorean Identities
$$\sin^2(x) + \cos^2(x) = 1$$
$$1 + \tan^2(x) = \sec^2(x)$$
$$1 + \cot^2(x) = \csc^2(x)$$

### Power Reduction Formulas
$$\sin^2(x) = \frac{1 - \cos(2x)}{2}$$
$$\cos^2(x) = \frac{1 + \cos(2x)}{2}$$

### Product-to-Sum Formulas
$$\sin(A)\sin(B) = \frac{1}{2}[\cos(A-B) - \cos(A+B)]$$
$$\cos(A)\cos(B) = \frac{1}{2}[\cos(A-B) + \cos(A+B)]$$
$$\sin(A)\cos(B) = \frac{1}{2}[\sin(A+B) + \sin(A-B)]$$

---

## 🔍 Worked Examples

### Example 1: Power of Sine (Easy ⭐)

**Problem:** $\int \sin^2(x) \, dx$

**Solution:**

**Step 1: Recognize the pattern**
```
Odd powers of sin/cos → can usually solve with u-substitution
Even powers → use power reduction formula
```

**Step 2: Apply power reduction**
$$\sin^2(x) = \frac{1 - \cos(2x)}{2}$$

**Step 3: Integrate**
$$\int \sin^2(x) \, dx = \int \frac{1 - \cos(2x)}{2} \, dx$$
$$= \frac{1}{2} \int [1 - \cos(2x)] \, dx$$
$$= \frac{1}{2} \left[ x - \frac{\sin(2x)}{2} \right] + C$$
$$= \frac{x}{2} - \frac{\sin(2x)}{4} + C$$

---

### Example 2: Odd Power of Sine (Easy ⭐)

**Problem:** $\int \sin^3(x) \, dx$

**Solution:**

**Step 1: Separate one sine**
$$\sin^3(x) = \sin^2(x) \cdot \sin(x) = (1 - \cos^2(x)) \sin(x)$$

**Step 2: Use u-substitution**
```
u = cos(x)
du = -sin(x) dx
```

**Step 3: Rewrite and substitute**
$$\int \sin^3(x) \, dx = \int (1 - \cos^2(x)) \sin(x) \, dx$$
$$= \int (1 - u^2)(-du)$$
$$= -\int (1 - u^2) \, du$$

**Step 4: Integrate**
$$= -\left[ u - \frac{u^3}{3} \right] + C$$
$$= -\cos(x) + \frac{\cos^3(x)}{3} + C$$

---

### Example 3: Trigonometric Substitution (Medium ⭐⭐)

**Problem:** $\int \sqrt{4 - x^2} \, dx$

**Solution:**

**Step 1: Identify the pattern**
```
√(a² - x²) with a = 2
→ Use substitution x = 2sin(θ)
```

**Step 2: Set up substitution**
```
x = 2sin(θ)
dx = 2cos(θ) dθ
√(4 - x²) = √(4 - 4sin²(θ)) = √(4cos²(θ)) = 2|cos(θ)| = 2cos(θ)
(assuming 0 ≤ θ ≤ π/2)
```

**Step 3: Substitute**
$$\int \sqrt{4-x^2} \, dx = \int 2\cos(\theta) \cdot 2\cos(\theta) \, d\theta$$
$$= 4\int \cos^2(\theta) \, d\theta$$

**Step 4: Use power reduction**
$$\cos^2(\theta) = \frac{1 + \cos(2\theta)}{2}$$
$$= 4 \int \frac{1 + \cos(2\theta)}{2} \, d\theta$$
$$= 2 \int [1 + \cos(2\theta)] \, d\theta$$
$$= 2 \left[ \theta + \frac{\sin(2\theta)}{2} \right] + C$$
$$= 2\theta + \sin(2\theta) + C$$

**Step 5: Back-substitute**
```
From x = 2sin(θ): sin(θ) = x/2, so θ = arcsin(x/2)
sin(2θ) = 2sin(θ)cos(θ) = 2 · (x/2) · √(1-(x/2)²)
        = x√(4-x²)/2
```

$$= 2\arcsin\left(\frac{x}{2}\right) + \frac{x\sqrt{4-x^2}}{2} + C$$

---

### Example 4: Another Trig Substitution (Medium ⭐⭐)

**Problem:** $\int \frac{1}{\sqrt{x^2 + 9}} \, dx$

**Solution:**

**Step 1: Identify pattern**
```
√(x² + a²) with a = 3
→ Use substitution x = 3tan(θ)
```

**Step 2: Set up substitution**
```
x = 3tan(θ)
dx = 3sec²(θ) dθ
√(x² + 9) = √(9tan²(θ) + 9) = 3√(1 + tan²(θ)) = 3sec(θ)
```

**Step 3: Substitute**
$$\int \frac{1}{\sqrt{x^2+9}} \, dx = \int \frac{1}{3\sec(\theta)} \cdot 3\sec^2(\theta) \, d\theta$$
$$= \int \sec(\theta) \, d\theta$$
$$= \ln|\sec(\theta) + \tan(\theta)| + C$$

**Step 4: Back-substitute**
```
From x = 3tan(θ): tan(θ) = x/3
sec(θ) = √(1 + tan²(θ)) = √(1 + x²/9) = √(x² + 9)/3
```

$$= \ln\left|\frac{\sqrt{x^2+9}}{3} + \frac{x}{3}\right| + C$$
$$= \ln\left|\frac{\sqrt{x^2+9} + x}{3}\right| + C$$

Using logarithm properties:
$$= \ln|\sqrt{x^2+9} + x| - \ln(3) + C$$
$$= \ln|\sqrt{x^2+9} + x| + C'$$ (where C' = C - ln(3))

---

### Example 5: Power of Cosine (Easy ⭐)

**Problem:** $\int \cos^4(x) \, dx$

**Solution:**

**Step 1: Apply power reduction twice**
$$\cos^2(x) = \frac{1 + \cos(2x)}{2}$$

$$\cos^4(x) = [\cos^2(x)]^2 = \left[\frac{1 + \cos(2x)}{2}\right]^2$$
$$= \frac{1 + 2\cos(2x) + \cos^2(2x)}{4}$$

**Step 2: Reduce $\cos^2(2x)$**
$$\cos^2(2x) = \frac{1 + \cos(4x)}{2}$$

$$\cos^4(x) = \frac{1}{4}\left[1 + 2\cos(2x) + \frac{1 + \cos(4x)}{2}\right]$$
$$= \frac{1}{4} + \frac{\cos(2x)}{2} + \frac{1}{8} + \frac{\cos(4x)}{8}$$
$$= \frac{3}{8} + \frac{\cos(2x)}{2} + \frac{\cos(4x)}{8}$$

**Step 3: Integrate**
$$\int \cos^4(x) \, dx = \frac{3x}{8} + \frac{\sin(2x)}{4} + \frac{\sin(4x)}{32} + C$$

---

## Trigonometric Substitution Table

| Expression | Substitution | Identity Used | Result |
|------------|--------------|---------------|--------|
| $\sqrt{a^2-u^2}$ | $u = a\sin\theta$ | $1-\sin^2\theta = \cos^2\theta$ | $a\cos\theta$ |
| $\sqrt{a^2+u^2}$ | $u = a\tan\theta$ | $1+\tan^2\theta = \sec^2\theta$ | $a\sec\theta$ |
| $\sqrt{u^2-a^2}$ | $u = a\sec\theta$ | $\sec^2\theta-1 = \tan^2\theta$ | $a\tan\theta$ |

---

## ⚠️ Common Mistakes & How to Avoid Them

### Mistake 1: Forgetting the Absolute Value

❌ **Wrong:**
```
√(4 - x²) = 2cos(θ)  ← What if cos(θ) < 0?
```

✅ **Correct:**
```
√(4 - x²) = 2|cos(θ)| = 2cos(θ)  ← Only if 0 ≤ θ ≤ π/2
```

Always specify the range of θ!

### Mistake 2: Wrong Back-Substitution

❌ **Wrong:**
```
θ = arcsin(x/2)
Forgetting to express everything in terms of x
```

✅ **Correct:**
```
θ = arcsin(x/2)
cos(θ) = √(1 - (x/2)²) = √(4-x²)/2
sin(2θ) = 2sin(θ)cos(θ) = ...
```

Draw a right triangle if needed!

### Mistake 3: Mismatching Substitutions

❌ **Wrong:**
```
∫√(x² + 4) dx
Using x = 2sin(θ)  ← This is for √(a² - x²), not √(a² + x²)!
```

✅ **Correct:**
```
∫√(x² + 4) dx
Using x = 2tan(θ)  ← For √(x² + a²)
```

---

## 📝 Practice Problems

### Easy Problems ⭐

1. $\int \sin^2(x) \, dx$
2. $\int \cos^2(3x) \, dx$
3. $\int \sin^3(x) \, dx$
4. $\int \sqrt{9 - x^2} \, dx$
5. $\int \frac{1}{\sqrt{1 + x^2}} \, dx$

**[Solutions →](./solutions-easy.md)**

### Medium Problems ⭐⭐

6. $\int \sin(2x)\cos(3x) \, dx$
7. $\int \sqrt{x^2 - 4} \, dx$
8. $\int \cos^4(x) \, dx$
9. $\int \tan^2(x) \, dx$
10. $\int \frac{x^2}{\sqrt{16 - x^2}} \, dx$

**[Solutions →](./solutions-medium.md)**

### Hard Problems ⭐⭐⭐

11. $\int \sin^5(x)\cos^2(x) \, dx$
12. $\int \frac{1}{(x^2 + 1)^2} \, dx$
13. $\int \sec^3(x) \, dx$
14. $\int \frac{x^3}{\sqrt{1+x^2}} \, dx$
15. $\int \sin^3(x)\cos^3(x) \, dx$

**[Solutions →](./solutions-hard.md)**

---

## ✅ Self-Assessment Checklist

- [ ] Understand power reduction formulas
- [ ] Apply trigonometric substitution correctly
- [ ] Match expressions to correct substitution type
- [ ] Back-substitute accurately
- [ ] Solve at least 12/15 practice problems

---

## 📚 Next Chapter

**Ready to continue?** Move to [Chapter 4: Partial Fractions Decomposition](../04-partial-fractions/README.md)

Or go back to [Main Module Guide](../README.md)
