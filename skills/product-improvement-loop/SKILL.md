---
name: product-improvement-loop
description: Autonomously inspect and iteratively improve an existing product or feature when the user delegates product selection, implementation, and verification. Use for open-ended product improvement, not a one-off review or a narrowly specified change.
---

# Product Improvement Loop

Improve the existing product through evidence-backed, bounded iteration. A valid
outcome may be a verified improvement, a rollback, or a decision that no change
is justified.

## Use this skill when

- The user delegates open-ended selection, implementation, and verification of
  an improvement to an existing product or feature.
- The product and its current behavior can be inspected directly.

## Do not use

- For a read-only audit or review.
- For a narrowly specified change whose product decision has already been made.
- For greenfield product creation without an existing baseline.

## Instructions

### Establish the Baseline

Before changing anything:

1. Inspect the product, relevant code, documentation, tests, and available user
   or product evidence.
2. Determine what can actually be run, rendered, inspected, or tested.
3. Separate observed facts from reasonable inferences and unsupported
   assumptions.
4. Preserve existing functionality, user changes, architecture, and design
   language unless changing one is necessary for the selected outcome.

If no sufficiently valuable improvement is supported by the evidence, recommend
stopping without manufacturing work and use the investor gate below. Do not call
a candidate the "highest-impact" problem when the evidence supports only "best
available candidate."

Do not infer authorization to deploy, publish, purchase, delete user data,
contact external parties, or take other consequential external actions.

### Run the Improvement Loop

Run no more than five loops. A loop need not produce an implementation.

1. **Product:** Select the single best-supported valuable problem. Identify who
   is affected, why it matters, the supporting evidence, and the strongest
   competing opportunity. Reject speculative or marginal work.
2. **Design:** Choose the smallest coherent response. Consider UI, behavior,
   copy, engineering, documentation, or no change; avoid cosmetic churn.
3. **Engineering:** Assess feasibility, risk, reversibility, and proportionality.
   Follow existing patterns and avoid unrelated refactoring. Implement only when
   the rationale is coherent and the result can be verified.
4. **Review:** Inspect the real result. For UI, render and interact with it; for
   logic, run relevant tests and inspect behavior; for content or configuration,
   validate the resulting artifact. Check usability, accessibility, edge cases,
   failure states, regressions, and code quality against the baseline. Revise or
   roll back a weaker result.
5. **Decide:** Continue concrete fixable work without escalation. When Review
   passes, the team recommends stopping, a material decision remains unresolved,
   or new authority is required, read
   [references/governance.md](references/governance.md) and use its investor gate.

Treat roles as decision responsibilities, not simulated personalities. Combine
or abbreviate straightforward stages, allow one role to cover another when
separate judgment adds no value, and omit inactive roles from reporting. Never
skip problem justification, real verification, or Review for an implemented
change.

For each active role, report only:

```text
[Role] Verdict: proceed | revise | veto | approve | stop
Evidence: <decisive evidence>
Next action: <one concrete action or none>
```

### Resolve Disagreement Proportionally

Prefer inspection or a small test over discussion. Begin with a concise
objection containing the challenged decision, contrary evidence, material risk,
and proposed resolution.

For a material disagreement about value, scope, experience, architecture,
safety, accessibility, regression risk, or approval that evidence cannot cheaply
resolve, read [references/governance.md](references/governance.md) and use its
formal debate protocol. Do not use formal debate for routine choices or
preferences.

### Stop and Report

Stop when the investor returns **BACK**, **STOP**, or **BLOCKED**. At the
five-loop limit, use the investor gate for the final decision rather than
starting another loop. Ask the user only when the investor returns **BLOCKED**
for a consequential decision that cannot be resolved safely from available
evidence and authority.

The final report must state:

- Final status: approved, stopped, blocked, or loop limit reached
- Problems investigated and evidence used
- What changed and what was rejected
- Verification performed and actual results
- Remaining weaknesses, risks, and strongest unimplemented opportunity
