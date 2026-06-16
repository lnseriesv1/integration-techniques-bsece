# Chapter 2: Integration by Parts
## Splitting Complicated Products into Manageable Pieces

---

## 🎯 Learning Objectives

After completing this chapter, you will:

- ✅ Understand the intuition behind integration by parts
- ✅ Master the integration by parts formula
- ✅ Apply the LIATE rule to choose u and dv
- ✅ Use the tabular method for repeated integration by parts
- ✅ Solve integrals of products of different function types
- ✅ Avoid common mistakes
- ✅ Apply integration by parts to BSECE problems

**Time Estimate:** 10-12 hours  
**Difficulty:** Beginner to Intermediate ⭐⭐  
**Prerequisites:** Chapter 1 (U-Substitution), basic differentiation and integration  

---

## 💡 Intuitive Explanation: Why Integration by Parts?

### The "Product Rule in Reverse" Analogy

Recall the **Product Rule** from differentiation:
$$\frac{d}{dx}[u \cdot v] = u'v + uv'$$

Integration by parts **reverses** this process. When we have an integral of a **product** of two different types of functions, we can use the "product rule backwards" to break it into simpler pieces.

### Real-World Analogy

Imagine you have a complicated task with two components:
- **Component A:** Something you know how to handle easily
- **Component B:** Something very difficult

What if you could rearrange the task so that:
- You integrate Component A (easy)
- You differentiate Component B (also easy)

That's exactly what integration by parts does!

**Example:** $\int x \cdot e^x \, dx$
- $x$ is easy to differentiate: $\frac{d}{dx}[x] = 1$
- $e^x$ is easy to integrate: $\int e^x \, dx = e^x$
- Result: We can break this into manageable pieces!

---

## 📋 The Integration by Parts Formula

$$\int u \, dv = uv - \int v \, du$$

### Breaking It Down:

1. **Choose u** - The part you'll differentiate
2. **Choose dv** - The part you'll integrate
3. **Find du** - Differentiate u
4. **Find v** - Integrate dv
5. **Apply formula** - Plug into $uv - \int v \, du$
6. **Evaluate** - Solve the remaining integral

---

## 🎓 The LIATE Rule (How to Choose u)

When you have a product, which part should be **u**? Use **LIATE priority**:

### **L** - Logarithmic (highest priority)
- $\ln(x)$, $\log(x)$, etc.
- Choose this as **u** if it appears

### **I** - Inverse Trigonometric
- $\arcsin(x)$, $\arccos(x)$, $\arctan(x)$, etc.
- Choose this as **u** if no logarithm

### **A** - Algebraic (polynomials)
- $x$, $x^2$, $3x+1$, etc.
- Choose this as **u** if no log or inverse trig

### **T** - Trigonometric
- $\sin(x)$, $\cos(x)$, $\tan(x)$, etc.
- Choose this as **u** if no L, I, or A

### **E** - Exponential (lowest priority)
- $e^x$, $2^x$, etc.
- Choose this as **u** only as last resort

**Memory Aid:** "**LIATE**" - Logarithmic, Inverse trig, Algebraic, Trigonometric, Exponential

---

## 🔍 Worked Examples

### Example 1: Polynomial Times Exponential (Easy ⭐)

**Problem:** $\int x \cdot e^x \, dx$

**Solution:**

**Step 1: Choose u and dv**
```
Using LIATE: Algebraic (x) comes before Exponential (e^x)
u = x          (easier to differentiate)
dv = e^x dx    (easy to integrate)
```

**Step 2: Find du and v**
```
du = 1 dx = dx
v = ∫e^x dx = e^x
```

**Step 3: Apply formula**
$$\int x \cdot e^x \, dx = x \cdot e^x - \int e^x \, dx$$

**Step 4: Evaluate**
$$= xe^x - e^x + C$$
$$= e^x(x - 1) + C$$

**Check:** $\frac{d}{dx}[e^x(x-1)] = e^x(x-1) + e^x(1) = e^x \cdot x$ ✓

---

### Example 2: Polynomial Times Trigonometric (Easy ⭐)

**Problem:** $\int x \sin(x) \, dx$

**Solution:**

**Step 1: Choose u and dv**
```
Using LIATE: Algebraic (x) before Trigonometric (sin x)
u = x
dv = sin(x) dx
```

**Step 2: Find du and v**
```
du = dx
v = ∫sin(x) dx = -cos(x)
```

**Step 3: Apply formula**
$$\int x \sin(x) \, dx = x(-\cos(x)) - \int (-\cos(x)) \, dx$$
$$= -x\cos(x) + \int \cos(x) \, dx$$

**Step 4: Evaluate**
$$= -x\cos(x) + \sin(x) + C$$

---

### Example 3: Logarithm Times Polynomial (Easy ⭐)

**Problem:** $\int x \ln(x) \, dx$

**Solution:**

**Step 1: Choose u and dv**
```
Using LIATE: Logarithmic (ln x) before Algebraic (x)
u = ln(x)      (choose log first!)
dv = x dx      (polynomial part)
```

**Step 2: Find du and v**
```
du = (1/x) dx
v = ∫x dx = x²/2
```

**Step 3: Apply formula**
$$\int x \ln(x) \, dx = \ln(x) \cdot \frac{x^2}{2} - \int \frac{x^2}{2} \cdot \frac{1}{x} \, dx$$

**Step 4: Simplify and evaluate**
$$= \frac{x^2 \ln(x)}{2} - \int \frac{x}{2} \, dx$$
$$= \frac{x^2 \ln(x)}{2} - \frac{x^2}{4} + C$$

---

### Example 4: Trigonometric Times Exponential (Medium ⭐⭐)

**Problem:** $\int e^x \sin(x) \, dx$

**Solution:**

This is tricky! When you have trigonometric and exponential together, neither has clear priority in LIATE. We need to do integration by parts **twice**.

**First Application:**
```
u = sin(x)          dv = e^x dx
du = cos(x) dx      v = e^x
```

$$\int e^x \sin(x) \, dx = e^x \sin(x) - \int e^x \cos(x) \, dx$$

**Second Application (for the remaining integral):**
```
u = cos(x)          dv = e^x dx
du = -sin(x) dx     v = e^x
```

$$\int e^x \cos(x) \, dx = e^x \cos(x) - \int e^x (-\sin(x)) \, dx$$
$$= e^x \cos(x) + \int e^x \sin(x) \, dx$$

**Combine:**
$$\int e^x \sin(x) \, dx = e^x \sin(x) - [e^x \cos(x) + \int e^x \sin(x) \, dx]$$
$$\int e^x \sin(x) \, dx = e^x \sin(x) - e^x \cos(x) - \int e^x \sin(x) \, dx$$

**Solve for the integral:**
$$2\int e^x \sin(x) \, dx = e^x \sin(x) - e^x \cos(x)$$
$$\int e^x \sin(x) \, dx = \frac{e^x(\sin(x) - \cos(x))}{2} + C$$

---

### Example 5: Inverse Trigonometric (Medium ⭐⭐)

**Problem:** $\int \arcsin(x) \, dx$

**Solution:**

**Step 1: Choose u and dv**
```
u = arcsin(x)   (Inverse trig - highest priority!)
dv = 1 dx = dx  (everything else)
```

**Step 2: Find du and v**
```
du = (1/√(1-x²)) dx
v = x
```

**Step 3: Apply formula**
$$\int \arcsin(x) \, dx = x \arcsin(x) - \int \frac{x}{\sqrt{1-x^2}} \, dx$$

**Step 4: Evaluate remaining integral (use u-substitution!)**

For $\int \frac{x}{\sqrt{1-x^2}} \, dx$:
- Let $w = 1-x^2$, then $dw = -2x dx$
- $\int \frac{x}{\sqrt{1-x^2}} \, dx = -\frac{1}{2}\int w^{-1/2} dw = -\sqrt{w} = -\sqrt{1-x^2}$

**Final Answer:**
$$\int \arcsin(x) \, dx = x \arcsin(x) + \sqrt{1-x^2} + C$$

---

### Example 6: Repeated Integration by Parts (Medium ⭐⭐)

**Problem:** $\int x^2 e^x \, dx$

**Solution:**

**First Application:**
```
u = x²          dv = e^x dx
du = 2x dx      v = e^x
```

$$\int x^2 e^x \, dx = x^2 e^x - \int 2x e^x \, dx$$

**Second Application (for $\int 2x e^x dx$):**
```
u = 2x          dv = e^x dx
du = 2 dx       v = e^x
```

$$\int 2x e^x \, dx = 2x e^x - \int 2 e^x \, dx = 2x e^x - 2e^x$$

**Combine:**
$$\int x^2 e^x \, dx = x^2 e^x - (2x e^x - 2e^x) + C$$
$$= x^2 e^x - 2x e^x + 2e^x + C$$
$$= e^x(x^2 - 2x + 2) + C$$

---

### Example 7: Using Tabular Method (Hard ⭐⭐⭐)

**Problem:** $\int x^3 \sin(x) \, dx$

For repeated integration by parts, we can use the **tabular method** instead of repeating the formula multiple times.

**Tabular Method Setup:**

```
Derivatives (u)  |  Integrals (dv)
    x³           |  sin(x)
    ↓            |  ↓
    3x²          |  -cos(x)
    ↓            |  ↓
    6x           |  -sin(x)
    ↓            |  ↓
    6            |  cos(x)
    ↓            |  ↓
    0            |  sin(x)
```

**Apply signs alternately:** (+) (-) (+) (-) ...

$$\int x^3 \sin(x) \, dx = -(x^3 \cos(x)) + (3x^2)(-\sin(x)) - (6x)\cos(x) + (6)\sin(x) + C$$

$$= -x^3 \cos(x) - 3x^2 \sin(x) + 6x \cos(x) + 6 \sin(x) + C$$

**Verify:** Take the derivative to check! ✓

---

## ⚠️ Common Mistakes & How to Avoid Them

### Mistake 1: Wrong LIATE Choice

❌ **Wrong:**
```
∫x ln(x) dx
u = x          (WRONG! Chose algebraic)
dv = ln(x) dx
```

This is a dead end - ln(x) is hard to integrate!

✅ **Correct:**
```
∫x ln(x) dx
u = ln(x)      (Logarithmic comes FIRST in LIATE!)
dv = x dx
```

### Mistake 2: Sign Errors

❌ **Wrong:**
```
∫x sin(x) dx
u = x, dv = sin(x) dx
du = dx, v = cos(x)  ← WRONG SIGN!

= x cos(x) - ∫cos(x) dx  ← Wrong
= x cos(x) - sin(x) + C  ← Wrong answer
```

✅ **Correct:**
```
∫x sin(x) dx
u = x, dv = sin(x) dx
du = dx, v = -cos(x)  ← CORRECT!

= -x cos(x) - ∫(-cos(x)) dx
= -x cos(x) + sin(x) + C  ← Correct
```

### Mistake 3: Forgetting Integration

❌ **Wrong:**
```
∫x ln(x) dx
u = ln(x), dv = x dx
du = (1/x) dx, v = x²  ← Should be x²/2!
```

✅ **Correct:**
```
∫x dx = x²/2 + C  (Don't include +C in integration by parts)
```

### Mistake 4: Selecting Exponential as u

❌ **Wrong:**
```
∫x e^x dx
u = e^x        (WRONG! E is lowest priority)
du = e^x dx    (This gets MORE complicated!)
```

✅ **Correct:**
```
∫x e^x dx
u = x          (A comes before E in LIATE)
du = dx        (Simpler, easier to work with)
```

---

## 🛠️ When to Use Integration by Parts

### Recognize These Patterns:

| Pattern | Use Integration by Parts? | Example |
|---------|---------------------------|----------|
| Polynomial × Exponential | ✅ YES | ∫x·e^x dx |
| Polynomial × Trigonometric | ✅ YES | ∫x·sin(x) dx |
| Polynomial × Logarithmic | ✅ YES | ∫x·ln(x) dx |
| Inverse Trig × anything | ✅ YES | ∫arcsin(x) dx |
| Logarithmic × anything | ✅ YES | ∫ln(x)·e^x dx |
| Trig × Exponential | ✅ YES (twice) | ∫e^x·sin(x) dx |
| Trig × Trig | ❌ NO | Use trig identities |
| Polynomial × Polynomial | ❌ NO | Just multiply out |
| Simple function (no product) | ❌ NO | Use u-substitution |

---

## 📝 Practice Problems

### Easy Problems ⭐ (Try These First!)

1. $\int x \cos(x) \, dx$
2. $\int x e^{2x} \, dx$
3. $\int x \sin(2x) \, dx$
4. $\int e^x \cos(x) \, dx$
5. $\int x^2 e^x \, dx$ (use tabular method)

**[Solutions →](./solutions-easy.md)**

### Medium Problems ⭐⭐ (Build Your Skills)

6. $\int x^2 \sin(x) \, dx$
7. $\int \ln(x) \, dx$ (hint: think of 1·ln(x))
8. $\int x \arcsin(x) \, dx$
9. $\int e^{2x} \sin(3x) \, dx$
10. $\int x^3 e^x \, dx$ (use tabular method)

**[Solutions →](./solutions-medium.md)**

### Hard Problems ⭐⭐⭐ (Challenge Yourself)

11. $\int x^2 \cos(x) \, dx$
12. $\int \arctan(x) \, dx$
13. $\int x e^{3x} \sin(x) \, dx$ (tricky!)
14. $\int x \sqrt{x+1} \, dx$ (use integration by parts + u-sub)
15. $\int x^2 \ln(x) \, dx$

**[Solutions →](./solutions-hard.md)**

---

## ✅ Self-Assessment Checklist

Before moving to Chapter 3, make sure you can:

- [ ] Explain why integration by parts works
- [ ] Correctly apply the LIATE rule
- [ ] Follow the formula $\int u \, dv = uv - \int v \, du$
- [ ] Perform integration by parts once
- [ ] Perform integration by parts twice (repeated)
- [ ] Use the tabular method for polynomial × trig/exp
- [ ] Solve at least 12/15 practice problems correctly
- [ ] Understand when to use integration by parts vs. u-substitution

---

## 📚 Resources

### Videos
- [Professor Leonard - Integration by Parts](https://www.youtube.com/watch?v=rfG8ge-xLrM)
- [Khan Academy - Integration by Parts](https://www.youtube.com/watch?v=Hf7nJ-RjqLc)
- [Tabular Method Visual](https://www.youtube.com/watch?v=Ll9M1V8bKhI)

### Interactive Tools
- [Integral Calculator](https://www.integral-calculator.com/) - Shows step-by-step
- [Wolfram Alpha](https://www.wolframalpha.com/) - Verify answers
- [Desmos](https://www.desmos.com/calculator) - Visualize functions

---

## 📖 Next Chapter

**Ready to continue?** Move to [Chapter 3: Trigonometric Integrals & Substitutions](../03-trigonometric-integrals/README.md)

Or go back to [Main Module Guide](../README.md)
