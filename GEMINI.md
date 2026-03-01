# Gemini CLI Agent System Instructions

This file defines the core mandates and architectural guidelines for the Gemini CLI agent when operating within the `system/agents` project.

## Project Scope
This project is a centralized repository for AI-assisted development configurations, including agent role definitions, expert system rules, and coding standards for the Fusion Labs monorepo.

## Core Mandates
- **Security First:** Never commit secrets, API keys, or sensitive credentials. Always scan for potential leaks before staging changes.
- **Link-Based Usage:** This project is designed to be linked into other repositories using `ln -s`. Ensure all paths are relative or clearly documented for external use.
- **Documentation Integrity:** Keep the `README.md` and `GEMINI.md` files updated as new tool configurations (e.g., `.claude`, `.cursor`) are added.

## Development Workflow
1. **Research:** Analyze existing rules in `gemini/rules/` and skills in `gemini/skills/`.
2. **Strategy:** Plan additions that align with Fusion Labs coding standards.
3. **Execution:** Apply surgical updates to configuration files.
4. **Validation:** Verify that all changes are compatible with the Gemini CLI.

## Sensitivity Checklist (Pre-Commit)
Before any commit, the agent MUST:
- Run `git diff` to review all changes.
- Scan for patterns like `sk-`, `sb_`, `SECRET`, `PASSWORD`.
- Verify that `mcp_config.json` and `settings.json` remain in `.gitignore`.
