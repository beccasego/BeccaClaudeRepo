# Sego CI Agent — Project Handoff Brief

**Purpose of this document.** This is the starting context for a Cowork project to build Sego's monthly Competitive Intelligence (CI) briefing system. It captures every locked design decision, the open threads still to resolve, the artifacts already built, and the recommended folder structure. Read this first; it replaces the reasoning from the originating chat so nothing gets re-litigated.

**Owner:** Becca Levin (Head of Strategy). **Automated agent:** named **Tracer** (builder TBD). **Primary readers of the output:** Jeevan Virk (CEO), Richard Tavare (Research), Greg Mullen (CMO / Clinical Development).

---

## 1. What we are building

A monthly CI briefing system for Sego's oncology programs, with two artifacts and (eventually) an agent that produces them.

- **The Tracker** — one structured store, the source of truth. One row per program × indication. All Sego-relevant competitor assets across all indications live here.
- **Per-indication memos** — one memo per indication, each a filtered view of the Tracker plus reasoning. Not one giant memo; the indication is the memo boundary.
- **The agent** (later, named **Tracer**) — refreshes the Tracker and generates the memos each month.

The core architecture is **DB → views**: the Tracker is the database; each memo is a view of it, scoped to one indication, enriched with reasoning and non-tracker searches.

---

## 2. Locked decisions

### 2.1 One memo per indication
The indication is the memo boundary because a CI memo is only coherent if everything in it shares a standard of care, competitive set, and patient population. Do not mix indications in one memo.

| Memo | Indication scope | Sego targets |
|---|---|---|
| Prostate | mCRPC (± mHSPC where earlier-line moves matter) | ACP3, KLK2 |
| CRC | Stage II/III early **and** metastatic, broadly | CEACAM5 |
| Lung — squamous | metastatic sqNSCLC | CLDN1 |
| Lung — adeno | metastatic non-sq NSCLC | MUC1-C |
| Bladder (possible) | urothelial | Nectin-4 |

Lung is two separate memos (squamous vs adeno diverge on SOC and pipeline). CRC spans early (Stage II/III) through metastatic, so its SOC section carries two settings, not one sequence.

### 2.2 Memo section structure (finalized)
Order, as built in the prostate master template:

1. **Executive summary** — 3–5 bullets, each a movement plus its implication.
2. **Movements this cycle** — the "what changed" table (Development / Target / Stage / Relevance / So-what / Status), sorted by relevance. Leads the substance. Strategically central "No change" rows are shown so the reader sees they were checked.
3. **Standard of care: where it is, where it is heading** — the narrative spine. Three beats: *where it is* → *where it's heading* → *did this cycle shift it?* Includes the **standing SOC-by-line map** (rows = lines of therapy; columns = current SOC + benchmark; a "Moved this cycle?" flag). This table is a reference map, NOT a new-data table — new data is Section 2's job.
4. **Target watch** — one subsection per Sego target, each tying the cycle's movement back to the SOC trajectory (what changed / how the SOC move affects the target / TPP implication).
5. **Primary competition being watched** — standing watchlist, ~10 molecules, two types: *SOC-movers* (late-stage, could reset SOC) and *shared-target* (hits a Sego target directly). Low churn month to month.
6. **China signals** — standing box for China-origin / early / preclinical signals; explicit "none this cycle" when empty.
7. **Landscape shifts (non-asset)** — treatment guidelines (NCCN/ESMO/EAU) and diagnostics/biomarker shifts. NOT tracker-derived (see 2.4).
8. **Catalyst calendar** — next ~12 months, from Tracker catalyst fields.
9. **Method and sources** — coverage statement + dated source list.

### 2.3 Design principles baked into the memo
- **Answer-first**: every section opens with a bold claim line stating the takeaway.
- **Narrative connective tissue**: the SOC-trajectory beats ("current SOC is X, next shift is Y, this cycle did/didn't move it") are the difference between a strategist's memo and a data dump. Most months "did it shift?" = "no," which is itself the signal.
- **Explicit no-change**: silence never means "nothing happened." State it.
- **Domain tagging**: preclinical vs clinical, and imaging vs therapeutic, tagged per claim (critical for RLT).
- **All modalities**: RLT, ADC, bispecific/TCE, small molecule, cell therapy, vaccine. Therapeutics primary; imaging agents tracked and tagged.
- **Sego house style**: no em dashes; roman numerals for in-sentence lists; minimal bold-for-emphasis in running prose. (The sub-labels like "What changed this cycle" are a deliberate scannability deviation — revisit if unwanted.)

### 2.4 What is and isn't in the Tracker
- **In the Tracker**: discrete, structured, per-asset facts. Label expansions are asset-level events and live in the relevant asset's row (they flow into Movements). Regulatory *designations* (BTD, Fast Track) are low-signal — not tracked.
- **NOT in the Tracker**: treatment guidelines and diagnostic/biomarker shifts. These are run as independent per-cycle searches when composing the memo (Section 7). No isotope-supply tracking at all (explicitly dropped).

### 2.5 The three-track monthly assembly (critical for the agent build)
The memo is **not** a template mechanically rendered from the Tracker. It is a reasoning step combining three retrieval tracks plus the prior memo:

| Track | Feeds | Source | Memory model |
|---|---|---|---|
| 1. Tracker refresh | Movements, watchlist, target facts, catalysts | Asset DB (structured, per-program) | Persistent; deltas = DB diff |
| 2. Non-asset searches | Landscape shifts (guidelines, diagnostics) | Standalone per-cycle searches | No DB; "what changed" reasoned vs prior memo |
| 3. Broad contextual sweep | SOC trajectory, exec summary, all "so what" synthesis | Open-ended field-level search each cycle | No finite denominator — highest recall risk |

Implications for the build:
- This is a **research agent that uses the Tracker as one input**, not an ETL job. Track 3 (the broad sweep) is the harder, more valuable half and the part most exposed to silent misses.
- The generation step must ingest the **prior memo** to reason about what actually shifted (especially for Tracks 2 and 3, which have no DB diff).

### 2.6 Tracker schema (built)
27 fields in 5 groups, one row per program × indication:
- **Identity**: Program/Asset, Sponsor, Sponsor type, China-based?, Target(s), Sego target touched, Indication, Line of therapy, **NCT number** (the join key — used to match programs to trial records and dedupe).
- **Modality**: Modality, Isotope (if RLT), Imaging vs therapeutic.
- **Stage & evidence**: Highest phase, Evidence tier, Key efficacy readout (holds endpoint values so on-demand endpoint comparisons work), Key safety signal, RP2D/dose status.
- **Competitive read**: Relevance to Sego (Validates/Threatens/Reprices/Neutral), TPP/positioning implication.
- **Delta engine**: First-seen, Last-updated, Status (NEW/UPDATED/No change/Deprioritized), What changed this cycle, Next catalyst, Catalyst date, Source, Source date.

Enum columns use dropdowns. A **Legend tab** documents usage, enums, and on-demand-view concepts (endpoint comparison, China filter, target dossier filter).

---

## 3. Open threads (still to resolve)

1. **Storage format for the agent. [DECIDED 2026-07-10]** The xlsx is a good *human view / prototype store* but a poor *source of truth* for code (opaque binary, unreadable diffs, no validation). Google Sheets is not available (not a Google-enabled company). **Decision: prototype in Excel now; migrate the source of truth to SQLite before Tracer's read/write code is written, then emit the xlsx + memo as generated views.** Rationale: SQLite's payoff (enum validation, auditable NEW/UPDATED/No-change diffs, safe programmatic writes) only matters once code owns the monthly read/write, which does not exist yet; meanwhile the schema will still be stress-tested (e.g. cloning prostate to CRC), and that churn is easier in Excel. The migration is a cheap one-time script because the schema is defined. Hard rule: SQLite must be in place before agent read/write logic is built, never after (else that logic is thrown away).
2. **Cross-indication signals.** Some developments (platform-level reads, a China RDC entrant hitting multiple targets) matter across memos. Recommendation: light repetition into each relevant memo rather than a separate document, so each memo stands alone. Confirm.
3. **Source list finalization.** Confirmed required: ClinicalTrials.gov, PubMed, bioRxiv, conference proceedings (ASCO/AUA/ESMO/SNMMI/AACR), treatment guidelines (NCCN/ESMO/EAU), FDA CDx/label actions, company disclosures, China CDE + Chinese-language preprints, sell-side/trade coverage. Full per-indication source checklist still to be locked (drives the source-coverage audit).
4. **Multi-indication dedup rule.** One row per program × indication means multi-indication assets spawn sibling rows. The agent needs a rule to keep shared attributes in sync across an asset's rows.
5. **Back-testing / recall validation** (parked, but flagged). How to pressure-test that updates comprehensively capture movement. Methods identified: recall vs known-answer set (back-test on the uploaded docs' time window), seeded canaries, conference-abstract reconciliation, source-coverage audit, delta-integrity checks (re-fetch by NCT), human spot-audit. Turn "is it working?" into a standing recall metric. Not yet built.
6. **The Tracer agent spec** — the culminating deliverable. Should encode: the three-track assembly (2.5), the tracker schema (2.6), the two retrieval routines (tracker refresh vs standalone non-asset searches), the storage decision (open thread 1), the dedup rule (4), and the source checklist (3).

---

## 4. Recommended Cowork folder structure

```
Sego-CI-Agent/
├── 00_brief/
│   └── Sego_CI_Agent_Handoff_Brief.md      ← this document
├── 01_tracker/
│   └── Sego_CI_Tracker.xlsx                 ← the built tracker (schema + seed rows)
├── 02_memo-templates/
│   └── Sego_CI_Memo_Prostate_Template.docx  ← the master template; clone per indication
├── 03_memos/                                ← generated monthly memos live here
│   ├── prostate/
│   ├── crc/
│   ├── lung-squamous/
│   ├── lung-adeno/
│   └── bladder/
├── 04_reference-examples/                   ← the source examples that shaped the design
│   ├── gosset-klk2-assessment.pdf
│   ├── gosset-nectin4-assessment.pdf
│   ├── gosset-tl1a-ibd-database.xlsx
│   ├── il13-il4ra-efficacy-comparison.xlsx
│   ├── mg-soc-report.docx
│   ├── nectin4-target-file.md
│   ├── alphasense-sqnsclc-report.pdf
│   └── mcrpc-rlt-ascoaua-2026.pdf
├── 05_agent-spec/                           ← Tracer's build spec (to be written)
│   └── (tracer_spec.md — TBD)
└── 06_sources/                              ← per-indication source checklists (to be locked)
    └── (source_checklist.md — TBD)
```

### Prompt for Cowork to set up the structure
> Create the folder structure above under a top-level project folder `Sego-CI-Agent/`. Place this brief in `00_brief/`, the tracker in `01_tracker/`, the memo template in `02_memo-templates/`, and the reference example files I'm providing into `04_reference-examples/` (rename them to the tidy names shown). Create the empty `03_memos/` indication subfolders, and stub `05_agent-spec/agent_spec.md` and `06_sources/source_checklist.md` as empty files with a one-line header each. Then read the brief in full and confirm you understand the locked decisions and open threads before we start work.

---

## 5. Suggested first moves in Cowork
Pick up from the open threads, in a sensible order:
1. Decide storage format (thread 1) — it gates the agent design.
2. Lock the source checklist (thread 3) — it gates recall and the non-asset searches.
3. Clone the prostate template to a second indication (e.g. CRC, to stress-test the two-setting SOC section) — confirms the template generalizes.
4. Draft the Tracer agent spec (thread 6), pulling in the three-track model and schema.
5. (Later) Build the back-test harness (thread 5) to get a baseline recall number before trusting the agent.
