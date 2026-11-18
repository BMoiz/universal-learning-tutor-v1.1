# Changelog

All notable changes to the Universal Learning Tutor (ULT) are documented here.

## [1.2] - 2026-11-18

### Added
- Three distinct operating modes: **Corrector**, **Lesson**, and **Exam**.
- Corrector workflow for evaluating an exact exercise and learner answer while withholding the correct solution unless requested.
- Lesson mode with two independent activities: lesson explanation and exercise solving.
- Exam workflow with learner-confirmed scope, exam-session restrictions, and post-submission grading.
- Language preference onboarding and preservation of original-language technical terminology with a glossary.
- Local-first, consent-based progress workflow with portable JSON/Markdown export/import.
- Timestamped progress records separated by subject, course, and academic year.
- Issue tracking for the historical 1.1 gaps and 1.2 verification work.

### Changed
- Exercise solving now uses one complete question at a time by default; splitting is reserved for learner request, independent subquestions in the source, or agreed accessibility adaptation.
- Exam scope must be confirmed by the learner. Tutorials and past papers are not treated as proof of current exam scope.
- Session recovery instructs the tutor to inspect all accessible conversation history and earlier attachments, while disclosing anything the host does not expose.
- Source hierarchy, contradiction handling, uncertainty tracking, and calculation verification have been strengthened.
- Visual learning is interactive-first only when a genuine supported renderer exists; otherwise the tutor must state the limitation and provide an honest fallback.
- Mastery claims require evidence and must not be inferred from passive reading or one isolated correct answer.
- Durable storage, PDF generation, cloud access, and interactive visuals are explicitly host-capability dependent; the tutor must not claim unsupported actions succeeded.

### Historical 1.1 issues tracked
The following issues record weaknesses identified during the 1.1 review. They remain open because the 1.2 instruction changes have not yet been validated through live behavioral tests:

- [#1 — Interactive visual learning](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/1)
- [#2 — Evidence-based mastery](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/2)
- [#3 — Socratic solution protection](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/3)
- [#4 — Portable progress transfer](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/4)
- [#5 — Explicit exam scope](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/5)
- [#6 — Source hierarchy and conflicts](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/6)
- [#7 — Independent calculation verification](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/7)
- [#8 — Session recovery and context access](https://github.com/BMoiz/universal-learning-tutor-v1.1/issues/8)

### Verification status
- The repository's acceptance-test document contains 28 tests.
- The progress JSON schema and example were syntax-checked after correction.
- **No live behavioral test on Claude or another host has been recorded yet.**
- Therefore, the items above are documented as specification-level changes, not as fully runtime-verified fixes.

### Not changed / still limited
- ULT remains an instruction-based Agent Skill, not a standalone application or model.
- Local file writing, persistent storage, cloud integrations, PDF creation, interactive rendering, and browsing depend on actual host capabilities and permissions.
- The repository is still named `universal-learning-tutor-v1.1`; the skill/documentation version is 1.2. The repository name has not been changed.
- No license has been added; standard copyright applies.

## [1.1] - Previous version

ULT 1.1 introduced the adaptive tutoring framework, Scope Lock, Socratic guidance, visual-learning intent, mastery tracking, session continuity, and progress templates. The issues linked above document weaknesses identified during its review.
