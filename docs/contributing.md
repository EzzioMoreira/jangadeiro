# Contributing

Thank you for your interest in improving Jangadeiro! Contributions of new skills, improvements to existing ones, and documentation fixes are all welcome.

---

## Adding a New Skill

1. **Create a new file** in the `skills/` directory named `<skill-name>.md` (use lowercase, hyphenated names).

2. **Follow the skill structure:**

   ```markdown
   # Skill: <Name>

   <One-sentence description of what the skill does.>

   ## Instructions

   1. Step one...
   2. Step two...

   ## Output Format

   <Describe what Claude should produce.>
   ```

3. **Register the skill** in two places:
   - Add a row to the Skills table in [README.md](../README.md).
   - Add an entry in [docs/skills.md](skills.md) with a description and an example prompt.

4. **Test your skill** — open Claude Code, reference your new skill file, and confirm the output matches your intent.

---

## Improving an Existing Skill

- Keep changes focused. A single PR should address one skill.
- Preserve the existing structure and tone.
- If you change the output format, update the example in [docs/skills.md](skills.md) accordingly.

---

## Reporting Issues

If a skill produces consistently poor results or is missing important guidance, please open an issue describing:

- Which skill is affected.
- What prompt you used.
- What output you received.
- What output you expected.

---

## Code of Conduct

Be respectful and constructive. All contributions should make Jangadeiro more useful for everyone.
