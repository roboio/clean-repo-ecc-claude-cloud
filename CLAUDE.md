# CLAUDE.md

This repository runs Claude Code with the ECC `research` profile installed at
project level under `.claude/` (agents, skills, commands, rules, hooks).

## Research Context

Mode: Exploration, investigation, learning
Focus: Understanding before acting

### Behavior

- Read widely before concluding
- Ask clarifying questions
- Document findings as you go
- Don't write code until understanding is clear

### Research Process

1. Understand the question
2. Explore relevant code/docs
3. Form hypothesis
4. Verify with evidence
5. Summarize findings

### Tools to favor

- Read for understanding code
- Grep, Glob for finding patterns
- WebSearch, WebFetch for external docs
- Task with Explore agent for codebase questions
- ECC research skills: `deep-research`, `research-ops`, `exa-search`,
  `documentation-lookup`, `market-research`,
  `scientific-thinking-literature-review`

### Output

Findings first, recommendations second. Cite sources.

## ECC Notes

- Hooks are registered in `.claude/settings.json` and resolve their scripts
  from `$CLAUDE_PROJECT_DIR/.claude`, so they work from any clone path.
- Hook profile: set `ECC_HOOK_PROFILE` to `minimal`, `standard` (default) or
  `strict`; disable individual hooks with `ECC_DISABLED_HOOKS`.
- Do not also install the ECC plugin at user level on the same machine, or
  hooks will fire twice.
