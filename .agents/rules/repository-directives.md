---
description: System instructions and architectural directives for the atlas-docs repository
---

# `atlas-docs` Repository Directives

When interacting with or generating content in the `atlas-docs` repository, you MUST adhere to the following architectural boundaries and directives:

## 1. Strategy vs. Execution
- **Strictly Strategic**: `atlas-docs` contains **ONLY** the definition of what needs to be done. It focuses exclusively on the "What" and the "Why" (Strategy, Concepts, Definitions).
- **No Implementation**: At no point shall execution, implementation details, automated scripts, workflows, code, or automations be stored here.
- **The "How" lives elsewhere**: All execution details live exclusively in executing repositories such as `atlas-claw`.

## 2. Distributed Repository Directives
- **Agents**: Every operational Agent must have its own localized repository. `atlas-docs` is responsible only for documenting the Agent's *name*, *responsibilities*, *capabilities*, and providing a *pointer* to the Agent's repository. All agent-specific skills, sub-agent definitions, and workflows must stay strictly inside that individual Agent's repository.
- **Projects**: Every Project must exist within its own decoupled repository (e.g., `atlas-lens`). Project-specific details, code, architecture logic, and frontend logic stay entirely localized to the individual project repositories.

## 3. Maintain the Ledger
This repository must remain a pure, unpolluted organizational ledger. Do not add code snippets, automation scripts, or functional configuration files into `atlas-docs`.

## 4. Organization Structure 🗂️
When creating new entities within `atlas-docs`, you must respect the following localized directory structure:
- **Goals:** Every documented Goal MUST have its own dedicated sub-folder within the `Goals/` directory (e.g., `Goals/Autonomous-Intelligence/`).
- **Initiatives:** Every documented Initiative MUST have its own dedicated sub-folder within the `Initiatives/` directory (e.g., `Initiatives/Overwatch/`). 
- **Projects:** Every documented project MUST have its own dedicated sub-folder within the `Projects/` directory (e.g., `Projects/atlas-lens/`). 
- **Agents:** Similarly, every Agent MUST have its own dedicated sub-folder within the `Agents/` directory using a descriptive name in the format `<role>-<name>` (e.g., `Agents/Archivist-Recon/`). 

## 5. Strategic Traceability 🔗
To maintain a cohesive and traversable ecosystem, all documented entities MUST include mandatory relational links:
- **Initiatives:** MUST always link to the high-level **Goals** they serve.
- **Projects:** MUST always link to the **Initiatives** they fall under.
- **Agents:** MUST always be clearly linked to one or more **Projects** they are assigned to work on.
- **Friendly Naming:** For visualization purposes (`atlas-lens`), every strategic document SHOULD include a friendly display name and a one-sentence summary in its header or frontmatter.

## 6. Ledger Maintenance 📝
Even though entities are housed in their own sub-folders, the root Ledger files (`Agents-Ledger.md`, `Projects-Ledger.md`, `Initiatives-Ledger.md`, `Goals-Ledger.md`, etc.) must always be manually updated to act as a central "Table of Contents".
- Whenever a new Agent, Project, Initiative, or Goal is added, you MUST update the corresponding Ledger with a high-level summary of its role, capabilities, and a link pointing to its dedicated folder's primary document.

