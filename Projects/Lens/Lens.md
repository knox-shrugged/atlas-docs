# Project: Lens

**Friendly Name:** Strategic Visualization Engine
**Description:** The primary interface for mapping strategy to reality.
**Repository:** [atlas-lens](../../../atlas-lens)
**Status:** Active
**Primary Initiatives:** [Panopticon](../../Initiatives/Panopticon/Panopticon.md)
**Lead Agent:** [Argus](../../Agents/Visualization-Argus/Argus.md)

## Overview

`Lens` is the premier visualization platform for the Atlas ecosystem. It transforms the static strategic text of `atlas-docs` into a dynamic, interactive architectural graph, allowing for total visibility over goals, initiatives, and their complex relationships.

## Interface Architecture

### Main Layout

The interface shall prioritize clarity and sophisticated aesthetics:

- **Navigation Bar:** A persistent top-level navigation bar.
- **Branding:** Title and logo situated in the upper-left corner.
- **Navigation Links:** Screen-switching controls distributed across the top navigation bar.

### Primary Screens

#### 1. Vision (Strategic Graph)

A comprehensive nodal graph visualizer mapping the ecosystem's hierarchy.

- **Hierarchy:** The ecosystem visualization must map the strategic flow across four primary layers:
  1.  **Goals:** Strategic Zenith (Supports recursive sub-goals).
  2.  **Initiatives:** Operational Frameworks (Can apply to multiple primary Goals, supports sub-initiatives).
  3.  **Projects:** Tactical Execution (Can apply to multiple primary Initiatives, supports sub-projects).
  4.  **Agents:** Operational Workforce (Supports nested sub-agents).
- **Relational Integrity:** The interface must handle **many-to-many relationships** and recursive nesting across all layers.
- **Role Summaries:** Agent nodes must display a concise summary of their primary role directly on the node.
- **Interactive Legend:** A comprehensive visual legend in the **bottom right**, identifying node types and operational status symbols.
- **Collapsible Hierarchy:** Nodes must support **expansion and collapse** to manage complex sub-structures and descendant branches.
- **Status Indicators:** Clear, intuitive icons for all operational statuses.

#### 2. Learnings

A structured data view for institutional knowledge.

- **Format:** A detailed table view aggregating past learnings and insights from across the ecosystem.

#### 3. Jobs

Real-time tracking of recurring ecosystem operations (cron jobs), explicitly aligned to their parent projects.

- **Format:** A sophisticated 7-day calendar view with a column for each day of the week.

#### 4. Tasks

Hierarchical tracking of one-off tactical missions and sub-tasks.

- **Format:** A premium tree-grid interface supporting recursive expansion/collapse of task hierarchies.
- **Relational Context:** Each task must explicitly display its parent project and assigned agent.

## Technical Foundation

- **Stack:** Vite + React.
- **Data:** Headless ingestion from `atlas-docs` via JSON.
- **Aesthetics:** Sophisticated dark-mode experience with glassmorphism and micro-animations.


