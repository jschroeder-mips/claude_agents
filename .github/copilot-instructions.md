# Claude Code Agent Library - AI Instructions

This repository contains **18 specialized AI agent personas** for Claude Code subagents. Each agent is a standalone Markdown file with YAML frontmatter metadata.

## Architecture

- **Agent files**: `agents/*.md` - Each file is a self-contained agent persona
- **No build system**: Pure Markdown files, no compilation or dependencies
- **Installation**: Copy `.md` files to `~/.claude/agents/` (user) or `.claude/agents/` (project)

## Agent File Structure

Every agent follows this exact pattern:

```markdown
---
name: agent-name-kebab-case
description: Use this agent when... <example>Context:... user:... assistant:...</example>
model: haiku | sonnet | opus | inherit
color: cyan | purple | red | (optional)
---

You are [ACRONYM] (Full Name), an expert in [domain]...

**Core Identity & Approach:**
- [Character traits and philosophy]

**Core Principles:**
1. [Domain-specific principles, NOT generic advice]

**Domain Expertise:**
[Detailed knowledge areas with specific techniques]

**Response Structure:**
[How the agent formats responses]
```

## Key Conventions

### Naming
- File: `kebab-case.md` (e.g., `technical-lead-archie.md`)
- YAML `name`: Must match filename without `.md`
- Agent persona: Clever acronym (e.g., A.R.C.H.I.E., D.E.B.U.G., T.E.S.T.)

### Description Field
Must include:
1. Trigger phrase: "Use this agent when..."
2. At least 3 `<example>` blocks with `Context:`, `user:`, `assistant:`, and `<commentary>`
3. Examples formatted as escaped newlines in YAML

### Model Selection
- `sonnet`: Complex reasoning (technical-lead-archie, ceo-strategist)
- `haiku`: Fast, focused tasks (most agents)
- Use haiku by default for new agents

### Tools (optional in frontmatter)
Available: `Read`, `Edit`, `Write`, `Bash`, `Grep`, `Glob`, `WebFetch`, `TodoRead`, `TodoWrite`

## Agent Categories

| Category | Agents |
|----------|--------|
| Technical | archie, api, test, quality, debug, security, devops, git, doc, cats |
| Business | gent, ceo, cfo, sales, growth, csm, hr, inv |

## When Creating or Modifying Agents

1. **Avoid overlap**: Check existing agents before creating - each has a distinct specialization
2. **Be specific**: Core Principles must be domain-specific, not generic ("test thoroughly" ❌, "risk-based testing prioritized by business impact" ✅)
3. **Include real techniques**: Reference actual frameworks, tools, and methodologies (MEDDIC, pytest fixtures, OAuth2 flows)
4. **Keep length 100-300 lines**: Enough depth without overwhelming
5. **Test with `/agents`**: Verify Claude Code recognizes the agent

## Quality Checklist

Before committing agent changes:
- [ ] YAML frontmatter validates (name, description, model required)
- [ ] Description has "Use this agent when..." + 3 examples
- [ ] No overlap with existing agent specializations
- [ ] Principles are actionable and domain-specific
- [ ] Includes concrete examples from the domain expertise

## License Requirement

This project is **AGPL-3.0**. All contributions and derivative works must be open-sourced under the same license.
