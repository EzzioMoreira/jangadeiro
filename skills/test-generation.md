# Skill: Test Generation

Generate meaningful, well-structured tests for the provided code. Act as an experienced engineer who values test quality over test quantity.

## Instructions

1. **Analyze the code under test** — understand its public interface, side effects, error paths, and implicit contracts before writing a single test.
2. **Choose the right test type**:
   - Unit tests for pure logic and individual functions.
   - Integration tests for interactions between components.
   - End-to-end tests only when the full stack behavior must be verified.
3. **Cover what matters**:
   - Happy path — the primary expected behavior.
   - Edge cases — empty inputs, boundary values, maximum sizes.
   - Error paths — invalid arguments, network failures, missing data.
   - Concurrency and state — race conditions, idempotency, side effects.
4. **Use the project's existing test framework, conventions, and helpers.** Do not introduce new testing libraries unless there is a compelling reason.
5. **Name tests descriptively** — a failing test name must tell the reader exactly what broke and under which condition.
6. **Keep tests independent** — each test must be able to run in isolation without relying on state left by another test.
7. **Avoid testing implementation details** — test behavior, not internal methods or private state.
8. **Mock external dependencies** conservatively — only mock what you cannot control (I/O, time, randomness, third-party services).

## Output Format

Provide the complete test file(s) ready to be added to the project. Include a brief comment at the top explaining the testing strategy chosen.

## Example Structure

```
// Strategy: unit tests covering the public API of <module>.
// External HTTP calls are mocked; the database is replaced with an in-memory fake.

describe('<Module>', () => {
  describe('<method>', () => {
    it('returns X when given Y', () => { ... });
    it('throws an error when Z is missing', () => { ... });
  });
});
```
