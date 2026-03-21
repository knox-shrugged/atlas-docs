# Project: Markdown Relationship Visualizer

* **Initiative:** Initiative-002 (Project Panopticon)
* **Goal:** Goal-003 (Total Architectural Observability)
* **Status:** Scoping / Planning

## Objective
Build an automated tool within `atlas-claw` that ingests all markdown files within the `atlas-docs` repository, reads their links and hierarchical structure, and outputs a dynamic visual node-graph.

## Requirements
1. **Parser:** Must be able to traverse all core directories (`Goals`, `Initiatives`, `Projects`, `Subordinates`, `Learnings`).
2. **Link Extraction:** Must identify markdown links (e.g., `[Initiative-002](../Initiatives/Initiatives-Ledger.md)`) and map them as connected nodes.
3. **Renderer:** Must convert the parsed data into a polished, premium visual format. This will be an interactive Vite + React + D3.js web application capable of deploying independently.

## Phase 1 Execution Plan
- [ ] **Repository Creation:** Scaffold a completely new repository named `atlas-lens` under the `knox-shrugged` organization.
- [ ] **Repository Rules:** Install an `.agents/rules/lens-operations.md` in the new repo informing the assigned sub-agent of its responsibilities.
- [ ] **Backend:** Write the ingestion parser logic to securely read markdown from `atlas-docs`.
- [ ] **Frontend:** Build a premium, interactive D3.js or React Flow UI.
- [ ] **Data Pipeline:** Automate the generation process so the graph is always perfectly synchronized with the brain (`atlas-docs`).
