# Chapter 1: U-Substitution (Change of Variables)
## The Foundation of Integration Techniques

---

## 🎯 Learning Objectives

After completing this chapter, you will:

- ✅ Understand the intuition behind u-substitution
- ✅ Master the 4-step u-substitution procedure
- ✅ Recognize when to use u-substitution
- ✅ Solve integrals using u-substitution
- ✅ Avoid common mistakes
- ✅ Apply u-substitution to BSECE problems

**Time Estimate:** 8-10 hours  
**Difficulty:** Beginner ⭐  
**Prerequisites:** Basic antiderivatives, chain rule concept  

---

## 💡 Intuitive Explanation: What is U-Substitution?

### The "Change of Perspective" Analogy

Imagine you have a complicated problem. Sometimes, if you look at it from a different angle or reorganize it, it becomes simple.

**Example:** The integral ∫2x·e^(x²) dx looks complicated. But if you notice that:
- The derivative of x² is 2x
- We have 2x right there in the problem!

We can **"zoom in"** on x² and treat it as a single unit. Suddenly, the integral becomes simple: ∫e^u du = e^u + C

### Why U-Substitution Works (The Chain Rule in Reverse)

Recall the **Chain Rule** from differentiation:
$$\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$$

U-substitution **reverses** this process! We're looking for integrals that have this form:
$$\int f'(g(x)) \cdot g'(x) \, dx$$

When we see this pattern, we can "undo" the chain rule by substituting.

---

## 📋 The 4-Step U-Substitution Procedure

### Step 1: Choose u
Identify the "inner function" that makes the integral simpler.

**Tip:** Usually, u is:
- A function whose derivative appears somewhere in the integrand
- Nested inside another function (like the exponent in e^(x²))

### Step 2: Find du
Differentiate your choice of u:
$$u = f(x) \implies \frac{du}{dx} = f'(x) \implies du = f'(x) \, dx$$

### Step 3: Rewrite the integral
Replace all instances of u and dx in the original integral:
$$\int f(x) \, dx \rightarrow \int g(u) \, du$$

### Step 4: Integrate and Back-Substitute
Integrate with respect to u, then substitute back x:
$$\int g(u) \, du = G(u) + C = G(f(x)) + C$$

---

## 🔍 Worked Examples

### Example 1: Basic U-Substitution (Easy ⭐)

**Problem:** Solve ∫2x(x² + 1) dx

**Solution:**

**Step 1: Choose u**
```
u = x² + 1
(The inner expression, and its derivative will give us the 2x!)
```

**Step 2: Find du**
```
du/dx = 2x
du = 2x dx  ✓ (This matches what we have!)
```

**Step 3: Rewrite**
```
∫2x(x² + 1) dx = ∫u du
```

**Step 4: Integrate and Back-Substitute**
```
∫u du = u²/2 + C
     = (x² + 1)²/2 + C
```

**Check:** d/dx[(x² + 1)²/2] = 2(x² + 1)·2x/2 = 2x(x² + 1) ✓

---

### Example 2: Exponential Function (Easy ⭐)

**Problem:** Solve ∫3e^(3x) dx

**Solution:**

**Step 1: Choose u**
```
u = 3x
(Exponent that will simplify the e^(3x))
```

**Step 2: Find du**
```
du/dx = 3
du = 3 dx  ✓ (Perfect match!)
```

**Step 3: Rewrite**
```
∫3e^(3x) dx = ∫e^u du
```

**Step 4: Integrate**
```
∫e^u du = e^u + C
        = e^(3x) + C
```

---

### Example 3: Trigonometric (Easy ⭐)

**Problem:** Solve ∫cos(2x) dx

**Solution:**

**Step 1: Choose u**
```
u = 2x
```

**Step 2: Find du**
```
du = 2 dx
So: dx = du/2
```

**Step 3: Rewrite**
```
∫cos(2x) dx = ∫cos(u) · (du/2)
            = (1/2)∫cos(u) du
```

**Step 4: Integrate**
```
= (1/2)sin(u) + C
= (1/2)sin(2x) + C
```

---

### Example 4: Polynomial Chain (Medium ⭐⭐)

**Problem:** Solve ∫x²(x³ + 2)^5 dx

**Solution:**

**Step 1: Choose u**
```
u = x³ + 2
(Highest power expression, raised to the 5th power)
```

**Step 2: Find du**
```
du/dx = 3x²
du = 3x² dx
So: x² dx = du/3
```

**Step 3: Rewrite**
```
∫x²(x³ + 2)^5 dx = ∫(x³ + 2)^5 · x² dx
                 = ∫u^5 · (du/3)
                 = (1/3)∫u^5 du
```

**Step 4: Integrate**
```
= (1/3) · u^6/6 + C
= u^6/18 + C
= (x³ + 2)^6/18 + C
```

---

### Example 5: Logarithm (Medium ⭐⭐)

**Problem:** Solve ∫(1/(2x + 1)) dx

**Solution:**

**Step 1: Choose u**
```
u = 2x + 1
```

**Step 2: Find du**
```
du = 2 dx
dx = du/2
```

**Step 3: Rewrite**
```
∫1/(2x + 1) dx = ∫(1/u) · (du/2)
               = (1/2)∫(1/u) du
```

**Step 4: Integrate**
```
= (1/2)ln|u| + C
= (1/2)ln|2x + 1| + C
```

---

### Example 6: Nested Radicals (Medium ⭐⭐)

**Problem:** Solve ∫(2x/√(x² + 3)) dx

**Solution:**

**Step 1: Choose u**
```
u = x² + 3
(Inside the square root)
```

**Step 2: Find du**
```
du = 2x dx  ✓ (Already in the integral!)
```

**Step 3: Rewrite**
```
∫(2x/√(x² + 3)) dx = ∫(1/√u) du
                    = ∫u^(-1/2) du
```

**Step 4: Integrate**
```
= u^(1/2)/(1/2) + C
= 2u^(1/2) + C
= 2√(x² + 3) + C
```

---

### Example 7: Quotient Rule (Hard ⭐⭐⭐)

**Problem:** Solve ∫(3x²/(x³ + 5)²) dx

**Solution:**

**Step 1: Choose u**
```
u = x³ + 5
(The denominator expression)
```

**Step 2: Find du**
```
du = 3x² dx  ✓ (Numerator!)
```

**Step 3: Rewrite**
```
∫(3x²/(x³ + 5)²) dx = ∫(1/u²) du
                     = ∫u^(-2) du
```

**Step 4: Integrate**
```
= u^(-1)/(-1) + C
= -1/u + C
= -1/(x³ + 5) + C
```

---

### Example 8: Trigonometric Composite (Hard ⭐⭐⭐)

**Problem:** Solve ∫sin(x)·cos(sin(x)) dx

**Solution:**

**Step 1: Choose u**
```
u = sin(x)
(The argument of cosine)
```

**Step 2: Find du**
```
du = cos(x) dx  ✓ (In the integral!)
```

**Step 3: Rewrite**
```
∫sin(x)·cos(sin(x)) dx
```

Wait - we need cos(x)dx but only have sin(x)dx. Let me reconsider:

Actually, with u = sin(x), du = cos(x)dx:
```
∫cos(sin(x))·cos(x) dx = ∫cos(u) du
```

**Step 4: Integrate**
```
= sin(u) + C
= sin(sin(x)) + C
```

---

## ⚠️ Common Mistakes & How to Avoid Them

### Mistake 1: Forgetting the Differential (du)

❌ **Wrong:**
```
∫2x(x² + 1) dx
u = x² + 1
= ∫u du  ← WRONG! Should check if du = 2x dx
```

✅ **Correct:**
```
∫2x(x² + 1) dx
u = x² + 1, du = 2x dx
= ∫u du
= u²/2 + C
```

### Mistake 2: Not Completely Substituting

❌ **Wrong:**
```
∫2x/(x² + 1) dx
u = x² + 1, du = 2x dx
= ∫(1/(x² + 1)) du  ← WRONG! Still have x² in the expression
```

✅ **Correct:**
```
∫2x/(x² + 1) dx
u = x² + 1, du = 2x dx
= ∫(1/u) du  ← ALL x² replaced with u
= ln|u| + C
= ln|x² + 1| + C
```

### Mistake 3: Forgetting to Back-Substitute

❌ **Wrong:**
```
∫x²√(x³ + 1) dx
u = x³ + 1, du = 3x² dx
= (1/3)∫√u du
= (1/3) · (2/3)u^(3/2) + C
= (2/9)u^(3/2) + C  ← INCOMPLETE!
```

✅ **Correct:**
```
= (2/9)(x³ + 1)^(3/2) + C  ← Back-substituted
```

### Mistake 4: Wrong "Partial" du

❌ **Wrong:**
```
∫3sin(3x) dx
u = 3x, du = 3 dx
So: dx = 3 du  ← WRONG!
```

✅ **Correct:**
```
u = 3x, du = 3 dx
So: dx = du/3  ← Correct!
∫3sin(3x) dx = ∫3sin(u) · (du/3)
             = ∫sin(u) du
             = -cos(u) + C
             = -cos(3x) + C
```

---

## 🎯 When to Use U-Substitution

### Recognize These Patterns:

| Pattern | u-substitution works? | Example |
|---------|----------------------|----------|
| ∫f(u)·u' dx | ✅ YES | ∫e^x · 1 dx |
| ∫u^n · u' dx | ✅ YES | ∫(x²+1)^5 · 2x dx |
| ∫(1/u)·u' dx | ✅ YES | ∫(1/(2x+1)) · 2 dx |
| ∫sin(u)·u' dx | ✅ YES | ∫sin(x³)·3x² dx |
| ∫e^u · u' dx | ✅ YES | ∫e^(3x) · 3 dx |
| ∫f(u) dx (where u' NOT in integral) | ❌ NO | ∫e^x dx alone - needs help |
| ∫f(x)g(x) dx (no chain) | ❌ NO | Use integration by parts instead |

---

## 📝 Practice Problems

### Easy Problems ⭐ (Try These First!)

1. ∫4x(2x² + 1) dx
2. ∫6x²(x³ - 2) dx
3. ∫5e^(5x) dx
4. ∫2sin(2x) dx
5. ∫3cos(3x) dx

**[Solutions →](./solutions-easy.md)**

### Medium Problems ⭐⭐ (Build Your Skills)

6. ∫x(x² + 1)^3 dx
7. ∫2x√(x² + 3) dx
8. ∫(2x)/(x² + 1) dx
9. ∫e^(2x+1) dx
10. ∫x²sin(x³) dx

**[Solutions →](./solutions-medium.md)**

### Hard Problems ⭐⭐⭐ (Challenge Yourself)

11. ∫x³(x⁴ - 1)^(1/3) dx
12. ∫(3x²)/(x³ + 2)² dx
13. ∫sin(x)cos(x) dx
14. ∫(2x + 1)/(x² + x + 1)² dx
15. ∫e^(√x)/√x dx

**[Solutions →](./solutions-hard.md)**

---

## 🛠️ Tools & Resources

### Interactive Learning
- [Desmos Graphing Calculator](https://www.desmos.com/calculator) - Visualize functions
- [Integral Calculator](https://www.integral-calculator.com/) - Step-by-step solutions
- [Wolfram Alpha](https://www.wolframalpha.com/) - Verify your answers

### Videos
- [3Blue1Brown - Chain Rule Intuition](https://www.youtube.com/watch?v=S0_qX4VJhMU)
- [Professor Leonard - U-Substitution](https://www.youtube.com/watch?v=JL7x_7sD_sM&t=0s)
- [Khan Academy - U-Substitution](https://www.youtube.com/watch?v=h8-NuZBLW0s)

### References
- [Formula Sheet](../resources/formula-sheet.pdf)
- [Trigonometric Identities](../resources/trig-identities.pdf)
- [Derivative Rules](../resources/derivative-rules.pdf)

---

## ✅ Self-Assessment Checklist

Before moving to Chapter 2, make sure you can:

- [ ] Explain u-substitution in your own words
- [ ] Follow the 4-step procedure correctly
- [ ] Choose appropriate u values
- [ ] Calculate du correctly
- [ ] Complete all easy problems (⭐)
- [ ] Solve at least 8/10 medium problems (⭐⭐)
- [ ] Understand the common mistakes section
- [ ] Verify answers using digital tools

---

## 📚 Next Chapter

**Ready to continue?** Move to [Chapter 2: Integration by Parts](../02-integration-by-parts/README.md)

Or go back to [Main Module Guide](../README.md)
