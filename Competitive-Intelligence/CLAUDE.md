# CLAUDE.md — Competitive Intelligence

CI briefing system, competitor tracking, CI tooling. Root `CLAUDE.md` rules
apply. This file adds CI-specific context.

## Folder layout

- `competitors/` — profiles and notes on specific companies
- `market-analysis/` — market sizing, trends, positioning
- `reports/` — synthesized CI reports
- `sources/` — raw inputs, clippings, links to watch (incl. `alphasense/`, `beacon/`)
- `templates/` — CI report templates
- `CI tooling/` — CI automation, incl. `Sego-CI-Agent/`

## Monthly CI briefing system

Five indication-specific memos:

| Memo | Indication | Target(s) |
|---|---|---|
| 1 | Prostate / mCRPC | ACP3, KLK2 |
| 2 | CRC | CEACAM5 |
| 3 | Lung-squamous | CLDN1 |
| 4 | Lung-adeno | MUC1-C |
| 5 | Bladder | Nectin-4 |

Single-asset Tracker (Excel) is the source of truth. Three retrieval tracks:
(i) Tracker refresh, (ii) standalone non-asset searches, (iii) broad contextual
sweep. The automated agent lives in `CI tooling/Sego-CI-Agent/`.

## CI tooling landscape

Clean-sheet comparison ranks Gosset top. Beacon is the incumbent to benchmark at
renewal, not auto-retain. Causaly is the head-to-head competitor. Others
evaluated: Cortellis, Convoke, Convexia.

## Voice

Synthesized CI reports read as internal analysis: `style/becca-voice.md`.
Anything external-facing uses `style/sego-writing-style/`.
