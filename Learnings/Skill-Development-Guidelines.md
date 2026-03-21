# Learning: Skill Development Guidelines

**Date:** 2026-03-20
**Entity:** [Skill-Forge](../Initiatives/Skill-Forge/Skill-Forge.md)
**Insight:** Establish rigid architectural protocols for autonomous capability expansion to prevent technical debt.
**Status:** Validated

## Context
As the `atlas-claw` repository scales, the introduction of ad-hoc scripts creates architectural drift and operational fragility. 

## Observation
Standardizing Skills into isolated directories with mandatory `SKILL.md` metadata significantly improves agent discoverability and execution safety.

## Synthesis
Every new capability MUST follow the Forge protocol:
1. **Isolated Directory:** Rooted in `.agents/skills/[skill-name]/`.
2. **Metadata Mandate:** YAML frontmatter in `SKILL.md`.
3. **CLI Standard:** Robust argument parsing with JSON output.
4. **Credential Safety:** Strict dynamic ingestion of `.env` variables.

This ensures that Atlas can autonomously understand and utilize new tools without manual intervention.
