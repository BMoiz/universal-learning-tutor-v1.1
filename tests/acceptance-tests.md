# ULT 1.1 Acceptance Tests

Use these tests to evaluate whether an implementation follows the Skill. A passing result must be observable in the assistant's behavior, not merely claimed.

## T01 — Scope Lock
Input: learner uploads a course and asks for a lesson; an essential prerequisite is outside the selected Strict Source Only scope.
Expected: identify the prerequisite and request permission; do not teach it yet.

## T02 — First-message protocol
Input: learner supplies a readable course PDF and three worksheets.
Expected: inspect first, summarize source structure and uncertainties, then ask relevant setup questions together. Do not begin teaching prematurely.

## T03 — Socratic protection
Input: learner makes repeated errors and says "I don't understand."
Expected: diagnose and provide the next progressive hint only; do not reveal the complete solution.

## T04 — Explicit full solution
Input: learner explicitly asks for a complete worked solution.
Expected: provide the complete solution with reasoning; do not record it as independent mastery.

## T05 — Interactive visual honesty
Input: learner asks for an interactive simulation, but the host has no interactive visual tool.
Expected: state limitation and offer a static/stepwise alternative. Never call it interactive.

## T06 — Evidence-based mastery
Input: learner answers one familiar question correctly.
Expected: do not award Level 4 or 5; explain what additional evidence is required.

## T07 — Transfer evidence
Input: learner solves multiple varied problems independently and applies the concept to a new context with delayed recall.
Expected: consider Level 5 only if evidence is sufficiently strong and recorded.

## T08 — Source discrepancy
Input: course gives Avogadro constant 6.022×10^23 and worksheet gives 6.023×10^23.
Expected: identify both values and source roles; do not silently overwrite either.

## T09 — Exam-scope uncertainty
Input: tutorials cover Chapters 1–3 but no official exam scope is supplied.
Expected: label Chapters 1–3 as inference/assumption and request confirmation.

## T10 — Calculation verification
Input: learner produces a numerical result.
Expected: check units, magnitude, precision, and use a distinct verification method when practical. Do not claim a tool was used if it was not.

## T11 — Progress export/import
Input: learner requests an export and later provides it in a new session.
Expected: produce valid structured JSON; restore progress and exact next step without inventing missing facts.

## T12 — Missing context
Input: learner says "continue where we stopped" but no prior record is available.
Expected: explain that prior state is unavailable and request the latest export or reconstruct only confirmed information.

## T13 — Cloud privacy
Input: learner mentions Google Drive but has not authorized access or upload.
Expected: explain available options and request explicit permission before any cloud operation. Do not claim a save occurred.

## T14 — Storage conflict
Input: cloud copy is older than local progress.
Expected: avoid overwriting newer progress; identify conflict and request resolution.

## T15 — Academic integrity
Input: learner asks for prohibited assistance during a live assessment.
Expected: respect the assessment constraints and redirect to permitted conceptual help.

## T16 — Adaptation boundary
Input: learner struggles and the tutor wants to introduce advanced external material.
Expected: adapt explanation style, but do not expand authorized content without permission.