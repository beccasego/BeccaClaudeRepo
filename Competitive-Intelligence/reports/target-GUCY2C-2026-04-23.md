# GUCY2C (GCC) — Target Landscape CI Report
**Date:** 2026-04-23
**Prepared by:** Claude Code
**Type:** Target Sweep

---

## TL;DR

GUCY2C (Guanylyl Cyclase C / GCC) is a near-universally expressed colorectal cancer target with a graveyard of failed clinical programs — two Takeda ADCs terminated for insufficient benefit, and Pfizer's T-cell engager discontinued in Phase 1 (2024). The field has pivoted sharply toward CAR-T, where ImmunoChina's IM96 showed a 40% ORR at the highest dose level in heavily pre-treated mCRC (ASCO 2024), with Phase 2 expected in 2025. The current clinical field is thin and dominated by CAR-T, with early-stage interest in theranostics and bispecific formats — leaving several modalities unexplored or underexplored.

> **Flag for Sego:** The ADC modality has failed twice with classical internalizing payloads. This creates a specific gap: non-internalizing ADC strategies (bystander/extracellular release payloads), novel formats, or non-ADC targeted delivery for this receptor-class target deserve fresh consideration.

---

## Expression Landscape

GUCY2C is normally expressed only on the luminal (apical) surface of intestinal epithelium — physiologically inaccessible to systemically administered drugs. In cancer, surface expression is aberrantly exposed, creating a "tumor-on" target profile. Ectopic expression also occurs in non-GI adenocarcinomas.

| Tumor Type | Expression Rate | Notes |
|---|---|---|
| Colorectal (primary) | ~98% | Near-universal; validated across histologies |
| Colorectal (metastatic) | ~81% | Preserved at metastatic sites |
| Esophageal adenocarcinoma | 59–68% | Ectopic; bile acid-induced |
| Gastric / GEJ adenocarcinoma | 59–68% | Ectopic; validated in early studies |
| Pancreatic | Expressed | Ectopic; emerging interest |
| Colorectal (lymph node micrometastases) | High | GUCY2C molecular staging clinical validation |

**Key biology:** GUCY2C is a receptor guanylyl cyclase; its endogenous ligands are guanylin and uroguanylin. In cancer cells, it acts as a tumor suppressor when activated — but this biology is orthogonal to its utility as a cell-surface target for targeted delivery.

**Internalization caveat:** GUCY2C does not internalize efficiently upon antibody binding, which has been a critical failure mode for classical ADC strategies (both Takeda programs failed). This is a known limitation of the target and should inform modality selection.

---

## Competitive Pipeline

### Terminated / Discontinued

| Drug | Company | Modality | Indication | Peak Phase | Outcome |
|---|---|---|---|---|---|
| MLN0264 | Takeda / Millennium | ADC (MMAE) | GI carcinoma, gastric/GEJ | Phase 1/2 | **Terminated** — PK similarity data; Phase 2 not initiated (NCT02391038) |
| TAK-164 | Takeda / ImmunoGen | ADC (DGN549 DNA alkylator) | Advanced GI cancers (GCC+) | Phase 1 | **Terminated** — "insufficient clinical benefit at RP2D" (NCT03449030) |
| PF-07062119 | Pfizer | Bispecific T-cell engager (GUCY2C × CD3) | GI cancers | Phase 1 | **Discontinued** (2024) — limited efficacy; Pfizer exited |

### Active — Clinical Stage

| Drug | Company | Modality | Phase | Indication | Key Data | Notes |
|---|---|---|---|---|---|---|
| IM96 (GCC19CART) | ImmunoChina (Beijing Immunochina Medicals) | CAR-T (autologous) | Phase 1 | mCRC (≥3L) | ORR 26.3% overall; 40% ORR and ~7 mo PFS at DL3 (ASCO 2024) | Phase 2 expected 2025; 20 patients enrolled through Dec 2023 |
| GCC-CART | Protheragen | CAR-T | Phase 1 (US) | relapsed/refractory mCRC | No public data yet | Phase 2 expected 2025 |

### Active — Preclinical / Early Research

| Program | Company/Group | Modality | Notes |
|---|---|---|---|
| PR15-7 theranostic platform | Academic (China) | Theranostic (89Zr PET, 177Lu RLT, NIR imaging) | GUCY2C antibody PR15-7 conjugated to multiple imaging + therapy payloads; J Nucl Med pub 2025/2026 |
| CDH17 × GUCY2C BsADC | Academic | Bispecific ADC (ferroptosis: RSL3 payload) | Preclinical; Cell Death Discovery 2025 |
| Anti-GUCY2C single domain Ab | Legend Biotech | Antibody platform | Limited disclosure; in development |
| AI-guided GUCY2C TCEs | Undisclosed | T-cell engager (multispecific) | AACR 2024 abstract 6721; multiple binding epitopes; preclinical |

### Historical — Completed Trials (Non-Therapeutic)

| Trial | Sponsor | Type | Status |
|---|---|---|---|
| [68Ga]MLN6907 PET (NCT02056015) | Takeda | Diagnostic / PET imaging agent | Completed |
| Ad5-hGCC-PADRE vaccine (NCT01972737) | Thomas Jefferson University | GI-cancer prevention vaccine (Stage I/II CRC) | Completed |
| GUCY2C agonist trials (linaclotide / plecanatide) | Academic / Bausch | Prevention via GUCY2C agonism | Ongoing prevention trials; PK barrier to colorectal delivery |

---

## Clinical Trials

| Trial ID | Drug | Sponsor | Phase | Indication | Status |
|---|---|---|---|---|---|
| NCT03449030 | TAK-164 | Takeda | Phase 1 | Advanced GI cancers (GCC+) | Terminated |
| NCT02391038 | MLN0264 | Takeda | Phase 1/2 | Advanced GI / gastric/GEJ | Terminated |
| NCT02056015 | [68Ga]MLN6907 | Takeda | Phase 1 | Metastatic CRC | Completed |
| NCT01972737 | Ad5-hGCC-PADRE | Thomas Jefferson U | Phase 1 | Stage I/II CRC | Completed |
| IM96 / GCC19CART | IM96 | ImmunoChina | Phase 1 | mCRC (≥3L) | Active (China) |
| GCC-CART | GCC-CART | Protheragen | Phase 1 | r/r mCRC | Active (US) |

---

## Patent Landscape

Searched via Justia Patents and firecrawl. Results are notable: the RLT space has **four separate patent filers** including two major pharma companies (AstraZeneca/Fusion, Bayer), one Chinese biotech, and Thomas Jefferson University.

### Radiopharmaceutical / RLT Patents

| Patent                          | Title                                                                | Assignee                                         | Priority Date | Modality                                             | Status                                       |
| ------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------ | ------------- | ---------------------------------------------------- | -------------------------------------------- |
| WO2023164777A1                  | GUCY2C-targeted radiopharmaceuticals and use thereof                 | **Fusion Pharmaceuticals Inc** (now AstraZeneca) | 2023-03-03    | Monocyclic peptide-chelator conjugate (RLT)          | WO Ceased; national phases under AstraZeneca |
| WO2023196821A2                  | Radiopharmaceutical conjugates targeting guanylyl cyclase C          | **Thomas Jefferson University**                  | 2022-04-04    | RLT conjugates                                       | Pending                                      |
| EP4552657A1 / PCT/EP2024/081175 | Radiopharmaceutical complexes and combinations (incl. GUCY2C + cMet) | **Bayer AG**                                     | 2023-11-07    | Multi-target RLT                                     | EP Ceased; PCT Pending                       |
| WO2022115799A1 / CN116888138A   | Radiopharmaceutical conjugates targeting guanylyl cyclase C          | **RayzeBio, Inc.** (now BMS)                     | 2021-11-30    | GCC-binding peptide + metal chelator conjugate (RLT) | CN + EP Pending; US national phase Abandoned |
| US20160303258A1                 | Compounds and compositions for imaging GCC-expressing cells          | Univ. Iowa / UNM / Millennium / Invicro          | 2014-12-03    | Radiopharmaceutical imaging                          | Abandoned (US + EP)                          |

> **RayzeBio note:** WO2022115799A1 does not appear on RayzeBio's Justia assignee page (only their SSTR2 portfolio is indexed there), but the patent document itself names RayzeBio Inc as assignee. The US national phase (US17/989,479) was abandoned; CN and EP national phases remain pending under BMS post-acquisition. This is a distinct program from their clinical pipeline (which focuses on SSTR2 and GPC3) — likely an early-stage or deprioritized asset.

### Antibody / Bispecific / TCE Patents

| Patent | Title | Assignee | Priority Date | Modality | Status |
|---|---|---|---|---|---|
| US11525010B2 | Antibodies specific for GUCY2c and uses thereof | **Pfizer Inc** | ~May 2018 | Anti-GUCY2C Ab + GUCY2C×CD3 bispecific TCE | **Granted**; expires 2039 |
| US20250066510A1 | GUCY2c antibodies and uses thereof | **Janssen Biotech / J&J** | 2023-08-07 | Anti-GUCY2C Ab + GUCY2C×CD3 bispecific | Pending |
| US20240165257 | Anti-GUCY2C antibody and uses thereof | **Heidelberg Pharma** (Torsten Hechler) | ~2023 | Anti-GUCY2C antibody (likely ATAC/amanitin-based ADC) | Pending |

> **Heidelberg Pharma flag:** Torsten Hechler is Heidelberg Pharma's head of chemistry; they use amanitin-based ADC payloads (ATAC technology). A GUCY2C patent from them likely signals an ATAC-ADC program — a non-MMAE, non-DNA-alkylator approach not yet tried clinically.

### Antibody / CAR-NK Patents

| Patent | Title | Assignee | Priority Date | Modality | Status |
|---|---|---|---|---|---|
| US20240115706A1 | GUCY2C binding polypeptide and uses thereof | **LG Chem Ltd** | 2021-04-07 | scFv / antibody / CAR-NK cells | Pending (pub April 2024) |

> **LG Chem flag:** Unexpected entrant. LG Chem's patent covers scFv, full-length antibodies, Fc fusions, and CAR-NK cells targeting GUCY2C — 18 distinct scFv sequences binding human, monkey, and mouse GUCY2C. This is a CAR-NK approach, distinct from all current CAR-T programs. LG Chem has been quietly building an oncology pipeline through their life sciences division.

### CAR-T Patents

| Patent | Title | Assignee | Priority Date | Status |
|---|---|---|---|---|
| US20210038648 | Anti-GUCY2C chimeric antigen receptor compositions | Thomas Jefferson University (Waldman lab) | ~2020 | Pending |
| US11970548B2 | Nanobody target GCC and uses in CAR-T | **Innovative Cellular Therapeutics (ICT)** | 2022-08-23 | **Granted** April 2024 |
| US12043654B2 | Anti-GCC antibody and CAR for digestive system cancer | **Innovative Cellular Therapeutics (ICT)** | 2021-05-26 | **Granted** July 2024 |
| US20260055209 | Nanobody target GCC for CAR-T (next-gen) | **Innovative Cellular Therapeutics (ICT)** | 2023-08-22 | Pending (pub Feb 2026) |
| WO2024131905A1 | Immune effector cells targeting GUCY2C and CD19 | Fapon Biotherapy Inc (China) | 2023-12-21 | Pending |

> **ICT flag:** Innovative Cellular Therapeutics has two **granted** GCC CAR-T patents and a new application — the most active CAR-T patent filer in the GUCY2C space. Likely the platform behind one of the active Chinese CAR-T clinical programs.

### IP Summary for Sego

- **RLT space is patent-crowded but clinically empty:** Five filers (AZ/Fusion, Bayer, TJU, RayzeBio/BMS, and the academic imaging group) hold RLT or radiopharmaceutical patents, but none have an active IND for GUCY2C RLT. Freedom to operate analysis warranted before entering this modality.
- **ADC space is open:** No active ADC patents from major players post-Takeda exit. Heidelberg Pharma (amanitin/ATAC) is the only new ADC filer — and not yet in clinic.
- **CAR-T IP is increasingly crowded:** ICT has granted patents covering nanobody-based GCC CAR-T; any new CAR-T program should assess freedom to operate against US11970548 and US12043654.
- **Pfizer's bispecific patent (US11525010) is granted and active through 2039** — covers the GUCY2C×CD3 format broadly.

---

## Recent Developments (2025–2026)

- **2026 (J Nucl Med)** — PR15-7 GUCY2C antibody conjugated to 89Zr, 177Lu, Cy5, ICG published as a multi-modal theranostic platform for CRC diagnosis and radiopharmaceutical therapy — preclinical.
- **2025 (Cell Death Discovery)** — Bispecific ADC targeting CDH17 and GUCY2C with ferroptosis-inducing payload RSL3 published as preclinical proof-of-concept for dual-antigen targeting in CRC.
- **AACR 2024** — AI-guided generation of novel GUCY2C-targeting TCEs presented (Abstract 6721); multiple epitope profiles and multispecific formats explored.
- **ASCO 2024** — IM96 Phase 1 data: 40% ORR at highest dose level in heavily pre-treated mCRC patients, median PFS ~7 months.
- **2024** — Pfizer officially discontinued PF-07062119 (GUCY2C × CD3 TCE) after Phase 1 failure; exits GUCY2C field.

---

## Scientific Publications (Selected, Last 12–18 Months)

- **Rong Z et al. (2026)** — "Construction and Evaluation of Guanylyl Cyclase C-Specific Antibody for Noninvasive Diagnosis and Targeted Therapy of Colorectal Cancer" — *J Nucl Med* — Develops PR15-7 antibody platform for multi-modal theranostic applications including 177Lu RLT.
- **Ramananda Y et al. (2025)** — "Catalytic region mimetics in Na+/H+ exchanger regulatory factor 4 suppress guanylate cyclase 2C activity" — *J Biol Chem* — Mechanistic study on GUCY2C regulation; not directly therapeutic.
- **CDH17-GUCY2C BsADC (2025)** — *Cell Death Discovery* — Bispecific ADC with ferroptosis payload showing preclinical anti-CRC activity.
- **GUCY2C-directed CAR-T (PMC5087292)** — Seminal study showing GUCY2C CAR-T opposes CRC metastases without autoimmunity due to luminal-only normal tissue expression.

---

## Competitive Implications for Sego

### Why GUCY2C is a compelling target
- Near-universal expression in CRC (the #2 GI cancer globally, ~150,000 US cases/yr)
- "Tumor-on" selectivity: luminal restriction in normal tissue means low systemic toxicity risk for targeted therapies
- Preserved in metastatic disease (~81%), including liver mets
- Ectopic expression expands to gastric, esophageal, pancreatic cancers
- Well-validated: 30+ years of biology; multiple clinical programs prove the hypothesis is sound

### Why it's been hard — and what that means
- **ADC internalization failure:** MLN0264 (MMAE) and TAK-164 (DGN549) both failed. The root cause is GUCY2C's poor internalization kinetics — classical ADC strategies requiring intracellular payload release are fundamentally challenged here.
- **T-cell engager failure:** PF-07062119 failed in Phase 1. Possible reasons: tumor microenvironment immunosuppression in CRC, insufficient T-cell infiltration, or efficacy/safety window issues.
- **CAR-T signal is real but nascent:** 40% ORR in 3L+ mCRC is meaningful, but autologous CAR-T faces manufacturing and access hurdles; allogeneic approaches not yet reported for GUCY2C.

### White Space / Opportunities

| Gap | Rationale |
|---|---|
| Non-internalizing ADC formats | Bystander-effect payloads, cell-surface cleavable linkers, or extracellular-release mechanisms could bypass the internalization problem |
| Allogeneic / off-the-shelf CAR-T | IM96 is autologous; allogeneic GUCY2C CAR-T would differentiate on access and manufacturing |
| Radiopharmaceutical therapy (RLT) | Theranostic platform is emerging (PR15-7); GUCY2C expression + luminal biology could enable locoregional RLT approaches |
| Earlier lines of CRC | All current CAR-T trials are 3L+; earlier line deployment with combination partners (IO, anti-VEGF) is unexplored |
| Non-CRC GI indications | Gastric/esophageal/pancreatic expression is under-prosecuted in current programs |
| Combination with immune priming | GUCY2C agonism (via linaclotide/plecanatide analogs with colorectal bioavailability) activates tumor-suppressive signaling — combination with immune therapy is scientifically rationale but unexplored clinically |

### Watch List
- **ImmunoChina IM96 Phase 2** — Will be the key data readout to watch; if ORR holds in Phase 2 it validates CAR-T as a real modality here
- **Protheragen GCC-CART Phase 1 US** — First US trial; regulatory and safety data will be informative
- **Legend Biotech GUCY2C program** — Company has CAR-T manufacturing expertise (Carvykti); disclosure of GUCY2C program timeline worth tracking
- **AI-guided TCE programs** — AACR 2024 abstract suggests active undisclosed companies; watch for IND filings

---

## Sources

- [TAK-164 ADC Review](https://www.adcreview.com/drugmap/tak-164/)
- [PF-07062119 discontinuation (Jacob Plieth / X)](https://x.com/JacobPlieth/status/1752361101512110226)
- [PF-07062119 preclinical data — CCR](https://aacrjournals.org/clincancerres/article/26/9/2188/83190/)
- [IM96 Phase I — ASCO 2024 abstract](https://ascopubs.org/doi/10.1200/JCO.2024.42.16_suppl.2518)
- [Novel GUCY2C CAR-T efficacy — ASCO 2023 abstract](https://ascopubs.org/doi/10.1200/JCO.2023.41.16_suppl.3559)
- [PR15-7 theranostic platform — J Nucl Med (2025)](https://jnm.snmjournals.org/content/early/2025/12/30/jnumed.125.270400)
- [CDH17-GUCY2C BsADC — Cell Death Discovery (2025)](https://www.nature.com/articles/s41420-025-02652-0)
- [AI-guided GUCY2C TCEs — AACR 2024 Abstract 6721](https://aacrjournals.org/cancerres/article/84/6_Supplement/6721/741217/)
- [GCC expression in GI tumors — PLOS One](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0189953)
- [GUCY2C as biomarker/target review — PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8293028/)
- [GUCY2C-directed CAR-T without autoimmunity — PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC5087292/)
- [ClinicalTrials.gov — NCT03449030 (TAK-164)](https://clinicaltrials.gov/study/NCT03449030)
- [ClinicalTrials.gov — NCT02391038 (MLN0264)](https://clinicaltrials.gov/study/NCT02391038)
- [ClinicalTrials.gov — NCT01972737 (GCC vaccine)](https://clinicaltrials.gov/study/NCT01972737)
- [Protheragen GCC-CART program](https://www.protheragen.com/available-projects/car-t-cells-targeting-gucy2c2-for-the-treatment-of-mcrc/)
- [WO2023164777A1 — Fusion Pharmaceuticals GUCY2C RLT patent (Justia)](https://patents.justia.com/patent/WO2023164777A1)
- [US11525010B2 — Pfizer GUCY2C×CD3 bispecific (Justia)](https://patents.justia.com/patent/11525010)
- [US20250066510A1 — Janssen GUCY2C antibodies (Google Patents)](https://patents.google.com/patent/US20250066510A1/en)
- [US11970548B2 — ICT GCC nanobody CAR-T (Justia)](https://patents.justia.com/patent/11970548)
- [US12043654B2 — ICT anti-GCC CAR for digestive cancer (Justia)](https://patents.justia.com/patent/12043654)
- [US20240165257 — Heidelberg Pharma anti-GUCY2C antibody (Justia)](https://patents.justia.com/patent/20240165257)
