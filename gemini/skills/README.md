# Skills

Skills are knowledge modules that Gemini loads based on context. They contain workflow definitions and domain knowledge tailored to the Fusion Labs workspace.

## Skill Categories

### Language & Code Patterns
| Skill | Description |
|-------|-------------|
| `golang-patterns/` | Idiomatic Go design patterns and best practices |
| `react-typescript/` | React + TypeScript + Vite patterns |
| `coding-standards/` | Universal coding standards across all languages |

### Testing
| Skill | Description |
|-------|-------------|
| `golang-testing/` | Go testing strategies (table-driven, benchmarks, fuzzing) |
| `tdd-workflow/` | Test-driven development workflow |

### Frameworks & APIs
| Skill | Description |
|-------|-------------|
| `gin-patterns/` | Gin web framework best practices (routing, middleware, JWT, GORM) |
| `api-design/` | REST API design patterns (naming, status codes, pagination, versioning) |

### Databases & Infrastructure
| Skill | Description |
|-------|-------------|
| `postgres-patterns/` | PostgreSQL patterns (GORM, indexing, query optimization) |
| `database-migrations/` | Migration best practices (golang-migrate, zero-downtime) |
| `docker-patterns/` | Docker & Docker Compose best practices |
| `deployment-patterns/` | CI/CD pipelines, health checks, production readiness |

### Security & Quality
| Skill | Description |
|-------|-------------|
| `security-review/` | Security checklists and patterns |
| `verification-loop/` | Comprehensive code verification workflow |

### Agent Workflow
| Skill | Description |
|-------|-------------|
| `iterative-retrieval/` | Progressive context retrieval (dispatch → evaluate → refine → loop) |
| `search-first/` | Research existing tools/libraries before writing custom code |
| `skill-stocktake/` | Audit skills for quality, relevance, and currency |

### Templates
| Skill | Description |
|-------|-------------|
| `project-guidelines/` | Fusion Labs project-specific guidelines template |

## Skill Structure

Each skill lives in its own directory with a `SKILL.md` file:

```
skills/
├── README.md
├── api-design/
│   └── SKILL.md
├── coding-standards/
│   └── SKILL.md
├── database-migrations/
│   └── SKILL.md
├── deployment-patterns/
│   └── SKILL.md
├── docker-patterns/
│   └── SKILL.md
├── gin-patterns/
│   └── SKILL.md
├── golang-patterns/
│   └── SKILL.md
├── golang-testing/
│   └── SKILL.md
├── iterative-retrieval/
│   └── SKILL.md
├── postgres-patterns/
│   └── SKILL.md
├── project-guidelines/
│   └── SKILL.md
├── react-typescript/
│   └── SKILL.md
├── search-first/
│   └── SKILL.md
├── security-review/
│   └── SKILL.md
├── skill-stocktake/
│   └── SKILL.md
├── tdd-workflow/
│   └── SKILL.md
└── verification-loop/
    └── SKILL.md
```

## Using Skills

Skills are loaded based on context. For example:

- Editing Go files → `golang-patterns` and `golang-testing` activate
- Working on Asset Diary backend → `gin-patterns` and `postgres-patterns` activate
- Writing React components → `react-typescript` activates
- Adding API endpoints → `api-design` activates
- Working with Docker → `docker-patterns` activates
- Before a PR → `verification-loop` activates
- Starting unfamiliar code → `iterative-retrieval` activates

## Creating New Skills

To add a new skill:

1. Create a directory: `skills/your-skill-name/`
2. Add a `SKILL.md` file with YAML frontmatter:

```markdown
---
name: your-skill-name
description: Brief description shown in skill list
---

# Your Skill Title

Brief overview.

## When to Activate

Describe scenarios where this skill applies.

## Core Concepts

Key patterns and guidelines.

## Code Examples

\`\`\`language
// Practical, tested examples
\`\`\`

## Best Practices

- Actionable guideline 1
- Actionable guideline 2
```

## Source

These skills were adapted from the [everything-claude-code](https://github.com/nicekid1/everything-claude-code) collection and customized for the Fusion Labs tech stack (Go, Gin, GORM, React, TypeScript, Vite, PostgreSQL, Redis, Docker).

---

**Remember**: Skills are reference material. They provide implementation guidance and demonstrate best practices. Use skills alongside project rules to ensure high-quality code.
