# Chapter 4: Partial Fractions Decomposition
## Breaking Down Complex Rational Functions

---

## 🎯 Learning Objectives

After completing this chapter, you will:

- ✅ Identify rational functions and when decomposition applies
- ✅ Decompose rational functions into partial fractions
- ✅ Handle distinct linear factors
- ✅ Handle repeated linear factors
- ✅ Handle irreducible quadratic factors
- ✅ Integrate resulting fractions
- ✅ Apply to BSECE: Laplace transforms and control systems

**Time Estimate:** 10-12 hours  
**Difficulty:** Intermediate ⭐⭐  
**Prerequisites:** Chapters 1-3, polynomial division, algebraic manipulation  

---

## 💡 Intuitive Explanation: Breaking Down Fractions

### Why Decompose?

Consider the integral:
$$\int \frac{5x + 1}{x^2 - 1} \, dx$$

This looks complicated. But what if we could break it into:
$$\frac{5x + 1}{x^2 - 1} = \frac{3}{x-1} + \frac{2}{x+1}$$

Now each piece is easy to integrate! That's the power of partial fractions.

### The Core Idea

Partial fractions **reverses** the process of adding fractions.

When you add fractions:
$$\frac{A}{x-1} + \frac{B}{x+1} = \frac{A(x+1) + B(x-1)}{(x-1)(x+1)}$$

Partial fractions **goes backwards**: Given the right side, find A and B.

---

## 📋 The Partial Fractions Process

### General Form

For a rational function $\frac{P(x)}{Q(x)}$:

1. **Check degree**: If degree of P ≥ degree of Q, do polynomial division first
2. **Factor denominator**: Write Q(x) as a product of linear and irreducible quadratic factors
3. **Set up decomposition**: Based on factor types (see below)
4. **Find constants**: Multiply through and solve for unknowns
5. **Integrate**: Integrate each partial fraction

---

## 🔍 Worked Examples

### Example 1: Distinct Linear Factors (Easy ⭐)

**Problem:** $\int \frac{5x + 1}{x^2 - 1} \, dx$

**Solution:**

**Step 1: Factor denominator**
$$x^2 - 1 = (x-1)(x+1)$$

**Step 2: Set up decomposition**
$$\frac{5x+1}{(x-1)(x+1)} = \frac{A}{x-1} + \frac{B}{x+1}$$

**Step 3: Find A and B**

Multiply both sides by $(x-1)(x+1)$:
$$5x + 1 = A(x+1) + B(x-1)$$

**Method 1: Substitution**
- Set $x = 1$: $5(1) + 1 = A(2) + 0 \Rightarrow A = 3$
- Set $x = -1$: $5(-1) + 1 = 0 + B(-2) \Rightarrow B = 2$

**Step 4: Verify**
$$\frac{3}{x-1} + \frac{2}{x+1} = \frac{3(x+1) + 2(x-1)}{(x-1)(x+1)} = \frac{3x + 3 + 2x - 2}{(x-1)(x+1)} = \frac{5x+1}{x^2-1}$$ ✓

**Step 5: Integrate**
$$\int \frac{5x+1}{x^2-1} \, dx = \int \frac{3}{x-1} \, dx + \int \frac{2}{x+1} \, dx$$
$$= 3\ln|x-1| + 2\ln|x+1| + C$$
$$= \ln|x-1|^3 + \ln|x+1|^2 + C$$
$$= \ln|(x-1)^3(x+1)^2| + C$$

---

### Example 2: Repeated Linear Factors (Medium ⭐⭐)

**Problem:** $\int \frac{7x + 1}{(x-2)^3} \, dx$

**Solution:**

**Step 1: Set up decomposition**

For $(x-2)^3$, include all powers:
$$\frac{7x+1}{(x-2)^3} = \frac{A}{x-2} + \frac{B}{(x-2)^2} + \frac{C}{(x-2)^3}$$

**Step 2: Find A, B, C**

Multiply by $(x-2)^3$:
$$7x + 1 = A(x-2)^2 + B(x-2) + C$$

**Substitution method:**
- Set $x = 2$: $7(2) + 1 = C \Rightarrow C = 15$

**Expand and compare coefficients:**
$$7x + 1 = A(x^2 - 4x + 4) + B(x - 2) + 15$$
$$7x + 1 = Ax^2 + (B-4A)x + (4A - 2B + 15)$$

Comparing coefficients:
- $x^2$: $0 = A \Rightarrow A = 0$
- $x^1$: $7 = B - 4(0) \Rightarrow B = 7$
- $x^0$: $1 = 0 - 2(7) + 15 = 1$ ✓

**Step 3: Decompose**
$$\frac{7x+1}{(x-2)^3} = \frac{7}{(x-2)^2} + \frac{15}{(x-2)^3}$$

**Step 4: Integrate**
$$\int \frac{7x+1}{(x-2)^3} \, dx = \int \frac{7}{(x-2)^2} \, dx + \int \frac{15}{(x-2)^3} \, dx$$

Using $\int (x-2)^n dx = \frac{(x-2)^{n+1}}{n+1}$:
$$= 7 \cdot \frac{(x-2)^{-1}}{-1} + 15 \cdot \frac{(x-2)^{-2}}{-2} + C$$
$$= -\frac{7}{x-2} - \frac{15}{2(x-2)^2} + C$$

---

### Example 3: Irreducible Quadratic Factor (Medium ⭐⭐)

**Problem:** $\int \frac{2x^2 + 3x + 2}{(x+1)(x^2+1)} \, dx$

**Solution:**

**Step 1: Set up decomposition**

For an irreducible quadratic, use $Bx + C$:
$$\frac{2x^2+3x+2}{(x+1)(x^2+1)} = \frac{A}{x+1} + \frac{Bx+C}{x^2+1}$$

**Step 2: Find A, B, C**

Multiply by $(x+1)(x^2+1)$:
$$2x^2 + 3x + 2 = A(x^2+1) + (Bx+C)(x+1)$$

**Substitution:**
- Set $x = -1$: $2 - 3 + 2 = A(2) \Rightarrow A = 1/2$

**Expand and compare:**
$$2x^2 + 3x + 2 = (1/2)(x^2+1) + (Bx+C)(x+1)$$
$$2x^2 + 3x + 2 = (1/2)x^2 + 1/2 + Bx^2 + Bx + Cx + C$$
$$2x^2 + 3x + 2 = (1/2 + B)x^2 + (B+C)x + (1/2 + C)$$

Coefficients:
- $x^2$: $2 = 1/2 + B \Rightarrow B = 3/2$
- $x^1$: $3 = B + C = 3/2 + C \Rightarrow C = 3/2$
- $x^0$: $2 = 1/2 + 3/2 = 2$ ✓

**Step 3: Integrate**
$$\int \frac{2x^2+3x+2}{(x+1)(x^2+1)} \, dx = \int \frac{1/2}{x+1} \, dx + \int \frac{(3/2)x + 3/2}{x^2+1} \, dx$$

For the second integral, split it:
$$\int \frac{(3/2)x}{x^2+1} \, dx + \int \frac{3/2}{x^2+1} \, dx$$
$$= (3/4)\ln(x^2+1) + (3/2)\arctan(x)$$

**Final answer:**
$$= (1/2)\ln|x+1| + (3/4)\ln(x^2+1) + (3/2)\arctan(x) + C$$

---

## ⚠️ Common Mistakes & How to Avoid Them

### Mistake 1: Wrong Number of Constants

❌ **Wrong:**
```
(x-1)²(x+2) with only ¾ fractions
```

✅ **Correct:**
```
(x-1)²(x+2) requires:
A/(x-1) + B/(x-1)² + C/(x+2)
```

### Mistake 2: Forgetting Polynomial Division

❌ **Wrong:**
```
If degree(numerator) ≥ degree(denominator),
try partial fractions directly ← WRONG!
```

✅ **Correct:**
```
Always do polynomial division first!
∫(x² + 5)/(x-1) dx = ∫[x + 1 + 6/(x-1)] dx
```

### Mistake 3: Wrong Form for Quadratic Factor

❌ **Wrong:**
```
1/[(x+1)(x²+2)] = A/(x+1) + B/(x²+2)  ← B should be Bx+C!
```

✅ **Correct:**
```
1/[(x+1)(x²+2)] = A/(x+1) + (Bx+C)/(x²+2)
```

---

## 📝 Practice Problems

### Easy Problems ⭐

1. $\int \frac{1}{x^2-1} \, dx$
2. $\int \frac{2x}{(x-1)(x-2)} \, dx$
3. $\int \frac{x+3}{x^2+2x-3} \, dx$
4. $\int \frac{1}{(x-1)^2} \, dx$
5. $\int \frac{3}{(x+1)^3} \, dx$

**[Solutions →](./solutions-easy.md)**

### Medium Problems ⭐⭐

6. $\int \frac{2x^2+3}{(x-1)(x+2)^2} \, dx$
7. $\int \frac{x}{(x+1)(x^2+1)} \, dx$
8. $\int \frac{x^3}{(x-1)(x+1)} \, dx$ (do polynomial division first!)
9. $\int \frac{1}{x^3-1} \, dx$ (factor as difference of cubes)
10. $\int \frac{2x^2+x}{(x^2+1)^2} \, dx$

**[Solutions →](./solutions-medium.md)**

### Hard Problems ⭐⭐⭐

11. $\int \frac{5x^2}{(x-1)^2(x+1)^2} \, dx$
12. $\int \frac{x^4}{(x^2+1)^2} \, dx$
13. $\int \frac{1}{x(x^2-1)} \, dx$
14. $\int \frac{x^2+1}{(x^2-1)^2} \, dx$
15. $\int \frac{3x^3+x^2}{(x^2+1)^2(x-1)} \, dx$

**[Solutions →](./solutions-hard.md)**

---

## ✅ Self-Assessment Checklist

- [ ] Identify when to use partial fractions
- [ ] Set up decomposition correctly
- [ ] Solve for unknown constants
- [ ] Integrate all fraction types
- [ ] Solve at least 12/15 practice problems

---

## 📖 Next Chapter

**Ready to continue?** Move to [Chapter 5: Special Techniques & Strategy](../05-special-techniques/README.md)

Or go back to [Main Module Guide](../README.md)
