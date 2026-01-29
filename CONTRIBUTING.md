# Contributing to Uniswap V4 Hooks Skill

Thank you for your interest in making V4 hook development safer! This document provides guidelines for contributing.

## Code of Conduct

- Be respectful and constructive
- Focus on security and correctness over style preferences
- Assume good intent from other contributors
- Help newcomers learn

## How to Contribute

### 1. Reporting Issues

**For general issues:**
- Use GitHub Issues
- Describe the problem clearly
- Include examples if applicable

**For security issues in the guidance:**
- Do NOT open a public issue
- Contact maintainers directly
- Allow time for correction

### 2. Suggesting Improvements

Open an issue with:
- Clear description of the improvement
- Why it matters for security
- Examples or references if available

### 3. Submitting Pull Requests

#### Small Changes (typos, clarifications)
- Fork the repo
- Make your changes
- Submit PR with clear description

#### Significant Changes (new patterns, vulnerabilities)

1. **Open an issue first** to discuss the change
2. Fork the repo
3. Create a feature branch: `git checkout -b feature/your-feature`
4. Make your changes
5. Test by installing the skill locally
6. Submit PR referencing the issue

## Content Guidelines

### Adding Vulnerability Patterns

When documenting a new vulnerability:

```markdown
### Vulnerability Name

**Risk Level:** Critical/High/Medium/Low

**Description:** Clear explanation of the vulnerability

**Vulnerable Code:**
```solidity
// BAD: Explanation of why this is dangerous
vulnerable_code_here();
```

**Secure Code:**
```solidity
// GOOD: Explanation of the fix
secure_code_here();
```

**Source:** Link to audit, exploit, or research
```

### Adding Code Templates

Templates should:
- Be complete and compilable
- Include inline security comments
- Follow Uniswap's code style
- Be tested with Foundry

### Writing Style

- Use imperative mood ("Add check" not "Added check")
- Be direct and concise
- Prioritize security over elegance
- Include code examples for complex concepts

## What We're Looking For

### High Priority
- New vulnerability patterns from audits
- Corrections to existing security advice
- Better code templates from production hooks
- Testing patterns and examples

### Medium Priority
- Clearer explanations of existing concepts
- Additional resources and references
- Edge cases and gotchas

### Lower Priority
- Style/formatting changes
- Reorganization without new content

## Testing Your Changes

Before submitting:

1. Install the skill locally in Claude Code
2. Test with prompts like:
   - "Create a basic afterSwap hook"
   - "What are the security risks of beforeSwapReturnDelta?"
   - "Review this hook for vulnerabilities" (with sample code)
3. Verify the guidance is accurate and helpful

## Review Process

1. Maintainers review for accuracy and security
2. Community feedback period for significant changes
3. Merge when approved

## Recognition

Contributors are recognized in:
- Git commit history
- README acknowledgments (for significant contributions)

## Questions?

Open a GitHub Discussion or Issue for questions about contributing.

---

Thank you for helping make Uniswap V4 hooks safer for everyone!
