# Institutional Knowledge: Skill Development Guidelines

**Date:** March 20, 2026
**Topic:** Standardizing capability expansion in `atlas-claw`

## Overview
To perpetually expand Atlas's operational capabilities (pursuant to Goal-004), we must continuously forge new "Skills." A Skill is an encapsulated directory of scripts, instructions, and credentials that teaches Atlas how to interact with an external API, database, or tool. 

To prevent `atlas-claw` from devolving into a chaotic mess of unstructured scripts, all new Skills MUST rigorously adhere to the following architectural guidelines.

## 1. Directory Structure
Every skill must be localized within its own isolated folder inside `atlas-claw/.agents/skills/`.

A standardized skill directory looks exactly like this:
```text
.agents/skills/[skill-name]/
├── SKILL.md                 # Core instructions and metadata (MANDATORY)
├── scripts/                 # Executable Python/Node/Bash scripts (MANDATORY if there's code)
│   ├── [client_name].py
│   └── requirements.txt     # Localized dependencies
├── examples/                # Example input/output payloads (Optional)
└── resources/               # Assets, templates, or raw materials (Optional)
```

## 2. The `SKILL.md` Protocol (The Metadata)
The `SKILL.md` file is the instruction manual that Atlas reads to understand how to use the skill. It MUST contain YAML frontmatter explicitly declaring the skill.

**Required Formatting:**
```markdown
---
name: "[Human Readable Name, e.g., Google Jules API Interaction]"
description: "[1-2 sentence description explaining exactly what the tool does and when Atlas should use it]"
---

# [Skill Title]
[Documentation on prerequisites, base API info, provided tools, and exact terminal commands to trigger them.]
```

## 3. Operational Standards
* **Credential Secrecy:** Hardcoding credentials inside a skill's `scripts/` directory is an absolute violation of Atlas Operations. Scripts MUST dynamically pull keys from the master `.env` file at the root of `atlas-claw` using `os.getenv()` or equivalent.
* **Command Line Interfaces:** All scripts intended to be triggered by Atlas must be built as robust CLI tools (e.g., utilizing Python's `argparse` or Node's `commander`). They must accept clean, distinct arguments (e.g., `--action create --payload "data"`).
* **Idempotency & Safety:** Scripts should be written with safety rails. If a script fails, it must fail gracefully and output a clear JSON error payload to `stdout` so that the agent can read the error and correct its course autonomously.

## 4. Maintenance & Auditing
* When a new tool or API is introduced to the tech stack, a corresponding Skill should immediately be scaffolded.
* Existing skills (like Zapier or Jules) must be periodically audited to ensure dependencies are secure and APIs have not been deprecated.
