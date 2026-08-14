# GTM Positioning

Go-to-market ContentPack: offers, positioning, messaging pillars, ICPs, campaigns, battle cards, and proof points.

MIT. Dual-host: **Claude Code**, **Grok Build**, and **Codex** (Agent Skill Standard). Writes OKF Markdown + YAML into a shared second-brain bundle so other agents and local jobs can read the same graph.

## Install

```bash
# Claude Code
/plugin marketplace add SpillwaveSolutions/gtm-positioning
/plugin install gtm-positioning@SpillwaveSolutions

# Skilz CLI
skilz install SpillwaveSolutions/gtm-positioning
```

Point the plugin at a shared knowledge root (default `knowledge/`). All sibling ContentPack plugins write into the same tree.

## Skills

| Skill | What it does |
|-------|----------------|
| `/gtm-init` | Scaffold the catalogs this plugin owns |
| `/gtm-capture` | Capture a noun into the shared second brain (deterministic write) |
| `/gtm-pack` | Build a bounded ContextPack from a root concept |
| `/gtm-validate` | Validate frontmatter, types, and links |
| `/gtm-doctor` | Health check of the bundle this plugin owns |

## Nouns this plugin may write

| Type | Meaning |
|------|---------|
| `Offer` | Sellable engagement or product |
| `PositioningStatement` | How we win the category |
| `MessagingPillar` | Repeatable message |
| `ValueProposition` | Why it matters to a buyer |
| `IdealCustomerProfile` | Who we sell to |
| `CompetitiveAlternative` | What they would do instead |
| `Objection` | GTM-level buyer concern |
| `CaseStudy` | Proof story |
| `ProofPoint` | Quantified or qualitative proof |
| `LandingPage` | Page that carries an offer |
| `SiteStatus` | Current site / offer page state |
| `TrafficSource` | How people arrive |
| `ConversionEvent` | Desired action |
| `Campaign` | GTM motion |
| `Experiment` | Message or page test |
| `PricingNote` | Packaging or price signal |
| `Packaging` | How the offer is bundled |
| `Testimonial` | Customer quote |
| `BattleCard` | How to talk vs an alternative |

## Relationships

| `rel` | Meaning |
|-------|---------|
| `owned_by` | GTM owner identity |
| `promoted_by` | Campaign or article promotes offer |
| `aimed_at` | Offer aimed at an ICP |
| `supported_by` | Proof point or case study |
| `competes_with` | Alternative |
| `tested_by` | Experiment |
| `related_to` | Soft association |
| `originates_from` | Provenance |

## Catalogs

- `offers/`
- `positioning/`
- `campaigns/`
- `icps/`
- `proof-points/`
- `battle-cards/`
- `experiments/`

## Deterministic write boundary

The model proposes. Schema-enforced scripts commit:

```bash
python3 scripts/gtm_common.py write \
  --bundle knowledge \
  --type Offer \
  --folder offers \
  --title "Example" \
  --author "Grok Bot: GTM Positioning"
```

Never invent `rel` values. Never write types owned by another plugin.



## Related plugins

- [second-brain-core](https://github.com/SpillwaveSolutions/second-brain-core) — shared pack engine and typed-edge conventions
- [project-knowledge-capture](https://github.com/SpillwaveSolutions/project-knowledge-capture) — the “why” second brain
- [system-architecture-capture](https://github.com/SpillwaveSolutions/system-architecture-capture) — the “what is running” second brain
- [wiki_ticket_sdd](https://github.com/SpillwaveSolutions/wiki_ticket_sdd) — visible work log

## License

MIT. Copyright 2026 Rick Hightower / contributors.
