# The SQL knowledge tree — a curriculum artifact

## Purpose

The Part 1 shop catalogue is a **theoretical relational design exercise**. It is not yet the operative backend of anything.

At **P2M1**, the learner starts a *separate* local SQLite knowledge tree. Every class from Part 2 forward contributes notes, topic links, references, and query practice. At **P4M4**, the indexed and curated notes become a **read-only, source-attributed** reference for the Hermes assembly. A fictional product catalogue can coexist in a separate namespace/database or carefully modeled linked area.

## Model, not supplied solution

Describe the fields and relationships in prose, then **write your own** table definitions, queries, and lookup interface. The course starter intentionally does **not** provide executable schema, migrations, or finished search UI before P3M3.

A reasonable conceptual model may include:
- `Topic` with optional parent topic and module identifier
- `Note` with topic, human-authored body, update date and note type
- `Source` with original author/title/link and verification status
- `Cross-link` between distinct notes/topics
- `Evidence` as a *reference/path* to saved labs, not a secret-containing file blob
- `Tag` or keyword for alternative retrieval
- Optional `Catalog concept` from the P1 theoretical design, separate from real commerce records

## Growth schedule

| Milestone | Learner-built capability |
| --- | --- |
| P1 capstone | Design synthetic catalogue keys/relations; demonstrate SQL literacy |
| P2M1 | Create private notes DB and insert a lesson note |
| P2M2 | Add note-to-note links and source provenance |
| P2M3 | Create/explain a useful search index |
| P2M4 | **Build local notes lookup by hand**, no AI code |
| P2M5 | Search/filter, test bad input, confirm parameterization |
| P2M6–M7 | Index lab evidence, demonstrate backup/restore |
| P3 | Add AI-related observations, attack tests and safety decisions |
| P4M2 | Read-only retrieval integration, limited scope |
| P4M4 | Rich, cited SQL knowledge index available to Hermes |

## Data management rules

- Keep the **live SQLite notes database local/private** by default. Do not put it in a hosted public web directory or static-site build.
- The private DB file and backups should be ignored by Git. Version only **schema documentation and deliberately redacted learning exports**, if desired.
- No passwords, tokens, personal data, private host inventories or secret prompts in note bodies, sources, evidence paths or Git commit history.
- Use parameterized inputs; never concatenate user-provided strings into SQL.
- Preserve provenance: a retrieved note is human-authored coursework, not automatically trusted instructions to an agent.
- Hermes integration begins read-only; never permit a retrieved note to become an executable command.

## What the future HTTP / Rootcamp UI can consume

The UI can safely use `data/course.json` and lesson Markdown. The actual SQL notes lookup should remain a **locally served, authenticated** interface if a browser interface is eventually built, with no exposed public database/admin port. Do not wire a static browser UI directly to a local private database file.

## First testing question at every milestone

“Can I retrieve my older notes accurately, show where they came from, and explain which query makes that possible?”
