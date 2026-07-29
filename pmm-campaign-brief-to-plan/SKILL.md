---
name: "pmm-campaign-brief-to-plan"
description: "Turns a launch campaign objective into a full execution plan — structured brief, pre/during/post-launch phases, week-by-week calendar, and success metrics — delivered as a Word document. Pulls brand context from the active project in memory/projects/ or whatever file the user points to. Use when the user says \"plan the launch of X\", \"build the campaign plan for this feature\", \"I need a campaign plan\", \"how do we launch this\", or any variant of turning a campaign goal into an actionable plan."
---

# Campaign Brief to Plan (generic)

Turns a launch objective into an executable campaign plan, aligned with the approved messaging of the active product/company, delivered as a Word document.

## Instructions

### Step 1: Load context

Look for the active project's brief in `memory/projects/` (or whatever context folder the user uses). If there's more than one project and it's unclear which one applies, ask. If no context file exists, ask the user for the product brief before proceeding and list all the fields that need to be completed — do not invent messages, segments, or numbers.

From the context, identify:
- The target segment(s) for the launch
- The applicable sales motion (PLG, sales-led, or hybrid)
- The correct pain trigger for that segment
- The canonical messages that apply

### Step 2: Gather missing input

If the user hasn't specified, ask **in a single message** (not several):

1. **What's launching?** Feature, module, product, update — brief description
2. **What's the main campaign objective?** (trials, demos booked, upgrades, adoption, other)
3. **What's the launch date?** Or estimated range
4. **Are channels already defined?** Email, LinkedIn, events, in-app, other — or leave it open
5. **Any constraints?** Budget, resources, fixed dates

If there's already enough context from the conversation, don't ask — use what's there.

### Step 3: Build the plan

Structure the plan into 4 blocks.

**Block A — Executive brief** (table)

| Field | Content |
|---|---|
| Campaign name | descriptive, not generic |
| What's launching | feature, module, or product |
| Campaign objective | primary metric + target number if applicable |
| Target segment | from context, with rationale |
| Champion | primary recipient, from context |
| Pain trigger | derived from context — regulatory, operational, financial, competitive, whichever applies |
| Central campaign message | derived from the context's core message, adapted to the launch |
| Launch date | date or week |
| Campaign duration | total weeks: pre + launch + post |

**Block B — Execution phases** (always three)

- *Pre-launch (2–3 weeks before):* build anticipation, prep channels. Actions: teaser to installed base, sales material prep, internal team brief, landing/in-app setup. Closing milestone: materials ready, team briefed.
- *Launch (launch week + 1 week):* maximum visibility and activation. Actions: announcement email, LinkedIn post, in-app notification, sales outreach, demo/webinar if applicable. Closing milestone: X activations / X demos booked.
- *Post-launch (2–3 weeks after):* convert interest into adoption, capture learnings. Actions: activation follow-up, nurture email, early case study if adoption is fast, results report. Closing milestone: campaign report with metrics vs. objective.

**Block C — Week-by-week calendar**

Table: Week | Phase | Key actions | Channel | Owner | Milestone. Weeks numbered -3 (pre-launch) to +3 (post); week 0 is launch week. Be specific — not "create content" but, for example, "write announcement email to installed base with a subject line based on [segment]'s pain trigger."

**Block D — Success metrics** (three levels)

- *Reach:* emails sent / open rate target, impressions / organic reach, landing visits or notification clicks
- *Activation:* trials started / demos booked / upgrades, activation rate (context's target if it exists, otherwise flagged as an assumption), usage in the first week
- *Business:* pipeline generated, conversion to paid (context's benchmark if it exists), incremental ARR/revenue attributed

Always include an "early warning signal" line: the indicator that, if red in week 1, means something needs adjusting before continuing.

### Step 4: Produce the Word document

Use the `docx` skill to generate the plan as a .docx file, saved in the active project's folder.

File name: `CampaignPlan_[CampaignName]_[MonthYear].docx`

Format: cover page with campaign name, date, and "[Company name from context] — Internal use" · table of contents · the 4 blocks as Heading 1 sections · tables with soft borders (CCCCCC) and CLEAR shading · footer with page number · Arial 11–12pt.

### Step 5: Consistency check

Before presenting the document, verify against the loaded context:
- Is the campaign's central message consistent with the approved core message?
- Is the pain trigger correct for the segment?
- Do the target numbers match the context, or are they flagged as an assumption if none exist?

If there are deviations, fix them in the doc before delivering.

## Examples

**Example 1 — Feature launch, context available**

User says: *"Plan the launch of our new mobile app for Q3."*

Actions:
1. Load `memory/projects/acme-widgets.md`, find core message, ICP, and canonical benchmarks
2. Ask the single clarifying-question message (objective, date, channels, constraints) since none were given
3. Build the 4 blocks using Acme's champion (IT Director) and pain trigger (compliance deadline)
4. Generate `CampaignPlan_MobileAppLaunch_Q32026.docx` with the `docx` skill
5. Run the consistency check against Acme's messaging framework before delivering

Result: a ready-to-use Word plan consistent with Acme's existing positioning, no invented numbers.

**Example 2 — No context file yet**

User says: *"Build a campaign plan for our new pricing tier."*

Actions:
1. Check `memory/projects/` — no file exists for this company
2. Ask the user for a product brief, positioning doc, or messaging framework before proceeding
3. Once provided, resume from Step 1

Result: no plan is generated until real context exists, avoiding a generic or contradictory output.

## Troubleshooting

**Issue: No context file exists and the user has none to share**
Cause: this is a brand-new project with no prior PMM decisions documented.
Solution: offer to help build the missing pieces first (e.g. positioning or messaging framework) before producing a campaign plan — a plan without a real core message and ICP will read as generic and may contradict future decisions.

**Issue: More than one project file matches the request**
Cause: the user works across multiple companies/products and didn't specify which one.
Solution: ask which project this campaign is for before loading context — never guess.

**Issue: The requested campaign objective conflicts with the loaded positioning (e.g., asks to lead with a mechanism the context says should never be the opening promise)**
Cause: the user may not be thinking about the approved hierarchy when describing what they want.
Solution: flag the conflict explicitly before building the plan — don't silently follow the approved framework or silently follow the request. Ask which should win for this specific campaign.

**Issue: The context file has no defined benchmarks for activation or conversion**
Cause: the product is early-stage or the context file wasn't populated with metrics.
Solution: mark those metric fields as "[Assumption — no benchmark in context, validate after first campaign]" rather than inventing plausible-sounding numbers.
