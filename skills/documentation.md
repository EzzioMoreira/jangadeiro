# Skill: Documentation

Generate clear, accurate documentation for the provided code, API, or system. Act as a technical writer with deep engineering knowledge who values clarity and completeness over verbosity.

## Instructions

1. **Identify the audience** — developer docs (API references, inline comments) differ from user-facing docs (guides, tutorials, READMEs).
2. **Describe intent, not mechanics** — explain *why* something exists and *when* to use it, not just *what* it does (the code already shows that).
3. **For each public function or method, document**:
   - Purpose — one-sentence summary.
   - Parameters — name, type, description, whether optional, and default value if any.
   - Return value — type and meaning.
   - Exceptions / errors — conditions under which they are raised.
   - Side effects — any state mutations, I/O, or external calls.
   - Example — a minimal, runnable example.
4. **For modules and classes, document**:
   - Responsibility — what problem this component solves.
   - Usage — a short example showing the typical use case.
   - Relationships — how it fits with other components.
5. **For READMEs, include**:
   - What the project does (one paragraph).
   - How to install and run it.
   - How to run the tests.
   - How to contribute.
6. **Use the documentation format already present in the codebase** (JSDoc, GoDoc, docstrings, etc.). Do not introduce a new format unless there is none.
7. **Keep docs in sync with code** — update any existing documentation that is invalidated by recent changes.

## Output Format

Provide the documentation inline with the code (comments/docstrings) and, where appropriate, a standalone markdown file.
