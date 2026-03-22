---
description: Add a new strategic project to the Atlas ecosystem
---

# Workflow: Add Project

This workflow standardizes the creation of new tactical projects within the Atlas ecosystem. 

## Requirements

When running this workflow, you MUST provide:
- **Project Name:** The sophisticated friendly name for the project (e.g., "Overwatch Intelligence Scraper").
- **Identifier:** A URL-friendly identifier for the repository and folder (e.g., "overwatch-intelligence-scraper").
- **Repository Name:** The full repository path (e.g., "knox-shrugged/overwatch-scraper").
- **Primary Initiative:** The link to the parent initiative in `atlas-docs/Initiatives/`.

## Execution Steps

### Step 1: Initialize the Project Container

// turbo
```bash
# Define your project identifier (e.g., PROJECT_ID="intelligence-scraper")
PROJECT_ID="[placeholder-id]"

# Create the project directory
mkdir -p Projects/$PROJECT_ID
```

### Step 2: Generate Project Documentation

// turbo
```bash
# Define variables
PROJECT_ID="[placeholder-id]"
PROJECT_NAME="[placeholder-name]"
REPO_NAME="[placeholder-repo]"
INITIATIVE_LINK="../../Initiatives/[placeholder-initiative]/[placeholder-initiative].md"

# Copy template and rename
cp Templates/Project-Template.md Projects/$PROJECT_ID/$PROJECT_ID.md

# Populate template placeholders (using sed or similar)
# Note: Manually edit the file if sed is too complex for specific multi-line blocks.
```

## Post-Completion Requirements

After creating the file, you must:
1. Update the **Status** to `Active`.
2. Ensure the **Primary Initiatives** link is correctly resolved.
3. Link the appropriate **Lead Agent** who will be executing the work.
