# Longevity

A longevity science knowledge base powered by Claude Code. Describe what you want to optimize, get evidence-based protocols back — precise to the milligram, grounded in real science from 40+ books and live research.

No code, no dependencies. Just markdown files + Claude Code slash commands + git.

## How It Works

One file (`longevity-knowledge.md`) contains distilled longevity science from books like Attia's *Outlive*, Sinclair's *Lifespan*, Walker's *Why We Sleep*, and 35+ others across 10 categories. When you run a command, Claude reads this file into context — it activates deep knowledge that produces expert-caliber output instead of generic wellness advice.

The `/design` command also runs **live web research** on your specific topic before generating the protocol, so you always get current evidence alongside the foundational knowledge.

Protocols are saved as `.md` files. You iterate on them in conversation. Git tracks everything.

## Your Data

Drop personal health data into `data/` and the agent uses it to personalize every protocol to *your* actual biomarkers — not generic population averages.

**Supported data:**
- Blood work / lab panels (PDF, CSV, text)
- DNA test results (23andMe, AncestryDNA reports)
- Doctor recommendations and notes
- Wearable exports (Whoop, Oura, Apple Watch, Garmin — CSV or summary)
- DEXA / body composition scans
- CGM reports (continuous glucose monitor)
- VO2max / fitness test results
- Current supplement stack / medications

Just drop files into `data/` — the agent reads whatever's relevant when you run `/design`.

## Commands

| Command | Example | What it does |
|---|---|---|
| `/design` | `/design morning supplement stack for metabolic health, male 35` | Full protocol with live research + science notes. Saves to `protocols/` |
| `/quick` | `/quick zone 2 cardio program` | Terse protocol — interventions table + steps, nothing else |
| `/adjust` | `/adjust swap NMN for NR, add creatine 5g/day` | Edit the active protocol file in place |
| `/save-protocol` | `/save-protocol` | Mark protocol as final, git commit |
| `/find-protocol` | `/find-protocol sleep optimization` | Search saved protocols by name, topic, or keyword |
| `/save` | `/save` | Git add + commit + push everything |

## Typical Workflow

```
> /design comprehensive sleep optimization protocol, currently sleeping 6hrs

  → Claude reads longevity-knowledge.md
  → Researches latest sleep science
  → Generates protocol with interventions, doses, biomarkers
  → Saves to protocols/2026-02-15-sleep-optimization.md

> /adjust add magnesium threonate and reduce melatonin to 0.3mg

  → Updates the same file with revised supplement stack

> /adjust add HRV tracking as a biomarker

  → Adds to biomarker targets table

> /save-protocol

  → Marks as Final, commits to git
```

## Project Structure

```
longevity/
├── CLAUDE.md                    # Agent personality, rules, protocol format
├── longevity-knowledge.md       # The brain — 40+ books, 10 longevity science categories
├── .claude/
│   ├── settings.local.json
│   └── commands/                # 6 slash commands
├── data/                        # Your health data (blood work, wearables, DNA, etc.)
├── protocols/                   # Saved protocols (YYYY-MM-DD-slug.md)
└── README.md
```

## Knowledge Categories

The knowledge file covers:

1. **Overall longevity frameworks** — Medicine 3.0, the four horsemen, Blue Zones
2. **Exercise & physical performance** — VO2max, zone 2, strength, stability
3. **Nutrition & metabolic health** — insulin resistance, glucose, fasting, CGM
4. **Sleep science** — sleep architecture, circadian code, CBT-I
5. **Cognitive health & neurodegeneration** — BDNF, Alzheimer's prevention, brain energy
6. **Supplements & pharmacological interventions** — NAD+, rapamycin, metformin, evidence grading
7. **Stress, HRV & nervous system** — cortisol, vagal tone, breathwork, allostatic load
8. **Biomarkers & testing** — ApoB, DEXA, VO2max, functional blood panel ranges
9. **Hormones & endocrine optimization** — HRT, thyroid, testosterone, sex-specific physiology
10. **Aging biology** — hallmarks of aging, telomeres, senolytics, epigenetic reprogramming

## Setup

1. Clone this repo
2. Open the folder in Claude Code
3. Run `/design` with whatever you want to optimize
