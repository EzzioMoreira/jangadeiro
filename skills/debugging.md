# Skill: Debugging

Systematically investigate and resolve bugs in the provided code. Act as an experienced engineer who debugs with evidence, not guesswork.

## Instructions

1. **Reproduce the problem first** — confirm you can trigger the bug reliably before attempting a fix. Document the exact steps, inputs, and environment needed.
2. **Understand the expected vs. actual behavior** — state precisely what should happen and what happens instead.
3. **Form a hypothesis** — based on the symptoms and code, propose the most likely cause. Be explicit: "I think the bug is in X because Y."
4. **Gather evidence**:
   - Read error messages and stack traces carefully — the root cause is often not at the top of the trace.
   - Add targeted logging or assertions to narrow down the problem area.
   - Inspect state at the point of failure (variable values, system state, network responses).
5. **Isolate the bug** — reduce the failing scenario to the smallest possible reproducible case.
6. **Fix the root cause, not the symptom** — a patch that suppresses the error without fixing the underlying cause creates new bugs.
7. **Verify the fix**:
   - Confirm the original bug no longer reproduces.
   - Run the full test suite to ensure no regressions were introduced.
   - Add a regression test that would have caught this bug before the fix.
8. **Document the bug and fix** — record what caused the bug, what was changed, and why, so the team can learn from it.

## Output Format

```
## Root Cause

<Explanation of what caused the bug.>

## Fix

<Description of the change made and why it resolves the root cause.>

## Regression Test

<Test that verifies the bug is fixed and will not regress.>

## Lessons Learned

<Optional: any pattern or practice to adopt or avoid in the future.>
```
