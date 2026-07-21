---
name: sego-deck-style
description: >
  Sego Therapeutics deck style guide — brand colors, Funnel Sans typography, card patterns,
  data callouts, language tone, and layout patterns for building Sego presentations.
  Use this skill whenever the user mentions Sego, Sego Therapeutics, radioligand therapy (RLT),
  radiopharmaceutical, or targeted radionuclide therapy in the context of building or editing
  a presentation or slide deck. Also triggers when a deck filename contains "Sego" or uses
  Sego brand colors (#002924, #B1C8B0, #D5ED99). Applies general investor pre-read deck
  conventions even when Sego branding is not explicitly requested for biotech pipeline content.
---

# Sego Deck Style Skill

Comprehensive style guide for building Sego Therapeutics presentations. Based on the official
Sego Brand Guidelines (October 2025) and validated against the Sego_PitchDeck_Oct25.pptx
(36 slides). Auto-applies when the deck context involves Sego, radioligand therapy (RLT),
or related biotech pipeline content.

## When This Skill Applies

Activate this skill when ANY of the following are true:
- The user mentions "Sego", "Sego Therapeutics", or the deck filename contains "Sego"
- The content references RLT, radioligand therapy, radiopharmaceutical, or targeted radionuclide therapy
- The existing deck already uses Sego brand colors (#002924 deep forest green, #B1C8B0 sage, #D5ED99 light green)
- The user invokes `/sego-deck-style` explicitly

If the deck is clearly for a different brand or company, do NOT apply Sego-specific styling — only apply the general preferences from §6.

---

## §1 — Color Palette

### Core Palette
| Token | Hex | Usage |
|-------|-----|-------|
| Dark Green | `#002924` | Section divider backgrounds, card header bars (problems/gaps), table headers, darkest pipeline stage |
| Sage | `#B1C8B0` | Intro/outro slide backgrounds, interstitial slides, card header bars (Sego's answer), data viz |
| Medium Green | `#61896E` | Interstitial slides, card fills, data visualization |
| Light Green | `#D5ED99` | Numbered step circles, card headers (advantages/highlights), data viz highlights (use sparingly) |

### Secondary Palette (Data Visualization)
Use to differentiate from the green palette in charts and infographics.

| Token | Hex | Family |
|-------|-----|--------|
| Dark Magenta | `#360105` | Magenta — warm reds for separate graphs |
| Medium Magenta | `#8F1A43` | Magenta — no-go indicators, source citations |
| Light Magenta | `#CD9FAF` | Magenta |
| Dark Blue | `#383D46` | Blue — cool tones for alternate data series |
| Medium Blue | `#5475E8` | Blue |
| Light Blue | `#BAD1D8` | Blue |

### Functional Palette
| Token | Hex | Usage |
|-------|-----|-------|
| Black | `#000000` | Title text (inherited from theme) |
| Canvas | `#DED6D3` | Data viz for non-focus data ("other" categories) |
| Off-White | `#F6F3F2` | Slide backgrounds |
| Dark Grey | `#656670` | **Primary body text color** (dominant — 175 uses in pitch deck vs 5 for black) |
| Light Grey | `#CFCFCF` | Lines in data viz, deselected UI states |
| White | `#FFFFFF` | Typography on dark backgrounds |
| Icon Grey | `#696A77` | All mono-width line icons |

**Key insight from the pitch deck:** Dark Grey #656670 is the actual primary body text color, not black. Black is used only for titles (via theme inheritance). All body text, labels, section labels, and footnotes use Dark Grey.

---

## §2 — Typography

### Typefaces
- **Funnel Sans** — Workhorse typeface for all communications. Available on Google Fonts.
- **Season Mix** — Reserved for large data display numbers only (dollar figures, percentages). NOT for body copy or headings.

### Type Scale — Brand Guidelines (canonical)
| Role | Font | Weight | Size | Letter-spacing | Line Height |
|------|------|--------|------|---------------|-------------|
| Heading (primary) | Funnel Sans | Light | 48pt | -1% | 130% |
| Heading (secondary) | Funnel Sans | Medium or Light | 32pt | -1% | 130% |
| Body Copy (primary) | Funnel Sans | Semibold or Regular | 24pt | 0% | 130% |
| Body Copy (secondary) | Funnel Sans | Semibold or Regular | 20pt | 0% | 130-150% |
| Folio / Caption | Funnel Sans | Regular | 16pt | 0% | 130-150% |
| Data Display | Season Mix | Regular | 96 or 128pt | 0% | 90% |

### Type Scale — Pitch Deck (actual usage, high-density investor pre-read)
In practice, the pitch deck uses significantly smaller sizes for dense content slides:

| Role | Font | Weight | Size | Count |
|------|------|--------|------|-------|
| Body text / section labels | Funnel Sans | Medium | 12pt | 228 uses |
| Card headers / emphasis | Funnel Sans | Medium | 14pt | 139 uses |
| Footnotes / small labels | Funnel Sans | Medium | 10pt | 84 uses |
| Source citations | Funnel Sans | Medium | 8pt | 6 uses |
| Data callout numbers | Season Mix | Regular | 40-52pt | 8 uses |
| Section labels above title | Funnel Sans | Medium | 12pt | consistent |

**Practical guidance:** Use the brand guide sizes (48/32/24/20/16pt) for standard or speaker-support decks. For dense pre-read investor decks, the pitch deck sizes (12/14/10/8pt) are the proven pattern. **Funnel Sans Medium is the workhorse weight** — used for body, labels, headers, and section markers. SemiBold appears in card header text; Bold is for inline emphasis only.

### Slide Title Rules
- Sentence case (first word capitalized + proper nouns only)
- Full assertion statements, not topic labels — convey the takeaway
- Often long-form (60+ chars), packing the key message into the title
- Mix of first-person ("We're building...", "Our translational strategy...") and third-person declarative ("Sego has an opportunity...")
- Examples from pitch deck:
  - "RLT pharmacology is complex; experience counts in optimizing & translating key properties"
  - "Innovation in RLT is handsomely rewarded: 6 acquisitions of >$1B value in last 2 years"
  - "We're building an in-house cyclic peptide platform for rapid identification & optimization of targeting vectors"

---

## §3 — Visual Elements

### Card Pattern (most common layout element)
Cards are the primary content container in the deck. Built from two shapes:

1. **Header bar:** `round2SameRect` (Round Same Side Corner Rectangle)
   - Height: ~36-43pt
   - Fill colors indicate semantic meaning:
     - Dark Green `#002924` → problems, gaps, industry context
     - Sage `#B1C8B0` → Sego's solution, response, capabilities
     - Light Green `#D5ED99` → advantages, highlights, key differentiators
   - Text: 14pt Funnel Sans Medium (or SemiBold), white on dark fills, dark on light fills

2. **Body area:** `roundRect` (Rounded Rectangle)
   - Height: ~270-310pt
   - Fill: white (`scheme:bg1`)
   - Text: 12pt Funnel Sans Medium, Dark Grey #656670

**Two-card layout:** Left card ~427-483pt wide + right card ~380-460pt wide, starting ~194pt from top.

### Numbered Step Circles
- Shape: `ellipse`, 27-28pt diameter
- Fill: Light Green `#D5ED99`
- Text: bold number, centered
- Used to mark steps, sections, or ordered items

### Freeform Shapes
The deck uses freeforms extensively (215 across 36 slides) for:
- Custom illustrations and diagrams
- Pipeline/timeline graphics
- Photo masks (rounded corners on 3 sides per brand guidelines)
- Connector arrows and decorative elements
- **NOT** for text content — text goes in roundRect/round2SameRect/textBox shapes

### Image Containers
Per brand guidelines: rounded corners on 3 sides, one sharp corner.
- Radius: 100px on 3 sides (for 1920x1080 slides)
- Margin: 16px between images

### Iconography
- Mono-width line icons with consistent stroke thickness
- Each icon = single clear concept, simple and functional
- Color: Dark Grey `#696A77` (NOT black, NOT body text grey)

### Data Visualization
- Light Green `#D5ED99` highlights areas of focus
- Canvas `#DED6D3` for non-focus data ("other" categories)
- Warm reds/magentas in separate graphs to prevent confusion
- Donut charts, bar charts, S-curves in theme greens
- Keep visualizations simple, legible, free of visual noise
- Combine rounded and straight edges (brand visual rhythm)

---

## §4 — Slide Layout Patterns

### Standard Content Slide Anatomy
From top to bottom:
1. **Section label** — (20, 84)pt, 12pt Funnel Sans Medium, Dark Grey. E.g. "The Opportunity", "Vision", "Our Team", "Our Thesis", "Use of Proceeds"
2. **Title** — placeholder at (21, 109)pt, sentence-case assertion statement
3. **"Confidential" badge** — (796, 20)pt, top-right corner, on all content slides
4. **Slide number** — (916, 20)pt, top-right
5. **Content area** — starts ~160-194pt from top

### Section Dividers
- Dark Green `#002924` background on left ~50%, full-bleed photo on right ~50%
- White Sego trefoil/triquetra icon overlaid on photo
- Small section label in lighter green above main title
- Title in large white text, left-aligned on dark half

### Two-Panel "Gaps → Solution" Pattern
- Left panel = problems/gaps (Dark Green header bar)
- Right panel = Sego response (Sage header bar)
- Each panel uses the card pattern (round2SameRect header + roundRect body)

### Target Deep-Dives (multi-section dense)
- Expression (left, with images), Biology & Feasibility (table with checkmarks), Landscape, Sego's Approach
- Compact single-column tables with bold key + regular description

### Tables
- Often single-column key-value format (1 column, multiple rows)
- Header row: Dark Green `#002924` fill when explicit
- Body: compact cells with bold category name + regular description on next line
- Multi-column comparison tables for competitive data (5-7 columns)
- Financial tables with logos inline

### Pipeline / Stage-Gate Diagrams
- Built with freeform shapes in the pitch deck (not chevrons/homePlate)
- When building in PowerPoint programmatically, `homePlate` (first stage) + `chevron` (subsequent) are acceptable alternatives
- Light Green `#D5ED99` numbered circles overlaid as step indicators
- Color gradient from lightest (Sage) to darkest (Dark Green)
- Descriptor text boxes below each stage

### Season Mix Data Callouts
- Large financial numbers: `$40M+`, `$60M` at 48-52pt Season Mix
- Percentages: `50%`, `75%`, `100%` at 40pt Season Mix
- Position varies — often top-right of slide or within data cards

---

## §5 — Language & Tone

### Voice
- **First person** when describing Sego's actions: "We're building...", "Our translational strategy...", "We are selecting..."
- **Third person declarative** for market/industry context: "Large pharma companies acquire innovation...", "RLT pharmacology is complex..."
- **Assertive and specific** — never hedging or vague

### Jargon & Abbreviations (use freely)
FIH, RLT, CMC, IND-enabling, mCRPC, CFR 211, GMP, ADC, TCE, CART, PSMA, SSTR2, RP2D, HTS, LC-MS/MS, ADME/PK, AUC, QOZ, QSBS

### Common Abbreviations
"addt'l", "tx", "F&F", "PC", "CRC", "sq ft"

### Quantitative Specificity
Always use concrete numbers: "$40M+", "6 acquisitions of >$1B value", "$335.42 billion", "45B member cyclic peptide library", "65K sq ft"

### Source Citations
- Position: bottom edge of slide
- Style: 8pt Funnel Sans Medium, Dark Grey #656670
- Format: academic style — "Source: Author et al, Journal Vol, Issue, p. XXX Year"

---

## §6 — General Slide-Making Preferences

These apply to ALL decks, not just Sego:

### Content Density
- **Pre-read investor deck style** — very high density, not speaker-support
- Multiple info layers per slide: title takeaway + data/visual + source + callouts
- Tables: compact 2-col key-value for value drivers; wider for competitive comparisons

### Slide Title Rules
- Sentence case only (first word capitalized + proper nouns)
- Full assertion statements conveying a conclusion or takeaway
- NOT topic labels — "Value Inflection Milestones" is the exception, not the rule

---

## §7 — Construction Notes (for the AI)

### Shape Recipes
- **Card header:** `round2SameRect`, ~36-43pt tall, fill per semantic meaning
- **Card body:** `roundRect`, ~270-310pt tall, white fill
- **Numbered circle:** `ellipse` 27pt, `#D5ED99` fill, bold number, zero-margin bodyPr, anchor=ctr
- **Pipeline (programmatic):** `homePlate` (first) + `chevron` (subsequent), `adj="20000"`/`adj="25000"`
- **Text in chevrons:** Funnel Sans SemiBold, centered, white on dark fills

### Key Reminders
- Always use `escapeXml()` for text in XML templates
- Pipeline color gradient: light→dark (earliest→latest stage)
- WCAG AA contrast (4.5:1) on all text
- Season Mix for large data callout numbers only
- Dark Grey `#696A77` for all icons
- Dark Grey `#656670` for body text (not black)
- "Confidential" at (796, 20)pt, slide number at (916, 20)pt
