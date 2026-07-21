# Sego Writing Style — Annotated Examples

Curated good/bad pairs drawn from the Sego diligence corpus. Each pair illustrates one
or more rules from `SKILL.md`. Use these as calibration when drafting or critiquing.

Topics covered:

1. Opening sentence (rule §1)
2. Quantitative thresholds early (§6)
3. Comparative framing (§8)
4. Multi-part question with a clear spine (§5)
5. Acknowledging uncertainty once (§7)
6. Distinguishing preclinical vs clinical evidence (§10)
7. Distinguishing imaging vs therapeutic relevance (§10)
8. Citations and gap-flagging (§10, §11)

---

## 1. Opening Sentence (§1)

### Topic: ACP3 positioning vs Pluvicto

Bad:

> "Sego has been thinking carefully about how ACP3-RLT fits into the prostate cancer
> landscape, given the dominance of Pluvicto and the evolving competitive set. There
> are several ways the asset could be positioned, including in combination, in
> sequence, or as a replacement."

Why it fails: opening describes a thinking process, not a position. Reader cannot
extract Sego's view from sentence one.

Good:

> "ACP3-RLT is designed to displace Pluvicto, not combine with it. Driven by ACP3's
> broad and highly specific expression profile in prostate cancer, our intent is to go
> head-to-head against Pluvicto in mCRPC. We expect to demonstrate significantly
> superior efficacy with a better safety profile, particularly the elimination of
> dose-limiting salivary gland toxicity."

Why it works: sentence one is a position. Sentence two provides the biological basis.
Sentence three provides the strategic differentiator.

---

## 2. Quantitative Thresholds Early (§6)

### Topic: Dose-limiting organ ratios

Bad:

> "Sego thinks about therapeutic index carefully, balancing tumor uptake against
> uptake in critical organs. We use both relative and absolute measures to evaluate
> candidates and decide whether they should advance."

Why it fails: no numbers in the first paragraph. Reader cannot calibrate rigor.

Good:

> "Sego applies rigorous, quantitative go/no-go thresholds: tumor-to-kidney absorbed
> dose ratio greater than 3, tumor-to-red-marrow greater than 20. These thresholds
> are derived from approved RLT product experience (Lutathera, Pluvicto) and
> external beam tolerance limits. Clinical dosimetry targets follow the same logic:
> tumor >100 Gy cumulative, kidney ≤23 Gy, red marrow ≤2 Gy."

Why it works: ratios in sentence one. Mechanism and precedent in sentence two.
Quantitative anchors throughout.

---

## 3. Comparative Framing (§8)

### Topic: Why cyclic peptides over antibodies for RLT

Bad:

> "Cyclic peptides have a number of attractive properties for RLT applications,
> including good affinity, reasonable specificity, and favorable pharmacokinetics.
> They are well-suited to the demands of radioligand delivery."

Why it fails: no comparison, no trade-off articulated, no signal of modality command.

Good:

> "Cyclic peptides offer the best balance of high target affinity, rapid tumor uptake,
> and rapid clearance for RLT. Antibodies provide high affinity and specificity, but
> their long circulation half-life sustains payload delivery to normal tissues and
> their Fc-gamma interaction drives hematologic toxicity irrespective of target
> expression. Small molecules are tunable but require a defined binding pocket, which
> not every target has. Peptides are administered at non-saturating mass doses with
> first-pass kinetics, which preserves tumor-to-normal dose ratios."

Why it works: explicit comparison across three modalities, each with a stated
trade-off. Signals modality command.

---

## 4. Multi-Part Question with a Clear Spine (§5)

### Topic: "Walk us through hit finding, optimization, and timeline."

Bad: interleaving timing into the chemistry discussion, then circling back to timing
later.

Good — global answer first, then proportional sections:

> "Sego runs hit finding through two parallel routes — de novo (mRNA, DEL, phage) and
> structure-based design from known ligands and crystal structures — with FTO
> evaluation in parallel. Cold optimization is the most resource-intensive phase and
> drives most of the timeline; hot optimization is shorter and selects among
> finalists.
>
> Hit finding (3–4 months for structure-based; longer for de novo): focused libraries
> of 0.1–10k members, ASMS-driven SAR, biophysical confirmation by SPR/ITC/DSF.
>
> Cold optimization: ligand-linker-chelator conjugates evaluated in cell binding,
> internalization, in vitro ADME, and xenograft PK. Tailoring physicochemical
> properties (avoiding excess charge, lipophilicity, aromaticity) keeps candidates in
> the chemical space that predisposes to fast renal clearance and high tumor uptake.
>
> Hot optimization: radiolabeling, cell killing, serum and formulation stability,
> mouse dosimetry. Several chemically distinct series advance to FIH Phase 0 to
> select the development candidate on human PK."

Why it works: sentence one covers all three subparts. Each section is proportional
and topic-clean. Timing is a single sentence in the lead, not scattered.

---

## 5. Acknowledging Uncertainty Once (§7)

### Topic: Translating mouse dosimetry to humans

Bad:

> "Mouse-to-human translation in RLT is admittedly difficult and a known limitation.
> We try to mitigate this through several approaches. Mouse dosimetry, while
> imperfect, can still provide useful directional information. We acknowledge that
> any mouse-derived prediction carries uncertainty when applied to humans."

Why it fails: the same uncertainty is acknowledged four times. Hedging signals lack
of conviction.

Good:

> "Mouse dosimetry is a poor predictor of human PK, as in most oncology modalities.
> Phase 0 microdosing closes that gap directly: an imaging dose of the therapeutic
> isotope generates human dosimetry rapidly, at lower regulatory burden, and at a
> fraction of Phase 1 cost. We make development-candidate decisions on human data,
> not mouse extrapolation."

Why it works: uncertainty stated once, control mechanism stated immediately, then
move on.

---

## 6. Distinguishing Preclinical vs Clinical Evidence (§10)

### Topic: Tb-161 rationale

Good:

> "Tb-161 is a next-generation radionuclide with Lu-177-like properties and additional
> high-energy Auger emission that enhances killing of micrometastases. Preclinically,
> the higher RBE supports lower administered activity for equivalent effect.
> Clinically, early data from the VIOLET trial (Liang, 2025) suggest Tb-161 can drive
> responses in patients who progressed after Lu-177 therapy."

Why it works: preclinical mechanism (RBE, Auger emission) is tagged separately from
clinical evidence (VIOLET trial). The reader can immediately weight each claim.

Bad pattern to avoid: blending "Tb-161 has shown improved efficacy" without
specifying whether the data are mouse, human, or theoretical.

---

## 7. Distinguishing Imaging vs Therapeutic Relevance (§10)

### Topic: M5A antibody data and CEACAM5 targeting

Good:

> "M5A binds the membrane-proximal IgC-like A3-B3 domains of CEACAM5, accessible on
> tumor cells but not in healthy colon (where expression is restricted to the apical
> membrane). Clinical imaging with 64Cu-M5A demonstrates this selectivity directly
> (Wong et al, 2023). The imaging readout is supportive of target accessibility for a
> peptide-based RLT, but does not establish therapeutic index — that requires
> dosimetry from a Phase 0 imaging dose of the therapeutic isotope."

Why it works: imaging evidence and therapeutic implication are explicitly separated.
Reader does not conflate target accessibility with therapeutic feasibility.

This distinction is critical for RLT and must be enforced in every answer that
references human imaging data.

---

## 8. Citations and Gap-Flagging (§10, §11)

### Topic: T-cell engager toxicity for CEACAM5

Good:

> "T-cell engagers targeting CEACAM5 have reported on-target, off-tumor GI toxicity
> at higher doses, particularly early after dosing (Nat Comm 2023). CAR-T programs
> have reported severe colitis after intraperitoneal administration (Med Onc 2025).
> These toxicities are modality-driven (immune activation, T-cell persistence) rather
> than target-driven."

Why it works: each claim is tagged to a citation. The differentiation between
modality-driven and target-driven toxicity is stated as a conclusion, not assumed.

Gap-flagging pattern when a citation is uncertain:

> "[CLAIM]. Citation needs verification — possibly [author/year] but please confirm
> before sending."

Never invent a citation. If the author or year is not known with confidence, flag it.

---

## Critique Walkthrough — Worked Example

User pastes this draft:

> "Sego has thought a lot about CRO selection and we have a comprehensive process for
> evaluating partners. We looked at multiple CROs across our development workflow,
> and we scored them on technical capabilities and other factors. Wuxi was selected
> as our primary CRO because of their capabilities, pricing, and our team's prior
> experience with them. We are evaluating additional CROs for different stages of
> work."

Critique-mode output:

Verdict — needs rewrite.

| # | Check | Status | Rationale |
|---|---|---|---|
| 1 | First sentence stands alone | Red | Opens with "thought a lot" — no position |
| 2 | Every sentence supports sentence one | Yellow | Sentences 2–4 OK but no anchor |
| 3 | Numbers in first paragraph | Red | Zero numbers anywhere |
| 4 | Shorter than first draft | Yellow | Could compress 30%+ |
| 5 | Diligence vs internal memo | Red | "Comprehensive process" is SOP language |
| 6 | Preclinical vs clinical | N/A | Topic is operational |
| 7 | Imaging vs therapeutic | N/A | Topic is operational |
| 8 | Uncertainty stated once | Green | No hedges |
| 9 | Comparative framing used | Yellow | No comparison among CROs evaluated |
| 10 | Citations real and dated | N/A | None needed |

Rewrite:

> "Wuxi is Sego's primary discovery CRO, selected after a structured evaluation of
> multiple providers against a Sego-defined RLT workflow. Wuxi was chosen on three
> dimensions: end-to-end capability across hit finding through in vivo radiation,
> competitive pricing, and direct prior experience between Sego team members and Wuxi
> teams. Sego is evaluating an additional 4–5 CROs to fill specialized roles —
> screening, medicinal chemistry, hot work — with on- and off-ramps gated to defined
> stage transitions, used sparingly to minimize disruption."

Gaps flagged:

- Number of CROs evaluated overall (was the universe 8? 10?) — confirm before send.
- Specific stage-gate criteria for on/off-ramping — referenced but not yet enumerated; consider attaching workflow diagram.
