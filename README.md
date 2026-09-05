# Agent Skills

A focused collection of reusable skills for AI coding agents.

[![skills.sh](https://skills.sh/b/vivekkartha/agent-skills)](https://skills.sh/vivekkartha/agent-skills)

Skills use the portable `SKILL.md` convention. Platform-specific metadata lives
inside each skill package so Codex, Grok, and other agent runtimes can be
supported without coupling the repository to one vendor.

## Available skills

### `product-improvement-loop`

Autonomously inspects an existing product, selects the strongest evidence-backed
improvement, implements the smallest coherent change, verifies the real result,
and uses bounded debate and an investor gate for material decisions.

### `medium-seo-publisher`

Research attainable keywords, write voice-matched Medium articles, and publish
only when explicitly requested. See its README for installation and use.

## Install

Install a skill with the Skills CLI:

```bash
npx skills add https://github.com/vivekkartha/agent-skills --skill medium-seo-publisher
```

Choose your agent when prompted. Agents without a skills installer can read the
skill's `SKILL.md` and relative reference files directly.

Invoke it with:

```text
Use medium-seo-publisher to research a topic and prepare a Medium article.
```
