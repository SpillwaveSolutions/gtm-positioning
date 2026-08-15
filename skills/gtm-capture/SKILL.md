---
name: gtm-capture
description: Capture a GTM Positioning noun into the shared second brain via the deterministic write helper.
---

# gtm-capture

## Process

1. Identify the noun type from the allowed list (see README).
2. Resolve identity: run `whoami`. If unclaimed, ask the user what to sign as, then `whoami --claim`. Do not invent a Grok Bot name.
3. Collect title, status, and optional typed links.
3. Write with the helper — do not hand-author frontmatter unless the user insists:

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/gtm_common.py" write \
  --bundle knowledge \
  --type Offer \
  --folder offers \
  --title "Example Offer" \
  --author "${SECOND_BRAIN_IDENTITY:?claim an identity first: brain.py whoami --claim}" \
  --tags "gtm"
```

4. Add typed links in a follow-up edit if needed (`rel` values from `docs/typed-edges.md`).
5. Validate.

Allowed types: Offer, PositioningStatement, MessagingPillar, ValueProposition, IdealCustomerProfile, CompetitiveAlternative, Objection, CaseStudy, ProofPoint, LandingPage, SiteStatus, TrafficSource, ConversionEvent, Campaign, Experiment, PricingNote, Packaging, Testimonial, BattleCard.
