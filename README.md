# ROOTCAMP — Root to boot

## version 0.4 | Course repository starter | Status: syllabus staged, teaching not yet underway**

Rootcamp is a short, practical path from desktop/network literacy to designing, securing, inspecting, and maintaining AI-operated systems. It is **not** a comprehensive computer science course or a plan to launch an autonomous commercial business.

## Four end-to-end projects

| Part | Capstone | Essential proof |
| --- | --- | --- |
| P1 | Theoretical shop catalogue | Explain relational design and handwritten SQL using synthetic examples; no functioning store |
| P2 | Defended workspace | Safe website + defensive browser extension + Kali lab + learner-built local SQLite class-notes lookup |
| P3 | Controlled-autonomy AI shop | Simulated order flow with explicit approvals, logs, attack tests, rollback, no real spending |
| P4 | Hermes control room | Assembled agent framework + read-only indexed course knowledge + approved tools + private Android-facing UI |

## Course rhythm

**Every subject:** short required reading written by a named human expert; recommended human sources; AI overview; an **ungraded** hands-on assignment; saved notes and evidence.

**Every module:** one **open-note graded assessment**, chosen to fit the learning outcome. It might be a concept defense, build inspection, safe stress test, notes query, or practical demonstration. A safety flaw requires a retest; ordinary misunderstandings become targeted revisit items.

**Every part:** a **working, demonstrated capstone** is required before advancing. In Part 1, 'working' means a reproducible *theoretical schema and query demonstration*, not an operating sales database.

## Where to begin

1. Open [Module 1.1](course/part-1/module-01/README.md).
2. Start with **[P1M1S01 — HTML and CSS: first Hello World](course/part-1/module-01/subjects/01-html-and-css-first-hello-world.md)**.
3. Save your reading notes and learner-authored files separately from the teaching materials.
4. Do the module assessment **only after** the subjects in the module.
5. Use `data/course.json` to connect an imported static Rootcamp UI. No UI or HTTP stack is assumed in this bundle.

## Directory map

- `course/` — 28 modules, 150 subject pages, 28 draft module assessment plans.
- `capstones/` — four final projects and completion gates.
- `docs/` — reading rules, learning/assessment rules, security, SQL notes tree, UI integration, and reviewer setup.
- `data/course.json` — stable module/subject ids and relative Markdown paths for your UI.
- `data/subject-backlog.csv` — lightweight, portable subject queue.
- `.github/copilot-instructions.md` — repo-wide Copilot reviewer directions.
- `AGENTS.md` — Codex-compatible agent instructions.
- `reference/Rootcamp_Study_Backlog_v0.3.md` — full prior Rootcamp specification preserved for reference.
- `templates/` — consistent subject and assessment authoring formats.

**AI coding boundary:** before **P3M3**, an AI may teach, question, and inspect already-written code but may **not** generate code for the student, fix a patch, complete an assignment, or construct the SQL notes lookup. The reading overview is not coding help. From P3M3 onward, AI-generated changes must be reviewed and tested.

## Paths and privacy

The user will create the actual Git repository under `Projects\rootcamp`. This ZIP is a starter to copy into that directory, not a remote commit. Begin as a **private** repository. Do not commit real credentials, personal customer records, private VM inventory, or your private notes database. See [`docs/SQL_NOTE_TREE.md`](docs/SQL_NOTE_TREE.md).

**No deployment, paid accounts, live store connection, or public machine port is required in Part 1.**
