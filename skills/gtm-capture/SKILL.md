---
name: gtm-capture
description: Capture a GTM Positioning noun into the shared second brain via the deterministic write helper.
---

# gtm-capture

## Process

1. Identify the noun type from the allowed list (see README).
2. Collect title, status, author identity, and optional typed links.
3. Write with the helper — do not hand-author frontmatter unless the user insists:

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/gtm_common.py" write \
  --bundle knowledge \
  --type Offer \
  --folder offers \
  --title "Example Offer" \
  --author "Grok Bot: GTM Positioning" \
  --tags "gtm"
```

4. Add typed links in a follow-up edit if needed (`rel` values from `docs/typed-edges.md`).
5. Validate.

Allowed types: Offer, PositioningStatement, MessagingPillar, ValueProposition, IdealCustomerProfile, CompetitiveAlternative, Objection, CaseStudy, ProofPoint, LandingPage, SiteStatus, TrafficSource, ConversionEvent, Campaign, Experiment, PricingNote, Packaging, Testimonial, BattleCard.
