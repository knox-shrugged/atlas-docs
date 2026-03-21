# Project: Jules Calibration

* **Initiative:** Initiative-003 (Project Skill Forge)
* **Goal:** Goal-004 (Persistent Skill Ascendancy)
* **Status:** Active / In Progress

## Objective
To rigorously audit and fine-tune the `google-jules` skill within `atlas-claw`, ensuring it natively adheres to the newly established Skill Development Guidelines. This involves standardizing the integration, implementing robust error handling, and expanding the command-line interface capabilities.

## Execution Requirements
1. **Metadata Standardization:** Ensure `SKILL.md` explicitly defines capabilities and usage rules via YAML frontmatter.
2. **Script Robustness (`jules_client.py`):**
   - Strictly pull `JULES_API_KEY` from the master `.env` file via environment variables.
   - Utilize a robust CLI parser (e.g., `argparse`).
   - Implement idempotent error handling with JSON-formatted `stdout` responses so the Atlas agent can gracefully interpret failures.
3. **Capability Verification:** Successfully connect and execute the `list_sources` endpoint from the local terminal to verify the bridge.
4. **Endpoint Expansion:** Add additional operational endpoints like `get_session_status` to allow autonomous monitoring of Jules's actions.

## Execution Plan
- [ ] Create this project document and register it in the `Projects-Ledger.md`.
- [ ] Audit and refactor `jules_client.py` for standard compliance (API keys and JSON output).
- [ ] Expand the CLI with new endpoints (status checking).
- [ ] Perform a live connection test to retrieve repository sources.
