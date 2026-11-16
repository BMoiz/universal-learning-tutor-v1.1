# Universal Learning Tutor (ULT)

**An adaptive, Socratic AI tutor for learning any academic subject or practical skill.**

ULT is a reusable, platform-independent Agent Skill. It turns a general-purpose AI assistant into a structured personal tutor that helps learners understand concepts, practise independently, diagnose mistakes, prepare for exams, and carry learning progress between sessions.

> **Core principle:** Teach learners how to think, not just what to answer.

## How ULT works

ULT follows a controlled learning cycle:

1. **Understand the learner** — establish the subject, goal, current level, deadline, preferred language, available study time, and constraints.
2. **Inspect learning materials** — examine uploaded textbooks, lecture notes, slides, worksheets, images, and exercises before teaching.
3. **Set the learning boundary** — ask what content may be used. ULT does not silently introduce material outside the learner's authorized scope.
4. **Build a learning map** — connect topics, prerequisites, exercises, objectives, and source documents; flag uncertainty and conflicting information.
5. **Teach adaptively** — adjust explanation depth, pace, examples, difficulty, and teaching strategy to observed performance.
6. **Guide practice** — use Socratic questions and progressive hints instead of immediately revealing complete solutions.
7. **Diagnose mistakes** — identify whether an error is conceptual, mathematical, procedural, algebraic, or caused by units, notation, or assumptions.
8. **Verify understanding** — assess mastery using independent evidence, varied problems, and transfer—not a single correct answer.
9. **Review and continue** — use active recall, spaced revision, exam simulations, and portable progress records.

## Main capabilities

- **Adaptive tutor:** changes pace, depth, examples, and difficulty as the learner progresses.
- **Socratic guidance:** provides one progressive hint at a time and protects the learner's opportunity to reason.
- **Scope Lock:** works within supplied materials unless the learner authorizes prerequisites, extensions, or external research.
- **Complete lessons:** structured explanations, definitions, formulas, examples, misconceptions, and understanding checks.
- **Visual learning:** prefers genuine interactive diagrams or simulations when the host platform supports them; otherwise clearly labels static alternatives.
- **Exercise analysis:** identifies known data, unknowns, concepts, conditions, units, and the next reasoning step.
- **Mistake diagnosis:** classifies errors and tracks recurring patterns without overgeneralizing from one mistake.
- **Evidence-based mastery:** tracks progress from Level 0 to Level 5 using demonstrated performance.
- **Exam preparation:** supports configurable practice tests, timed simulations, grading, and post-exam analysis.
- **Calculation verification:** checks units, precision, plausibility, dimensions, and independent methods where practical.
- **Learning continuity:** exports and imports progress using portable JSON and Markdown templates.
- **Source integrity:** distinguishes source statements from explanations, assumptions, derivations, and external research.

## How to use it

### Option 1 — Use as an Agent Skill
1. Download the repository or the packaged Skill release.
2. Keep SKILL.md at the root of the Skill folder.
3. Include the references/ and templates/ folders alongside it.
4. Import or upload the Skill using an AI platform that supports Agent Skills/custom skills.
5. Enable the Skill in that platform and start a learning conversation.

The exact import process depends on the AI platform and its current Skill support.

### Option 2 — Use the instructions manually
Open SKILL.md, copy its instructions into an AI assistant's custom instructions or a new conversation, and provide the learning material you want to study. This works as a manual fallback, but platform features such as file handling and persistence may differ.

### Suggested first message
> Act as my Universal Learning Tutor. I want to study [subject] for [goal/deadline]. My current level is [level]. I will provide my course materials. Inspect them first, then ask me the necessary setup questions. Do not start teaching until we agree on the authorized scope.

### Scope authorization levels
- **A — Strict Source Only:** use only the materials supplied by the learner.
- **B — Necessary Prerequisites:** allow only prerequisites essential to understand the supplied material.
- **C — Extended Explanations:** allow relevant deeper explanations and supplementary examples.
- **D — Research and Expansion:** allow external research and broader learning.

ULT's adaptive teaching does not grant permission to expand the content scope.

## Supported subjects and skills

ULT is designed to be domain-independent. It can support academic and practical learning such as:
- Mathematics, physics, chemistry, and biology.
- Engineering, technology, and applied sciences.
- Programming, computer science, and data-related topics.
- Languages, writing, and communication.
- Medicine and other professional or technical study.
- Humanities, social sciences, and general knowledge.
- Practical skills and structured self-learning.

Quality depends on the clarity and reliability of the supplied material and the capabilities of the AI model being used. ULT does not replace qualified professional instruction or advice in high-stakes fields.

## Languages

ULT does not impose a fixed language list. The learner can request a teaching language, and the tutor should respond in that language when the underlying AI model supports it. It can also be asked to explain in one language while preserving technical terms in another, or to provide bilingual terminology.

Language quality, dialect accuracy, speech support, and document extraction depend on the selected AI model and host platform. No claim is made that every language or dialect has been equally tested.

## Platform compatibility and limitations

ULT is written as a platform-independent instruction Skill, not a standalone application or AI model. It can be adapted to AI assistants that accept custom instructions or support Agent Skills. Actual capabilities depend on the host:
- File reading depends on the platform's supported file types and upload limits.
- Interactive visuals require a real interactive tool or renderer.
- Web research requires an available browsing/search capability and appropriate authorization.
- Cross-session continuity requires exported progress files or a real connected storage integration.
- Cloud storage is **not built in**; it must be provided by a supported integration and explicitly authorized by the learner.

ULT must never pretend that an unavailable tool was used or that progress was saved when no save operation succeeded.

## Repository structure

- SKILL.md — main Agent Skill instructions and operating rules.
- references/ — focused guides for tutoring, visuals, source integrity, calculations, mastery, and continuity.
- templates/progress.schema.json — JSON Schema for validating learning progress records.
- templates/progress.example.json — example portable progress record.
- templates/session-summary.md — reusable end-of-session summary.
- tests/acceptance-tests.md — behavioral acceptance tests for evaluating an implementation.

## Version

**ULT 1.1** — includes strict scope control, interactive-first visual guidance, stronger Socratic protection, evidence-based mastery, source/uncertainty tracking, calculation verification, and portable session continuity.

## License

No license has been added yet. Until a license is selected and committed, standard copyright applies and reuse/redistribution permissions are not explicitly granted.
