# AEPT-AI Contributor Commons Verification

- **Verification date:** July 29, 2026
- **Status:** PASS

## Browser and interaction checks

The interactive HTML was loaded in headless Chromium and tested at:

| Viewport | Document width | Horizontal overflow | Console errors | Minimum visible button height |
|---|---:|---:|---:|---:|
| Desktop, 1440 x 1000 | 1440 px | 0 elements | 0 | 76 px |
| Tablet, 768 x 1024 | 768 px | 0 elements | 0 | 66 px |
| Mobile, 390 x 844 | 390 px | 0 elements | 0 | 66 px |

The following interactions passed:

- All three license-route tabs update the route title, facts, market label, and warning.
- Arrow-key tab navigation updates the selected route and focus.
- Desktop mind-map branch selection updates the accessible detail panel.
- Exactly one route remains selected.
- Exactly one desktop mind-map branch remains pressed.
- All 16 displayed primary-source links use HTTPS.

## Machine-vision gate

Visual inspection was paired with deterministic DOM measurement:

- Desktop hero: no clipping, overlap, or illegible text observed.
- Desktop mind map: all six nodes, branch connectors, core promise, and labels remain inside the graph boundary.
- Mobile hero: type wraps without horizontal clipping.
- Mobile mind map: the graph changes to a readable six-card tree.
- Decorative desktop flow arrows are removed at mobile width.
- Quantitative overflow count is zero at all tested widths.

## SHA-256 artifact hashes

```text
B6F4CDE303DD83B06D60525C4B1B8D85BF508EAC9F75EF0039F2788AEF8969B3  AEPT-AI-Contributor-Commons-Blueprint-2026-07-29.md
801CB82CF757C428A1BF61337A9840580BEC18D5F4D8CE3C96DD2F81EF16D9B2  AEPT-AI-Contributor-Commons-Mind-Map-2026-07-29.html
B13ED246E888C82D58B626C6D58AAAEA926F8CEC72CA1CB4EF8D75E0485982E2  AEPT-AI-Contributor-Commons-Mind-Map-Preview.png
```
