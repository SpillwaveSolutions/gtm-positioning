# Typed edges — GTM Positioning

Direction matters. Packs follow outbound edges by default.

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

Unknown `rel` values are treated as `info` by validation. Do not invent new names in this plugin.
