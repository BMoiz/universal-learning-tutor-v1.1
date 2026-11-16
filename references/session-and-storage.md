# Progress Record, Persistence, and Session Continuity

## Required progress fields
Project identity; objective/deadline; learning configuration; authorized scope; source registry and source roles; topic map; completion state; mastery level and evidence; mistake profile; revision plan; next actions; session state; assumptions; unknowns; source conflicts.

## Formats
- JSON is canonical for restoration.
- Markdown is readable and portable.
- PDF is optional when supported.

Use templates/progress.schema.json and templates/progress.example.json.

## Export
Offer/export after meaningful sessions, topic completion, before context limits, before platform/model changes, or on request. Do not claim permanent persistence unless a real save operation succeeds.

## Import
Validate; identify project/version; restore scope and configuration; restore progress, evidence, errors, and session state; flag stale/missing/conflicting data; ask only essential questions; resume from the last meaningful step. Never invent missing progress.

## Cloud storage
Provider-independent: Google Drive, Dropbox, OneDrive, or other actually supported providers. Cloud storage is optional. Obtain explicit permission before connecting, reading, uploading, or modifying. Do not request credentials in chat. Do not upload course sources without authorization. Avoid overwriting newer versions; detect conflicts; ask before ambiguous resolution; confirm only after provider success. Manual export/import always remains available.

Suggested layout:
ULT/Learning_Projects/<Project_Name>/
  Sources/
  Progress/progress.json
  Progress/progress.md
  Exercises/
  Assessments/
  Revision/

## Session recovery
At session end summarize studied content, independent evidence, mistakes, mastery changes, unfinished work, and exact next step. At session start inspect available progress records. If previous context is unavailable, say so and restore only from available files or confirmed information.