# Sego Therapeutics — DD Response Playbook

**Purpose:** Canonical answers to recurring diligence themes. Refine over time as positioning evolves. Use as the source of truth when drafting investor-specific DD responses.

**Last updated:** 2026-05-27

**Source docs:** Avidity (Apr 2026), Polaris (May 2026), Avego (May 2026), NVF (May 2026, finalized), Running List (ongoing)

### Answer style & length (calibrated from NVF finalized responses)
- 8–10 sentences per question, ~1–2 short paragraphs
- First-person plural ("We believe," "We plan," "We'll hold off")
- Conversational but precise; fewer granular numbers than internal docs
- Use "Note:" sections for caveats, IP sensitivity, or secondary points
- "Small molecules and peptides" (not just "cyclic peptides") when describing Sego's binder formats
- References inline as (Last name, Journal, Year); omit URLs in investor-facing docs
- When a program is deprioritized, lead with the positive reason (BD opportunity), not the weakness

---

## How to Use This Playbook

Each section maps to a recurring DD theme. Within each theme:
- **Core position** = the answer-first statement investors should walk away with
- **Supporting detail** = quantitative backing and key proof points
- **Key references** = citations used in prior responses
- **Asked by** = which investors raised this (to anticipate follow-ups)

---

## 1. Target Selection Strategy

**Core position:** Sego's target selection is RLT-bespoke — not lifted from ADC or IO target lists. We evaluate tumor-specific *accessibility* (not just expression), prioritize novel targets with few competing RLT programs, and set an expression bar deliberately above PSMA.

**Supporting detail:**
- IHC H-scores of 200–300, expressed in >60% of tumor cells (vs PSMA H-score 150–200)
- Copy number alone is insufficient; membrane localization, internalization, recycling rate, and expression homogeneity all matter
- Calibration benchmarks: PSMA (~200K copies, H-score 150–200), SSTR2 (~50K copies, H-score 100–150), DLL3 (~6K copies, H-score 10–50)
- Tumor-specific accessibility paradigm: targets like CLDN1 and CEACAM5 are shielded by polarity in healthy tissue but exposed in tumors
- 40 targets evaluated; 6 prioritized (ACP3, KLK2, CLDN1, MUC1-C, CEACAM5, GCC → GCC deprioritized to make room for in-license)
- Additional targets under deep diligence: tight/adherens junction proteins (claudins, cadherins, nectins) and apically expressed targets (mucins)

**Key references:**
- PSMA copy number / H-score benchmarks (internal analysis)

**Asked by:** Avidity, Polaris, Running List

---

## 2. Isotope Selection & Chelator Strategy

**Core position:** 225Ac is our primary therapeutic isotope; 161Tb is our differentiated second isotope for mixed disease burden. 68Ga and 177Lu are paired imaging/benchmarking isotopes. A single DOTA/DOTAGA chelator covers all four, eliminating manufacturing complexity.

**Supporting detail:**

### Half-life "mismatch" (peptide clearance vs isotope half-life)
- We are NOT trying to pair isotope/serum half-life — Lutathera and Pluvicto don't either
- Same format (peptides/small molecules) and isotope half-life (7–10 days) as approved RLTs
- Med chem optimization drives: (1) high-affinity rapid tumor uptake/internalization with sufficient circulation to reach intratumoral Cmax, and (2) rapid renal clearance with minimal kidney retention
- Once isotope is delivered intracellularly, long half-life of 225Ac/161Tb becomes an asset — extends cumulative tumor dose while vector has cleared

### 161Tb rationale
- Beta emission (comparable to 177Lu) for crossfire debulking of bulky tumors + Auger emission for single CTCs and sub-mm micromets
- Early clinical data: responses in patients who progressed after standard 177Lu therapy / Pluvicto (Liang, Am J Nucl Med Mol Imaging, 2025; Hofman, Lancet Oncol, 2025)
- Particularly effective for internalized molecules where Auger electrons gain proximity to DNA
- Higher RBE may allow reduced administered activity for same therapeutic effect
- Historically understudied due to lack of cGMP supply — now resolved with multiple suppliers (TerThera, ITM, Isotopia) and Nusano (online 2027)

### 161Tb production
- Starting material: highly enriched 160Gd (>98% enrichment vs ~21.9% natural abundance)
- Process nearly identical to 177Lu production (well established)
- Supply chain risk: enriched isotope production historically dominated by Russia; Western investment expanding (DOE Isotope Program, URENCO)
- University of Utah (23 min away) can supply research quantities; Nusano provides strategic access

### Chelator strategy
- Off-the-shelf DOTA/DOTAGA — stable for 68Ga, 177Lu, 161Tb, 225Ac
- Single multi-radionuclide chelator reduces CMC complexity and avoids PK impact from chelator switching

**Isotope supplier table:** See Avidity DD doc for full supplier matrix (225Ac, 161Tb, 177Lu, 68Ga with R&D/cGMP status)

**Asked by:** Avidity, Polaris, Running List

---

## 3. Cyclic Peptide Platform Rationale (vs Antibodies, Small Molecules)

**Core position:** Cyclic peptides provide the optimal balance for RLT: high affinity and specificity comparable to antibodies, rapid tumor penetration and clearance, no Fc-gamma interaction, non-saturating mass doses, and engineering flexibility for internalization — all translating to a wider therapeutic index.

**Supporting detail:**

| Property | Antibodies | Cyclic Peptides | Small Molecules |
|---|---|---|---|
| Affinity | High | High (comparable) | Variable, can be lower |
| Clearance | Days–weeks | ~10s of minutes | Rapid |
| Fc biology | Yes (marrow tox) | None | None |
| Dosing | Saturating | Non-saturating | Non-saturating |
| Internalization | Yes | Engineerable | Target-dependent |
| Kidney retention | N/A | Engineerable | Variable |
| Target scope | Broad | Broad | Limited to pockets/active sites |

- Antibody problem for RLT: prolonged exposure → sustained payload delivery to normal tissues; Fc-gamma receptor interaction → hematologic toxicity irrespective of target expression
- Small molecule limitation: best suited for targets with clear binding pockets/enzymatic sites (e.g., PSMA, SSTR2); not every target is amenable
- Peptide RLT advantage: "snapshot" exposure (first-pass kinetics) vs antibody "video" (days of repeated tissue sampling)

**Asked by:** Avidity, Polaris, Running List

---

## 4. RLT vs ADC Positioning

**Core position:** RLT toxicity is predictable and quantifiable via Phase 0 dosimetry before therapeutic dosing. ADC toxicity is payload- and linker-dependent, often unpredictable, and only fully characterized after each individual Phase 1 study. This is the core structural differentiator on shared targets.

**Supporting detail:**

### ADC platform-intrinsic failure modes
- Viable targets fail due to platform liabilities, not target biology: CEACAM5 ADC (tusamitamab ravtansine) → ocular toxicity + slow internalization limiting efficacy (Gazzah, Ann Oncol, 2022); TAK-164 (GCC ADC) → hepatotoxicity from maytansinoid DM1 via non-cleavable linker (Kim, Cancer Chemother Pharmacol, 2023); MUC1-N ADCs → circulating decoy antigen sequesters antibody
- Each linker-payload combination has a known dosing ceiling: SN-38 ADCs (sacituzumab govitecan) → dose-limiting GI toxicity from linker hydrolysis; MMAE ADCs → peripheral neuropathy and ocular toxicity
- Unpredictable class toxicities (ILD) emerge independent of target biology, payload, or linker chemistry; cannot be anticipated preclinically

### RLT structural advantages
- Organ-at-risk exposure governed by ligand PK and target expression, both measurable via Phase 0 imaging dosimetry before any therapeutic dose
- RLT cytotoxicity via crossfire and direct ionization from radionuclide decay — does not depend on internalization or lysosomal trafficking (targets with slow internalization like CEACAM5 remain fully exploitable)
- Expected DLOs restricted to kidney (clearance-driven) and marrow (blood-pool exposure) — absent are hepatic, ocular, pulmonary, and GI signals that derailed ADC programs on these same targets
- Both modalities carry potential for manageable hematologic toxicity

### Positioning note (NVF feedback, May 2026)
- Do NOT claim earlier-line or combo advantages over ADCs — multiple ADCs already approved 1L (urothelial, DLBCL, AML) and combining with IO (Padcev + pembro, TROP2 ADCs + CPI in TNBC)
- Stick to: predictability of tox, payload-class ceilings, ILD risk, dosimetry-defined safety vs empirical DLT discovery

**Asked by:** Avidity, Polaris, NVF, Running List

---

## 5. Target-Specific Programs

### 5a. ACP3 (Prostatic Acid Phosphatase)

**Core position:** ACP3 is expressed in ~95% of PC patients across disease stages including PSMA-negative mCRPC, with no expression in salivary gland or kidney — eliminating Pluvicto's two dose-limiting toxicities.

**Supporting detail:**
- Transmembrane forms natively internalized; active site amenable to small molecule and peptide targeting
- BMS/RayzeBio OncoACP3: non-internalizing small molecule; early FIH shows strong tumor uptake and reduced off-tumor vs PSMA (SNMMI 2025). Preclinical data shows no internalization → limits Auger/alpha efficacy (Georgiev, Nat Biomed Eng, 2025)
- OncoACP3 human dosimetry: bone marrow is highest absorbed dose organ (0.0913 mGy/MBq); ~5-hr blood half-life may drive cumulative marrow exposure toward DLT with 225Ac (Brosch-Lenz, J Nucl Med, 2026)
- Sego: internalizing small molecules and peptides with 225Ac/161Tb; targeting shorter blood half-life to reduce marrow dose
- Note: not all differentiation strategies disclosed in DD responses due to IP sensitivity
- Positioning: randomized comparator pivotal vs Pluvicto in full mCRPC population (not PSMA enrichment); then rapid expansion into earlier lines

**Key references:**
- Georgiev, Nat Biomed Eng, 2025 (PMID 40571760)
- Brosch-Lenz, J Nucl Med, 2026 (first human dosimetry of OncoACP3)
- SNMMI 2025 presentation (uroToday link)

**Asked by:** Avidity, Polaris, Avego, Running List

### 5b. KLK2

**Core position:** KLK2 expression is restricted to prostate with overexpression across PC stages, maintained in PSMA-negative disease. JNJ's antibody program toxicities (ILD, hematologic) were modality-driven, not target-driven — Sego's small molecule/peptide approach eliminates all three mechanisms.

**Supporting detail:**
- JNJ-6420 Phase 1 (n=89): 4 treatment-related deaths (2 ILD at cumulative ≥600 μCi), 9% ILD incidence, 63% thrombocytopenia in ≥150 μCi cohorts (ASCO 2024, JCO 42:5010)
- Antibody + alpha-emitter = fundamental pharmacologic mismatch: prolonged circulation with high-LET isotope generates unavoidable cumulative normal-tissue radiation; viable TI unlikely with dose modification alone
- Three antibody liabilities: (i) prolonged blood residence → sustained marrow/lung irradiation, (ii) Fc-gamma engagement → nonspecific heme tox, (iii) saturating mass doses → off-target exposure
- Sego small molecules and peptides eliminate all three: short half-life (tens of minutes), no Fc domain, non-saturating doses
- Ph 0 imaging confirms lung and marrow dosimetry before any therapeutic dose
- Clinical positioning: backbone agent in earlier-line prostate cancer with ARPI combination potential (wider TI enables chronic co-administration)

**Asked by:** Avidity, Polaris, Running List

### 5c. CLDN1

**Core position:** CLDN1 is a tight junction protein with high tumor expression and tumor-specific accessibility — junctional CLDN1 in healthy tissue is shielded from circulating ligands; non-junctional CLDN1 in cancer is exposed.

**Supporting detail:**
- Binder design: monocyclic peptides targeting ECL1 or ECL2 extracellular loops; only bind non-junctional CLDN1 in tumors
- Preference for binders that do NOT share Alentis mAb epitope, but will benchmark head-to-head
- Lead indication: lung squamous (high CLDN1 expression + radiosensitivity)
- Requires nano-disk format or on-cell screening (transmembrane protein); in silico ligand design as parallel path

**Key references:**
- Roehelen, J Hepatol, 2023 (non-junctional CLDN1 accessibility in tumors, NHP safety of anti-CLDN1 mAb)
- Alentis Therapeutics mAb (competitor benchmark)

**Asked by:** Avidity, Polaris, NVF, Running List

### 5d. CEACAM5

**Core position:** Extensive human imaging data de-risks CEACAM5 as an RLT target. Historical ADC, BiTE, and CAR-T limitations were modality-driven. RLT aligns better with CEACAM5 biology — no dependence on internalization or tumor-immune microenvironment.

**Supporting detail:**
- ADCs: slow internalization, payload class AEs (ocular), narrow TI (ESMO 2022)
- CAR-T: on-target/off-tumor colitis (Med Onc 2025)
- BiTEs: GI issues at higher doses (Nat Comm 2023)
- Merck M9140 (ADC): 31% ORR in 3L+ mCRC (vs 1–2% SOC); advancing to Ph III (H1 2026)
- CEACAM5 apical polarity in healthy GI → less accessible to RLT; 64Cu-M5A imaging confirmed minimal normal colon uptake (Wong, Cancer Biother Radiopharm, 2023)
- M5A binds N-terminal IgV-like domain (accessible on tumors, not healthy colon); TCR approach recognizes HLA-presented peptides on both healthy and tumor cells → different tox profile

**Key references:**
- Wong et al 2023 (Liebertpub)
- Parkhurst et al 2011 (Mol Ther)
- PROCEADE-CRC01 (PMID 40739424)

**Asked by:** Avidity, Polaris, Running List

### 5e. MUC1-C

**Core position:** Dual discovery approach — cyclic peptides mimicking MUC1-N/MUC1-C SEA domain interaction, plus de novo DEL and mRNA display selections against recombinant MUC1-C ECD.

**Supporting detail:**
- MUC1 undergoes autoproteolytic cleavage at SEA domain → MUC1-N shed in cancer, exposing 58-aa MUC1-C ECD
- SEA domain structure: PDB 2ACM (Macao, Nat Struct Mol Biol, 2006) — resolves MUC1-N/MUC1-C interface, defines α3 and α4 helices of MUC1-C ECD
- Historical MUC1-N ADCs failed: shed MUC1-N acts as circulating decoy, sequestering antibody before tumor delivery (Panchamoorthy, JCI Insight, 2018)
- Sego targets MUC1-C directly: 3D1 mAb (Kufe group) binds α3 helix with 17 nM affinity, internalizes into tumor cells, no reactivity with normal epithelium (Panchamoorthy, JCI Insight, 2018) — validates the epitope for peptide design
- Appropriate reagents commercially available for both approaches

**Key references:**
- Macao, Nat Struct Mol Biol, 2006 (PDB: 2ACM, SEA domain NMR structure)
- Panchamoorthy, JCI Insight, 2018 (3D1 mAb targeting MUC1-C α3 helix)

**Asked by:** Avidity, NVF, Running List

---

## 6. Research & Discovery Engine

**Core position:** Sego's discovery cascade co-optimizes the full ligand-linker-chelator conjugate from day one, uses ICP-MS multiplexed in vivo PK to triage rapidly, and carries 3–5 candidates per target into FIH rather than committing to a single lead on mouse data.

**Supporting detail:**

### Hit finding (two routes)
1. De novo: mRNA, DEL, phage display
2. Structure-based design from known ligands/crystal structures + FTO evaluation

### Cold optimization
- Full conjugates (ligand + linker + chelator + cold metal) from the start
- Focused libraries (0.1–10K members) + ASMS workflows for dense SAR
- Biophysical corroboration: SPR, ITC, DSF
- In vitro ADME: solubility, serum/blood stability, acid stability, mast cell degranulation, transporter substrate testing
- Chemical space discipline: avoid overly cationic, lipophilic, or aromatic compounds → predispose to fast renal clearance

### Hot optimization
- Radiolabeling, cell binding, internalization → confirm cold-metal studies
- Cell killing, serum stability, formulation stability → efficacy ranking
- Murine dosimetry → biodistribution (poor predictor of human PK, but identifies differentiated profiles)

### ICP-MS multiplexed PK
- Non-radioactive, multiplexed in vivo PK of lead compounds
- Quick triage of tumor and organ uptake without radiolabeling
- More ligand+linker+chelator combinations tested in vivo; clearer SAR

### Stage gates / go-no-go
- Affinity: <10 nM
- No highly charged, excessively lipophilic compounds
- Dose-dependent, target-specific cell killing in vitro
- Tumor:kidney absorbed dose >3
- Tumor:red marrow absorbed dose >20
- Tumor cumulative dose >100 Gy; Kidney ≤23 Gy; Red marrow ≤2 Gy

### Cost per program
- ~$2.6M preclinical (Hit ID $600K, Cold Opt $1M, Hot Opt $500K, IND enabling $500K) — excludes FTEs
- ~$20M FIH through Ph 1/2 ($2.4M FIH + $18M Ph 1/2)

### Target feasibility ranking
1. **ACP3, KLK2** — existing small molecule / peptide starting points, known binding positions, established affinity; 3–4 month hit finding (vs 9–12+ de novo)
2. **CEACAM5** — published A3-B3 domain binders; team has direct phage/mRNA display experience
3. **MUC1-C** — dual approach (MUC1-N interaction + de novo)
4. **CLDN1** — transmembrane protein; requires additional expression/purification work

**Asked by:** Avidity, Polaris, Running List

---

## 7. Ph 0 / FIH Clinical Strategy

**Core position:** Sego's Ph 0 design selects the lead compound in humans — not mice — by running 3–5 candidates through quantitative 177Lu imaging dosimetry before committing capital to a full therapeutic program.

**Supporting detail:**

### Study design
- Cohort 1 (Candidate Selection): 3 patients per peptide × 3–5 candidates; pre-specified criteria for tumor uptake/retention, OAR washout, predicted absorbed doses
- Cohort 2 (Candidate Dosimetry): 6 additional patients per passing candidate to refine dosimetry and select lead
- Cost premium: ~30% vs single candidate; adds ~3 months
- 177Lu as imaging isotope (well-suited to quantitative SPECT; has US DMF, EU MA)

### Regulatory strategy
- **Ex-US first**: Australia, South Africa, UK — Ph 0 not classified as clinical trial; lighter preclinical package
- **US**: eIND pathway under FDA's Exploratory IND guidance (microdose ≤100 μg); INTERACT meeting submitted (July 2026) to align on multi-candidate design requirements
- **Not Germany**: §13(2b) AMG framework unsuitable for structured comparative evaluation; BfArM slow for radiopharma approvals

### Differentiation vs Aktis
1. Lead selection in humans, not mice (3–5 candidates head-to-head)
2. Higher bar for safety/TI — designing for earlier-line use
3. Company-sponsored trials (not IIT) — Sego controls enrollment and owns data

### Dosimetry-based patient selection (3 layers)
1. Qualifying lesion uptake > reference organ (liver); SUVmax + SUVmean + SUVmin floor
2. Individualized predicted absorbed dose: tumor >100 Gy, kidney ≤23 Gy, marrow ≤2 Gy
3. Exclusion of discordant off-target uptake patterns

### 177Lu → 225Ac translation
- Peptide PK driven by vector, not radiometal → 177Lu time-activity curves re-weighted by 225Ac decay scheme
- Standard physics-based approach; enables specific, higher 225Ac starting dose vs no human data
- Minimal further optimization: same chelator (DOTA), same construct; primary variables are radiolabeling conditions and formulation stability (explored preclinically in parallel)

**Asked by:** Avidity, Polaris, Avego, Running List

---

## 8. Manufacturing & Infrastructure

**Core position:** Vertical integration saves ~57% vs CDMO over 2 years ($8.5M on 4 Ph 0 + 1 Ph 1 programs), is already in flight for Dec 2026 completion, and is structurally de-risked by Wasatch's $6.5M TI commitment and equipment lease structure.

**Supporting detail:**

### CDMO vs internal economics (2028–2029)
| | CDMO | Sego Internal | Savings |
|---|---|---|---|
| 2-yr total (4 Ph 0 + 1 Ph 1) | $14.98M | $6.44M | $8.54M (57%) |
| Breakeven | Favorable at ≥2 Ph 0 programs | | |

### Wasatch investment structure
- $20M equity + build investment for Seed
- $6.5M TI within building lease → offsets ~40% of $15M total build cost
- $2.6M GMP equipment in equipment lease (not CapEx)
- Option in IRA for additional $20M equity at Series A

### Stage 1 vs Stage 2
- Stage 1 (Dec 2026): supply early clinical studies through Ph 2
- Stage 2 (Series A timing): expanded capabilities for Ph 3 and commercial; may defer to CDMO

### Strategic advantages
- Nusano adjacency (SLC) → full control of isotope delivery, eliminate decay losses
- Huntsman Cancer Center as local clinical site
- CDMO alternative adds 12 months (6 tech transfers, scheduling constraints)
- Single-site regulatory simplicity
- Synergy with preclinical hot lab (shared shielding, HVAC, waste, personnel)
- **4x M&A value premium**: Fusion ($2.4B), RayzeBio ($4.1B), Point — all had manufacturing; vs Mariana, 3B Pharma without

### Team manufacturing experience
- Greg: multiple radiopharma clinical dev through approval; tech transfer to CDMOs/radiopharmacies (123I PARPi, 225Ac SSTR2, 177Lu SSTR2, 18F PARPi, 68Ga PSMA, 99mTc DMSA)
- Brandon Buckway: built GMP facility at U of Utah; ANDA/NDA manufacturing site for FDG, Axumin, Vizamyl, Pylarify, Posluma, Cerianna
- Jeevan: scaled commercial supply for Lutathera and Pluvicto at AAA/Novartis
- Richard: three 89Zr antibody diagnostics to FIH via academic and CDMO routes

**Asked by:** Polaris, Avego, Running List

---

## 9. Clinical Development & Combination Strategy

**Core position:** RLT's orthogonal, physics-based MOA and organ-at-risk (not systemic) toxicity profile make it a practical combination partner across most oncology drug classes. Dosing strategy is biomarker- and indication-driven, not schedule-driven.

**Supporting detail:**

### Combination rationale
- Minimal overlapping tox with IO, ADCs, BiTEs, TKIs
- Chemo: sequenceable (between cycles, drug holidays); chemo-radiation is already SoC in many solid tumors
- RLT as backbone therapy provided cumulative OAR limits not exceeded

### Alternative dosing (fractionated, BCR-driven, MRD-triggered)
- Prostate (ACP3): BCR-triggered post-primary therapy failure
- CRC/GI: ctDNA-defined MRD positivity post-resection/chemo
- Schedule modulation as tactical lever once biomarker population is defined

### Prior-RLT patients
- Include, not exclude (clinical + commercial need)
- Cumulative dose accounting: OAR tolerance minus prior exposure
- Stratify RLT-naïve vs RLT-experienced; individualized per-cycle activity

### Theranostic pairing
- Co-develop matched imaging Dx from FIH onward
- Single regulatory filing for companion Dx + standalone staging indication
- Team has direct experience across full theranostic value chain (development, approval, commercialization, radiopharmacy distribution)

**Asked by:** Avidity, Polaris, Running List

---

## 10. Development Timeline & Financing

**Core position:** ACP3 and KLK2 enter clinic early 2028. Series A ($150M) targeted mid-2028 with FIH data from two programs.

**Supporting detail:**

### Seed milestones
- Two FIH studies: first completed mid-2028, second with interim data mid-2028 (completing end 2028)
- Acceleration levers: (1) rational design from known chemical matter (3–4 months vs 9–12+ de novo), (2) ICP-MS multiplexed PK, (3) matched CRO-to-target scientific fit

### Series A projection
- $150M raise supporting 2–4 programs in clinical development
- 2 programs to Ph 1/2 efficacy readouts + 2 additional programs into FIH
- Clinical efficacy data "highly valuable and transactable" — benchmarks: RayzeBio $4.1B (Ph 1 SSTR2), Fusion $2.4B (Ph 1 PSMA); both fast-follow programs
- Phase 0 dosimetry benchmarks: OncoACP3 acquired by BMS for $1.35B; Aktis valued at $1.2B at IPO — both largely on Phase 0 dosimetry of lead compound

### In-licensing optionality
- Dozens of inbound partner conversations; 5+ assets evaluated (near clinic or with FIH data)
- GCC deprioritized to make room for in-license
- Active outreach: Chinese RLT companies, European/American academic centers
- In-license could add another route to clinic in Seed round

### CRO strategy
- Wuxi selected as primary CRO (capabilities, pricing, team experience)
- 4–5 additional CROs under evaluation
- Stage-gate on/off ramps at each workflow transition; ramp sparingly

**Asked by:** Avidity, Polaris, Avego, Running List

---

## 11. Competitive Landscape & RLT Market Positioning

**Core position:** RLT will become a backbone oncology modality, moving earlier in treatment and in combination. Sego is positioned to set the standard on novel targets with best-in-class dosimetry-driven development.

**Supporting detail:**

### RLT as first-line
- Earlier-line patients: better organ function, larger dose budget, longer survival horizons → amplify benefit-to-risk
- Pluvicto already moving into earlier lines in real time
- Combinable with IO, TKIs, hormone therapy, PARPi — orthogonal MOA
- FDA Frontrunner initiative as regulatory tailwind

### Delivery challenges (and Sego's answers)
- Isotope access: Nusano adjacency
- Last-mile delivery: radiopharmacy network partnerships (team has commercialization experience)
- Hospital investment: theragnostic centers expanding (Huntsman Cancer Institute)
- Regulatory: FDA Aug 2025 draft guidance on dosimetry-based patient selection aligns with Sego's approach

### RLT discovery — "less empirical"
- Systematic go/no-go criteria (affinity, physicochemical properties, cell killing)
- Where empiricism remains (mouse-to-human PK translation), Ph 0 microdosing bridges the gap directly in humans
- "One of the most compelling and underappreciated advantages of the RLT modality"

**Asked by:** Polaris, Running List

---

## 12. Safety & Toxicity Framework

**Core position:** Sego engineers against known RLT failure modes (Lutathera marrow, Pluvicto salivary/kidney) with quantitative dosimetry thresholds and Phase 0 imaging as a per-patient safety gate.

**Supporting detail:**

### Quantitative thresholds
- Tumor:kidney absorbed dose ratio >3
- Tumor:red marrow absorbed dose ratio >20
- Tumor: >100 Gy cumulative
- Kidney: ≤23 Gy cumulative (EBRT limit)
- Red marrow: ≤2 Gy cumulative
- Salivary gland: ≤26 Gy cumulative (where applicable)

### Target-driven safety advantages
- First 5 targets (GCC deprioritized): no known red marrow expression
- ACP3: no salivary gland or kidney expression (eliminates Pluvicto's DLTs)
- Accessibility paradigm: polarized/junctional targets in healthy tissue → minimal on-target/off-tumor exposure

### Polarized target learnings (PSMA precedent)
- Healthy prostate: negligible PSMA RLT uptake (apical expression shielded)
- Salivary gland: complex mechanism (target-specific + nonspecific uptake); Sego avoids targets with salivary/kidney expression
- Inflammation risk: acknowledged potential for altered polarization in comorbidities (IBD, severe asthma) — flag for exclusion criteria

### Per-patient dosimetry verification
- Phase 0 imaging flags unexpected off-target exposure before therapeutic dosing
- Population-level thresholds become per-patient verification criteria
- Cumulative dose accounting for prior-RLT patients

**Asked by:** Avidity, Polaris, Running List

---

## Appendix: Question Cross-Reference by Investor

| Theme | Avidity | Polaris | Avego | NVF | Running List |
|---|---|---|---|---|---|
| Target selection | ✓ | ✓ | | ✓ | ✓ |
| Isotope selection | ✓ | ✓ | | ✓ | ✓ |
| Platform (peptides) | ✓ | ✓ | | | ✓ |
| RLT vs ADC | ✓ | ✓ | | ✓ | ✓ |
| ACP3 | ✓ | ✓ | | ✓ | ✓ |
| KLK2 | ✓ | ✓ | | ✓ | ✓ |
| CLDN1 | ✓ | | | ✓ | ✓ |
| CEACAM5 | ✓ | | | ✓ | ✓ |
| MUC1-C | ✓ | | | ✓ | ✓ |
| Ph 0 / FIH strategy | ✓ | ✓ | ✓ | | ✓ |
| Manufacturing | | ✓ | ✓ | ✓ | ✓ |
| Clinical / combo | ✓ | ✓ | | | ✓ |
| Timeline / financing | ✓ | ✓ | ✓ | ✓ | ✓ |
| Safety / dosimetry | ✓ | ✓ | | ✓ | ✓ |
| CRO strategy | | | ✓ | | ✓ |
| Competitive landscape | | ✓ | | | ✓ |
