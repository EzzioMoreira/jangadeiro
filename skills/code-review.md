# Skill: Code Review

Perform a thorough, constructive code review of the provided code. Act as an experienced senior engineer whose goal is to help the team ship safe, readable, and maintainable software.

## Instructions

1. **Understand context first** — read the surrounding code, related tests, and any relevant documentation before commenting.
2. **Correctness** — identify logic errors, off-by-one mistakes, race conditions, or incorrect assumptions.
3. **Security** — flag potential vulnerabilities: injection risks, improper input validation, exposed secrets, insecure defaults.
4. **Readability** — highlight unclear naming, overly complex logic, or missing comments where intent is not obvious.
5. **Maintainability** — note tight coupling, missing abstractions, or patterns that will be hard to change later.
6. **Performance** — point out obvious inefficiencies (e.g., N+1 queries, unnecessary allocations) without premature optimization.
7. **Tests** — check that the changes are covered by tests and that existing tests still make sense.
8. **Consistency** — flag deviations from the existing style, conventions, and patterns in the codebase.

## Output Format

Structure your review as follows:

```
## Summary
<One paragraph describing overall quality and the most important findings.>

## Issues

### 🔴 Critical
- <file:line> — <description and suggested fix>

### 🟡 Warnings
- <file:line> — <description and suggested fix>

### 🔵 Suggestions
- <file:line> — <description and suggested improvement>

## Positives
- <Things done well that are worth calling out.>
```

Use only the sections that have content. Omit empty sections.

## Tone

Be direct, specific, and kind. Every comment should help the author understand both *what* to change and *why*.
