# Sego CI - Sourcing and Scraping Design

**Purpose.** The reasoning doc for how the Tracer agent gathers information without missing things. Accumulates decisions and open questions across working sessions. The final locked, per-indication checklist lives in `source_checklist.md`; this doc is the "why" behind it. Started 2026-07-10.

---

## Core principle

Recall cannot be managed against an infinite denominator. "Did we miss anything?" is unanswerable until it is converted into a bounded, enumerable set of channels, each with a defined refresh cadence and a completeness check. Any competitive signal that cannot reach us through at least one enumerated channel is a structural blind spot. The design goal: every (signal type x geography) cell maps to at least one channel, ideally two for high-value cells, and every empty cell is declared explicitly rather than missed accidentally. Bias hard toward recall over precision: a missed competitor is worse than a false positive, which the Tracker's relevance field discards downstream.

---

## Decisions locked

1. **Aggregator posture (2026-07-10).** Paid aggregators (AlphaSense, Gosset, Sleuth) are a bridge, not a backbone. Uses: (i) seed - one-time upload to bootstrap the Tracker baseline; (ii) interim updates while subscriptions remain active; (iii) recall benchmark / known-answer set for the back-test (open thread 5). **Sunset risk: subscriptions expected to lapse later in 2026.** Implication: the independent free-API + China pipeline must be live before subscriptions lapse, or we lose both the update source and the benchmark at once. This moves the independent build forward in priority.
2. **China is the priority blind spot.** English sources (CT.gov, PubMed) systematically under-represent China-origin and early-stage assets. A China-native channel layer plus translated vocabulary is required, not optional. A China component is wanted in the web-search / RSS layer.
3. **Storage (ref, decided 2026-07-10).** Prototype in Excel; migrate source of truth to SQLite before Tracer read/write code is written. (See handoff brief open thread 1.)

---

## Coverage matrix - signal type x geography

Columns: US/EU (well-indexed English) | China | Other (JP/KR). Fill each cell with channel(s). Empty cell = declared blind spot.

| Signal type | US/EU | China | Other |
|---|---|---|---|
| Trial events | CT.gov (API) | chinadrugtrials.org.cn, ChiCTR (scrape) | WHO ICTRP |
| Publications | PubMed/PMC (API) | CNKI, Wanfang (sub) | PubMed |
| Preprints | bioRxiv/medRxiv (API) | ChinaXiv (scrape) | - |
| Conference | ASCO/AUA/ESMO/SNMMI/AACR | CSCO (scrape/manual) | - |
| Regulatory | openFDA, EMA | CDE, NMPA (scrape) | PMDA (JP) |
| Corporate/financial | SEC EDGAR (API) | HKEXnews (bilingual), STAR | - |
| Deal/BD | PR wires, sell-side, Endpoints | PharmaDJ, Endpoints China | - |
| Patents | USPTO/EPO, PatentsView, Lens | CNIPA (via Google Patents/Lens) | - |
| Preclinical/platform | preprints, posters, patents, company sites | ChinaXiv, CDE, patents | - |

Status: skeleton. Needs per-target refinement and identification of the double-covered high-value cells.

---

## Access tiers (= build effort)

- **Tier A - Structured API** (low effort, stable): CT.gov v2, PubMed/PMC, bioRxiv/medRxiv, openFDA, SEC EDGAR full-text, PatentsView / Lens.org, NIH RePORTER, Open Targets, ChEMBL.
- **Tier B - Feeds** (low-med): company IR RSS, PR wires (PRNewswire/BusinessWire), journal TOC RSS, FDA RSS, English-language China news RSS.
- **Tier C - Scrape** (high effort, fragile, needs browser agent): CDE, chinadrugtrials.org.cn, ChiCTR, HKEXnews, conference abstract portals, company pipeline pages, ChinaXiv.
- **Tier D - Subscription/manual**: AlphaSense, Gosset, Sleuth, Patsnap Synapse, PharmCube/Insight, Yaozh, CNKI, sell-side, KOL networks.

**Already wired as live connectors in this Cowork environment:** ClinicalTrials.gov, PubMed/PMC (full-text article server), bioRxiv/medRxiv, Open Targets, ChEMBL, a browser agent (for Tier C), and M365 (Outlook/SharePoint). Build effort therefore concentrates on Tier C (China + conferences) and the Tier A pieces not yet wired (SEC EDGAR, openFDA, patents, NIH RePORTER).

---

## China layer (deep dive, 2026-07-10)

### Channels
| Signal | Native channel | Access | Notes |
|---|---|---|---|
| Trial registrations | chinadrugtrials.org.cn (CDE registry) | Scrape | Primary. Chinese UI. Not in CT.gov. |
| Academic trials | ChiCTR (chictr.org.cn) | Scrape / WHO ICTRP | WHO primary registry |
| Regulatory / IND / priority review | CDE (cde.org.cn), NMPA (nmpa.gov.cn) | Scrape | Acceptance + review status = earliest signal |
| Corporate filings | HKEXnews (hkexnews.hk) | Scrape / feed | Chapter-18A biotechs; often bilingual (English available) |
| US-listed China ADRs | SEC EDGAR | API | BeiGene, Zai Lab, etc. (English) |
| Conference | CSCO abstracts | Scrape / manual | China's ASCO |
| Patents | CNIPA (via Google Patents / Lens.org) | API (machine-translated) | Early target-intent signal |
| Literature | CNKI, Wanfang | Subscription | Chinese journals |
| Preprints | ChinaXiv (chinaxiv.org) | Scrape | CAS preprint server |
| Aggregated intel | Patsnap Synapse, PharmCube/Insight, Yaozh | Subscription | Patsnap has English UI + API + strong China coverage - most build-friendly paid China source |

Genuinely Chinese-only must-scrape core: CDE + chinadrugtrials + ChiCTR + CSCO + ChinaXiv. HKEX and Patsnap are substantially English-accessible.

### China RSS / web-search layer
- English-language China-focused news feeds (have RSS, high yield): PharmaDJ, Endpoints News China, Fierce Biotech Asia, BioCentury China.
- Scheduled browser sweeps of Chinese-only registries (CDE / chinadrugtrials / ChiCTR) filtered by the six targets + indications, on a cadence with a "last swept" watermark.

### Translated vocabulary (STARTER - needs native oncology reviewer validation before first live sweep)
| Concept | Chinese |
|---|---|
| Prostate cancer / mCRPC | 前列腺癌 / 转移性去势抵抗性前列腺癌 |
| Colorectal cancer | 结直肠癌 (结肠癌 / 直肠癌) |
| NSCLC squamous / adeno | 肺鳞癌 / 肺腺癌 |
| Urothelial / bladder | 尿路上皮癌 / 膀胱癌 |
| Radioligand therapy / radiopharmaceutical | 放射性配体疗法 / 放射性药物 / 放射性核素治疗 |
| ADC | 抗体偶联药物 |

Target symbols (KLK2, ACP3, CEACAM5, CLDN1, MUC1-C, Nectin-4) and isotopes (Ac-225, Lu-177, Pb-212) generally appear as-is in Chinese text and carry over.

---

## Controlled vocabulary (all sources) - TO BUILD

Per-target query dictionary driving every keyword source: gene symbol + all aliases + protein names + isotope terms + modality terms + Chinese synonyms. Bad queries miss signals even from good sources, so this is a first-class design artifact, not an afterthought.

---

## Seed report inventory (known-answer set for back-test)

In `04_reference-examples/`: gosset-klk2-assessment, gosset-nectin4-assessment, gosset-tl1a-ibd-database (+v2), il13-il4ra-efficacy-comparison, mg-soc-report, nectin4-target-file, alphasense-sqnsclc-report, mcrpc-rlt-ascoaua-2026, sleuth-china-landscape-analysis, sleuth-2l-nsclc-analysis.
China seed sources (merged into Tracker 2026-07-10): `20260513_China_RLT Co List.xlsx` (39 companies + 18 academic programs + target overlap; Beacon/PharmCube-sourced) and `20260720_SegoTx_China Strategy_v2.pptx` (deck slides 7-9 = ~47 preclinical China assets). Full landscape now lives in Tracker tabs China Landscape / China Academic / China Target Overlap / China Preclin (deck); 21 qualifying assets promoted to main Tracker rows.
Beacon ADC dataset (merged 2026-07-10): 4 exports (targets set 68; NSCLC 342; CRC 291; Prostate 226 Active ADCs). 84 unique Sego-target ADC/RLT assets promoted to Tracker rows (deduped); full indication landscapes kept as tabs Beacon ADC - NSCLC/CRC/Prostate. Note: targets-set export excluded Nectin-4. Precision caveat: Beacon "MUC-1"/"MUC1*"/"tMUC1" tagged as MUC1-C in the Sego-target column but are broad-MUC1, not confirmed C-terminal; E (Target[s]) preserves the raw Beacon string.
**Pending:** further seed reports from Becca; controlled-vocabulary dictionary (China + Beacon asset/sponsor names now available as raw material); refine MUC1-C vs broad-MUC1 tagging.

---

## Open questions / next

- Which high-value matrix cells get double coverage (>=2 independent channels)?
- Build the per-target controlled vocabulary dictionary (incl. validated Chinese terms).
- Decide the one paid China source to retain short-term (Patsnap Synapse is the leading candidate).
- Define refresh cadence + watermark model per channel.
- Add Becca's additional seed reports.
- Design the recall back-test (diff our output vs aggregator known-answer set) before subscriptions lapse.
