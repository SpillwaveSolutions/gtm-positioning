---
name: gtm-validate
description: Validate GTM Positioning concepts: required fields, types, and in-bundle links.
---

# gtm-validate

```bash
python3 "${CLAUDE_PLUGIN_ROOT}/scripts/gtm_common.py" validate --bundle knowledge
```

Fail on missing `type`/`title` or broken absolute links.
