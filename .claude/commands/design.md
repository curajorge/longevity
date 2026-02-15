---
description: "Generate a full longevity protocol with research + science notes"
argument-hint: "<goals, interventions, constraints — be casual>"
---

Read `longevity-knowledge.md` into context first — it contains the book-sourced science that makes your output excellent.

Then read `CLAUDE.md` for the protocol output format and rules.

**Research step:** Before generating the protocol, use WebSearch to find the latest evidence on the user's specific topic. Search for:
- Recent clinical trials or meta-analyses (last 2-3 years)
- Current dosing recommendations from longevity researchers
- Any safety updates or contraindication changes
- Summarize 2-3 key findings from the search to inform the protocol

Parse the user's input for: goals, specific interventions requested, constraints (age, conditions, current stack), time horizon, and category. Default to "Chronic" time horizon if not specified.

Generate a full protocol following the format in CLAUDE.md. Include:
- Precise intervention table with doses, mechanisms, and evidence levels
- Step-by-step implementation with timing and conditions
- Biomarker targets with testing frequency
- Risks and contraindications for every pharmacological intervention
- Quick Rationale grounded in the knowledge file + latest research

Save the protocol to `protocols/YYYY-MM-DD-slug.md` where the slug describes the protocol.

Tell the user the file path. This is now the active protocol — future `/adjust` commands will update it.

User wants: $ARGUMENTS
