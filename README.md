# Universal Learning Tutor (ULT)

**A universal adaptive learning system with three distinct modes: Corrector, Lesson, and Exam.**

ULT is a reusable, platform-independent Agent Skill for academic subjects and practical skills. It helps learners evaluate their own answers, study a topic or solve exercises independently, and sit realistic practice exams built from authorized course materials.

> **Core principle:** Build the learner's ability to think and work independently—not dependence on ready-made answers.

## The three modes

### 1. Corrector
Give ULT the exact exercise and your answer. It evaluates correctness, reasoning, completeness, method, units, and presentation; identifies and explains errors; and tells you what needs attention.

**It does not reveal the correct answer or full solution unless you explicitly ask.**

### 2. Lesson
Choose one of two separate activities:
- **Explain a lesson/topic:** receive an adaptive, structured explanation.
- **Solve exercises:** work on one complete question at a time. ULT does not split a question into sub-steps unless you ask, the original question contains separate subquestions, or you agree that accessibility requires it.

The two activities are not automatically linked. Solving an exercise does not force a lesson, and a lesson does not force an exercise.

### 3. Exam
ULT designs a formal practice exam using confirmed lesson scope, course exercises, and past-year papers as templates for style and structure. Before generating it, ULT asks which topics are included and confirms duration, difficulty, marks, question types, and permitted tools.

The learner receives an exam-only PDF when the host platform supports real PDF generation. During the active exam, ULT provides no academic explanations, hints, answers, or solving assistance. It waits for the learner's submission. After submission, it grades and provides a detailed review.

## How ULT works

1. **Inspect available context:** read accessible PDFs, documents, images, copied exercises, and relevant prior conversation context before onboarding.
2. **Build an internal learning map:** identify course structure, exercises, source roles, progress, unresolved issues, and next steps. This map is not automatically durable storage.
3. **Choose language and terminology:** use the learner's preferred language while preserving important technical terms from the source and explaining them in a glossary.
4. **Set Scope Lock:** choose Strict Source Only, Necessary Prerequisites, Extended Explanations, or Research and Expansion.
5. **Choose a mode:** Corrector, Lesson, or Exam.
6. **Configure the selected mode:** ask only relevant questions about pace, depth, feedback, time, assessment scope, and other preferences.
7. **Work and record evidence:** adapt to the learner, diagnose mistakes, and track mastery without overstating progress.
8. **Preserve continuity:** use portable progress exports or a real, explicitly authorized storage integration.

## Scope authorization

- **A — Strict Source Only:** use only supplied material.
- **B — Necessary Prerequisites:** introduce only essential prerequisites and label them.
- **C — Extended Explanations:** allow relevant deeper explanations, examples, and methods.
- **D — Research and Expansion:** allow external research and cite sources where possible.

Adaptive teaching never grants permission to expand the content scope. Past exams are templates and historical evidence; they do not prove what is included in the next exam.

## Language and terminology

ULT begins in the language most used by the learner in accessible context, then asks for the preferred learning language. It can preserve technical terminology in the original language of the course while explaining it in the learner's chosen language. A glossary can record the source term, translation, explanation, and context. Language quality depends on the host AI model.

## Progress saving and privacy

ULT builds an internal working map but does not claim that this is permanently saved. Durable storage requires an actual supported location and the learner's explicit permission.

- Local saving is preferred when the platform can genuinely access it.
- If local writing is unavailable, ULT should suggest a downloadable JSON/Markdown export that the learner can keep on their device.
- Cloud storage is optional and requires explicit authorization.
- Progress records should be timestamped and separated by subject, course, and academic year. New records should not silently overwrite older progress.
- Original course files are not copied to storage unless separately authorized.

## Core capabilities

- Adaptive teaching and learner-preference setup.
- Corrector mode with answer evaluation and protected solutions.
- Lesson mode with separate lesson explanation and exercise-solving activities.
- One complete exercise question at a time by default.
- Exam mode with confirmed scope, blueprint, exam-only PDF, protected sitting, and post-exam grading.
- Scope Lock and source hierarchy.
- Socratic hints and solution protection outside active exams.
- Mistake diagnosis and calculation verification.
- Interactive-first visuals when the host supports them.
- Evidence-based mastery levels 0–5.
- Bilingual technical glossary.
- Portable progress export/import and optional authorized storage.
- Explicit uncertainty and assumption tracking.

## Supported subjects and skills

ULT is domain-independent and can support mathematics, physics, chemistry, biology, engineering, technology, programming, computer science, data, languages, writing, communication, medicine and professional study, humanities, social sciences, and practical skills. Quality depends on the reliability of supplied sources and the host model.

## Platform compatibility and limitations

ULT is an instruction Skill, not a standalone application or AI model. Capabilities depend on the host platform:
- Reading previous conversation history and earlier attachments is possible only when the host exposes them.
- Local storage requires real local file access; otherwise use manual export/download.
- Cloud storage requires an actual integration and explicit permission.
- A downloadable PDF requires a real file-generation capability.
- Interactive diagrams require an actual interactive renderer/tool.
- Web research requires browsing and authorization under the selected scope.

ULT must state limitations honestly and never claim unavailable actions succeeded.

## Repository structure

- `SKILL.md` — primary operating instructions.
- `references/` — detailed mode, onboarding, integrity, visuals, calculation, mastery, and storage guides.
- `templates/progress.schema.json` — progress-record schema.
- `templates/progress.example.json` — example record.
- `templates/session-summary.md` — session close template.
- `tests/acceptance-tests.md` — behavioral acceptance tests.

## Version

**ULT 1.2** — introduces three distinct modes (Corrector, Lesson, Exam), a structured onboarding sequence, language-aware technical terminology, internal learning-map handling, and local-first consent-based progress storage.

## License

No license has been added. Until a license is selected and committed, standard copyright applies and reuse/redistribution permissions are not explicitly granted.
