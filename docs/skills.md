# Skills Reference

This document describes all skills available in Jangadeiro and how to use them with Claude Code.

---

## What is a Skill?

A skill is a markdown file that instructs Claude Code on how to approach a specific engineering task. Each skill defines:

- **Goal** — the desired outcome.
- **Instructions** — a step-by-step guide for Claude to follow.
- **Output format** — the structure of the expected response.

Skills are designed to be reused across projects. You can reference them directly in your conversations with Claude Code.

---

## Available Skills

### [code-review](../skills/code-review.md)

**Purpose:** Perform a thorough, constructive code review.

**When to use:** When you want a second opinion on a diff, a PR, or any piece of code before merging or shipping.

**Example prompt:**
```
Using the code-review skill, review the following diff: <paste diff>
```

---

### [test-generation](../skills/test-generation.md)

**Purpose:** Generate meaningful, well-structured tests.

**When to use:** When you need to add test coverage to new or existing code.

**Example prompt:**
```
Using the test-generation skill, write tests for the following function: <paste code>
```

---

### [refactoring](../skills/refactoring.md)

**Purpose:** Improve code quality without changing observable behavior.

**When to use:** When code is working but hard to read, maintain, or extend.

**Example prompt:**
```
Using the refactoring skill, improve the following module: <paste code>
```

---

### [documentation](../skills/documentation.md)

**Purpose:** Generate clear, accurate documentation.

**When to use:** When a function, module, API, or project lacks good documentation.

**Example prompt:**
```
Using the documentation skill, document the following API: <paste code>
```

---

### [debugging](../skills/debugging.md)

**Purpose:** Systematically investigate and resolve bugs.

**When to use:** When you have a reproducible bug and need help finding the root cause.

**Example prompt:**
```
Using the debugging skill, help me fix this bug: <describe bug and paste relevant code>
```

---

## Combining Skills

Skills can be chained. For example, a common workflow is:

1. Use **debugging** to identify and fix a bug.
2. Use **test-generation** to add a regression test.
3. Use **code-review** to verify the overall change.
