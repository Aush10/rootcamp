# ROOTCAMP
## Root to Boot — Study Backlog & Competency Rubric v0.3

**Revision date:** 2026-11-19  
**Status:** Designed, not yet taught or assessed  
**Course shape:** Four parts; seven modules per part; one cumulative capstone at the end of each part  
**Original intent:** A high-speed, outcome-directed technical crash course, *not* a computer science degree or exhaustive cybersecurity qualification  
**Operating motto:** *You don't need to know everything AI can do. You need to know what it cannot reliably do—and be able to understand, secure, test, repair, and push the systems around it.*

> **North star:** Build the practical human skills required to inspect and maintain increasingly automated systems: files, scripts, networks, hosting, credentials, databases, tools, applications, agents, and the boundary between machine autonomy and human responsibility.

### Design decisions in this revision

1. **JavaScript, Node.js, Java, and Kubernetes** stay in Part 1, after Git and before Python. Kubernetes remains an orientation, not cluster administration.
2. **Security begins immediately** with file permissions, backups, local-only ports, and safe system navigation. Part 1 cloud CLI remains guided, read-only, and payment-free.
3. **Part 1 capstone is only a theoretical shop catalogue.** Demonstrate SQL/database literacy through an original schema, relationships, sample records, joins, indexes, and a model of order flow. It is **not** a working shop, service, transactional backend, or production database.
4. **Starting in Part 2, a personal SQL class-notes tree becomes a compulsory learning artifact.** Every module adds structured notes, questions, evidence, and cross-references to a local SQLite database. The student writes a small lookup interface from scratch and expands it throughout the course.
5. **No AI-generated code or AI coding-agent assistance through Parts 1–2 and Part 3 Modules 3.1–3.2.** Part 3 Module 3.3 is the first AI coding workshop. AI may be discussed as a subject earlier, but must not write, edit, or repair the student's code. This is a deliberate *functional-competence gate*, not an anti-AI rule.
6. **Part 2 produces a defended online workspace, browser security suite, Kali lab, and independently written notes lookup.** The web storefront remains a facade; there is no autonomous AI.
7. **Part 3 teaches AI as a historical engineering trend**, then focuses on credential security, prompt/code injection, packages, containers, network permissions, approvals, and bounded agents before any storefront integration.
8. **The AI shop remains a security demonstrator**, not a promised profit engine. Order/payment/fulfillment actions are simulated first and require human authorization for real-world use.
9. **Part 4 is an assembly exercise.** Hermes is chosen because the learner must build and wire together the agent's components, not because it is categorically better than Copilot, Codex, Grok, or other assistants. Verify the exact Hermes project and its interface at teaching time.
10. **By Part 4 Module 4.4**, the growing SQL knowledge tree must provide an extensive, well-indexed, permission-limited lookup for Hermes and include the sample shop catalogue as a distinct data domain.
11. **The course stays short and utilitarian.** Record rabbit holes without making them prerequisites. Do not sacrifice required safety checks or reproducibility to meet a time box.

---

## 0. How Rootcamp teaches

**The Rootcamp loop: See → Do → Break safely → Fix → Explain → Save.**

**Human-first coding contract:** From 1.1 through 3.2, the learner must author all source code, SQL, scripts, database migrations, and lookup-interface logic personally. Handbooks, documentation, conceptual explanations, and pre-written worked examples may be studied, but AI must not generate or repair submitted code. At **3.3**, AI coding assistance becomes an explicit subject: compare, review, and test it against the human-written baseline. If the learner cannot explain a line or reproduce the core function without an agent, it does not count as proven competence.

**Persistent class-notes contract:** From 2.1 onward, each module inserts at least one structured note and one queryable cross-reference in the local SQLite notebook. This notebook is simultaneously the class record, indexing practice, and later the Hermes retrieval corpus. Secrets, authentication tokens, personal customer data, and private keys never belong in it.

- **See:** Follow one small, carefully scoped, safe example.
- **Do:** Recreate it without copying blindly.
- **Break safely:** Trigger an intentional failure in a local, reversible lab—not in a live service or someone else's system.
- **Fix:** Identify cause, test the repair, and roll back if necessary.
- **Explain:** State what happened in plain language and where AI could get it wrong.
- **Save:** Commit the result, test output, and recovery notes to the lab notebook.

**Hard time boxes:** Favor the stated hours. At time limit, park optional questions in the **Rabbit-Hole Register** instead of abandoning the next dependency. A failed *mandatory safety gate* is not a rabbit hole; it must be repaired before moving into deployment or autonomy.

**Study output:** A portable repository `rootcamp/` with `part-1/` to `part-4/`, `labs/`, `capstones/`, `glossary/`, `security/`, `references/`, and `rabbit-holes.md`; also a local `rootcamp_notes.sqlite` (backed up safely, never auto-published). Keep secrets, private data, local config, and heavyweight VM images out of Git. If database backups are tracked, use a sanitized, small, deliberately exportable copy.

### Module assessment rubric — 100 points

| Dimension | Points | What earns it |
|---|---:|---|
| **Make it work** | 35 | Run the expected command, demo the workflow, and produce the artifact |
| **Understand it** | 20 | Explain inputs, outputs, dependencies, and common failure modes in your own words |
| **Secure it** | 30 | Identify trust boundary, apply relevant permissions/secrets/validation controls, and show at least one negative test |
| **Repair and reproduce it** | 15 | Save setup steps, a test/log, and a rollback, restore, or troubleshooting path |

**Normal pass:** 70/100 and a working artifact. **Security-critical pass:** all applicable mandatory controls below must be demonstrated; numerical scores cannot compensate for an unaddressed high-risk flaw. A failed security gate pauses *exposure or agent permissions*, not the rest of the theoretical learning.

**Additional non-negotiable gates:** In Parts 1–2, code submitted as personal work must be demonstrably human-authored. From Part 2 onward, the student must be able to insert, search, update, link, and back up class notes using their own SQL and lookup code. Passing Part 3.3 requires showing where agent-generated code differs from—and may compromise—the learner's baseline.

### Mandatory safety gates

- **Gate A — Before sharing or exposing a service (Part 1 → Part 2):** Know exactly which process runs, which files it reads, what address/port it binds to, what data it holds, and how to stop it; have a tested backup; do not expose an administrative service to the public internet. The Part 1 catalogue is only a schema exercise and must not be presented as a functioning store database.
- **Gate B — Before publishing the Part 2 website:** HTTPS and correct domain, no exposed credentials, no public database/admin ports, minimal extension permissions, explicit sharing settings, dependency review, logs, and rollback instructions. Prove the SQLite class-notes database remains private and the handmade lookup can run locally without AI or hosted accounts.
- **Gate C — Before any Part 3 AI can operate within the storefront:** Document the trust boundaries; test prompt injection and malicious input; use least-privilege tool/API scopes, controlled network egress, secret isolation, input/output validation, audit logs, spending caps, and human approvals. Passing static code tests alone is insufficient.
- **Gate D — Before Hermes gains real tool or remote capabilities (Part 4):** Individually approve every integration; use read-only first, identity-based access, revocable tokens, restrictive network rules, bounded context/memory, monitoring and recovery. Verify the SQL index has provenance and clean retrieval boundaries; do not expose a raw shell, desktop session, model admin endpoint, or VM to the public internet.

**Human authority rule:** AI may analyze, draft, recommend, and run reversible sandbox tests. It may not independently authorize a real purchase, refund, advertisement spend, credential change, account permission change, or release to production. Any later exception requires a separately designed and documented approval policy; the course does not assume one.

---

# PART 1 — Roots: Files, Code, Local Tools, and a Theoretical SQL Catalogue

**Goal:** Learn enough Windows/Linux, Office/Workspace, shells, code, source control, containers, and database fundamentals to construct a reproducible *local* project. The capstone is a **conceptual database design**, not a deployable storefront or shop backend.

**Core hours:** Approx. **56–70 hours**, plus **4–8 hours for the capstone** (planning estimates, not guarantees).

## 1.1 — Hello World: Desktop, Web, SQL, and Common Tools
**Time:** 6–8 hours

**Learn:** CSS and the smallest HTML page; SQLite basics; Microsoft 365 apps and Google Workspace; Kiwi Browser and browser settings; Hello World in the browser; what an HTTPS handshake and a certificate/thumbprint (fingerprint) mean.

**Do:** Make a one-page `rootcamp-hello` site and a tiny SQLite table. Open each in an appropriate tool. Identify a certificate fingerprint *without* treating it as a password or trusting a screenshot of it.

**Secure:** Identify the difference between trusted software/downloads and unknown extensions; distinguish application files from operating-system files.

**Evidence:** Screenshot, source file, SQL query result, and a five-sentence explanation of HTTPS.

**Do not deep-dive:** CSS layouts, relational theory, or TLS internals beyond the first useful mental model.

## 1.2 — Office Automation, File Explorer, and Storage Safety
**Time:** 6–8 hours

**Learn:** Macros in Excel (VBA or Office Scripts) and Google Sheets (Apps Script); XML as a data format; HTTPS boilerplates; Windows File Explorer, hidden extensions, file types, Windows tools, system directories, OneDrive/Microsoft cloud and sharing settings; introductory Linux paths (`/home`, `/etc`, `/var`, `/usr`) and permissions.

**Do:** Automate one spreadsheet action, export a sample XML document, create a project folder, make a read-only cloud share with test content, and then revoke it.

**Secure:** Show how to recognize dangerous file extensions and unexpected macros; do **not** modify Windows system folders or Linux system configuration as a learning shortcut; demonstrate backup and restore of a small sample folder.

**Evidence:** Macro/script, sample file tree, redacted permission screenshots, backup/restore checklist.

**Correction:** XML is markup/data; the macro code is in a scripting language.

## 1.3 — Command Shells, Bash, Git, and GitHub
**Time:** 10–12 hours

**Learn:** Command Prompt, PowerShell, Bash, Git Bash; current directory, path, environment variable, standard output/error, exit status; Windows vs Linux directory conventions; VS Code; Git add/commit/branch/merge, GitHub repositories, `.gitignore`, README and basic Git recovery.

**Do:** Set up `rootcamp/`; run safe navigation commands in Windows and Linux; use Git from the CLI; create a branch, merge it and undo a harmless test change.

**Secure:** Understand user vs administrator/root; inspect permissions and identify a secret before it is accidentally committed. Never run unexplained internet-sourced shell commands with elevated privileges.

**Evidence:** Repo history, annotated terminal screenshots, `.gitignore`, one recovery example.

## 1.4 — Languages and Build Boxes: JavaScript, Node, Java, Kubernetes
**Time:** **10–14 hours** (expanded, deliberately)

**Learn in this exact order:**
1. **JavaScript** in the browser: values, functions, DOM and one button action.
2. **Node.js**: JavaScript outside the browser, packages/npm, scripts and a minimal HTTP server.
3. **Java**: JVM/JDK/JRE, source versus bytecode, Hello World, VS Code Java setup; Java across Windows/macOS/Linux; Java 7 as historical context, *not* a recommended modern runtime.
4. **Build tooling**: what `npm`, `pip`, and later Gradle do—and why they differ.
5. **Containers and orchestration concepts**: what an image, container, pod, service and Kubernetes cluster are; learn the vocabulary and diagram how Kubernetes differs from Docker. A local simulator/demo is **optional**.
6. **The box**: localhost, a local sandbox, port binding, VS Code remote/container connections, GitHub Codespaces and prebuild environments as concepts. No requirement to create a billable hosted workspace.

**Do:** Run JavaScript in a page; start a **localhost-only** Node server; compile/run Java; document a simple reproducible workspace; diagram one service as local process → container → Kubernetes pod/service (conceptual).

**Secure:** Follow the **Part 1 Safe Local Port Lab** at the end of this file. Never open a router port or a cloud inbound rule in Part 1.

**Evidence:** Three Hello Worlds, Node server source, local connection verification, stopped-process screenshot and architecture sketch.

**Why time expands:** JavaScript/Node and Java are genuinely separate concepts; Kubernetes earns an orientation, not an operational certification.

## 1.5 — Python Basics
**Time:** 8 hours

**Learn:** Running a `.py` file, variables, functions, collections, files, errors, imports, virtual environments, `pip`, basic SQLite access and parameterized SQL.

**Do:** Write a small Python script that creates, queries, and prints *fictional catalogue sample rows* in a disposable SQLite database. This is a database-literacy exercise, not a storefront application. Test one invalid input.

**Secure:** Never build SQL by concatenating user input; keep configuration and secret placeholders outside source control.

**Evidence:** `catalog_cli.py`, local DB, sample output and one negative test.

## 1.6 — Jupyter, Docker, and Repeatable Local Packaging
**Time:** 6–8 hours

**Learn:** Jupyter notebooks, kernels, `.ipynb` versus reusable `.py`, Docker images/containers, ports, volumes, environment variables, image provenance and logs.

**Do:** Explore sample catalog data in a notebook; run a Python service in a locally isolated container; stop, remove and rebuild it.

**Secure:** Bind only to localhost when publishing a test port; do not mount sensitive home folders or the Docker socket into an untrusted container; verify package/image sources.

**Evidence:** Notebook, Dockerfile, build/run/log/cleanup commands, test result.

## 1.7 — Cloud CLI and Cloud Studio: Guided Tour Only
**Time:** 10–12 hours, including practice and recap

**Learn:** What cloud CLIs, hosted shells, projects, regions, IAM roles, service accounts, credentials, storage, logging, APIs and cloud workspaces are used for. Compare local CLI help and **read-only sample output** from documentation; introduce provider studios and cloud development environments without requiring live provisioning.

**Do:** Install a CLI only if useful; demonstrate offline `--help`/version/config inspection and interpret fictional resource listings. Sketch a cloud deployment and its cost/security questions on paper.

**Secure:** **No paid resources, no mandatory credit card, no public ports, no real API keys, no cloud deployment, no elevated roles** as course requirements. If authentication is offered as optional later, it is separated from this introductory tour.

**Evidence:** Command glossary, provider-neutral architecture sketch, cost/permission decision checklist.

### CAPSTONE 1 — Theoretical Shop Catalogue: Prove SQL Literacy

**Design, don't operate:** Produce a paper/Markdown ERD and a SQLite-compatible schema for a *hypothetical* print-on-demand shop. The objective is to explain relational structure, not to make a functioning storefront or database-backed sales service. A tiny **disposable** SQL sample is allowed to demonstrate comprehension; it never becomes a live operational backend.

**Minimum conceptual entities:** `designs`, `products`, `suppliers`, `listings`, `mock_orders`, `order_items`, `fulfillment_events`, `audit_events`. Distinguish primary key, foreign key, one-to-many, many-to-many, optional relationships, unique constraints, nullability, and status/state history. Use cents for hypothetical prices and fake identifiers/addresses.

**Mandatory passes (human-written SQL; no AI coding):**
- Draw and narrate a relational diagram. Explain why products, designs, suppliers and listings should not be forced into a single table.
- Write `CREATE TABLE` definitions and illustrative `INSERT`, `SELECT`, `JOIN`, `UPDATE`, and `CREATE INDEX` statements on a small synthetic dataset.
- Show at least one query that retrieves a product with its linked design and proposed supplier, and explain a query plan/index in ordinary language.
- Deliberately test a duplicate/invalid key or forbidden relationship, then explain which constraint stops it.
- Demonstrate a backup/restore of a **throwaway** SQLite file (no real customer data, credentials, or unreleased artwork).
- Sketch the hypothetical chain `listing → simulated order → approval → printer → shipping → audit` without implementing integrations or transactions.

**Output:** `capstones/theoretical-catalogue/` containing the learner-authored ERD, `catalog_model.sql`, `sample_queries.sql`, synthetic sample rows, a plain-language explanation, and literacy/restore evidence.

**Transition to Part 2:** Keep the catalogue as a *reference model*. Start a **separate personal class-notes SQLite knowledge tree** in 2.1. The catalogue can later be implemented and indexed alongside it, but do not substitute an e-commerce app for the class-notes objective.

**Gate A:** Complete the local-port and storage checklist before Part 2's hosting work.

---

# PART 2 — Networks, Security Lab, and a Storefront-Shaped Workspace

**Goal:** Learn what an online application and its protective infrastructure are made of; create a defended, auditable surface without putting an AI agent in control.

**Core hours:** Modules 2.1–2.6 have roughly **36–45+ hours** specified; capstone 2.7 remains **as long as needed**. The “+” reflects 2.4 being a minimum. SQL note entry/lookup is **embedded** in these modules, not another semester of database theory.

### The growing SQL class-notes tree (begins at 2.1)

**Design intent:** SQL is now the **notation and storage format for coursework**, not just a topic to study. The student builds a queryable, linked record of what was learned; every class contributes to a growing knowledge tree that Hermes will eventually consult. A 'tree' here means relational records linked by `parent_topic_id`, not a special type of SQL database.

**Lean starter schema (SQLite, typed by the learner):**
- `topics(topic_id, parent_topic_id, module_code, title)` — parent/child hierarchy by part, module, concept.
- `notes(note_id, topic_id, title, body, note_kind, authored_at, updated_at)` — written study notes, definitions and troubleshooting entries.
- `links(from_note_id, to_note_id, relationship)` — cross-topic references; the knowledge graph may have more than one relationship per note.
- `evidence(evidence_id, note_id, file_path, result, recorded_at)` — pointers to local lab screenshots/commands/tests rather than embedding sensitive binaries.
- `sources(source_id, note_id, citation, source_location, checked_at)` — provenance and references.
- `tags(note_id, tag)` — simple alternative lookups.

**Manual progression:** 2.1 create DB and enter a note → 2.2 create relational links → 2.3 add and explain indexes → 2.4 build a local lookup UI/CLI → 2.5 search, filter, and test bad input → 2.6 connect VM/security evidence safely → 2.7 demonstrate search, backup, and restore without AI. Begin with `SELECT ... WHERE` and parameterized queries, then add SQLite FTS5 later if available/needed. Never paste API keys, tokens, passwords, personal customer data, or private machine inventory into notes.

**Interface:** An entirely human-written, **local-only** command-line search program is sufficient at first. A simple HTML/browser frontend is optional. It must let the student search by term, module, tag, and ID; display a note's source and linked notes; and open related evidence by a safe file path or reference. No AI autocomplete, code generation, or autonomous editing before 3.3. This is a demonstration of competence, not a test of graphical polish.

**Growth rule:** In each module, add at least **one note, one cross-link, and one verified query** to `rootcamp_notes.sqlite`. Preserve a migration/schema history, use backups, and record errors/fixes. In Part 3 add security cases and AI concepts; in Part 4 build the catalog and Hermes-oriented index as distinct related domains.

## 2.1 — Routing and Physical/Logical Networks
**Time:** 2–5 hours

**Learn:** LAN, WAN, MAC, IP, DNS, DHCP, NAT, gateway, router, switches, Wi-Fi, DSL and the path between client and server. Clarify original terms "routaments" and "MAC1" in the glossary.

**Do:** Draw the *logical* home/lab path from browser → router → DNS → server; find your own machine's local network configuration. **SQL notebook 2.1:** Independently create `rootcamp_notes.sqlite`, define starter tables, insert the first network note, and retrieve it by ID.

**Secure:** Keep the diagram private; redact public IPs and equipment identifiers from published notes.

## 2.2 — Handshakes, Standards, and Trust
**Time:** Up to 8 hours

**Learn:** HTTP/HTTPS, TCP/IP, TLS, DNS, SSH, certificates, authentication versus authorization, trust chains, protocol versioning, web security history and standards bodies.

**Do:** Trace a benign HTTPS visit through DNS, TCP/transport establishment, TLS validation and request/response. **SQL notebook 2.2:** Add handshake, TLS and certificate notes and a cross-link; demonstrate a `JOIN` that displays linked concepts.

**Secure:** Recognize certificate errors, mixed content and why "encrypted" does not mean "authorized."

## 2.3 — Contemporary Networks and Protected Access
**Time:** 6–8 hours

**Learn:** 5G, developing 6G ideas, DOCSIS, multiplexing, AI-native networking as a developing concept, addresses and ports, VPN/tunnels, Tor and unconventional routing, firewalls and safe exposure.

**Do:** Compare three access networks and rehearse an **offline** exposure design: asset, public endpoint, authentication, TLS, minimal firewall rule, logs, abuse controls and rollback. **SQL notebook 2.3:** Add an index and show a query that finds all routing/security notes; explain what the index helps and when it may not.

**Secure:** Do not publish a service just to learn port forwarding; first use the Part 1 loopback example as the known-good reference. Any real later publishing is step-by-step, with validation after each change.

## 2.4 — Cloudflare, Full Stack, and Hosting Foundations
**Time:** At least 8 hours

**Learn:** Cloudflare's role in DNS/edge tooling, domains, static/dynamic hosting, frontend/backend, Ruby on Rails as an example, Gradle as build automation, executables, server-side packaging, local/global state, storage and deployments.

**Do:** Publish a static storefront *facade* or preview site using a chosen platform **only after Gate A**. Do not put an admin dashboard or database directly on the public internet. **SQL notebook 2.4:** Build the first fully self-written **local-only** lookup CLI (or simple UI) with `search <term>`, `show <id>`, and `module <code>`. Its DB is never deployed with the public site.

**Secure:** Verify DNS/HTTPS, artifact contents, permissions, logs and takedown steps; check costs before accepting any paid provider offer.

## 2.5 — Webhooks, Widgets, Developer Tools, and Platforms
**Time:** 6 hours

**Learn:** Browser developer tools, Lighthouse, webhooks, widgets, Docker refresher, extension permissions, integration patterns for Meta, Amazon, Shopify, Notion, Slack, Webull and weather data; Oracle/Canary terminology pending verification.

**Do:** Build a local signed-or-verified mock webhook receiver and safe widget; create a permissions matrix for a hypothetical platform integration. **SQL notebook 2.5:** Add parameterized search by tag and linked reference; test quote characters, empty values, and nonsensical input without SQL injection.

**Secure:** Discuss spoofed webhooks, idempotency, rate limits, replay, and why browser client code cannot securely hide an API key.

## 2.6 — Defensive Browser Security Suite and Kali VM
**Time:** 6–10 hours

**Learn:** Oracle VM VirtualBox (or the user's existing hypervisor), guest/host networking, snapshots, shared folders, Kali Linux basics, VS Code vs Visual Studio, safe browser-extension architecture and permission prompts.

**Do:** Use the existing VM, inventory its setup, take a snapshot and restore it; create a simple browser extension that displays page security information (for example HTTPS/security headers when available) without broad surveillance permissions. **SQL notebook 2.6:** Record redacted VM/snapshot metadata and link lab evidence paths in the notes database; test a backup and safe restore.

**Secure:** Use Kali only on owned/authorized test environments; prefer NAT/isolated VM networking for beginner labs; do not grant arbitrary shell or browser-history access to the extension.

## 2.7 — Root to Boot: Website + Online Security Workspace
**Time:** Open-ended capstone

**Learn:** Website build, publish, monitor, update and rollback. Run Lighthouse (performance, accessibility, best practices, SEO). Maintain a separate security checklist; Lighthouse is **not** a penetration test.

**Do:** Put the **read-only, non-AI** storefront facade online, using **static fictional entries derived from** the theoretical catalogue in Capstone 1 (for example hand-written mock JSON). **Do not yet construct a working shop database.** Include a basic documentation page for the defensive suite. Demonstrate the privately stored SQL notebook and its local lookup separately.

**Secure:** Make a deployment preflight, test and rollback worksheet before publishing; use only a scoped deployment account and minimum permissions.

### CAPSTONE 2 — The Defended Workspace

**Build:** A storefront-shaped test website plus a security-suite browser extension, Kali VM lab, network map, hosted/preview workspace, and **privately maintained SQL class-notes tree with an independently written lookup interface**.

**Mandatory passes:**
- Demonstrate Windows and Kali lab isolation, snapshots and restore.
- Show a minimal-permission extension and explain exactly what it can/cannot see.
- Test HTTPS, headers as applicable, dependencies, credential scanning, backup and rollback.
- Run and save Lighthouse results plus a separate threat model.
- Without AI coding support, **insert, update, search, link, index, back up, and restore class notes** using the learner's own code; find a note from 2.1 using the lookup built in 2.4.
- Prove there is **no AI-connected browser automation, production payment flow, public SQL port or internet-facing raw VM admin service**.

**Output:** `capstones/defended-web/`: site, extension, VM notes, network/permission diagrams, deployment procedure, Lighthouse evidence and rollback runbook; plus `notebook/` (learner-authored schema/migrations/lookup source, sanitized sample export, search test, restore proof).

**Gate B:** Website may be presented publicly only if the deployment/security checklist passes.

---

# PART 3 — AI History, Agency, and the Secured AI Shop

**Goal:** Understand AI development as a historical trajectory, then evaluate and build a *bounded* AI workflow in a realistic business setting with clear limits on autonomy.

**Suggested total:** **40–56 hours** including recommended time boxes for previously unspecified modules; not a promise of mastery. The product survey is a historical debrief, not a popularity ranking.

## 3.1 — LLM History, the Big Five, and Direction of Travel
**Time:** 4 hours

**Learn:** GPT/OpenAI, Claude/Anthropic, Gemini/Google, Grok/xAI and Copilot/Microsoft as historically distinct ecosystems; their origins, design goals, product/integration patterns, similarities and weaknesses. Treat "Muse" and other names as watchlist items until identified. Introduce previous model generations before discussing currently available models, plausible next directions and **uncertain** forecasts.

**Do:** Create a historical timeline and compare published/historical model approaches to one *goal-oriented* task (coding, long-document reasoning, workflow integration, etc.) using a hand-authored matrix. Label claims: **established**, **reported**, **observed in lab**, **speculative**. Add timeline and provenance notes to the SQL notebook. **No AI-generated code yet.**

**Secure:** Include hallucination, automation bias, privacy, data retention uncertainty, and difference between model capacity and system permissions.

**Not the task:** A star rating, chatbot fandom comparison, or unverified promise about "next gen."

## 3.2 — The Living AI Bible: Terms and Disputes
**Time:** 3–4 hours

**Learn:** Bots, assistants, agents, orchestration, subagents, monoliths, swarms, tokens, turns, context, memory, tools, APIs, keys, permissions, subscriptions versus token/API billing, retrieval, RAG, evaluations and tool calling.

**Do:** Make a versioned glossary: agreed meaning, disputed meaning, example, counterexample and relevance to security; enter glossary topics and cross-links in the SQL notebook. **No AI coding assistance yet.**

**Secure:** Distinguish *instruction* from *authorization*, *memory* from *truth*, and *context* from *long-term storage*.

## 3.3 — Coding Agents and Tool Ecosystems
**Time:** Recommended 4–6 hours

**Learn:** Copilot, Codex, Antigravity, Fusion/agents, xBuild, Perplexity and the unresolved names "sixth," "convergio" and "non." Study tool permissions, IDE workflows, generated code review, tests, logs and costs; verify product details when this module is taught.

**Do:** **First permitted AI coding workshop.** Preserve the learner's working human-written SQL lookup as a baseline. Ask two available assistants to propose a *low-risk enhancement in an isolated branch/copy*. Compare the diff, tests, tool requests, security assumptions, reversibility and any changes that would silently expand privileges. Merge nothing unexplained.

**Secure:** Do not approve terminal execution or dependency installs solely because an assistant asks. Read the command first. Never replace the hand-written lookup with generated code merely to claim a result; compare generated output to the student's own working implementation.

## 3.4 — Workflows, Agents, and "Swarms"
**Time:** 6 hours

**Learn:** Scripted workflow vs single agent vs orchestrated team vs swarm; where multi-agent complexity helps or harms. Survey Azure, DeepSeek, BigQuery and distributed/cloud patterns as examples, without conflating model provider, compute platform and analytics warehouse.

**Do:** Draw one deterministic order-validation workflow and a two-agent alternative. Choose the simpler design unless the complex one demonstrates clear value.

**Secure:** Restrict each agent's identity, tools, context and ability to delegate; prevent circular tool loops and runaway usage.

## 3.5 — Specialized AI and Predictive Systems Watchlist
**Time:** Recommended 3–4 hours

**Learn:** Investigate the originally named Azumo, DeepThink, Gozi, Karizno, GenAI labs, BlackRock Aladdin, market prediction systems, and "relish and muster" after confirming exact referents. Separate marketing claims, proprietary facts, independent evidence and speculation.

**Do:** Create a source-validation table with relevance, evidence, risks, assumptions and unresolved names. Store source provenance and disputed claims as distinct SQL note records.

**Secure:** Discuss why model output or a proprietary financial model is not a substitute for real verification.

## 3.6 — Build a Bounded Agent and Agent Hub
**Time:** Recommended 8–12 hours

**Learn:** Tool specifications, API calls, identity, tool policies, audit logging, limits, orchestration, retries, dead-letter/failed jobs, secure prompts, sandbox testing, evaluations and an approval UI.

**Do:** Build an assistant that can read a public issue plus a **sanitized, read-only export** of the class-notes index and theoretical catalogue; propose a website improvement, run tests in a disposable workspace, and request human review. It cannot write to the authoritative notes DB, merge, or deploy without explicit authorization.

**Secure:** Complete **Gate C** before connecting an agent to the actual storefront service.

**Mandatory security mini-labs (in your own lab):**
- **Prompt injection:** Plant an untrusted instruction in a mock product description and demonstrate the assistant *does not* follow it as a privileged command.
- **Code injection / unsafe execution:** Feed invalid or hostile-looking input to an application endpoint; verify it is rejected and logged without executing.
- **Secrets:** Confirm API keys are server-side, scoped, masked in logs, revocable and absent from Git/browser bundles.
- **Packages/containers:** Check dependency source, versions and image provenance; scan/inspect before granting execution.
- **Network/API:** Demonstrate allowed destinations, timeouts, retries, rate limits, webhook verification and auth failure.
- **Human override:** Cancel a queued action and prove it does not run.

## 3.7 — The AI Shop as a Security Demonstrator
**Time:** Recommended 12–20 hours for initial demo; refine as needed

**Business simulation:** Original hand-painted designs appear on products such as shirts and accessories. A possible eventual fulfillment chain is listing → order → print-on-demand production → distributor or direct shipping → support and updates. Channels such as Etsy, Amazon, eBay, and a user-owned site are *potential* sales surfaces; print partners are separate. Supplier terms, API access, brand/IP rights, taxes, returns and real economics must be verified **before live commerce**.

**Learn:** Order state machines, work orders, inventory and pricing logic, queueing, fulfillment events, help-desk triage, blog and advertising drafts, failure handling and security monitoring.

**Do:** Build an *AI-assisted simulation*: **implement the hypothetical catalogue for test purposes** → fake buyer event → validated order → human approval queue → mock printer API → mock shipment status → AI-drafted support response → human approval. Track each event and index its conceptual lessons in the separate class-notes DB.

**Secure:** AI has no payment instruments, no direct production ordering permission, no ad-spend capability, no unrestricted private customer data, no unattended deployment, and no right to bypass approval by rewriting its own prompts.

### CAPSTONE 3 — Controlled Autonomy, Not Autonomous Commerce

**Build:** A test storefront where an AI agent demonstrates useful work **inside a sandboxed, observable, permission-limited workflow**.

**Mandatory passes:**
- Test normal and malformed orders, duplicate webhooks, prompt injection, attempted unauthorized tool calls and cancellation.
- Confirm passwords/keys do not appear in prompts, logs, browser bundles or Git.
- Show the exact approval point for purchases, advertising spend, external publishing and refunds.
- Trigger a mock supplier outage and demonstrate retry, stop, manual takeover, audit trail and rollback.
- Explain which steps can be delegated to AI and which must remain under human authority.
- Trace one agent decision to a **versioned, sanitized SQL note** and show that an instruction planted in a note cannot override tool permissions. Keep the authoritative notebook read-only to the agent.

**Output:** `capstones/ai-shop/`: threat model, agent/tool manifest, test suite, event logs, approval screenshots, incident runbook and simulated fulfillment receipts.

**Gate C:** No storefront-connected AI action may be enabled until every applicable item passes. Reading a sanitized catalog is a smaller trust decision than placing an order; grant permissions incrementally.

---

# PART 4 — Hermes: Use All the Tools You Already Built

**Goal:** Assemble a personally administered, inspectable, cross-device agent system using lessons from the first three parts. Hermes is deliberately **not** introduced earlier: it is the **assembly platform for learning agent internals**—tool interfaces, memory/retrieval, identity, orchestration, context, and client access—not a claim that Hermes outperforms complete coding assistants. The course runs from a bare framework install to a Kali/Windows-accessible system and a Gradle-built Android-facing client.

**Time:** 4 hours for 4.1; remaining modules are project-driven. Suggested initial planning boxes below are optional rather than mandatory.

## 4.1 — Back to Basics
**Time:** 4 hours

**Learn:** Microsoft suite refresh, Excel, Git Bash, regex, databases, basic permissions and restore procedures.

**Do:** Repeat a spreadsheet transformation, Git recovery and SQL query **without using an agent**; use the handmade note lookup to retrieve a lesson from Part 2 and identify a design change learned in Part 3.

**Secure:** Verify you can recognize when agent-proposed commands would access the wrong folder, database or environment.

## 4.2 — Identify Hermes; Set Up Database and Memory
**Time:** Suggested 6–8 hours

**Learn:** Confirm the *exact* intended Hermes project, publisher, license, platform support and capabilities before installation; API credentials; SQLite vs server database; `AGENTS.md` conventions if supported; agent memory, retrieval and backups. Distinguish the **SQLite class-notes knowledge tree**, the **simulated shop catalogue**, and the agent's transient context memory.

**Do:** Install the verified project in a restricted local environment, attach **read-only, sanitized copies** of the class-notes database and the simulated shop catalogue (or a combined read-only retrieval view), and show query logs plus an explicit schema allowlist. Do not yet grant the agent write access to either authoritative data store.

**Secure:** Do not hand the agent unrestricted SQL, OS access or a real API key in a committed file.

## 4.3 — Build Small, Verifiable Hermes Tools
**Time:** Suggested 6–8 hours

**Learn:** Tool contracts, schema validation, authorization, PGP fundamentals, Git Bash, cloud CLI, optional Kiwi integration, privilege boundaries and error handling.

**Do:** Write one low-risk tool (e.g., query a sanitized class note by module/ID, query a mock product, validate file hashes, generate a report). Add integrations one at a time, test then revoke.

**Secure:** Keep arbitrary shell execution, cloud modification, PGP private-key usage and browser automation **off by default**. Treat commands proposed by AI as untrusted.

## 4.4 — Security Suite + Reviewable Orchestration **and the Hermes SQL Knowledge Index**
**Time:** Suggested 8–10 hours (keep course pace; move optional indexing refinements to rabbit holes)

**Learn:** Connect the existing defensive extension or its trusted backend to Hermes; website audits, structured tool output, workflows, agent handoffs and draft advertising plans. Consolidate Part 2–3 course notes, test evidence, troubleshooting, glossary, and the **simulated shop catalogue** into a coherent, indexed, queryable knowledge resource with provenance.

**Do:**
1. Expand or migrate the independently built SQL notebook so Hermes can look up **classes, lessons, concepts, tests, fixes, and sources** by module, tag, keyword, or related note; preserve the parent/child tree and cross-links.
2. Bring the shop catalogue from its Part 1 theoretical model and Part 3 sandbox implementation into a **separate catalog domain/table family**. Relate catalog procedures and failure modes to class notes via explicit links rather than mixing real/simulated operational records into lecture notes.
3. Add suitable ordinary indexes; evaluate SQLite FTS5 **only if available and justified**. Show lookup results with `note_id`, source/provenance, time/version, and a clear indication of whether content is verified or merely a student's hypothesis.
4. Expose **read-only, parameterized, allowlisted query tools** for Hermes. Return bounded snippets and explicit citations/record IDs. Treat every note body and product description as untrusted *data*, not operational instructions.
5. Have Hermes request a site-health report, connect the observed issue to an indexed lesson, create a Git issue, and suggest an ad draft—without posting or paying.

**Secure:** Run SQL injection and prompt-injection negative tests; show no direct database file write, no broad arbitrary SQL tool, no public DB port, no API keys in the notebook, and full audit logs for retrieval/tool use. Demonstrate recovery from a corrupted *copy* and a stale or false note. Browser-to-agent permissions remain explicitly limited.

**Capstone checkpoint:** By the end of **4.4**, the SQL database contains both an **extensive coursework lookup index** and the **catalogue reference for Hermes**, searchable without relying on an LLM for correctness. The student can demonstrate the exact SQL query behind an agent's retrieved answer.

## 4.5 — Bounded Context and Private Cross-Device Access
**Time:** Suggested 10–12 hours

**Learn:** Rolling summaries, retrieval, context-budget management, provenance, memory deletion/correction, Windows/Kali access panels, Docker deployment and private Cloudflare-based access patterns.

**Do:** Create a window-like short-term context plus **retrieval from the indexed, source-linked SQL class notebook**; demonstrate recall, citations and hallucination checks; expose only an authenticated **application endpoint** to authorized devices if a remote option is needed.

**Secure:** A Cloudflare Tunnel is not permission management by itself. Require strong authentication, least privilege, TLS, access policies, logs and revocation. **Never publish a raw Windows/Kali shell, remote desktop, database admin interface or unprotected agent console.** `localhost` means local to the device/container's own network context, not universal remote access.

## 4.6 — Cradle to Gradle: Android Client
**Time:** Suggested 8–12 hours

**Learn:** PWA vs native Android, Kotlin and Gradle basics, authenticated client/server separation, Android app signing/distribution concepts, integration with agent-backed services; verify "Quail" and "VS agents" before using them.

**Do:** Build a minimal phone interface that sends a request, displays a response, shows activity history, and requires authorization for privileged actions.

**Secure:** Keep provider API keys on the backend; mobile apps are untrusted clients. Support session revocation and test a lost-device scenario.

## 4.7 — Git Good: Private API, BigQuery, and Next-Step Certificates
**Time:** Suggested 8–12 hours

**Learn:** Private API specifications, identity of users vs agents, API registration versus authorization, Google BigQuery for event analytics, cloud logging, budgets, Google learning/certificate pathways and an AI cloud workspace overview.

**Do:** Register an agent through an authenticated, minimally scoped API; send **sanitized analytics events** (not private customer records or secrets) to an optional BigQuery learning environment or local stand-in; document the setup and cost controls.

**Secure:** Keep the transactional database separate from analytics; if BigQuery or another cloud service needs a paid account, use a local simulated alternative for the required lab.

### CAPSTONE 4 — The Hermes Control Room

**Build:** A personal agent operating through a transparent dashboard with a **restricted, searchable class-notes tree and separate simulated shop catalogue**, selected tools, security-suite information, bounded memory, optional private cloud access and an Android-facing client.

**Mandatory passes:**
- Demonstrate authenticated, logged and reversible **read-only** operation first.
- Ask Hermes a question about a Part 2 security lesson and a Part 3 shop simulation; trace both answers to **exact SQL record IDs, permitted queries and source status**. Correct an outdated note manually and prove the next retrieval reflects the revision.
- Prove unsafe tool requests are denied and approvals cannot be forged by tool output.
- Prove logs redact secrets and separate instructions from untrusted retrieved content.
- Revoke one token, disable one tool, restore database backup, rebuild container and test access loss.
- Demonstrate human recovery when the AI returns a false answer, fails a task, loops, leaks a simulated secret, or proposes an unsafe deployment.
- Show a one-page architecture diagram with each trust boundary and the human override point.

**Output:** `capstones/hermes-control-room/`: architecture, app/client, tool catalog, indexed notebook schema/query tests and provenance example, memory design, test/approval log, access-control policy, restore runbook and future certificate roadmap.

**Gate D:** Only add a capability after its scope, failure handling, monitoring, revocation and owner are documented.

---

## Special worked example — A safe Part 1 porting lab

**Purpose:** Create the exact, concrete reference case you can work backward from in Part 2. This is a **localhost-only** tutorial, not a public deployment or router configuration.

1. **Make a lab directory** with only sample files; do not serve your whole home, desktop, or system directory.
2. **Create a minimal Node HTTP server** with an explicit loopback bind. Example `server.js`:

   ```js
   const http = require('node:http');
   const server = http.createServer((_req, res) => {
     res.writeHead(200, {'Content-Type': 'text/plain'});
     res.end('Rootcamp localhost lab\n');
   });
   server.listen(3000, '127.0.0.1', () => {
     console.log('Only local: http://127.0.0.1:3000');
   });
   ```

3. **Run** `node server.js` from the lab directory with normal user privileges.
4. **Verify** from the same computer: `curl http://127.0.0.1:3000` (or open that URL locally). Record output.
5. **Inspect the listening address** using `netstat`/`Get-NetTCPConnection` (Windows) or `ss` (Linux). Confirm `127.0.0.1:3000`, not `0.0.0.0:3000`.
6. **Explain the boundary:** The process accepts local connections, but it has *not* authenticated users and has *not* been safely published. The loopback binding is the protective property being demonstrated, not an excuse to ignore vulnerabilities.
7. **Stop** using Ctrl+C. Verify the URL no longer responds.
8. **Record the rollback:** delete disposable lab artifacts; no router, firewall, cloud or account configuration should have been changed.

**Stop condition:** If the service binds to all interfaces unexpectedly, terminate it and correct the code before proceeding. Do not bypass a firewall warning to “get the demo working.”

**The Part 2 extension of this example** is not “open the port.” It is to sketch and then, when justified, verify: domain, edge/proxy, TLS, user auth, allowed routes, firewall boundaries, logs, deployment provenance, cost controls and rollback—**one change, one verification at a time**.

---

## The AI Shop: Why this particular prototype matters

The product itself (a painted-design shirt or accessory) is not the educational innovation. The **automated chain of custody** is:

`design → product listing → visitor → order intent → fraud/validation checks → human authorization → print provider → shipment updates → support → audit`

Every arrow crosses a trust boundary or a reliability boundary. A modern human maintainer needs to understand **who may initiate a step, what can fail, what can be spoofed, what can be reversed, and what evidence proves the action actually happened**.

**Economic stance:** The user envisions a near-equilibrium print-on-demand business where fulfillment and automation costs roughly balance revenue. Rootcamp does **not** claim those margins are verified, stable, or profitable. Price/fee calculations, marketplace terms, refunds, chargebacks, ad costs, taxes, and rights to designs are deferred to an optional real-commerce due-diligence exercise.

**Human skill proposition:** The enduring skill is not getting an agent to sell a sweater. It is maintaining the filesystem, permissions, networks, identity, data integrity, observability, incident response and recovery that make automated businesses trustworthy. The class-notes SQL tree is the training bridge: the human learns how retrieval works **before** granting an agent the power to retrieve.

---

## Working backlog and study discipline

For **every module**, save:
- [ ] One diagram or a five-sentence explanation
- [ ] One runnable artifact, screenshot or trustworthy test result
- [ ] One deliberate failure and a demonstrated fix
- [ ] One security boundary and the control that protects it
- [ ] One stop/revoke/restore procedure
- [ ] One short entry in `rabbit-holes.md` for anything interesting but not necessary today
- [ ] From Part 2 onward: at least one new SQL class note, a linked record, and a passing hand-authored lookup/query test

### Project-state labels

`BACKLOG` → `IN LAB` → `DEMO WORKS` → `SECURITY CHECKED` → `GATE PASSED` → `MAINTENANCE`

A module can be studied without a production release. **Working** and **safe to expose** are different statuses.

### Minimum evidence template

```text
Module:
Date:
Goal:
What I built:
Commands/actions:
Test that passed:
Failure I triggered:
How I fixed it:
Security boundary:
How to stop/undo/revoke:
Where files and evidence live:
SQL notebook note_id/topic_id:
SQL lookup/query I ran (Part 2+):
Source/provenance attached:
Was any AI code used? (Not allowed before 3.3):
One follow-up rabbit hole:
```

### Rabbit-Hole Register (not blockers until they touch a safety gate)

- Kubernetes operational cluster administration
- TLS cryptography internals and PKI operations
- 6G standards timelines and AI-native networking claims
- Deep Ruby on Rails, Gradle internals and native Android architecture
- Comparative agent frameworks and emerging AI lab/product names
- Provider-specific cloud certification tracks
- Live e-commerce profitability, payment processing and tax operations

### Unverified or ambiguous names retained verbatim

`routaments`; `MAC1`; `cel`; `cloud studio`; `Oracle/Canery`; `5/7`; `Muse`; `Fusion`; `xBuild`; `sixth`; `convergio`; `non`; `azumo`; `deepthink`; `gozi`; `karizno`; `relish and muster`; `Quail`; `Kiwi`; and the specific **Hermes AI** distribution to install.

These labels are *investigation notes*, not confirmed products or standardized technical terms. Do not silently convert them to unrelated software.

### Reference topics to verify with official documentation when teaching

- Git / GitHub / VS Code; Node.js and Java/JDK; Python and `pip`; Jupyter; Docker; Kubernetes; SQLite
- Microsoft 365 / Google Workspace; Windows and Linux filesystem security
- OWASP web and AI/LLM application security guidance; NIST cybersecurity and AI risk frameworks
- Cloudflare security and private access documentation; current mobile and browser extension permission models
- Chosen AI models/agents, their actual API features, costs, data policies and tool permission surfaces
- Hermes project's current publisher, release/version, platform, support and license

*Links and product capabilities are intentionally not asserted as current in this offline curriculum revision.*

---

## Graduation test — "Root to boot"

By the end, explain and demonstrate—without delegating the explanation to the AI:

1. **Where the data lives** and how to back it up, inspect it, and restore it—including the **student-authored class-notes SQL tree and the separate fictional shop catalogue**.
2. **Which machine runs which process**, under whose authority, and through what network route.
3. **What is trusted, what is untrusted**, and where user, service, and agent identities differ.
4. **What the agent can actually do**, which privileges it lacks, and how it could be fooled.
5. **How an automated workflow fails** and how a person safely interrupts, repairs, and restarts it.
6. **How to push a controlled improvement** from development through review and testing to deployment.
7. **How to keep learning** through documentation, an issues backlog, a **human-built lookup**, and a certificate plan without getting stuck in every rabbit hole.
8. **How Hermes reaches an answer** by retrieving a bounded, provenance-labeled SQL record and how to correct a bad record without letting it become an instruction or unauthorized tool call.

**If those eight statements can be proven with the four capstones, Rootcamp has accomplished its specific mission.**
