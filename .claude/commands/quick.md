---
description: "Generate a terse protocol — no explanations"
argument-hint: "<goals, interventions, constraints>"
---

Read `longevity-knowledge.md` into context — same knowledge, minimal output.

Read `CLAUDE.md` for rules.

Parse the user's input.

Output ONLY:
1. Protocol name
2. Interventions table (dose, mechanism, evidence level)
3. Implementation steps (timing, doses, no explanations)

No rationale, no notes section, no prose. Just the protocol.

Save to `protocols/YYYY-MM-DD-slug.md`. Tell the user the file path.

User wants: $ARGUMENTS
