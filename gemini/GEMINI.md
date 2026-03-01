# Gemini Agent Guide

This file provides context and instructions for the Gemini CLI agent when operating within the Fusion Labs monorepo.

## Overview

Fusion Labs is an AI-first development environment. The Gemini agent is equipped with specialized skills and Model Context Protocol (MCP) servers to handle polyglot development (Go, TypeScript, React), database management (Postgres, Redis), and system operations.

## Architecture

The agent environment is organized as follows:

- **`mcp_config.json`** - Definitions for external tool integrations.
- **`skills/`** - Domain-specific expert guidance and workflows.
- **`antigravity/`** - Advanced context tracking and session history.

## Model Context Protocol (MCP) Servers

The following servers are configured and available:

- **`context7`** - Live documentation lookup for programming libraries.
- **`firecrawl`** - Web scraping and crawling for up-to-date information.
- **`github`** - Integration for PRs, issues, and repository management.
- **`filesystem`** - Direct operations on the `/Users/jasonnnnnnnn/fusion-labs` directory.
- **`postgres`** - Database operations for the development environment.
- **`redis`** - Cache management and session data.
- **`sequential-thinking`** - Enhanced reasoning for complex problem-solving.
- **`magic`** - Magic UI component implementation details.

## Available Skills

Activate these skills using `activate_skill(name)` for expert guidance:

- **`tdd-workflow`** - Test-driven development with high coverage requirements.
- **`verification-loop`** - Final quality checks before code completion.
- **`react-typescript`** - Frontend development with Vite and Tailwind.
- **`golang-patterns`** & **`golang-testing`** - Idiomatic Go development.
- **`postgres-patterns`** - Database design and optimization.
- **`security-review`** - Security audits for code and infrastructure.
- **`docker-patterns`** - Containerization best practices.
- **`gin-patterns`** - Web development with the Gin framework.
- **`coding-standards`** - Universal project style guidelines.

## Development Workflows

### 1. Planning and Analysis
- Use `sequentialthinking` for complex architectural decisions.
- Use `codebase_investigator` for system-wide dependency mapping.

### 2. Implementation
- Follow TDD patterns using the `tdd-workflow` skill.
- Adhere to the `coding-standards` and project-specific guidelines.

### 3. Verification
- Execute `verification-loop` before finalizing any significant change.
- Run project-specific linting and test suites (e.g., `npm run lint`, `go test ./...`).

## Contributing

When adding new capabilities:
- **Skills**: Add new skill directories to `system/agents/gemini/skills/` with a `SKILL.md` file.
- **MCP**: Update `mcp_config.json` with new server definitions.
