# Agent Skills

A collection of [Agent Skills](https://agentskills.io) for Claude Code and Claude.ai.

## Available Skills

| Skill | Description |
|-------|-------------|
| [youtrack](skills/youtrack/) | Manage YouTrack issues, agile boards, projects, and users via the `yt` CLI |
| [azdevops](skills/azdevops/) | Manage Azure DevOps projects, repos, PRs, pipelines, and work items via the `azdevops` CLI |

## Installation

### Claude Code

Copy a skill into your Claude skills directory:

```bash
cp -r skills/youtrack ~/.claude/skills/
```

### claude.ai

Add `skills/{skill-name}/SKILL.md` to your project knowledge, or paste its contents into the conversation.

## Creating a New Skill

See [AGENTS.md](AGENTS.md) for conventions and best practices when adding skills to this repo.

Quick summary:

1. Create `skills/{skill-name}/SKILL.md` with valid frontmatter (`name`, `description`)
2. Add any scripts to `skills/{skill-name}/scripts/`
3. Package it: `cd skills && zip -r {skill-name}.zip {skill-name}/`

The `name` field in frontmatter must exactly match the directory name.
