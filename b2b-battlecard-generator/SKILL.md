---
name: b2b-battlecard-generator
description: >
  Generates a sales-ready battlecard for one named competitor: positioning snapshot, win themes, objection rebuttals, discovery questions, and a one-page cheat sheet reps use in live deals. Use for a single competitor deliverable, not a full CI program (see b2b-competitive-intelligence) or a buyer-facing comparison (see b2b-competitive-comparison). Triggers: "build a battlecard for [competitor]", "how do we beat [competitor]", "prep the team for a deal against [competitor]".
---

# B2B Battlecard Generator

Battlecards are opinionated sales weapons, not balanced analyses. Every line should help a rep win the next conversation — if it reads like marketing copy, or a rep wouldn't actually say it under deal pressure, cut it.

## Step 0: Gather inputs

| Input | Required? |
|---|---|
| Your product name and the competitor's name | Required |
| Target persona | Required |
| Deal context (SMB / mid-market / enterprise) | Recommended |
| Sales stage focus (discovery / evaluation / late-stage) | Recommended |
| Known differentiators, common objections, win/loss notes | Optional but high-value — incorporate directly if provided |

If inputs are missing, infer reasonable defaults from the competitive dynamics of the category, label them as assumptions, and proceed — a battlecard built on stated assumptions beats a blank page.

## Output: nine sections, always all nine

Full section-by-section writing rules are in `references/battlecard-template.md`. Summary:

1. **Competitive snapshot** — four facts, no paragraphs: what they are, who they typically win against, where they're genuinely strong, where they're vulnerable.
2. **Head-to-head positioning** — where we win decisively, where they win (be honest — a rep who knows where they lose is better prepared than one who thinks the product is perfect), framed as "different in ways that matter" rather than "better."
3. **Win themes** — 3-6 narratives anchored in customer outcomes, not feature lists.
4. **Discovery questions** — 6-10 questions that expose competitor weaknesses or surface a requirement that favors this product, written as a rep would actually ask them.
5. **Objections and rebuttals** — for each, what the buyer says, what they really mean, and a response under four sentences.
6. **Competitive landmines** — pricing traps, feature-comparison traps, and demo pitfalls specific to this competitor.
7. **Sales talk track** — a 30-second positioning answer plus 2-3 verbatim call snippets, written as the rep would say them out loud.
8. **When you win / when you lose** — specific signals for each, plus late-stage recovery moves.
9. **Cheat sheet** — three things to always say, three to never say, three questions to always ask. Printable, scannable in ten seconds.

## Guardrails

- Never fabricate a competitor weakness. Without evidence, label it "commonly reported" or "worth probing" rather than stating it as fact.
- No marketing language — "innovative", "leading", "best-in-class" get deleted on sight.
- Be honest about where the competitor is genuinely strong; a battlecard with no acknowledged weaknesses reads as denial, and reps stop trusting it.
- Take a side. This document is opinionated, not a fair comparison — for that, use `b2b-competitive-comparison` instead.

## Optional enhancements

If win/loss notes are provided, extract patterns and quote buyer language directly rather than paraphrasing. If pricing data is provided, add a tactical pricing-anchoring section. If multiple personas are in scope, produce persona-specific discovery questions and objection variations rather than one generic set.

## Step 10: Export to Canva

Once the nine sections are written, check `references/canva-template.md` for a designated battlecard Brand Template.

- **Template designated** — use the Canva connector to autofill that template, mapping each section to the field names recorded there, then share the export link.
- **No template designated yet** — use the Canva connector to search for battlecard or sales one-pager templates, show 2-3 candidates, and once the user picks one, save its ID and field-name mapping into `references/canva-template.md` so future battlecards skip the search.
- **Canva connector not connected** — skip this step, deliver the battlecard as a Markdown or Word document instead (see the `docx` skill), and mention that connecting Canva from Settings enables direct designed export.
