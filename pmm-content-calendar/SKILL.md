---
name: "pmm-content-calendar"
description: "Generates a monthly editorial calendar for any product/company with themes, formats, channels, and dates — covering LinkedIn, email marketing, and long-form content (blog/articles) — delivered as a Word document ready to execute. Pulls validated content angles and canonical messages from the active project context in memory/projects/. Use when the user says \"build the content calendar\", \"what do we publish this month\", \"I need the editorial plan\", \"organize the campaign content into a calendar\", \"what LinkedIn posts do we do\", \"plan this quarter's content\", or any variant of turning a strategy or campaign into a concrete publishing calendar."
---

# Content Calendar (generic)

Turns an approved strategy or campaign into an executable monthly editorial calendar, aligned with the active product's messaging.

## Instructions

### Step 1: Load context

Look for the active project's brief in `memory/projects/`. If unclear which project applies, ask. Identify validated content angles and canonical messages — the calendar should amplify what's already approved, not invent new themes from scratch.

### Step 2: Gather input

If not specified, ask **in a single message**:

1. **Is there a base campaign or strategy?** (if this follows directly from a campaign plan or demand gen campaign, use that output directly)
2. **For what month/period?** (specific month or week range)
3. **Main objective for the period?** (build awareness, activate trials, mature leads, support a launch)
4. **Any fixed dates?** (industry events, regulatory deadlines, feature launches)

If there's enough context in the conversation, build the calendar directly.

### Step 3: Define cadence per channel

Use these as a starting point, adjust if the user or context specifies otherwise:

| Channel | Suggested cadence | Why |
|---|---|---|
| LinkedIn (posts) | 3 per week | Enough to build presence without saturating |
| LinkedIn (long article) | 1 per month | Thought leadership and LinkedIn SEO |
| Email to contact base | 1–2 per month | Stays present without driving unsubscribes |
| Blog / long-form article | 1–2 per month | SEO and amplification via LinkedIn |

### Step 4: Build the calendar

**Theme logic:** each week needs a theme that connects channels together — the same theme works across LinkedIn, email, and blog in different formats, not copies of the same text.

**Example theme week:**
- Theme: [a specific, quantifiable pain point from context]
- LinkedIn Mon: short post with a question hook
- LinkedIn Wed: carousel with before/after
- LinkedIn Fri: testimonial or impact stat
- Blog: article going deeper on the theme
- Email (if it falls that week): article announcement + demo CTA

**Theme bank:** pull from context's validated content angles and canonical messages — do not invent themes. If context has fewer than 4-5 validated angles, ask whether to derive additional ones from the messaging pillars (flag these as new, not yet validated) or keep the calendar shorter.

**Monthly calendar structure:** for each week, a table — Day | Channel | Format | Theme/Angle | Opening copy or core idea | CTA | Pillar.

**Weekly notes:** context for why that theme fits that moment (e.g., a week before month-end → a regulatory-deadline angle is timely).

**Distribution rules:**
- No more than 2 consecutive weeks on the same pillar — rotate
- At least 1 "educational" (non-promotional) piece per month, for credibility
- At least 1 piece with a quantifiable data point (canonical benchmark) per week
- If there's a launch or key date in the month, the prior week is dedicated to anticipation

### Step 5: Produce the Word document

Use the `docx` skill. Save in the active project's folder.

File name: `ContentCalendar_[MonthYear].docx`

Structure: cover page (month, period objective, active channels) · month summary (central theme, milestones, metrics to track) · monthly view (4–5 week table, one row per week with the theme) · detailed week-by-week view (expanded table with all Step 4 fields) · theme bank appendix for quick reference · tracking metrics (engagement per channel, open rates, traffic).

### Step 6: Consistency check

Verify before delivering: all themes derive from approved messaging (no invented messages); pillar distribution is balanced; numbers in hooks match context's canonical figures; no piece opens with a mechanism/differentiator as the main promise.

## Examples

**Example 1 — Calendar following a campaign plan**

User says: "Now build the content calendar for August based on the mobile app launch plan."

Actions:
1. Load context and the just-generated campaign plan for the mobile app launch
2. Use the launch's central message and pain trigger as the month's dominant theme
3. Build the 5-week view with the pre-launch week dedicated to anticipation per the distribution rules
4. Generate `ContentCalendar_Aug2026.docx`

Result: a calendar that visibly ladders up to the campaign rather than running a parallel, disconnected content plan.

**Example 2 — Thin theme bank**

User says: "Build next month's content calendar."

Actions:
1. Load context — only 2 validated content angles exist
2. Ask whether to derive 2-3 additional angles from the messaging pillars (flagged as new) or keep the month lighter on content
3. Build the calendar per the user's choice

Result: no fabricated themes presented as validated; the gap is surfaced instead of papered over.

## Troubleshooting

**Issue: The same theme repeats across multiple weeks without variation**
Cause: the theme bank is too thin to fill the month.
Solution: flag the gap directly rather than repeating — suggest either a shorter calendar or deriving new angles (marked as unvalidated) from the messaging pillars.

**Issue: Numbers in the hooks don't match what's in context**
Cause: a benchmark was approximated instead of pulled directly from the knowledge base.
Solution: go back to context and use the exact figure, or mark it "[Assumption — validate]" if no canonical number exists for that claim.

**Issue: Calendar leans heavily on one pillar despite the distribution rule**
Cause: the theme bank itself is skewed toward one pillar.
Solution: note this explicitly in the delivery — either rebalance by deriving new angles for underused pillars, or flag that the messaging framework itself may need more coverage there.
