# Common Mistakes Gallery
## Learn from Errors - Chapter 1-5 Comprehensive

---

## 🚫 Chapter 1: U-Substitution Mistakes

### Mistake 1.1: Forgetting the Differential

```
❌ WRONG:
   ∫2x·e^(x²) dx
   u = x²
   = ∫e^u du  ← INCOMPLETE! What happened to du?
   = e^u + C = e^(x²) + C  ← WRONG ANSWER

✅ CORRECT:
   ∫2x·e^(x²) dx
   u = x², du = 2x dx ← CRUCIAL!
   = ∫e^u du
   = e^u + C = e^(x²) + C
   
   Check: d/dx[e^(x²)] = e^(x²)·2x ✓
```

### Mistake 1.2: Incomplete Substitution

```
❌ WRONG:
   ∫(x/(x² + 1)) dx
   u = x² + 1, du = 2x dx
   = ∫(1/u) du  ← Wait, where's the x? Should be (1/u)·du
   = ln|u| + C = ln|x² + 1| + C

✅ CORRECT:
   ∫(x/(x² + 1)) dx
   u = x² + 1, du = 2x dx
   Need to rewrite: x dx = du/2
   = ∫(1/u)·(du/2)
   = (1/2)ln|u| + C
   = (1/2)ln|x² + 1| + C
```

### Mistake 1.3: Wrong Partial du

```
❌ WRONG:
   ∫sin(5x) dx
   u = 5x, du = 5 dx
   dx = 5 du  ← WRONG!
   = ∫sin(u)·5 du = -5cos(u) + C  ← WRONG ANSWER

✅ CORRECT:
   ∫sin(5x) dx
   u = 5x, du = 5 dx
   dx = du/5  ← CORRECT!
   = ∫sin(u)·(du/5)
   = (1/5)∫sin(u) du
   = -(1/5)cos(u) + C
   = -(1/5)cos(5x) + C
   
   Check: d/dx[-(1/5)cos(5x)] = (1/5)sin(5x)·5 = sin(5x) ✓
```

### Mistake 1.4: Forgetting to Back-Substitute

```
❌ WRONG:
   ∫2x(x² + 1)^5 dx
   u = x² + 1, du = 2x dx
   = ∫u^5 du
   = u^6/6 + C  ← INCOMPLETE!

✅ CORRECT:
   ∫2x(x² + 1)^5 dx
   u = x² + 1, du = 2x dx
   = ∫u^5 du
   = u^6/6 + C
   = (x² + 1)^6/6 + C  ← BACK-SUBSTITUTE!
```

---

## 🚫 Chapter 2: Integration by Parts Mistakes

### Mistake 2.1: Wrong LIATE Choice

```
❌ WRONG:
   ∫x·ln(x) dx
   Choose u = x (Algebraic)
   du = dx, dv = ln(x) dx
   But v = ∫ln(x) dx is HARD!
   ← This path leads nowhere

✅ CORRECT:
   ∫x·ln(x) dx
   Logarithmic comes FIRST in LIATE!
   u = ln(x) (Logarithmic)
   dv = x dx
   du = (1/x) dx, v = x²/2
   = (x²/2)·ln(x) - ∫(x²/2)·(1/x) dx
   = (x²/2)·ln(x) - (x²/4) + C
```

### Mistake 2.2: Sign Errors

```
❌ WRONG:
   ∫x·sin(x) dx
   u = x, dv = sin(x) dx
   du = dx, v = cos(x)  ← WRONG SIGN!
   = x·cos(x) - ∫cos(x) dx  ← WRONG
   = x·cos(x) - sin(x) + C  ← WRONG ANSWER

✅ CORRECT:
   ∫x·sin(x) dx
   u = x, dv = sin(x) dx
   du = dx, v = -cos(x)  ← CORRECT!
   = x·(-cos(x)) - ∫(-cos(x)) dx
   = -x·cos(x) + ∫cos(x) dx
   = -x·cos(x) + sin(x) + C
   
   Check: d/dx[-x·cos(x) + sin(x)]
          = -cos(x) + x·sin(x) + cos(x) = x·sin(x) ✓
```

### Mistake 2.3: Choosing Exponential as u

```
❌ WRONG:
   ∫x·e^x dx
   u = e^x (Exponential)
   du = e^x dx, dv = x dx
   This makes du MORE complex!

✅ CORRECT:
   ∫x·e^x dx
   Algebraic comes BEFORE Exponential in LIATE
   u = x (Algebraic)
   du = dx, dv = e^x dx, v = e^x
   = x·e^x - ∫e^x dx
   = x·e^x - e^x + C
   = e^x(x - 1) + C
```

### Mistake 2.4: Forgetting Coefficient in dv Integration

```
❌ WRONG:
   ∫x·e^(2x) dx
   u = x, dv = e^(2x) dx
   v = e^(2x)  ← WRONG! Forgot to account for 2x
   = x·e^(2x) - ∫e^(2x) dx
   = x·e^(2x) - e^(2x) + C  ← WRONG ANSWER

✅ CORRECT:
   ∫x·e^(2x) dx
   u = x, dv = e^(2x) dx
   v = e^(2x)/2  ← CORRECT!
   = x·(e^(2x)/2) - ∫(e^(2x)/2) dx
   = (x/2)·e^(2x) - (1/4)e^(2x) + C
   = e^(2x)(x/2 - 1/4) + C
```

---

## 🚫 Chapter 3: Trigonometric Integrals Mistakes

### Mistake 3.1: Wrong Power Reduction Formula

```
❌ WRONG:
   ∫sin²(x) dx
   Use cos² formula instead
   = ∫(1 + cos(2x))/2 dx  ← WRONG FORMULA!
   = x/2 + sin(2x)/4 + C  ← WRONG ANSWER

✅ CORRECT:
   ∫sin²(x) dx
   sin²(x) = (1 - cos(2x))/2  ← CORRECT FORMULA!
   = ∫(1 - cos(2x))/2 dx
   = (1/2)∫[1 - cos(2x)] dx
   = (1/2)[x - sin(2x)/2] + C
   = x/2 - sin(2x)/4 + C
```

### Mistake 3.2: Wrong Trig Substitution

```
❌ WRONG:
   ∫√(x² + 4) dx
   Pattern: √(x² + a²) where a = 2
   Use x = 2sin(θ)  ← WRONG!
   This is for √(a² - x²), not √(a² + x²)

✅ CORRECT:
   ∫√(x² + 4) dx
   Pattern: √(x² + a²) where a = 2
   Use x = 2tan(θ)  ← CORRECT!
   Then √(x² + 4) = 2sec(θ)
   dx = 2sec²(θ) dθ
```

### Mistake 3.3: Forgetting Absolute Value Signs

```
❌ WRONG:
   From x = 3sin(θ):
   √(9 - x²) = 3cos(θ)  ← What if cos(θ) < 0?

✅ CORRECT:
   From x = 3sin(θ) with -π/2 ≤ θ ≤ π/2:
   √(9 - x²) = 3|cos(θ)| = 3cos(θ)  ← Specified range!
```

### Mistake 3.4: Incomplete Back-Substitution

```
❌ WRONG:
   ∫√(4 - x²) dx
   x = 2sin(θ), dx = 2cos(θ) dθ
   = ∫2cos(θ)·2cos(θ) dθ
   = 4∫cos²(θ) dθ
   = 4[θ/2 + sin(2θ)/4] + C
   = 2θ + sin(2θ) + C  ← INCOMPLETE!

✅ CORRECT:
   (continuing...)
   θ = arcsin(x/2)
   sin(2θ) = 2sin(θ)cos(θ) = 2·(x/2)·√(4-x²)/2 = x√(4-x²)/2
   = 2arcsin(x/2) + x√(4-x²)/2 + C
```

---

## 🚫 Chapter 4: Partial Fractions Mistakes

### Mistake 4.1: Wrong Number of Constants

```
❌ WRONG:
   1/[(x-1)²(x+2)] 
   = A/(x-1) + B/(x+2)  ← Missing a constant for (x-1)²!

✅ CORRECT:
   1/[(x-1)²(x+2)]
   = A/(x-1) + B/(x-1)² + C/(x+2)  ← Three constants needed!
```

### Mistake 4.2: Wrong Form for Quadratic Factor

```
❌ WRONG:
   1/[(x+1)(x² + 2)]
   = A/(x+1) + B/(x² + 2)  ← B should be Bx + C!

✅ CORRECT:
   1/[(x+1)(x² + 2)]
   = A/(x+1) + (Bx + C)/(x² + 2)  ← Bx + C for irreducible quad!
```

### Mistake 4.3: Forgetting Polynomial Division

```
❌ WRONG:
   ∫(x² + 5)/(x - 1) dx
   Try partial fractions directly
   But degree(numerator) ≥ degree(denominator)
   ← Can't use partial fractions without division first!

✅ CORRECT:
   Polynomial division first:
   (x² + 5)/(x - 1) = x + 1 + 6/(x - 1)
   
   ∫(x² + 5)/(x - 1) dx = ∫[x + 1 + 6/(x-1)] dx
                        = x²/2 + x + 6ln|x-1| + C
```

### Mistake 4.4: Coefficient Errors

```
❌ WRONG:
   (3x + 2)/[(x-1)(x+2)] = A/(x-1) + B/(x+2)
   3x + 2 = A(x+2) + B(x-1)
   
   Set x = 1: 5 = A(3)  →  A = 5/3
   Set x = -2: -4 = B(-3)  →  B = 4/3  ← Wrong!
   
   Check: (5/3)(x+2) + (4/3)(x-1) = (9x + 6)/3 = 3x + 2 ✓
   But verify -4 = 4/3·(-3) = -4 ✓  Actually correct!

✅ CORRECT:
   (3x + 2)/[(x-1)(x+2)] = 5/3/(x-1) + 4/3/(x+2)
   
   Integrate:
   = (5/3)ln|x-1| + (4/3)ln|x+2| + C
```

---

## 🚫 Chapter 5: Special Techniques Mistakes

### Mistake 5.1: Wrong Completing Square Form

```
❌ WRONG:
   x² + 6x + 10
   = (x + 6)² + 10  ← Wrong!

✅ CORRECT:
   x² + 6x + 10
   = (x² + 6x + 9) + 1  ← Complete: need (6/2)² = 9
   = (x + 3)² + 1
```

### Mistake 5.2: Misapplying Reduction Formula

```
❌ WRONG:
   ∫cos⁴(x) dx
   Using reduction for sin:
   = -1/4·cos³(x)sin(x) + ...  ← Wrong formula!

✅ CORRECT:
   ∫cos^n(x) dx = 1/n·cos^(n-1)(x)sin(x) + (n-1)/n·∫cos^(n-2)(x) dx
   
   ∫cos⁴(x) dx = 1/4·cos³(x)sin(x) + 3/4·∫cos²(x) dx
```

### Mistake 5.3: Wrong Technique Choice

```
❌ WRONG:
   ∫(x + 1)/√(x² + 4) dx
   Immediately use trig substitution
   x = 2tan(θ), ...
   ← Actually, split this first!

✅ CORRECT:
   ∫(x + 1)/√(x² + 4) dx
   = ∫x/√(x² + 4) dx + ∫1/√(x² + 4) dx
   
   First integral: u = x² + 4, du = 2x dx
   = (1/2)∫(1/√u) du = √(x² + 4)
   
   Second integral: trig substitution or arcsinh
   = sinh⁻¹(x/2)
```

---

## 📋 Mistake Prevention Checklist

```
✓ ALWAYS verify your answer by differentiation
✓ Check that du matches the remaining dx
✓ Be careful with signs (especially in integration by parts)
✓ Don't forget constant of integration: +C
✓ Use absolute value signs where needed (logs)
✓ Back-substitute ALL variables
✓ Complete the square BEFORE attempting trig substitution
✓ Factor denominators COMPLETELY
✓ Use Wolfram Alpha or Integral Calculator to verify
✓ When stuck, try rewriting or combining techniques
```

---

**Remember: Mistakes are learning opportunities! Work through these examples carefully.**
