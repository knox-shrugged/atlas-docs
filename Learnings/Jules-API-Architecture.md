# Learning: Jules API Architecture

**Date:** 2026-03-20
**Entity:** [Jules Calibration](../Projects/Jules-Calibration/Jules-Calibration.md)
**Insight:** Discovery of undocumented schema requirements for GitHub-backed coding sessions in the Jules v1alpha API.
**Status:** Validated

## Context
During the calibration of the `google-jules` skill, we encountered persistent `400 INVALID_ARGUMENT` errors despite following preliminary schema documentation.

## Observation
Manual payload testing revealed that the `githubRepoContext` object must be explicitly and rigorously defined within the `sourceContext` for successful session creation.

## Synthesis
All Atlas execution clients interfacing with the Jules API must strictly implement the `githubRepoContext` nesting pattern. 

### Implementation Payload
```json
{
  "sourceContext": {
    "source": "sources/github/owner/repo",
    "githubRepoContext": {
      "startingBranch": "main"
    }
  },
  "prompt": "Task description",
  "automationMode": "AUTO_CREATE_PR"
}
```
Moving forward, always refer to the latest [Official API Reference](https://developers.google.com/jules/api) before deployment.
