---
name: gtm-init
description: Scaffold the GTM Positioning catalogs in a shared second-brain bundle.
---

# gtm-init

Create the catalogs this plugin owns inside a shared knowledge root.

## Process

1. Confirm target (default `knowledge/`).
2. Run:

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/gtm_common.py" init-bundle \
  --bundle knowledge \
  --title "GTM Positioning" \
  --catalogs "offers,positioning,campaigns,icps,proof-points,battle-cards,experiments"
```

3. Point the user at `sample-knowledge/` for a fictional demo.

## Done when

- `knowledge/index.md` exists
- Each owned catalog has `index.md`
