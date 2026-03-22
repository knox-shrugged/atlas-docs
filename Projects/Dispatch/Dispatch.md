# Project: Dispatch

**Friendly Name:** Task Dispatch Engine
**Description:** The operational command center for creating, delegating, and tracking tasks across the Atlas ecosystem.
**Repository:** [atlas-claw](../../../atlas-claw)
**Status:** Active
**Primary Initiatives:** [Taskmaster](../../Initiatives/Taskmaster/Taskmaster.md)
**Lead Agent:** [Mr. Carson](../../Agents/Chief-of-Staff-Carson/Carson.md)

## Overview

Dispatch is the execution backbone of the Taskmaster initiative. It provides the infrastructure within `atlas-claw` to decompose strategic objectives into discrete, actionable tasks, assign them to the appropriate agents, and relentlessly track their progress through to completion. Where Atlas Knox defines *what* must be done, Dispatch ensures it *gets done* — on time, on target, and with full accountability.

## Core Functions

1.  **Task Creation:** Programmatic generation of standardized task records from strategic objectives, with automatic linkage to parent projects and initiatives.
2.  **Agent Delegation:** Intelligent routing of tasks to agents based on capability, domain, and current workload.
3.  **Status Tracking:** Continuous monitoring of task progress, with automated follow-up and escalation for stalled or blocked items.
4.  **Dependency Management:** Cross-objective task dependency resolution, ensuring sequencing and coordination across the ecosystem.

## Execution Model

Dispatch operates as a **persistent orchestration layer** within `atlas-claw`:
*   **Command-Driven:** Tasks are initiated by Atlas Knox or triggered programmatically via workflows and automation hooks.
*   **Agent-Aware:** Maintains awareness of all active agents, their capabilities, and current assignments.
*   **Audit Trail:** Every delegation, status change, and completion is logged for full operational traceability.

## Technical Foundation

- **Stack:** Node.js, Python (Orchestration Scripts)
- **Data:** Standardized task records in `atlas-docs/Activities/Tasks/`
- **Integrations:** Google Jules API, Zapier MCP, Linear (future)
