---
name: docstring
description: Add or update Python docstrings following project conventions. Use when asked to write, add, or fix docstrings.
allowed-tools: Read, Edit, Glob
---

# Docstring Skill

Add or update docstrings for all functions, methods, and classes in the target file(s).

## Rules

1. **Opening newline** — insert a blank line immediately after the opening `"""`:
   ```python
   def foo():
       """
       Do something.
       """
   ```

2. **Verb form** — start the summary with a base verb, not third-person singular:
   - "Return" not "Returns"
   - "Load" not "Loads"
   - "Strip" not "Strips"

3. **Section format** — Google-style only:
   ```python
   """
   Summary line.

   Args:
       param_name: Description.

   Returns:
       Description of the return value.

   Raises:
       ExceptionType: When and why it is raised.
   """
   ```
   - Omit sections that do not apply.
   - For classes, put `Args` in the class docstring, not in `__init__`.

4. **American English** — "normalize" not "normalise", "behavior" not "behaviour", etc.

5. **Do not change** logic, signatures, inline comments, or any non-docstring content.

## Steps

1. Read the target file(s).
2. Identify every function, method, and class missing a docstring or violating the rules above.
3. Add or rewrite each docstring to comply with all four rules.
