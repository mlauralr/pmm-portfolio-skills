---
name: b2b-win-loss-analysis
description: >
  Analyzes win/loss interview transcripts and CRM deal data specifically, to find why deals are won or lost, segmented by persona and competitor. Narrower than b2b-ci-analyst-reporter — use this when the input is deal outcome data specifically, not broader market or review signals. Triggers: "analyze our win-loss interviews", "why are we losing to [competitor]", "what patterns are in our closed-lost deals".
---

# B2B Win/Loss Analysis

The job is finding cross-deal patterns, not summarizing individual deals. Never rephrase a single transcript — synthesize across every deal provided into named, weighted themes.

## Reasoning steps before writing output

1. Normalize all deal data — strip anecdotes, extract the core reason per deal.
2. Cluster similar reasons across deals into named themes.
3. Weight by frequency, and by deal size (ARR) if available.
4. Separate signal from noise — a one-off complaint is noise unless it's high-stakes; a pattern across three or more deals is signal.
5. Run a delta analysis — always compare wins against losses to find what actually differentiates the outcome, not just what's present in losses alone.

## Output: produce the full report, skip a section only if the data genuinely can't support it (and say so)

1. **Executive summary** — five bullets max: primary win driver, primary loss driver, most dangerous competitive threat if present, biggest messaging or product gap, one recommended immediate action.
2. **Win drivers** — top reasons, each with a sharp label (not generic), the evidence behind it, and the messaging or product strength it maps to.
3. **Loss drivers** — grouped only into categories with actual evidence: product gaps, pricing/packaging, competitive displacement, sales execution gaps, timing/procurement.
4. **Competitive insights** (if competitor data is present) — who this product loses to and why, positioning gaps, recurring "deal traps," and where it consistently beats them.
5. **Persona insights** (if role data is present) — differences in objections and decision criteria by role (economic buyer, champion, technical/IT, procurement). Populate only rows with actual evidence.
6. **Messaging and positioning gaps** — what's resonating in wins, what's missing or unclear, and specific repositioning angles grounded in the data.
7. **Product feedback signals** — repeated feature requests, deal-breaking gaps, and a must-have vs. nice-to-have split based on frequency and deal impact.
8. **Recommendations** — 3-7 prioritized actions, each with impact, owner, and timeframe (immediate / near-term / strategic).

## Handling thin data

If the dataset is small (fewer than roughly 5 deals) or missing key fields, open with an explicit data-note flagging insufficient sample size for strong confidence, then proceed anyway with low-confidence findings clearly flagged inline rather than refusing to analyze.

## Input flexibility

Handle any combination of: deal outcome labels, interview transcripts or rep debriefs, CRM fields (stage lost, reason codes, deal size, competitor), and segment context (industry, size, personas involved). If outcomes aren't explicitly labeled, infer from context clues (e.g., "we went with another vendor") and note the inference.
