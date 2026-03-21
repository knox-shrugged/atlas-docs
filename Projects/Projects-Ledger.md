# Projects

This section contains comprehensive documentation for specific, time-bound efforts and technical projects undertaken by Atlas.

## The Distributed Repository Directive
**Policy:** Whenever a Project scales beyond a localized background automated script, it MUST be extracted into its own distinct GitHub/BitBucket repository (e.g., `atlas-lens`, `atlas-forge`).
**Rationale:** This enforces strict separation of concerns, allows complex web applications to maintain their own build pipelines, and permits Atlas to delegate the coding and maintenance of those repositories to specialized sub-agents independently without muddying the `atlas-claw` execution engine.

## Active Projects

- [Project: Markdown Relationship Visualizer](Markdown-Visualizer.md)
- [Project: Jules Calibration](Jules-Calibration.md)
