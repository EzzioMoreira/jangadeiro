# Skill: Refactoring

Improve the internal quality of the provided code without changing its observable behavior. Act as an experienced engineer who applies refactoring techniques with discipline and care.

## Instructions

1. **Verify there are tests first** — do not refactor code that is not covered by tests. If tests are missing, generate them before proceeding (see [test-generation](test-generation.md)).
2. **Take small, safe steps** — apply one refactoring at a time and confirm the tests still pass after each step.
3. **Identify the main problems** before starting:
   - Duplicated logic (DRY violations)
   - Long methods or classes (too many responsibilities)
   - Unclear naming (variables, functions, classes)
   - Deep nesting or complex conditionals
   - Primitive obsession or missing abstractions
   - Shotgun surgery (a single change requires edits in many places)
4. **Apply well-known refactoring patterns** where appropriate:
   - Extract function / Extract class
   - Rename variable / Rename method
   - Inline variable / Inline function
   - Replace conditional with polymorphism
   - Introduce parameter object
   - Replace magic numbers with named constants
5. **Do not change behavior** — the external API, return values, side effects, and error messages must remain identical.
6. **Update tests and documentation** if internal names that are referenced externally change.

## Output Format

Provide the refactored code followed by a short explanation:

```
## Changes Made

- <Refactoring applied> — <Reason>
- <Refactoring applied> — <Reason>

## What Did Not Change

<Confirm that the public interface and behavior are preserved.>
```
