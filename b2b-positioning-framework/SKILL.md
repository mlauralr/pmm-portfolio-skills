---
name: b2b-positioning-framework
description: >
  Builds B2B product positioning from scratch: category frame, target buyer, problem statement, differentiation, and messaging architecture. Use when there is no existing positioning, or the user asks to define the value proposition, category, or "why us" from zero. If positioning already exists but isn't converting, use b2b-repositioning-framework instead. Triggers: "build our positioning", "what's our value proposition", "how do we define our category", "we're not sure how to explain what we do".
---

# B2B Positioning Framework

Positioning connects what a product does to why the market needs it now. It is not a tagline — it is the internal logic that every sales conversation, landing page, and pitch deck should trace back to.

## Step 0: Gather context

Ask for what's missing before drafting:

| Input | Why it matters |
|---|---|
| Product / solution description | Raw material for value extraction |
| Target market and ICP | Grounds buyer context and category framing |
| Primary use cases / jobs to be done | Connects product to buyer progress |
| Competitive alternatives | Needed for differentiation and whitespace |
| Sales motion (PLG / sales-led / hybrid) | Shapes how positioning performs in market |
| Market maturity (emerging vs. crowded) | Determines category-creation vs. category-competition strategy |

If inputs are incomplete, infer from the product description and state the assumptions explicitly rather than stalling.

## Method: five layers, in order

Work through these in sequence — skipping to messaging before the market frame and problem statement are settled produces positioning that reads well but collapses under a hard sales question. Full detail, prompts, and the output template for each layer are in `references/methodology.md`.

1. **Market frame** — is this category being created, redefined, or competed in? What changed to make the old approach insufficient now? (e.g., a renewable energy operator running 60 sites on spreadsheets and legacy SCADA reports hits a scale threshold where manual monitoring can no longer catch downtime before it costs a full day of production.)
2. **Target buyer and context** — who this is for, behaviorally: their trigger event, constraints, and stage of awareness.
3. **Core problem statement** — the primary problem in the buyer's own words, its downstream consequences, and why current workarounds fail. Specificity beats generality: "uptime issues surface in a monthly report, three weeks after the revenue was already lost" is a problem statement; "operations lack visibility" is not.
4. **Unique value and differentiation** — the outcome that changes for the buyer, backed by proof, plus the "why us" factor a competitor can't easily copy.
5. **Competitive positioning** — direct competitors, indirect alternatives (including "keep doing it manually"), and the strategic whitespace no one has claimed.

## Output

Produce, in order: a one-sentence positioning statement ("For [buyer], who [context], [product] is a [category] that [value], unlike [alternative], because [differentiator]"), then the five layers above written out, then a short messaging architecture (core message pillar + 2-4 supporting pillars, each with a claim and proof points) that feeds directly into `b2b-messaging-framework` if the user wants it expanded into full channel copy.

See `references/methodology.md` for the complete layer-by-layer breakdown, competitor mapping table, and language guidelines (outcome verbs to use, vague SaaS terms to avoid).

## Guardrails

- Ground every claim in outcomes, not capabilities — "asset performance monitoring" is a capability; "catching downtime before it costs a day of production" is an outcome.
- Reflect the real competitive landscape. Buyers who evaluate renewable energy asset management tools usually know the other 2-3 vendors already; pretending they don't exist undermines credibility.
- A positioning statement that a sales rep can't use in the first 60 seconds of a call isn't finished yet.

## Advanced options

If requested: segment-specific positioning variants, persona-level value propositions, a category-creation narrative, or elevator-pitch versions at 30 seconds / 2 minutes / board level. Ask which before producing all of them.
