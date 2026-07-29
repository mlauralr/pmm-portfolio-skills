---
name: b2b-case-study-generator
description: >
  Generates an outcome-driven B2B case study from customer results: challenge, why they chose you, the solution, implementation story, and measured business impact. Use for a customer success story, reference story, or ABM/late-stage deal asset. Works from partial data — produces a draft with directional language where metrics are missing. Triggers: "write a case study for [customer]", "create a customer success story", "turn this win into content".
---

# B2B Case Study Generator

A case study is a proof-of-transformation story, not a testimonial compilation or a product brochure. The best ones don't describe success — they make the next buyer imagine their own success is the natural next step.

## Step 0: Gather inputs

| Input | Required? |
|---|---|
| Product/company name, customer organization (or anonymized placeholder if NDA applies) | Required |
| Customer industry, target persona reading this | Required |
| Primary use case, solution details | Required |
| Outcomes / metrics | Required — quantified preferred, directional acceptable with a qualifier |
| Before-state / pain points, implementation timeline, competitive context, tone | Recommended |

If metrics are missing, produce the draft with directional language ("significantly reduced," "substantially faster") and flag exactly where a real number should go before publication — a well-structured draft with marked placeholders beats waiting for perfect data.

## Output: ten sections

Full section-by-section writing rules are in `references/methodology.md`. Summary:

1. **Headline** — names the transformation, not the product. Produce 2-3 options.
2. **Executive summary** — 4-6 sentences: who the customer is, the challenge, the solution, the headline result. Should work as a standalone pull quote out of context.
3. **The challenge** — the before state, specific and layered (operational, business risk, scale, human cost). This is the most commonly underdeveloped section; the sharper the before, the more powerful the after.
4. **Why they chose us** — what was evaluated, why alternatives fell short on this buyer's specific criteria, 3-5 decision drivers.
5. **The solution** — practical, not promotional: what was deployed, how it fit the existing stack, feature-to-outcome mapping for anything mentioned.
6. **Implementation story** — rollout approach, timeline, adoption strategy, and the friction points that came up. A story with no friction isn't credible.
7. **Results and business impact** — bullet format, each result stated as metric, outcome, and timeframe context.
8. **Customer perspective** — 1-3 quotes that sound like a real operator, specific and persona-authentic. If none are available, produce draft quotes clearly labeled for customer approval.
9. **Key takeaways** — 3-5 lessons that generalize the story to a reader who isn't this exact customer.
10. **Call to action** — matched to the deal stage this asset supports (awareness, evaluation, or late-stage).

## Guardrails

- Never fabricate a metric. Use directional language with a qualifier and the customer's own words when a number isn't available.
- A case study that mentions no implementation friction reads as unbelievable — buyers know rollouts are never perfectly smooth.
- Delete forbidden phrases on sight: "game-changing," "revolutionary," "paradigm shift," "best-in-class."
- The customer is the protagonist. The product is what enabled them, not the subject of the story.

## Optional enhancements

If win/loss data is available, strengthen "why they chose us" with real evaluation patterns. If multiple customer stories are in scope, produce a templatized version that scales across segments. If requested, adapt the narrative arc into a 2-3 minute video testimonial script.

## Step: Export to Canva

Once the ten sections are written, check `references/canva-template.md` for a designated case study Brand Template.

- **Template designated** — use the Canva connector to autofill it, mapping each section to the recorded field names, then share the export link.
- **No template designated yet** — search Canva for case study templates, show 2-3 candidates, and once the user picks one, save its ID and field-name mapping into `references/canva-template.md`.
- **Canva connector not connected** — skip this step, deliver the case study as a Markdown or Word document (see the `docx` skill), and mention that connecting Canva from Settings enables direct designed export.
