# Integration Technique Selection Flowchart (Text Version)
## Step-by-Step Decision Guide

---

## Level 1: Initial Inspection

```
┌─ Question: Can I identify a function and its derivative?
│  • Look for f(x) and f'(x) appearing together
│  • Example: ∫2x·e^(x²) dx  →  f(x) = x², f'(x) = 2x
│
├─ YES → GO TO LEVEL 2.1 (U-Substitution)
│
└─ NO → Continue to next question
   
   ┌─ Question: Is this a rational function P(x)/Q(x)?
   │  • Numerator and denominator are polynomials
   │  • Example: ∫(3x+1)/(x²-1) dx
   │
   ├─ YES → GO TO LEVEL 2.2 (Partial Fractions)
   │
   └─ NO → Continue to next question
      
      ┌─ Question: Is this a product of 2+ different types?
      │  • Different types: polynomial, trig, exponential, log, inverse trig
      │  • Example: ∫x·sin(x) dx  →  algebraic × trigonometric
      │
      ├─ YES → GO TO LEVEL 2.3 (Integration by Parts)
      │
      └─ NO → Continue to next question
         
         ┌─ Question: Does it involve trig or radical expressions?
         │  • Powers of sin/cos/tan/sec
         │  • √(a²-u²), √(a²+u²), √(u²-a²)
         │  • Example: ∫sin²(x) dx or ∫√(4-x²) dx
         │
         ├─ YES → GO TO LEVEL 2.4 (Trig Techniques)
         │
         └─ NO → GO TO LEVEL 2.5 (Special Techniques)
```

---

## Level 2.1: U-Substitution Path

```
┌─ Step 1: Choose u
│  • u = the inner function
│  • Look for function whose derivative is visible
│  
├─ Step 2: Calculate du
│  • du/dx = ?
│  • Solve for: du = ? dx
│  • Is du exactly what's left in integral?
│    ├─ YES → Proceed
│    └─ NO → Adjust by constant (multiply/divide)
│
├─ Step 3: Rewrite integral in terms of u
│  • Replace ALL x with u expressions
│  • Replace dx with du expression
│  
├─ Step 4: Integrate
│  • ∫g(u) du = ?
│  
└─ Step 5: Back-substitute
   • Replace u back with original x expression
   • Final answer must be in terms of x
```

**When to choose U-Substitution:**
- Clear chain rule structure
- Function and its derivative visible
- Nested functions

---

## Level 2.2: Partial Fractions Path

```
┌─ Step 0: Check degrees
│  If degree(numerator) ≥ degree(denominator):
│  ├─ Do polynomial division FIRST
│  └─ Then apply partial fractions to remainder
│
├─ Step 1: Factor denominator completely
│  • Factor into: (linear factors) × (irreducible quadratics)
│  • Example: (x-1)²(x² + 2x + 3)
│
├─ Step 2: Set up decomposition form
│  • (x-a) → A/(x-a)
│  • (x-a)^n → A/(x-a) + B/(x-a)² + ... + Z/(x-a)^n
│  • x² + bx + c → (Ax+B)/(x²+bx+c)  [NOTE: Ax+B, not A,B]
│
├─ Step 3: Find unknown constants
│  • Multiply both sides by common denominator
│  • Method 1: Substitution (set x = roots)
│  • Method 2: Coefficient comparison (match powers)
│
├─ Step 4: Decompose into simple fractions
│  • Each fraction is now integrable
│  
└─ Step 5: Integrate term by term
   • ∫A/(x-a) dx = A·ln|x-a| + C
   • ∫(Ax+B)/(x²+px+q) dx = ...
```

**When to choose Partial Fractions:**
- Rational function (polynomial ratio)
- Denominator factors nicely
- Can reduce to simple pieces

---

## Level 2.3: Integration by Parts Path

```
┌─ Step 1: Apply LIATE rule to choose u
│  Priority:  L > I > A > T > E
│  • L: Logarithmic (ln, log)
│  • I: Inverse trig (arcsin, arccos, arctan)
│  • A: Algebraic (x, x², polynomials)
│  • T: Trigonometric (sin, cos, tan)
│  • E: Exponential (e^x, a^x)
│
├─ Step 2: Choose remaining part as dv
│  • dv = (everything else) dx
│  • Usually easier to integrate
│
├─ Step 3: Calculate du and v
│  • du = (derivative of u) dx
│  • v = ∫dv (integrate dv)
│
├─ Step 4: Apply formula
│  • ∫u dv = uv - ∫v du
│
├─ Step 5: Evaluate remaining integral
│  • ∫v du might itself need:
│    ├─ Another integration by parts, OR
│    ├─ U-substitution, OR
│    └─ A known formula
│
└─ Step 6: Combine and simplify
   • Add back uv - ∫v du result
```

**When to choose Integration by Parts:**
- Product of different function types
- One factor easier to differentiate
- Other factor easier to integrate
- Examples: x·sin(x), e^x·cos(x), x·ln(x)

---

## Level 2.4: Trigonometric Techniques Path

```
┌─ Branch A: Powers of trig functions
│  ├─ If power is EVEN:
│  │  ├─ Use power reduction formulas
│  │  ├─ sin²(x) = (1 - cos(2x))/2
│  │  └─ cos²(x) = (1 + cos(2x))/2
│  │
│  └─ If power is ODD:
│     ├─ Separate one factor
│     ├─ Use Pythagorean identity
│     └─ Apply u-substitution
│        • For odd sin: let u = cos(x)
│        • For odd cos: let u = sin(x)
│
├─ Branch B: Radical expressions
│  ├─ If √(a² - u²):
│  │  ├─ Use substitution: u = a·sin(θ)
│  │  ├─ Creates: √(a²cos²(θ)) = a|cos(θ)|
│  │  └─ Range: -π/2 ≤ θ ≤ π/2
│  │
│  ├─ If √(a² + u²):
│  │  ├─ Use substitution: u = a·tan(θ)
│  │  ├─ Creates: √(a²sec²(θ)) = a|sec(θ)|
│  │  └─ Range: -π/2 < θ < π/2
│  │
│  └─ If √(u² - a²):
│     ├─ Use substitution: u = a·sec(θ)
│     ├─ Creates: √(a²tan²(θ)) = a|tan(θ)|
│     └─ Range: 0 ≤ θ < π/2 or π ≤ θ < 3π/2
│
└─ Step: Back-substitute
   • Draw right triangle if needed
   • Express trig functions in terms of x
   • Simplify to get final answer
```

**When to choose Trig Techniques:**
- Powers of trig functions: sin^n, cos^n, tan^n
- Radical expressions with specific forms
- After trig identities might simplify the problem

---

## Level 2.5: Special Techniques Path

```
┌─ Check 1: Quadratic in denominator or under radical?
│  ├─ YES → Complete the square first
│  │        Then apply appropriate technique
│  └─ NO → Continue
│
├─ Check 2: High powers of trig functions (n ≥ 3)?
│  ├─ YES → Consider reduction formulas
│  │        ∫sin^n or ∫cos^n can use recursive formula
│  └─ NO → Continue
│
├─ Check 3: Nested radicals or complex irrational?
│  ├─ YES → Try substitution to eliminate inner radical
│  │        May need multiple substitutions
│  └─ NO → Continue
│
├─ Check 4: Can you rewrite the integrand?
│  ├─ YES → Try:
│  │        • Factor differently
│  │        • Multiply by 1 (e.g., multiply/divide by something)
│  │        • Split into simpler pieces
│  │        • Use algebraic identities
│  └─ NO → Continue
│
└─ Check 5: Combine multiple techniques
   └─ Example: Try u-sub first, then integrate by parts on result
```

**When to choose Special Techniques:**
- Standard techniques don't apply
- Requires creativity and rewriting
- Often combining multiple methods
- Last resort when others don't work

---

## Decision Tree Summary Table

```
┌──────────────────────────────────────────────────────────────────┐
│ FEATURE IN INTEGRAL              → TECHNIQUE                     │
├──────────────────────────────────────────────────────────────────┤
│ f(u) · u' together               → U-SUBSTITUTION                │
│ P(x)/Q(x) rational function      → PARTIAL FRACTIONS             │
│ Product of different types       → INTEGRATION BY PARTS          │
│ Powers of sin/cos/tan            → TRIG INTEGRALS                │
│ √(a²-u²), √(a²+u²), √(u²-a²)    → TRIG SUBSTITUTION             │
│ Quadratic ax²+bx+c               → COMPLETING THE SQUARE          │
│ High powers (n≥3)                → REDUCTION FORMULA              │
│ Nested radicals                  → SPECIAL (nested subst)         │
│ Product of rational & irrational → COMBINATION                    │
│ None of above / Complex          → REWRITE + TRY AGAIN            │
└──────────────────────────────────────────────────────────────────┘
```

---

## Example Walkthroughs

### Example 1: ∫x·sin(x) dx

```
Step 1: Not f(u)·u' → Not pure u-sub
Step 2: Not rational → Not partial fractions  
Step 3: Product (algebraic × trig) → INTEGRATION BY PARTS
        u = x (Algebraic), dv = sin(x)dx
        du = dx, v = -cos(x)
        = -x·cos(x) + ∫cos(x)dx
        = -x·cos(x) + sin(x) + C ✓
```

### Example 2: ∫(2x+3)/(x²+x+1) dx

```
Step 1: Not obvious u-sub
Step 2: Not partial fractions (irreducible quad in denominator)
Step 3: Not really a "product" to use IBP
Step 4: Quadratic! Complete the square
        x² + x + 1 = (x + 1/2)² + 3/4
Step 5: Split the numerator
        = ∫2x/(x²+x+1) dx + ∫3/(x²+x+1) dx
        
        First: Let u = x²+x+1, du = (2x+1)dx
        Second: Use arctan formula after completing square
        
        Result: ln|x²+x+1| + √3·arctan((2x+1)/√3) + C ✓
```

### Example 3: ∫√(9-x²) dx

```
Step 1: Not f(u)·u'
Step 2: Not rational
Step 3: Not product for IBP
Step 4: Has √(a²-x²) form! → TRIG SUBSTITUTION
        x = 3·sin(θ), dx = 3·cos(θ)dθ
        √(9-x²) = 3·cos(θ)
        
        = ∫3·cos(θ)·3·cos(θ) dθ
        = 9∫cos²(θ) dθ
        = 9·[θ/2 + sin(2θ)/4] + C
        
        Back-substitute: θ = arcsin(x/3), sin(2θ) = (2x/9)·√(9-x²)
        = (9/2)arcsin(x/3) + (x/2)√(9-x²) + C ✓
```

---

**Use this flowchart to guide your technique selection!**
