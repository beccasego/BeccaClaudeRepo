---
name: sego-writing-style
description: >
  Sego Therapeutics writing style for diligence answers, investor memos, BD pre-reads,
  board narratives, and external-facing prose. Enforces answer-first structure (first
  sentence fully answers), quantitative thresholds introduced early, comparative framing
  (RLT vs ADC/EBRT, peptides vs antibodies), and a confident, non-defensive tone. Use
  whenever the user drafts, rewrites, critiques, or reviews prose for sophisticated
  life-sciences investors, partners, or regulators involving Sego, RLT, radioligand
  therapy, radiopharmaceuticals, or targeted radionuclide therapy. Triggers on phrases
  like "diligence question", "draft a response", "investor memo", "BD pre-read",
  "rewrite this", "tighten this", or any request to produce or edit external Sego prose.
  Apply even when not explicitly invoked if the output is external Sego writing.
---

# Sego Writing Style Skill

Style guide for Sego external prose — diligence Q&A, investor communications, BD
materials, board narratives, regulator-facing responses. The goal is clarity,
authority, and decision-useful communication for a skeptical but rational reader.

This skill operates in two modes:

1. **Draft mode** — when generating a new answer or memo, follow the rules below
   from sentence one.
2. **Critique mode** — when the user pastes a draft and asks for review, rewrite,
   tightening, or feedback, score the draft against §11 (Final Quality Check) and
   produce a rewritten version that complies.

When uncertain which mode applies, default to drafting in style and offer to critique
on request.

---

## §1 — Core Principle: First Sentence Fully Answers the Question

Every answer is complete in the first sentence. A reader who reads only the first
sentence must correctly understand Sego's position.

Correct openings:

- "ACP3-RLT is designed to displace Pluvicto, not combine with it."
- "Sego applies quantitative go/no-go thresholds based on tumor-to-organ absorbed dose ratios."
- "We plan to advance 3–5 candidates into Phase 0 at ~30% incremental cost versus a single-candidate approach."

Incorrect openings (these set up context instead of answering):

- "Sego has a comprehensive process for…"
- "Preclinical imaging plays an important role…"
- "There are several factors to consider…"

If the first sentence describes a process, history, or framework rather than stating
Sego's position, rewrite it.

---

## §2 — Preferred Answer Template

| Sentence | Function |
|---|---|
| 1 | Direct answer to the question |
| 2–4 | Evidence, mechanism, precedent |
| Optional final | Strategic implication (risk reduction, capital efficiency, differentiation) |

Most answers fit within 1–3 short paragraphs. If a draft runs longer, cut.

---

## §3 — Supporting Paragraphs Only Justify the Opening Claim

After sentence one, every following sentence must (i) explain why the answer is
correct, (ii) provide evidence or precedent, or (iii) describe how risk is controlled.

Do not introduce new claims later in the answer. If a later paragraph changes how the
first sentence is interpreted, the structure is wrong — restructure or split the
question.

---

## §4 — Write for Diligence, Not for Documentation

Diligence answers are not operating manuals.

Avoid:

- Step-by-step workflows unless explicitly requested
- Exhaustive assay lists
- Internal SOP-style language
- "Comprehensive process" framings

Emphasize:

- Decision points
- Stage gates
- Capital efficiency
- Human translatability
- Probability of success

Reframe technical detail as: "This allows us to make a go/no-go decision earlier and
with less capital at risk."

If a paragraph does not help an investor understand risk, speed, or probability of
success, cut it or collapse it.

---

## §5 — Multi-Part Questions Need a Clear Spine

When a question has multiple components: (i) sentence one provides a global answer
that covers all parts, (ii) subsequent paragraphs address each component cleanly and
proportionally, (iii) topics do not interleave (for example, do not mix timing and
biology in the same paragraph).

Headers are not required. The structure should be obvious on a fast read.

---

## §6 — Quantitative Thresholds Are a Strength — Use Them Early

Numbers sharpen credibility and reduce ambiguity. Whenever available, include ratios,
absorbed dose limits (Gy), time deltas (months), cost deltas (%), or copy-number /
H-score thresholds.

Best practice: introduce the key number in the first paragraph, often in the first
sentence.

Examples:

- Tumor-to-kidney absorbed dose ratio >3, tumor-to-red-marrow >20
- Tumor: >100 Gy cumulative; kidney ≤23 Gy; red marrow ≤2 Gy
- ~30% incremental cost vs single-candidate path
- IHC H-scores of 200–300 in greater than 60% of tumor cells

---

## §7 — Acknowledge Uncertainty Once, Then Close the Loop

Scientific uncertainty is acceptable. Unbounded uncertainty is not.

Pattern:

1. State the uncertainty
2. Immediately state the mechanism that controls it (Phase 0 imaging, dosimetry, gating, comparator binders, etc.)
3. Move on

Do not re-qualify the same risk later in the answer. Hedging in multiple paragraphs
signals lack of conviction.

---

## §8 — Comparative Framing Is Preferred

Strong answers compare options where comparisons exist:

- RLT vs ADCs vs EBRT vs T-cell engagers vs CAR-T
- Peptides vs antibodies vs small molecules
- Phase 0 microdosing vs traditional Phase 1 development
- Internal CMC vs outsourced models
- Lutathera vs Pluvicto on toxicity mechanism

Comparisons clarify trade-offs and signal command of the modality landscape. Use them
whenever they are available.

---

## §9 — Tone: Confident, Precise, Non-Defensive

Write declaratively and on evidence. Avoid:

- Over-hedging ("may potentially")
- Anticipating every possible objection
- Defensive justifications
- Apologetic framing of risk

Assume a skeptical but rational reader. State the position. Provide the evidence.
Stop.

---

## §10 — Mechanics That Matter

These rules materially improve clarity and memorability and must be applied in every
draft:

- Do not bold words for emphasis. Assume the reader knows what is important. Use structure and placement to signal priority.
- When listing items, even within a sentence, use roman numerals: (i), (ii), (iii). This improves recall.
- Prefer short sentences. This is not prose. Each sentence should carry meaning.
- Use the word "and" only in a list. This forces long sentences to break into clear units.
- Use the fewest words possible. If a word does not add information, remove it.
- Distinguish preclinical evidence from clinical evidence explicitly. Never blur the two.
- Distinguish imaging relevance from therapeutic relevance explicitly. This is critical for RLT.
- Cite primary sources where available (author, journal/year, or guidance date). Do not fabricate citations. If a citation is not known, flag the gap rather than invent one.

---

## §11 — Final Quality Check (run before delivering any draft)

Before returning a draft, verify each item:

| # | Check | If no |
|---|---|---|
| 1 | Can the first sentence stand alone as the answer? | Rewrite sentence one |
| 2 | Does every sentence support sentence one? | Cut or split |
| 3 | Are numbers introduced in the first paragraph? | Move them up |
| 4 | Is this shorter than a likely first draft? | Cut |
| 5 | Does this read like diligence rather than an internal memo? | Strip SOP language |
| 6 | Is preclinical vs clinical evidence cleanly distinguished? | Tag each claim |
| 7 | Is imaging vs therapeutic relevance cleanly distinguished? | Tag each claim |
| 8 | Are uncertainties stated once with a control mechanism? | Consolidate hedges |
| 9 | Are comparisons used where they exist (RLT vs ADC, peptide vs mAb, etc.)? | Add the comparison |
| 10 | Are all citations real and dated? | Remove or flag any unverified claim |

If it feels long, it is.

---

## Critique Mode — Output Format

When the user asks for review, rewrite, or tightening of an existing draft, return:

1. Verdict — one sentence: pass / needs rewrite / needs restructure.
2. Scorecard — table of the §11 checks with green / yellow / red per row and a one-line rationale per row.
3. Rewrite — full rewritten answer that complies with §1–§10. Do not return a partial rewrite unless the user asks for one.
4. Gaps flagged — bullet list of any factual claims that need user verification (citations, numbers, dates).

Do not reproduce the user's original draft in the output. Show only the rewrite.

---

## Reference Material

Annotated good/bad pairs from the Sego diligence corpus live in `examples.md`. Read
that file when the user asks for examples, when a particular section of the rubric
needs reinforcement, or when calibrating tone for a specific topic (target selection,
dosimetry thresholds, CMC, BD strategy, in-licensing criteria).

For deck-context prose (slide cards, callouts, titles), the `sego-deck-style` skill
governs visual treatment and high-density layout patterns. The two skills are
independent — apply this skill to the prose itself, regardless of where it lands.
                                                                                                                                                                                                                                                 