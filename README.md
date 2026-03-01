# AI Agents & Configs

A central repository for AI-assisted development configurations, agents, and expert system rules for use across Fusion Labs projects.

## Project Structure

Currently, this repository contains:
- **`gemini/`**: Configurations for the Gemini CLI agent.
  - `agents/`: Specialized agent role definitions.
  - `skills/`: Expert procedural guidance (TDD, Security, etc.).
  - `rules/`: Language-specific coding patterns and standards.
  - `GEMINI.md`: Root configuration and system instructions.

## Future Support
- **`.claude/`**: Planned support for Claude Code and related tools.
- **`.cursor/`**: Planned support for Cursor IDE custom rules and prompts.

## Usage: Linking Configurations

To use these configurations in your local project without duplicating files, use the `ln` (link) command to create a symbolic link. This ensures your project always uses the latest version from this repository.

### For Gemini CLI

Navigate to your project root and run:

```bash
# Create a symbolic link to the gemini folder
ln -s ~/path/to/gemini .gemini
```

### Understanding the `ln` Command

- `ln`: The standard Unix command to link files or directories.
- `-s` (Symbolic): Creates a "symbolic" or "soft" link. This is like a shortcut or alias; if you delete the link, the original files remain safe.
- `[SOURCE]`: The full path to the configuration folder in this repo.
- `[DESTINATION]`: The name the link will have in your project (e.g., `.gemini`, `.cursorrules`).

**Example for future Cursor support:**
```bash
ln -s ~/path/to/.cursorrules .cursorrules
```

## Contributing

When adding new skills or rules, ensure they follow the established project patterns and are tested against the relevant AI agent.
