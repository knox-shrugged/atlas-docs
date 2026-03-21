# Atlas-Docs

**Mission:** This repository serves as the central documentation hub for all projects and initiatives of Atlas.

Here we capture the following fundamental aspects of the Atlas ecosystem:

- **[Vision](http://localhost:5177/):** The primary dynamic visualization and strategic ledger of the ecosystem (Atlas Lens).
### 📋 Documentation Vector Templates
All new strategic or tactical entries **MUST** strictly adhere to the standardized formats defined in the [Templates/](Templates/) directory. Each categorical domain requires its specific template for consistent ecosystem visualization:

- **[Strategic Goals](Goals/):** High-level objectives ([Goal Template](Templates/Goal-Template.md)).
- **[Initiatives](Initiatives/):** Operational frameworks ([Initiative Template](Templates/Initiative-Template.md)).
- **[Projects](Projects/):** Tactical executions ([Project Template](Templates/Project-Template.md)).
- **[Operational Activities](Activities/):** Dynamic registry of **Jobs** ([Job Template](Templates/Job-Template.md)) and **Tasks** ([Task Template](Templates/Task-Template.md)).
- **[Autonomous Agents](Agents/):** The official registry of autonomous actors ([Agent Template](Templates/Agent-Template.md)).
- **[Institutional Learnings](Learnings/):** Structured repository for insights ([Learning Template](Templates/Learning-Template.md)).

- **[Ethos](.agents/rules/core-identity.md):** The core persona, voice, and behavioral guidelines for Atlas.




***

### 🛑 Architectural Boundary: Strategy vs. Execution
It is a fundamental principle of this repository that **`atlas-docs` contains ONLY the definition of what needs to be done.** 

At no point shall execution or implementation details be stored here.
- **The "What" and the "Why"** live strictly within `atlas-docs` (Strategy, Concepts, Definitions).
- **The "How"** lives exclusively in executing repositories such as `atlas-claw` (Workflows, Scripts, Code, Automations). 

### 📦 Distributed Repository Directives
1. **Agents:** Every operational Agent must have its own localized repository. `atlas-docs` only documents the *name*, *responsibilities*, *capabilities*, and *pointer* to the Agent's repo. All agent-specific skills, sub-agent definitions, and workflows stay strictly inside that Agent's repository.
2. **Projects:** Every Project must similarly exist within its own decoupled repository (e.g., `atlas-lens`). Project-specific details, code, and frontend logic stay entirely localized to the project repository.

This repository must remain a pure, unpolluted organizational ledger.
