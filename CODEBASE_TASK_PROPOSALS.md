# Codebase Task Proposals

## 1) Typo fix task
**Issue found:** The project tagline in `README.md` is grammatically incorrect: "Jacob Get Help From The Brave Mascots".

**Proposed task:** Update the sentence to "Jacob Gets Help from the Brave Mascots" (fixes subject-verb agreement and normalizes title casing).

**Why this matters:** This is the first text users see, and typos reduce project credibility.

---

## 2) Bug fix task
**Issue found:** The `.gitignore` appears tailored to an old Flash/AIR stack (`*.swf`, `*.air`, `*.ipa`, `*.apk`, `bin-debug/`), but does not ignore common modern tooling artifacts (e.g., `.env`, `node_modules/`, `.venv/`, coverage outputs).

**Proposed task:** Replace or extend `.gitignore` with language/tool-specific patterns that match the actual stack used by this repository.

**Why this matters:** Missing ignore rules can cause accidental commits of secrets or large generated artifacts, which is a practical repository hygiene bug.

---

## 3) Comment/documentation discrepancy task
**Issue found:** The README only contains a name and one tagline, while `.gitignore` comments reference Eclipse/Flash Builder compiler settings. The docs do not describe that technology choice, and likely no longer reflect the intended project setup.

**Proposed task:** Reconcile documentation by adding a "Project Overview" section in `README.md` that states the current stack and removing/updating stale `.gitignore` comments tied to Flash Builder.

**Why this matters:** Inconsistent docs/comments mislead contributors and create setup mistakes.

---

## 4) Test improvement task
**Issue found:** No test suite or verification instructions are present in the repository.

**Proposed task:** Add at least one baseline CI check (e.g., lint + smoke test), and document how to run it locally in `README.md`.

**Why this matters:** Even minimal automated checks prevent regressions and create a foundation for future development.
