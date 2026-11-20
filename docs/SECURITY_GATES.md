# Rootcamp security gates — hard stops only where necessary

Rootcamp is a learning environment. Use owned/authorized machines and test accounts only. Don't conduct scans or exploit exercises against unknown systems. Save enough detail to reproduce the lab without publishing secrets, sensitive inventories, or internet-facing administrative access.

## Continuous rules

- Least-privilege file and account permissions; no unexplained administrator/root execution.
- Check untrusted downloads, extensions, dependencies, and packages before installation.
- No live customer data, payment methods, real external transactions, or publicly accessible VM/admin ports during course demos.
- Verify backups and a rollback path before changing important configuration.
- Keep passwords, API keys, tokens, cookies and signing keys out of Git, screenshots, AI prompts and the SQL notes tree.
- Human approval for irreversible actions, releases, money movement, account permissions, credential rotation, or ad spend.

## Gate A — Part 1 sandbox / before Part 2

Demonstrate local-only bind/address, intended port, process stop, no router forwarding, no exposed credentials; storage/share settings and a tested backup. Module **1.4** includes mandatory sandbox inspection. Module **1.7** stays an observation-only, payment-free cloud CLI tour.

## Gate B — Part 2 hosting / before any public website

At **2.4** review staging exposure, HTTPS, permission models, cloud share settings, secret handling, vulnerable dependencies, database privacy, admin-panel access, logging and rollback. Recheck during the Part 2 capstone. Only public content may be published; the class-notes SQLite tree stays private.

## Gate C — Part 3 AI storefront activation

At **3.6** and capstone: use mock products/orders, explicit tool allowlist, scoped credentials (or no real credentials), budget/cost limits, prompt- and code-injection tests, logs, approvals, and a kill switch. An AI must not be able to buy, refund, advertise, change settings, or access privileged terminals on its own.

## Gate D — Part 4 Hermes integration

At **4.4** and capstone: check framework provenance/version, trusted extensions and tools, SQL query permissions, source provenance and retrieval boundaries, secrets, identity-based private access, recovery, and controlled remote interfaces. Start Hermes access **read-only** and require separate permission review for each new tool.

## Status recording

- **CLEAR:** evidence shows the boundary is working as designed.
- **FIX THEN RETEST:** confirmed unsafe exposure/action path.
- **NOT YET TESTED:** cannot cross that gate.
- **REVISIT:** nonblocking educational deficit, tied to a follow-up task.

Passing a checklist is a training result, **not** a guarantee of production security.
