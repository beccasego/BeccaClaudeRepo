# Competitive Intelligence Sweep — Prompt Template

Use this prompt with Claude Code to run a structured CI sweep on a company or therapeutic target.

## MCP Servers Available (use these instead of raw URL fetching)
- **pubmed** — structured PubMed/NCBI E-utilities search (MeSH, filters, 100+ results)
- **paperplain** — multi-source paper search across PubMed, ArXiv, Semantic Scholar
- **fetch** — fetch any URL as clean text (ClinicalTrials.gov, SEC EDGAR, company pages)
- **firecrawl** — deep web scraping and search; use for patent databases (Justia, Espacenet, Lens.org)
- **brave-search** — web search (requires API key — skip if not set up, use WebSearch fallback)

## Patent Search Notes
- Use **firecrawl_search** with `site:patents.justia.com` or `site:lens.org` for structured patent results
- Justia returns clean structured data; Google Patents blocks direct fetch
- Firecrawl results can be very large — save to subagent for parsing if they exceed context
- Search both the target name AND synonyms (e.g. "GUCY2C" AND "guanylyl cyclase C" AND "GCC")
- Always check: assignee, priority date, modality claimed, national phase status
- Key patent databases: Justia (justia.com/patents), Lens.org, Espacenet (worldwide.espacenet.com)

---

## Single Company Sweep

```
Run a competitive intelligence sweep on [COMPANY NAME].

Use the following tools in parallel where possible:

1. **Pipeline** — fetch [COMPANY] website pipeline page using the fetch MCP. Also scrape their
   most recent investor day or R&D day presentation if findable.

2. **Clinical Trials** — use the fetch MCP to call:
   https://clinicaltrials.gov/api/v2/studies?query.term=[COMPANY]&pageSize=30&format=json
   Summarize all active/recruiting trials by drug, indication, and phase.

3. **Recent News** — search for "[COMPANY NAME] biotech" news from the last 90 days.
   Focus on: fundraising, partnerships, trial readouts, FDA actions, leadership changes.

4. **Publications** — use the pubmed MCP to search for publications by [COMPANY] authors
   in the last 2 years. Flag any key mechanism, safety, or efficacy findings.

5. **SEC Filings** (public companies only) — use the fetch MCP to call:
   https://efts.sec.gov/LATEST/search-index?q=%22[COMPANY]%22&dateRange=custom&startdt=[YEAR-01-01]&forms=10-K,10-Q,S-1
   Extract: pipeline disclosures, cash/runway, recent financings, risk factors mentioning programs.

6. **Job Postings as CI signal** — use the puppeteer MCP to scrape [COMPANY]'s careers page.
   New roles in clinical ops, regulatory affairs, medical affairs, or a new TA signal pipeline moves.

Output as a structured report saved to:
Competitive-Intelligence/reports/[COMPANY]-[YYYY-MM-DD].md

Use the report format in ci-report-format.md.
```

---

## Therapeutic Target Sweep

```
Run a competitive intelligence sweep on the therapeutic target [TARGET NAME / PATHWAY].

Use the following tools in parallel where possible:

1. **Competitive Landscape** — search for companies with programs against [TARGET].
   What modalities are being pursued (small molecule, ADC, antibody, cell therapy, RLT, etc.)?

2. **Clinical Activity** — use the fetch MCP to call:
   https://clinicaltrials.gov/api/v2/studies?query.term=[TARGET]&query.intr=[TARGET]&pageSize=40&format=json
   Summarize by company, drug, indication, and phase.

3. **Recent Science** — use the pubmed MCP to search "[TARGET] cancer" sorted by date,
   last 12 months, at least 15 results. Also run paperplain MCP for ArXiv preprints.
   Flag: mechanism papers, biomarker findings, new indication data, safety signals.

4. **News & Deals** — search "[TARGET] drug development partnership deal 2025 2026"
   and "[TARGET] biotech clinical data readout". Note financings, licensing deals, M&A.

5. **Expression / Indication Landscape** — which tumor types express [TARGET] at meaningful
   levels? Which are approved vs. exploratory vs. not yet studied?

6. **Patent Landscape** — use firecrawl_search to search for patents:
   - Query 1: `site:patents.justia.com [TARGET] cancer antibody` — structured patent list
   - Query 2: `"[TARGET]" radiopharmaceutical patent site:patents.justia.com OR site:lens.org`
   - Query 3: `"[TARGET]" [SYNONYM] ADC OR CAR-T OR bispecific patent`
   - For each patent found: assignee, priority date, modality claimed, legal status (active/abandoned/granted)
   - Flag any from large pharma (Pfizer, AZ, BMS, Merck, Roche, Novartis, Lilly, Bayer)
   - Flag any RLT/radiopharmaceutical claims specifically
   - Note: firecrawl results may be large — delegate to a subagent for parsing if needed

7. **Sego Positioning** — based on all of the above:
   - What indications are uncrowded?
   - What modalities are missing or underrepresented?
   - What safety liabilities exist in current programs that could be addressed?
   - What patient populations are underserved?
   - What IP space is open vs. blocked?

Output as a structured report saved to:
Competitive-Intelligence/reports/target-[TARGET]-[YYYY-MM-DD].md

Use the report format in ci-report-format.md.
```

---

## Batch Sweep (Multiple Companies)

```
Run a CI sweep on each of the following companies and save individual reports for each:

- [COMPANY 1]
- [COMPANY 2]
- [COMPANY 3]

For each: use the fetch MCP for ClinicalTrials.gov, SEC EDGAR (if public), and pipeline page.
Use the pubmed MCP for recent publications. Search for news from the last 90 days.

After all individual reports are done, write a comparison summary to:
Competitive-Intelligence/reports/batch-comparison-[YYYY-MM-DD].md

The comparison should include: pipeline stage by indication, modality comparison,
financing status, key upcoming catalysts, and relative competitive positioning.
```

---

## Quick News Flash (lightweight, no report)

```
Quick update on [COMPANY / TARGET]: what happened in the last 30 days?
Search news, check for new ClinicalTrials.gov registrations, and scan for any press releases.
Give me 5-10 bullet points, no file needed.
```
