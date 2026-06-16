# Visual Guides & Flowcharts
## Integration Techniques Companion

---

## 📊 Master Decision Tree

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    WHICH INTEGRATION TECHNIQUE TO USE?                      │
└─────────────────────────────────────────────────────────┬───────────────────┘
                                                          │
                                    ┌─────────────────────▼──────────────────┐
                                    │ Do you see f(u) and u' together?       │
                                    │ (Function and its derivative)           │
                                    └────────────────┬──────────────┬────────┘
                                                     │              │
                                              YES ◄──┴──► NO        │
                                                     │              │
                          ┌──────────────────────────▼──┐           │
                          │  USE U-SUBSTITUTION ✓        │           │
                          │  Let u = inner function      │           │
                          │  Find du                     │           │
                          │  Substitute & simplify       │           │
                          │  Integrate                   │           │
                          │  Back-substitute             │           │
                          └──────────────────────────────┘           │
                                                                     │
                                    ┌────────────────────────────────▼──────┐
                                    │ Is it a RATIONAL FUNCTION?             │
                                    │ P(x)/Q(x) where P,Q are polynomials   │
                                    └────────┬──────────────────┬───────────┘
                                             │                  │
                                      YES ◄──┴──► NO            │
                                             │                  │
                          ┌──────────────────▼──┐               │
                          │ PARTIAL FRACTIONS ✓  │               │
                          │ Factor denominator   │               │
                          │ Set up decomposition │               │
                          │ Find constants       │               │
                          │ Integrate            │               │
                          └──────────────────────┘               │
                                                                 │
                                    ┌───────────────────────��────▼──────┐
                                    │ Is it a PRODUCT of 2+ different   │
                                    │ function types?                    │
                                    │ (poly × trig, poly × exp, etc.)    │
                                    └────────┬──────────────┬───────────┘
                                             │              │
                                      YES ◄──┴──► NO        │
                                             │              │
                          ┌──────────────────▼──┐           │
                          │ INTEGRATION BY       │           │
                          │ PARTS ✓              │           │
                          │ Choose u (LIATE)     │           │
                          │ Choose dv            │           │
                          │ Apply: u·v - ∫v·du   │           │
                          │ (May repeat)         │           │
                          └──────────────────────┘           │
                                                             │
                                    ┌────────────────────────▼──────┐
                                    │ Does it involve:               │
                                    │ • Powers of sin/cos/tan/sec?   │
                                    │ • √(a²-u²), √(a²+u²), √(u²-a²)?│
                                    └────────┬──────────────┬────────┘
                                             │              │
                                      YES ◄──┴──► NO        │
                                             │              │
                   ┌─────────────────────────▼──┐            │
                   │ TRIG TECHNIQUES ✓           │            │
                   │ • Power reduction formulas  │            │
                   │ • Trig substitution         │            │
                   │ • Pythagorean identities    │            │
                   │ • Separate odd power        │            │
                   └─────────────────────────────┘            │
                                                              │
                                    ┌─────────────────────────▼──────┐
                                    │ SPECIAL TECHNIQUES:             │
                                    │ • Completing the square         │
                                    │ • Reduction formulas            │
                                    │ • Irrational rewrite            │
                                    │ • Nested substitution           │
                                    │ • Combine multiple techniques   │
                                    │ • Try rewriting the integrand   │
                                    └────────────────────────────────┘
```

---

## 1️⃣ Chapter 1: U-Substitution Quick Reference

### The Process (4 Steps)

```
┌─────────────────────────────────────────────────────────┐
│ STEP 1: CHOOSE u                                        │
│ ────────────────────────────────────────────────────────│
│ Look for: • Inner function (nested)                    │
│           • Function whose derivative appears nearby    │
│ Example: u = x² + 1  (because d/dx[x²+1] = 2x)         │
└─────────────────────────────────────────────────────────┘
                         ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 2: FIND du                                         │
│ ────────────────────────────────────────────────────────│
│ Differentiate u:  du/dx = f'(x)                        │
│ Isolate:  du = f'(x) dx                                │
│ Example: du = 2x dx                                     │
└─────────────────────────────────────────────────────────┘
                         ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 3: REWRITE the integral                            │
│ ────────────────────────────────────────────────────────│
│ Replace all x terms and dx:                            │
│ ∫f(x) dx  →  ∫g(u) du                                  │
│ Example: ∫2x(x²+1) dx = ∫u du                          │
└─────────────────────────────────────────────────────────┘
                         ↓
┌─────────────────────────────────────────────────────────┐
│ STEP 4: INTEGRATE & BACK-SUBSTITUTE                     │
│ ────────────────────────────────────────────────────────│
│ Integrate with respect to u:  ∫g(u) du = G(u) + C      │
│ Substitute back x:  G(f(x)) + C                        │
│ Example: = u²/2 + C = (x²+1)²/2 + C                    │
└─────────────────────────────────────────────────────────┘
```

### Pattern Recognition

```
╔════════════════════════════════════════════════════════════╗
║ DOES THIS LOOK LIKE U-SUBSTITUTION?                        ║
╠════════════════════════════════════════════════════════════╣
║                                                            ║
║  ✓ ∫e^(3x) · 3 dx              → u = 3x                   ║
║  ✓ ∫2x(x²+1)^5 dx              → u = x² + 1               ║
║  ✓ ∫sin(x³) · 3x² dx           → u = x³                   ║
║  ✓ ∫cos(2x) · 2 dx             → u = 2x                   ║
║  ✓ ∫(1/(2x+1)) · 2 dx          → u = 2x + 1              ║
║  ✗ ∫e^x dx                     → Can't see u·du together  ║
║  ✗ ∫x sin(x) dx                → No derivative relationship║
║  ✗ ∫(1/x) dx                   → Wait, u = ln(x)! This ok║
║                                                            ║
╚════════════════════════════════════════════════════════════╝
```

### Common Substitutions Chart

```
┌──────────────────┬─────────────┬─────────────────────────┐
│  Pattern in ∫    │  Choose u   │  Then du =              │
├──────────────────┼─────────────┼─────────────────────────┤
│ e^(ax)           │ u = ax      │ a dx  (watch for a!)    │
│ sin(bx) or cos   │ u = bx      │ b dx                    │
│ (f(x))^n · f'(x) │ u = f(x)    │ f'(x) dx                │
│ 1/(g(x)) · g'(x) │ u = g(x)    │ g'(x) dx                │
│ √(h(x)) · h'(x)  │ u = h(x)    │ h'(x) dx                │
│ 1/x              │ u = ln(x)   │ (1/x) dx                │
└──────────────────┴─────────────┴─────────────────────────┘
```

---

## 2️⃣ Chapter 2: Integration by Parts

### The Formula Explained

```
     ∫ u dv  =  u·v  -  ∫ v du
       │         │      │      │
       │         │      │      └─ Integrate leftover
       │         │      └─────── What you have after using u·v
       │         └─────────────── The u and v parts multiplied
       └─────────────────────── What you're trying to integrate
```

### LIATE Priority Table

```
╔═══════════════════════════════════════════════════════════════╗
║           LIATE PRIORITY (Choose u First!)                   ║
╠═══════════════════════════════════════════════════════════════╣
║                                                               ║
║  1st Priority (L): LOGARITHMIC                               ║
║     ln(x), log(x), ln(f(x))                                  ║
║     ALWAYS choose these as u!                               ║
║                                                               ║
║  2nd Priority (I): INVERSE TRIGONOMETRIC                     ║
║     arcsin(x), arccos(x), arctan(x), etc.                   ║
║     Choose these as u if no logarithm                       ║
║                                                               ║
║  3rd Priority (A): ALGEBRAIC (Polynomials)                   ║
║     x, x², 3x+2, x³, etc.                                    ║
║     Choose if no L or I present                             ║
║                                                               ║
║  4th Priority (T): TRIGONOMETRIC                             ║
║     sin(x), cos(x), tan(x), etc.                            ║
║     Choose if no L, I, or A                                 ║
║                                                               ║
║  5th Priority (E): EXPONENTIAL (Last Resort)                 ║
║     e^x, 2^x, a^x                                           ║
║     Only choose if nothing else is available                ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

### Step-by-Step Example: ∫x·sin(x) dx

```
┌─────────────────────────────────────────────────┐
│ IDENTIFY: This is a product of different types  │
│ x (Algebraic) × sin(x) (Trigonometric)          │
│ A comes before T in LIATE → u = x               │
└────────────────┬────────────────────────────────┘
                 │
        ┌────────▼─────────┐
        │ u = x            │
        │ dv = sin(x) dx   │
        └────────┬─────────┘
                 │
        ┌────────▼─────────┐
        │ du = 1 dx = dx   │
        │ v = -cos(x)      │
        └────────┬─────────┘
                 │
        ┌────────▼──────────────────────────────┐
        │ ∫x·sin(x) dx = x·(-cos(x)) - ∫(-cos(x)) dx
        │              = -x·cos(x) + ∫cos(x) dx  │
        │              = -x·cos(x) + sin(x) + C  │
        └────────┬──────────────────────────────┘
                 │
        ┌────────▼──────────────────────────┐
        │ VERIFY by differentiation:        │
        │ d/dx[-x·cos(x) + sin(x)]          │
        │ = -cos(x) + x·sin(x) + cos(x)     │
        │ = x·sin(x) ✓                      │
        └───────────────────────────────────┘
```

### Tabular Method Visualization

```
 For ∫x³·sin(x) dx:

 DERIVATIVES (u)  │  INTEGRALS (dv)  │  SIGN  │ PRODUCT
 ─────────────────┼──────────────────┼────────┼──────────────────────
  x³              │  sin(x)          │  (+)   │  x³·(-cos(x))
  ↓ d/dx          │  ↓ ∫             │        │
  3x²             │  -cos(x)         │  (-)   │  -3x²·(-sin(x))
  ↓ d/dx          │  ↓ ∫             │        │
  6x              │  -sin(x)         ��  (+)   │  +6x·(cos(x))
  ↓ d/dx          │  ↓ ∫             │        │
  6               │  cos(x)          │  (-)   │  -6·sin(x)
  ↓ d/dx          │  ↓ ∫             │        │
  0               │  sin(x)          │  (STOP)│

 RESULT: -x³·cos(x) + 3x²·sin(x) + 6x·cos(x) - 6·sin(x) + C
```

---

## 3️⃣ Chapter 3: Trigonometric Integrals

### Power Reduction Formula Guide

```
╔═══════════════════════════════════════════════════════════════╗
║     REDUCING POWERS OF SINE AND COSINE                       ║
╠═══════════════════════════════════════════════════════════════╣
║                                                               ║
║ EVEN POWERS → Use Power Reduction Formulas                   ║
║                                                               ║
║   sin²(x) = [1 - cos(2x)] / 2                                ║
║   cos²(x) = [1 + cos(2x)] / 2                                ║
║   sin²(x)·cos²(x) = [1 - cos(4x)] / 8                        ║
║                                                               ║
║ ODD POWERS → Separate 1 factor, use Pythagorean Identity    ║
║                                                               ║
║   sin³(x) = sin²(x)·sin(x) = [1-cos²(x)]·sin(x)             ║
║   cos³(x) = cos²(x)·cos(x) = [1-sin²(x)]·cos(x)             ║
║                                                               ║
║   Then use u-substitution:                                   ║
║   • For odd sin: let u = cos(x)                              ║
║   • For odd cos: let u = sin(x)                              ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

### Trigonometric Substitution Flowchart

```
                WHICH TRIG SUBSTITUTION?
                        │
        ┌───────────────┼───────────────┐
        │               │               │
    √(a²-x²)        √(a²+x²)       √(x²-a²)
        │               │               │
    Use x = a·sin(θ) │ Use x = a·tan(θ) │ Use x = a·sec(θ)
        │               │               │
    Identity:       Identity:       Identity:
    sin²+cos²=1     tan²+1=sec²     sec²-1=tan²
        │               │               │
   Result:          Result:         Result:
   a·cos(θ)         a·sec(θ)        a·tan(θ)
        │               │               │
    Range:          Range:          Range:
    -π/2≤θ≤π/2      -π/2<θ<π/2      0≤θ<π/2 or π≤θ<3π/2
```

### Right Triangle Reference (for Back-Substitution)

```
For x = a·sin(θ):              For x = a·tan(θ):

      ╱|                            ╱
     ╱ │                           ╱  
а  ╱  │ √(a²-x²)                  ╱___
   ╱θ  │                         ╱  a²+x²
  ╱____|                        ╱ x  θ
   x                           ╱____
                                  a

sin(θ) = x/a                 tan(θ) = x/a
cos(θ) = √(a²-x²)/a         sec(θ) = √(a²+x²)/a

For x = a·sec(θ):

      ╱|
     ╱ │ √(x²-a²)
 x  ╱  │
   ╱ θ │
  ╱____|  
   a

sec(θ) = x/a
tan(θ) = √(x²-a²)/a
```

---

## 4️⃣ Chapter 4: Partial Fractions

### Decomposition Setup Guide

```
┌─────────────────────────────────────────────────────────────┐
│ FACTOR TYPE          │  DECOMPOSITION FORM                 │
├─────────────────────────────────────────────────────────────┤
│                      │                                      │
│ (x-a)                │  A/(x-a)                            │
│                      │                                      │
│ (x-a)²               │  A/(x-a) + B/(x-a)²                 │
│                      │                                      │
│ (x-a)³               │  A/(x-a) + B/(x-a)² + C/(x-a)³      │
│                      │                                      │
│ (x-a)(x-b)           │  A/(x-a) + B/(x-b)                  │
│                      │                                      │
│ (x-a)²(x-b)          │  A/(x-a) + B/(x-a)² + C/(x-b)       │
│                      │                                      │
│ (x²+ax+b)            │  (Ax+B)/(x²+ax+b)                   │
│ [irreducible]        │  (NOTE: Use Ax+B, not A and B!)     │
│                      │                                      │
│ (x²+ax+b)²           │  (Ax+B)/(x²+ax+b) + (Cx+D)/(x²+ax+b)²
│ [irreducible]        │                                      │
│                      │                                      │
└─────────────────────────────────────────────────────────────┘
```

### Solving Constants: Methods Comparison

```
╔════════════════════════════════════════════════════════════╗
║  METHOD 1: SUBSTITUTION (Fastest for roots)               ║
╠════════════════════════════════════════════════════════════╣
║                                                            ║
║  Example: (5x+1)/[(x-1)(x+1)] = A/(x-1) + B/(x+1)        ║
║                                                            ║
║  Multiply by (x-1)(x+1):                                  ║
║  5x + 1 = A(x+1) + B(x-1)                                 ║
║                                                            ║
║  Set x = 1:  6 = A(2)  →  A = 3                           ║
║  Set x = -1: -4 = B(-2)  →  B = 2                         ║
║                                                            ║
╚════════════════════════════════════════════════════════════╝

╔════════════════════════════════════════════════════════════╗
║  METHOD 2: COEFFICIENT COMPARISON                         ║
╠════════════════════════════════════════════════════════════╣
║                                                            ║
║  Example: (5x+1)/[(x-1)(x+1)] = A/(x-1) + B/(x+1)        ║
║                                                            ║
║  Multiply: 5x + 1 = A(x+1) + B(x-1)                      ║
║  Expand:   5x + 1 = Ax + A + Bx - B                      ║
║            5x + 1 = (A+B)x + (A-B)                       ║
║                                                            ║
║  x terms:   5 = A + B                                     ║
║  constants: 1 = A - B                                     ║
║                                                            ║
║  Solve: A = 3, B = 2                                      ║
║                                                            ║
╚════════════════════════════════════════════════════════════╝
```

### Integration After Decomposition

```
AFTER DECOMPOSING, you'll have these forms:

    A                 →  A·ln|x-a| + C
   ───────               ────────────
   x - a

    A                 →  A·(x-a)^(-n+1)/(-n+1) + C
   ───────────           
   (x-a)^n

   Ax+B               →  (A/2)ln|x²+bx+c| + [B-Ab/2]·arctan(...)
   ────────
   x²+bx+c
```

---

## 5️⃣ Chapter 5: Special Techniques

### Completing the Square Transformation

```
For: ax² + bx + c

STEP 1: Factor out leading coefficient (if a ≠ 1)
        a(x² + (b/a)x) + c

STEP 2: Complete inside parentheses
        a(x² + (b/a)x + (b/2a)² - (b/2a)²) + c
        = a[(x + b/2a)² - (b/2a)²] + c

STEP 3: Simplify
        = a(x + b/2a)² - b²/(4a) + c
        = a(x + b/2a)² + (c - b²/4a)
        = (x + h)² + k    where h = b/2a, k = c - b²/4a

EXAMPLE: x² + 4x + 5
        = (x² + 4x + 4) + 1
        = (x + 2)² + 1
```

### Reduction Formula Pattern

```
For ∫sin^n(x) dx:

        ┌─────────────────────────────────────────────┐
        │ ∫sin^n(x) dx = -1/n · sin^(n-1)(x)·cos(x)   │
        │             + (n-1)/n · ∫sin^(n-2)(x) dx    │
        └─────────────────────────────────────────────┘

This creates a RECURSIVE pattern:
  sin^n  → sin^(n-2)  → sin^(n-4)  → ... → sin^0 or sin^1

EXAMPLE: For ∫sin^4(x) dx

∫sin^4  = -1/4·sin³·cos + 3/4·∫sin² dx
        = -1/4·sin³·cos + 3/4·[x/2 - sin(2x)/4]
        = -1/4·sin³·cos + 3x/8 - 3sin(2x)/16
```

### Multiple Technique Flowchart

```
        COMPLEX INTEGRAL
              │
        ┌─────┴─────┐
        │           │
    Try 1st     Try 2nd
   technique   technique
        │           │
    Works? ──N─→ Works? ──N─→ Try 3rd technique
        │           │           │
       Y│          Y│      Works? ──N─→ Rewrite/Reconsider
        │           │           │
        ▼           ▼          Y│
    ┌────────┐ ┌────────┐      ▼
    │COMBINE │ │COMBINE │   ┌────────┐
    │  WITH  │ │  WITH  │   │COMBINE │
    │ 1st    │ │ 2nd    │   │ WITH   │
    │        │ │        │   │  3rd   │
    └────────┘ └────────┘   └────────┘
        │           │           │
        └───────────┴───────────┘
              │
              ▼
        FINAL ANSWER
```

---

## 📚 Technique Comparison Matrix

```
╔════════════════╦═════════════════╦═══════════╦════════════════╗
║ Technique      ║ Best For        ║ Difficulty║ Common Mistakes║
╠════════════════╬═════════════════╬═══════════╬════════════════╣
║ U-Substitution ║ Nested functions║ Easy      ║ Forgetting du  ║
║                ║ Chain rule form ║           ║ or not all x   ║
╠════════════════╬═════════════════╬═══════════╬════════════════╣
║ Integration by ║ Products of     ║ Medium    ║ Wrong LIATE    ║
║ Parts          ║ different types ║           ║ Sign errors    ║
╠════════════════╬═════════════════╬═══════════╬════════════════╣
║ Trig Integrals ║ Powers of trig  ║ Medium    ║ Wrong identity ║
║                ║ Trig subst.     ║           ║ Back-subst     ║
╠════════════════╬═════════════════╬═══════════╬════════════════╣
║ Partial        ║ Rational        ║ Medium    ║ Wrong # of     ║
║ Fractions      ║ functions       ║           ║ constants      ║
╠════════════════╬═════════════════╬═══════════╬════════════════╣
║ Special        ║ Complex integrals║ Hard      ║ Choosing wrong ║
║ Techniques     �� Mixed types     ║           ║ technique      ║
╚════════════════╩═════════════════╩═══════════╩════════════════╝
```

---

## 🎯 Quick Decision Checklist

```
┌───────────────────────────────────────────────────────────────┐
│ WHEN SOLVING AN INTEGRAL, ASK YOURSELF:                       │
├───────────────────────────────────────────────────────────────┤
│                                                               │
│ □ Can I see a function and its derivative together?          │
│   ↳ YES → U-SUBSTITUTION                                    │
│                                                               │
│ □ Is this P(x)/Q(x) with Q factored?                        │
│   ↳ YES → PARTIAL FRACTIONS                                 │
│                                                               │
│ □ Is this a product of TWO different function types?         │
│   ↳ YES → INTEGRATION BY PARTS (use LIATE)                 │
│                                                               │
│ □ Does it have sin, cos, tan, √(±x²)?                       │
│   ↳ YES → TRIG TECHNIQUES or TRIG SUBSTITUTION              │
│                                                               │
│ □ Does the denominator have x² + bx + c?                    │
│   ↳ YES → Complete the square first!                        │
│                                                               │
│ □ Is this a high power like sin⁴ or cos⁵?                   │
│   ↳ YES → Consider REDUCTION FORMULA                         │
│                                                               │
│ □ None of the above?                                         │
│   ↳ Try REWRITING or COMBINING TECHNIQUES                   │
│                                                               │
└───────────────────────────────────────────────────────────────┘
```

---

## 📊 Visual Summary: All Techniques Side-by-Side

```
╔═════════════════════════════════════════════════════════════════════╗
║                     INTEGRATION TECHNIQUES SUMMARY                  ║
╠═════════════════════════════════════════════════════════════════════╣
║                                                                     ║
║ CH.1 U-SUB          │ CH.2 BY PARTS        │ CH.3 TRIG             ║
║ ────────────────    │ ──────────────────   │ ─────────────         ║
║ Chain Rule Reverse  │ Product Rule Reverse │ Identities & Subst    ║
║                     │                      │                       ║
║ ∫f(u)·u' dx         │ ∫u dv = uv - ∫v du   │ sin²,cos²,√(a²-u²)    ║
║                     │                      │                       ║
║ Look for nested     │ LIATE priority:      │ Power reduction:      ║
║ + derivative visible│ L>I>A>T>E            │ sin²x = (1-cos2x)/2   ║
║                     │                      │                       ║
║ Substitution table  │ Tabular method for   │ Trig substitution     ║
║ at Chapter 1        │ repeated IBP         │ table at Chapter 3    ║
║                     │                      │                       ║
╠═════════════════════╦═════════════════════════════════════════════╣
║                     ║                                             ║
║ CH.4 PARTIAL        ║ CH.5 SPECIAL TECHNIQUES                    ║
║ ─────────────────   ║ ────────────────────────────────────────   ║
║ Rational Functions  ║ Advanced Strategies                        ║
║                     ║                                             ║
║ P(x)/Q(x)           ║ • Completing square                        ║
║ Factor Q, decompose │ • Reduction formulas                       ║
║                     ║ • Nested substitutions                     ║
║ Three factor types: ║ • Irrational rewrites                      ║
║ • Linear            ║ • Multiple techniques                      ║
║ • Repeated linear   ║ • Problem rewriting                        ║
║ • Irreducible quad  ║                                             ║
║                     ║ USE DECISION TREE:                         ║
║ Find constants A,B  ║ Try 1st tech → 2nd → 3rd → Special        ║
║ by substitution or  ║                                             ║
║ coefficient compare ║ When to use: "Nothing else works!"         ║
║                     ║                                             ║
╚═════════════════════╩═════════════════════════════════════════════╝
```

---

## 🖨️ Print-Friendly Quick Reference

```
TOP INTEGRATION TECHNIQUES (1-Page Cheat Sheet)

[U-SUBSTITUTION]  [INTEGRATION BY PARTS]  [TRIG INTEGRALS]
1. Choose u       1. Choose u (LIATE)     1. Power reduction
2. Find du        2. Choose dv             2. Trig substitution
3. Rewrite        3. Calculate v & du      3. Use identities
4. Integrate      4. Apply: uv - ∫v·du    4. Separate odd power
5. Back-sub       5. Back-substitute       5. Use u-substitution

[PARTIAL FRACTIONS]  [SPECIAL TECHNIQUES]
1. Check degree      1. Completing square
2. Factor denom      2. Reduction formulas
3. Set up form       3. Multiple techniques
4. Find constants    4. Rewrite integrand
5. Integrate each    5. Decision tree
```

---

**Save this page for quick reference while solving integrals!**
