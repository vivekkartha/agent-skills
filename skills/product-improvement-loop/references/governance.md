# Governance for Material Decisions

Read this reference only when a material disagreement requires formal debate or
when a reviewed result is ready for the investor gate.

## Formal Debate

Invoke debate using one precise decision and only the relevant roles:

```text
Invoke debate
Decision: <one precise decision>
Reason: <why it is material>
Participants: <relevant roles>
```

Use at most two rounds:

1. Each participant gives its position, evidence, principal risk, and
   recommendation.
2. Each addresses the strongest opposing argument, states what evidence would
   change its position, and gives a final recommendation.

Consensus is not required. Do not implement while a foundational decision is
unresolved. Debate occurs within the current improvement loop and the same issue
must not be debated again without materially new evidence.

Decision ownership:

- Product owns prioritization and user-value decisions.
- Design owns interaction and experience decisions within the accepted goal.
- Engineering owns technical feasibility and implementation safety.
- Review may veto material quality, accessibility, regression, or verification
  failures.
- The investor resolves only material value, scope, or stop/continue deadlocks
  remaining after debate.

Record the decision, owner, supporting evidence, rationale, unresolved dissent,
and next action.

## Investor Gate

The investor is a final or exceptional decision gate, not a routine participant.
Invoke it only when Review has passed and the team recommends approval, the team
recommends stopping, a material value or scope deadlock remains after debate, or
continuing requires authority beyond the current mandate.

Evaluate whether the result creates meaningful value, is coherent and usable,
is supported by actual evidence, has no unresolved material regression or
quality failure, and is proportionate in cost and risk.

Return one verdict:

- **BACK:** approve the reviewed result and stop.
- **CONTINUE:** name the single most important outcome required next.
- **STOP:** further investment is unjustified; explain why.
- **BLOCKED:** essential authority or information is missing.

Efficiently rejecting weak or unnecessary work is a positive result. Do not use
the investor persona to manufacture anger, urgency, or punishment.
