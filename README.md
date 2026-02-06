# Gemini API Development Skill

Agent skill for building applications with the Gemini API. Teaches AI agents current model specs, SDK usage, and best practices.

## Install

```bash
# Install all skills from the repo
npx skills add treyn-create/gemini-skill-test

# Or install only this skill
npx skills add treyn-create/gemini-skill-test --skill gemini-api-development
```

## Contents

- **SKILL.md** – Instructions for agents working with Gemini API (models, SDKs, docs)
- Compatible with Cursor, Claude Code, VS Code Copilot, Gemini CLI, and Antigravity (AGY)

## How the skill uses latest docs

The skill keeps agents up to date by directing them to the live Gemini API docs index:

1. **llms.txt index** – Agents fetch `https://ai.google.dev/gemini-api/docs/llms.txt` to discover all available documentation pages.
2. **On-demand pages** – When needed, agents fetch specific pages (e.g. `function-calling.md.txt`, `models.md.txt`) in `.md.txt` format from the same domain.

Because agents pull docs at runtime instead of from static content, they always use the latest Gemini API documentation—no skill updates required when Google ships new models or API changes.
