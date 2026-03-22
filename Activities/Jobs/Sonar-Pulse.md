# Job: Sonar-Pulse

**Friendly Name:** Sonar Intelligence Pulse
**Description:** Automated reconnaissance routine to trigger the Sonar ingestion pipeline.
**Status:** Active
**Schedule:** Every 12 Hours
**Project:** [Sonar](../../Projects/Sonar/Sonar.md)

## Overview
The Sonar Pulse is the primary operational routine for synchronizing our tactical intelligence with external reality. It ensures that the Sonar Intelligence Engine is triggered, high-signal feeds are processed, and the results are synthesized into the strategic record.

## Procedure
1. **Initialize Reconnaissance:** Trigger the `atlas-sonar` ingestion engine to poll all active RSS and newsletter targets.
