# Agent Skills

Portable skills for AI agents.

[![skills.sh](https://skills.sh/b/vivekkartha/agent-skills)](https://skills.sh/vivekkartha/agent-skills)

## Install

Install the Medium workflow:

```bash
npx skills add https://github.com/vivekkartha/medium-seo-publisher
```

Choose your agent when prompted. To install it for every supported agent, add
`--agent '*'`. Agents without a skills installer can read the skill's
`SKILL.md` and relative files in `references/`.

Use it with a plain request:

```text
Use medium-seo-publisher to research a topic and prepare a Medium article.
```

## Available skills

### `medium-seo-publisher`

Research attainable keywords, write voice-matched Medium articles, and publish
only when explicitly requested. [Open its dedicated repository.](https://github.com/vivekkartha/medium-seo-publisher)

### `product-improvement-loop`

Inspect an existing product, choose a supported improvement, implement it, and
verify the result. [Read its SKILL.md.](skills/product-improvement-loop/SKILL.md)
