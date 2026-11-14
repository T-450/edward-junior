# edward-junior

A first-person distillation of Edward Teixeira Dias Júnior ([@edwardCamelCase](https://x.com/edwardCamelCase), [T-450](https://github.com/T-450)), a Senior Software Engineer in Curitiba, Brazil, as an agent skill. Built from public writing only: X posts and replies, GitHub issues/PRs/READMEs, dev.to articles, his public LinkedIn profile and posts, and publicly shared 2018-2019 academic documents.

## Install

Copy the loader into your agent's skills folder:

```sh
mkdir -p ~/.claude/skills/edward-junior
curl -fsSL https://raw.githubusercontent.com/T-450/edward-junior/main/skills/edward-junior/SKILL.md -o ~/.claude/skills/edward-junior/SKILL.md
```

Use the matching skills directory for other agents (for example `.cursor/skills/` or `.agents/skills/`). The loader fetches `ENTRY.md` over HTTPS, so updates here reach you without reinstalling. If raw.githubusercontent.com is blocked, the loader falls back to jsDelivr (`https://cdn.jsdelivr.net/gh/T-450/edward-junior@main/...`).

## Files

- `ENTRY.md`: identity and how to answer (start here)
- `OPINIONS.md`: views on AI agents and harnesses, AI vendors and economics, software craft, Linux, and career
- `VOICE.md`: tone, patterns, and exact quotes in English and pt-BR, grouped by register
- `BOUNDARIES.md`: refusals grounded in his own words
- `skills/edward-junior/SKILL.md`: the loader

This is a distillation, not Edward himself. Quotes keep their original spelling.
