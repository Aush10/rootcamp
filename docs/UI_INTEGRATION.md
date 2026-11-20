# Integrating the learner's HTTP stack and Rootcamp UI

This bundle supplies **content and a stable data index, not a web server or UI application**. The user will bring the existing ready-to-run HTTP server and Rootcamp UI to `Projects\rootcamp`.

## Stable inputs

- `data/course.json`: course → parts → modules → subject pages. Each subject includes a stable ID, path, current content state and whether its overview and assignment are ready.
- `data/subject-backlog.csv`: same subjects as a simple import/lookup list.
- `course/part-X/module-YY/README.md`: module landing Markdown.
- `course/part-X/module-YY/subjects/NN-*.md`: subject pages.
- `course/part-X/module-YY/assessment.md`: open-note module assessment.
- `capstones/part-X.md`: capstone project and completion gate.

Paths in JSON are repository-root-relative POSIX-style strings. The HTML UI should adapt them to its own router at import time. All 150 subject IDs are stable; visible subject names may be edited without changing their IDs.

## Content states

- `backlog`: only a skeleton, *not* a taught lesson.
- `ready`: reading/overview/exercise drafted for the teaching session.
- Future: `studying`, `done`, `revisit`, `verified`.
- Do **not** interpret a lesson marked ready as completed, graded, or source-verified.

## Safety

Public-facing UI may show syllabus, exercises, and sanitized demos. **Do not serve private SQL notes, tokens, actual environment variables, local machine inventory, or private lab reports from a public HTTP root.** Avoid opening network listeners until the Part 1 local-port lesson and review are completed.

## Porting a previous course skeleton

The earlier 'insurance LG course' was not available in this workspace, so its files/styles/routes were not copied. To merge later:
1. Place its templates/theme components in a separate folder.
2. Map its course/module/lesson types onto `data/course.json`.
3. Preserve P#M#S## IDs and assessment/capstone separation.
4. Import Rootcamp Markdown as content, not executable directives.
5. Test that any search/browser code reads only approved public content.

This avoids inventing the unseen source system.
