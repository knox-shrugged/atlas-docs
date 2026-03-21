# Institutional Knowledge: Jules API Architecture

**Date:** March 20, 2026
**Topic:** Google Labs Jules API Structure & Documentation Navigation

## Core Resource
The official developer documentation and API reference for Google Labs Jules can be found securely documented here:
[https://developers.google.com/jules/api](https://developers.google.com/jules/api)

## Context & Learning
During **Project: Jules Calibration**, we discovered an undocumented schema shift when attempting to trigger the `CreateSession` endpoint (`POST /v1alpha/sessions`). While earlier resources suggested the schema looked like:
```json
{
  "sourceContext": { "source": "sources/github/owner/repo" },
  "prompt": "Task description"
}
```

The strict validation parser inside Jules returned repetitive `400 INVALID_ARGUMENT` errors. Following manual payload testing and external documentation reference, we uncovered the precise object structure for creating a GitHub-backed coding session. 

A successful `CreateSession` payload must rigorously define the nested `githubRepoContext` object:
```json
{
  "sourceContext": {
    "source": "sources/github/owner/repo",
    "githubRepoContext": {
      "startingBranch": "main"
    }
  },
  "prompt": "Task description",
  "automationMode": "AUTO_CREATE_PR",
  "title": "Optional Title"
}
```

## Protocol Application
Moving forward across all Atlas pipelines, any custom shell script, python API execution client, or tool referencing the Jules API *must* strictly default to reading the updated structs at `https://developers.google.com/jules/api` before attempting automated payload execution.
