# Contributing to Integration Techniques Module

Thank you for your interest in contributing! This module is built by the community, for students.

## How to Contribute

### 🐛 Report Issues

Found an error, typo, or confusing explanation?

1. Go to [Issues](https://github.com/lnseriesv1/integration-techniques-bsece/issues)
2. Click **New Issue**
3. Use descriptive title: e.g., "Chapter 1 Example 3 has wrong answer"
4. Describe the problem clearly
5. Include:
   - Chapter number
   - Problem/example number
   - What's wrong
   - What should be correct

### 💡 Suggest Improvements

Have an idea to make the module better?

1. Open a **Discussion** or **Issue** with tag "enhancement"
2. Describe your suggestion
3. Explain why it would help students
4. Examples of improvements:
   - Better explanations
   - Additional worked examples
   - More practice problems
   - New visualizations
   - Video links

### ✏️ Submit Content (Pull Request)

Want to add or improve content?

#### Step 1: Fork & Clone
```bash
# Fork the repository on GitHub
# Then clone your fork
git clone https://github.com/YOUR-USERNAME/integration-techniques-bsece.git
cd integration-techniques-bsece
```

#### Step 2: Create a Branch
```bash
git checkout -b improve/your-improvement-name
# Example: improve/add-more-examples-chapter-2
```

#### Step 3: Make Your Changes
- Edit markdown files
- Add images or diagrams
- Add practice problems
- Improve explanations

#### Step 4: Commit
```bash
git add .
git commit -m "Add: [Description of changes]"
# Example: git commit -m "Add: 5 worked examples for trig substitution"
```

#### Step 5: Push
```bash
git push origin improve/your-improvement-name
```

#### Step 6: Create Pull Request
1. Go to your fork on GitHub
2. Click **Compare & pull request**
3. Write a clear title and description
4. Submit!

---

## Content Guidelines

### Writing Style

✅ **DO:**
- Write for **complete beginners** (assume no prior knowledge)
- Use **simple language** (avoid jargon)
- Include **intuitive explanations** before formal math
- Give **visual examples** (diagrams, graphs)
- Explain the **"why"** not just the "how"
- Use **plenty of worked examples**

❌ **DON'T:**
- Assume students know advanced concepts
- Use overly formal or dense language
- Skip steps in worked examples
- Forget to explain why a technique is needed

### Format

**Markdown Structure:**
```markdown
# Chapter Title

## 🎯 Learning Objectives
- Bullet points

## 💡 Intuitive Explanation
Plain language introduction

## 📋 The Procedure
Step-by-step instructions

## 🔍 Worked Examples
### Example 1: [Description] (⭐)
**Problem:** ...
**Solution:** ...
**Check:** ...

## ⚠️ Common Mistakes
- Mistakes and fixes

## 📝 Practice Problems
### Easy ⭐
1. Problem...

### Medium ⭐⭐
...

## ✅ Self-Assessment
- Checklist
```

### Worked Examples

Each worked example should:
- ✓ Start with **Problem:** statement
- ✓ Show **Solution:** step-by-step
- ✓ Include **Check:** verification
- ✓ Be progressively more complex
- ✓ Highlight common mistakes

**Template:**
```markdown
### Example 1: [Brief Description] (⭐)

**Problem:** ∫2x(x² + 1) dx

**Solution:**

Step 1: [Your explanation]
Step 2: [Your explanation]
...

**Check:** [Verify by differentiation]
```

### Practice Problems

- Include at least 15 problems per chapter
- Organize by difficulty: ⭐ (Easy), ⭐⭐ (Medium), ⭐⭐⭐ (Hard)
- Start with simple cases, progress to complex
- Provide answer key (in separate file)
- Show work for all solutions

### Diagrams & Images

Use free tools:
- **Desmos** for function graphs
- **Draw.io** for flowcharts
- **GeoGebra** for geometric visualizations
- **Asymptote** or **TikZ** for mathematical diagrams

**Save as:**
- `.png` for images (higher quality)
- `.svg` for diagrams (scalable)

---

## Quality Standards

Before submitting, ensure your contribution:

### Accuracy ✓
- [ ] All mathematics is correct
- [ ] Solutions verified (double-checked)
- [ ] Formulas match standard references
- [ ] No typos or spelling errors

### Clarity ✓
- [ ] Suitable for complete beginners
- [ ] Clear step-by-step explanations
- [ ] Visual aids included where helpful
- [ ] Jargon explained or avoided

### Completeness ✓
- [ ] Includes worked examples
- [ ] Has practice problems with solutions
- [ ] Self-assessment checklist included
- [ ] Links to resources/tools

### Formatting ✓
- [ ] Follows markdown style guide
- [ ] Proper equation formatting (LaTeX)
- [ ] Consistent with existing chapters
- [ ] Images properly sized and credited

---

## Equation Formatting

Use **LaTeX** syntax for math:

**Inline equations:**
```markdown
The integral is $\int x^2 dx$
```

**Display equations:**
```markdown
$$\int x^n dx = \frac{x^{n+1}}{n+1} + C$$
```

**Common symbols:**
```
\int           integral sign
\sum           sum
\frac{a}{b}    fraction
\sqrt{x}       square root
\theta         theta
\infty         infinity
\pm            plus-minus
\neq           not equal
```

---

## Review Process

1. **Submission:** You create a Pull Request
2. **Review:** Maintainers review your changes
3. **Feedback:** We may request improvements
4. **Revision:** You make changes
5. **Approval:** Once approved, we merge!

**Timeline:** Usually 2-7 days depending on complexity

---

## Types of Contributions

### 🌟 We Especially Welcome:

1. **New Worked Examples**
   - Additional examples for each chapter
   - Real BSECE applications
   - Common student mistakes illustrated

2. **Practice Problems**
   - More problems (easy, medium, hard)
   - With detailed solutions
   - Relevant to engineering

3. **Visualizations**
   - Graphs of functions
   - Step-by-step animation explanations
   - Flowcharts for technique selection

4. **Video Links**
   - YouTube tutorials explaining concepts
   - Recommendations with timestamps
   - Teaching different approaches

5. **BSECE Applications**
   - Circuit analysis examples
   - Signal processing problems
   - Real-world engineering scenarios

6. **Translations**
   - Filipino language sections
   - Local context and examples
   - Culturally relevant problems

7. **Bug Fixes**
   - Typos and spelling errors
   - Incorrect mathematics
   - Broken links

---

## Community Standards

### Be Respectful 🤝
- Treat others with kindness
- Assume good intentions
- Welcome diverse perspectives
- Constructive feedback only

### Be Helpful 🙌
- Answer questions in Issues
- Review others' contributions
- Share resources
- Help fellow students

### Be Honest 🎯
- Admit when you're wrong
- Cite sources
- No plagiarism
- Give credit

---

## License

All contributions are licensed under **CC BY-NC-SA 4.0**. By contributing, you agree to this license.

---

## Questions?

📧 **Email:** Open an Issue  
💬 **Chat:** GitHub Discussions  
🐛 **Report bugs:** GitHub Issues  

---

**Thank you for making this module better for everyone! 🎓**
