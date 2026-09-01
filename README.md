# Agent Skills

A focused collection of reusable skills for AI coding agents.

Skills use the portable `SKILL.md` convention. Platform-specific metadata lives
inside each skill package so Codex, Grok, and other agent runtimes can be
supported without coupling the repository to one vendor.

## Available skills

### `product-improvement-loop`

Autonomously inspects an existing product, selects the strongest evidence-backed
improvement, implements the smallest coherent change, verifies the real result,
and uses bounded debate and an investor gate for material decisions.

## Install for Codex

Copy a skill into the Codex skills directory:

```bash
cp -R skills/product-improvement-loop ~/.codex/skills/
```

Invoke it with:

```text
$product-improvement-loop
```
